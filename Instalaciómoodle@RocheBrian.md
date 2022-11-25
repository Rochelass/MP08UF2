# Instal·lació moodle

Per a començar haurem d'afergir el ssh

![image](https://user-images.githubusercontent.com/104194787/203824274-fd62dc35-e871-45dc-acc6-1bc5cbba4601.png)

Seguidament el que farem serà instalar el apache2

![image](https://user-images.githubusercontent.com/104194787/203826244-03deed88-4c73-4911-be4a-31f152a799b8.png)

Instal·larem mariadb

![image](https://user-images.githubusercontent.com/104194787/203828883-94047302-eca3-444b-abf6-1edb0d67dca3.png)

Ara instal·larem la configuració de mysql

![image](https://user-images.githubusercontent.com/104194787/203829044-413cea1b-9025-49b2-8778-dd1e240f279e.png)

![image](https://user-images.githubusercontent.com/104194787/203829255-4f6e9ea9-dace-4966-aae0-2f61e8874bf1.png)

Comprovem que podem entrar a mariadb

![image](https://user-images.githubusercontent.com/104194787/203829505-85769915-2306-4846-9830-08a7491055e7.png)

Seguidament inst·lalarem el php7.3

![image](https://user-images.githubusercontent.com/104194787/204018246-de9728ee-07d8-4fed-9d9a-93c347c49cda.png)

![image](https://user-images.githubusercontent.com/104194787/204019427-4269c1b4-e237-4e1a-b653-1b36c143ba54.png)

Llavors un cop instal·lat editarem el fitxer per a que es mostre index.php a canvi de index.html.

![image](https://user-images.githubusercontent.com/104194787/203830357-41550f08-b804-482e-bf19-09abe8a38cb7.png)

Seguidament reiniciarem el servidor apache2

![image](https://user-images.githubusercontent.com/104194787/203830529-d061e937-2c5b-4767-aab5-35f474ac4d16.png)

Ara comprovarem que el servidor està actiu

![image](https://user-images.githubusercontent.com/104194787/203830644-cea8b388-343f-46bd-99e5-01c2ff935665.png)

Llavors el que haure de fer serà crear el fitxer index.php

![image](https://user-images.githubusercontent.com/104194787/203830863-2bb81af0-3eac-4df9-8c80-d22ba5281646.png)

![image](https://user-images.githubusercontent.com/104194787/203831054-27d025fe-75b9-45b2-9a12-795054efb80e.png)

Seguidament instal·larem el moodle

![image](https://user-images.githubusercontent.com/104194787/203825041-658851f7-911d-459f-8373-f1ec01fdf778.png)

Llavors descomprimirem la carpeta

![image](https://user-images.githubusercontent.com/104194787/203831654-7f920b39-0965-4b81-ab26-0a9607b34722.png)

Canviarem els permisos

![image](https://user-images.githubusercontent.com/104194787/203831808-84422c65-2502-411d-9fff-c27b04f69ca8.png)

Entrarem al directori de /home, crearem la carpeta "moodledata" i li afegirem els permisos.

![image](https://user-images.githubusercontent.com/104194787/203832227-d41d9beb-fda7-4f40-a375-017bd0877bd1.png)

Seguidament accedirem a la base de dades amb el mode de root.

![image](https://user-images.githubusercontent.com/104194787/203832884-0179948d-fc81-4a53-ac97-1518934891d6.png)

Ara crearem l'usuari de "moodlemanager" dins de la base de dades.

![image](https://user-images.githubusercontent.com/104194787/203833375-839405b2-bdd1-4905-b358-e7c0e2f3c010.png)

Seguidament lo que haurem de fer serà crear la base de dades de moodle

![image](https://user-images.githubusercontent.com/104194787/203833463-d4029bc7-ca23-4a4c-9ece-af1f3857dbb6.png)

Ara li haurem de donar els permisos al usuari

![image](https://user-images.githubusercontent.com/104194787/203833718-e9842ea8-348f-499f-9406-725b5e63aed5.png)

![image](https://user-images.githubusercontent.com/104194787/203833848-a9a2d6e5-829b-4434-afe1-6f1153eaf0e6.png)

Seguidament entrarem al buscador i posarem (la nostra ip)/moodle

![image](https://user-images.githubusercontent.com/104194787/204021266-7f9c42f6-9c41-4564-ad4a-031758dd3fc6.png)

