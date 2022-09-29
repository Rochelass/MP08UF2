# Instal·lació de owncloud a Linux

Instalar Owncloud en Ubuntu 22.04 LTS.

## Instalar Apache:

Instalam el servidor Apache:
Per a instal·lar-lo haurem de fer la següent comanda

``` (falta captura) sudo apt install apache2 ```

Seguidament lo que haurem de fer serà desactivar el llistat de directoris del servidor amb la següent comanda:



``` (falta captura) sudo sed -i "s/Options Indexes FollowSymLinks/Options FollowSymLinks/" /etc/apache2/apache2.conf ```



# Instalar MariaDB:

Instalarem MariaDB:
``` sudo apt-get install mariadb-server mariadb-client -y ```
Y configuramos la instalación:

sudo mysql_secure_installation
Aquí es interesante:

Deshabilitar usuarios anónimos.
Deshabilitar acceso remoto como root.
Eliminar las bases de datos de testeo y el acceso a las mismas.
Actualizar las tablas de privilegios.
Por último reiniciamos el servidor MariaDB.

sudo systemctl restart mariadb.service` o `sudo service mariadb.service restart
Crear la base de datos de owncloud:
Entramos en MariaDB:

sudo mysql -u root -p
Creamos la base de datos:

CREATE DATABASE owncloud;
Creamos un usuario llamado ownclouduser con una contraseña que podría ser Admin1234.

CREATE USER 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234';
Le damos acceso al usuario a la base de datos creada:

GRANT ALL ON owncloud.* TO 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234' WITH GRANT OPTION;
Aplicamos los cambios y salimos:

FLUSH PRIVILEGES;
EXIT;
Instalar PHP y sus módulos necesarios:
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:ondrej/php
Actualizamos los paquetes con el repositorio añadido:

sudo apt update
Instalamos PHP y los módulos necesarios:

Hemos de tener en cuenta los requisitos de Owncloud antes de instalar los módulos.

sudo apt install php7.4 libapache2-mod-php7.4 php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-apcu php7.4-smbclient php7.4-ldap php7.4-redis php7.4-gd php7.4-xml php7.4-intl php7.4-json php7.4-imagick php7.4-mysql php7.4-cli php7.4-mcrypt php7.4-ldap php7.4-zip php7.4-curl -y
Después de la instalación editamos el fichero php.ini y cambiaremos algunos valores:

sudo nano /etc/php/7.1/apache2/php.ini
Los valores que hemos de cambiar son los siguientes:

file_uploads = On allow_url_fopen = On memory_limit = 256M upload_max_filesize = 100M display_errors = Off date.timezone = Europe/Madrid

Instalamos Owncloud:
Descargamos la última versión del programa y descomprimimos los ficheros, además movemos los archivos de Owncloud a "/var/www/html/owncloud".

cd /tmp && wget https://download.owncloud.com/server/stable/owncloud-complete-latest.zip
unzip owncloud-10.0.8.zip
sudo mv owncloud /var/www/html/owncloud/
Cambiamos propietario y permisos de los directorios de owncloud. www-data para que los pueda usar Apache, 755 para que los pueda ejecutar y leer cualquier usuario de Linux:

sudo chown -R www-data:www-data /var/www/html/owncloud/
sudo chmod -R 755 /var/www/html/owncloud/
Configurar Apache:
Vamos a configurar Apache:

sudo nano /etc/apache2/sites-available/owncloud.conf
Debemos dejar un fichero como el siguiente, pero cambiando el ServerName y el ServerAlias por los nombres y alias de nuestro propio dominio.

Instalación owncloud

Habilitamos owncloud y el módulo rewrite:

sudo a2ensite owncloud.conf
sudo a2enmod rewrite
sudo a2enmod headers
sudo a2enmod env
sudo a2enmod dir
sudo a2enmod mime
Reiniciamos Apache:

sudo service Apache2 restart
A partir de este momento podemos acceder a owncloud desde el navegador para ello debemos introducir nuestra IP seguida de "/owncloud" en el mismo, por ejemplo si nuestra IP es 172.31.84.197 pondremos en el navegador 172.31.84.197/owncloud y podremos acceder al servicio.

Ya en el navegador creamos una cuenta de administración y ponemos los datos de MariaDB que hemos configurado anteriormente.

Acceder a Owncloud desde fuera de nuestro equipo:
Podemos acceder a nuestro owncloud desde la red local o desde Internet, para Internet deberás conocer la IP pública del equipo o del router bajo el que está.

Acceder desde LAN

Para acceder desde LAN deberemos indicar en el fichero de cconfiguración de owncloud la IP del equipo donde se aloja:

Buscamos el fichero config.php y lo editamos.

En el campo trusted domains añadimos la IP del equipo que hace de servidor.

Quedaría una cosa así:

Instalación owncloud

Donde la IP sería la de nuestro equipo servidor en vez de 192.168.1.133.

Ahora ya podríamos acceder a Owncloud desde cualquier equipo en la misma red.
