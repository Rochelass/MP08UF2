# Activitat 3

## Llistar Virtual Hosts Apache
Llistem els Virtual Hosts d'Apache amb la següent comanda:

```
apache2ctl -S
```

**3.3.-** Al directori **Learn more about owncloud** hi ha informació en forma de fitxers pdf. Consulta'ls i respon aquestes preguntes:

· Quin són els tres tipus de protecció de dades que ofereix Owncloud?

**1. Encriptació en transit**

**2.1. Encriptació al resetejar**

**2.2. Encriptació al resetejar amb clau mestra amb el modo segur de hardware(HSM)**

**3. Encriptacio de punt a punt**
· Fes una petita descripció de cada un d'ells.

**1: El xifratge en trànsit brinda protecció a owncloud sobre HTTPS utilitzant el protocol TLS més recent que tots els navegadors i clients poden admetre.**

**2: Encryption at Rest i Encryption at Rest with Master: tots els fitxers dels servidors d'aplicacions Owncloud abans de desar-los a l'emmagatzematge real.**

**3: End-to-End Encryption: és el nivell més alt de confidencialitat de dades convinada amb el més alt nivell de protecció de dades. És la única solució que pot pretendre assegurar-ho cap tercer no autoritzat pot accedir les dades xifrades**

· Per quina raó ens recomana utilitzar Owncloud per als documents de Microsoft Office de la nostra empresa?
  
**Perquè emmagatzema tots els documents i correus electrònics directament al núvol. Amb Owncloud i les seves aplicacions integrades de Microsoft, els empleats poden aprofitar d'una productivitat total i una connectivitat ininterrompuda sense ningun tipus de risc d'accessos no autoritzats o violacions de la privadesa ja que tenen les dades centralitzades al núvol privat.**

· Això passa a tots els països?

**No, perquè als Estats Units, la llei dels EUA requereix que les empreses dixen obert l'accés a les dades dels usuaris de Microsoft**

· Quina és la llicència d'OWncloud Enterprise?

**AGPLv3**

· I la d'Owncloud Standard?

**Llicència comercial ownCloud per als mòduls empresarials i empresarials d'ownCloud Server**

· Es poden veure videos en Streaming directament des de Owncloud?

**Si**

· Es poden connectar directoris de Google Drive a Owncloud?

**Si**

· I Dropbox?

**Si**

· Compta Owncloud amb antivirus? En cas afirmatiu com es diu? 

**Si, anomenat ClamAV**


**3.4.-** Mostra els següents canvis de paràmetres d'usuari:

- Posa't una imatge d'usuari.
- Afegeix el teu mail de l'Institut.
- Canvia l'idioma a català.
- Mostra la versió d'Owncloud instal·lada.
