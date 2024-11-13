# Instal·lació i configuració de clouds

Per instal·lar una cloud hem de descarregar el seu codi i seguir el manual genèric d'instal·lació d'aplicacions.

En resum:
* Descarregar el codi font.
* Portar el codi de la cloud al directori arrel del servidor web.
* Descomprimir el contingut directament al directori arrel, en el nostre cas `/var/www/html`.
* Entrar a la web `http://localhost` amb el navegador i seguir les instruccions.

## Enllaços 
* ***OwnCloud***: http://www.owncloud.org
* ***Nextcloud***: http://www.nextcloud.com

## Heu de baixar el .zip de Nextcloud Server
https://download.nextcloud.com/server/releases/latest.zip

## Heu de baixar el .zip de ownCloud Server
https://download.owncloud.com/server/stable/owncloud-complete-20240724.zip

### Instal·lar la versió 7.4 de PHP a Ubuntu 24.04

Per a poder instal·lar ownCloud necessitarem la versió 7.4 de PHP, per a instal·lar-la al nostre sistema haurem de fer les següents comandes:

Actualitza les llistes de paquets i actualitza tots els paquets existents al vostre sistema. 

Instal·leu els requisits previs de PPA:
```bash
sudo apt install software-properties-common -y
```
Instal·la les eines necessàries per treballar amb els arxius de paquets personals (PPA).
```bash
LC_ALL=C.UTF-8 sudo add-apt-repository ppa:ondrej/php -y
```
Actualitza ara els repositoris:
```bash
sudo apt update
```
Instal·la les llibreries de PHP de la versió 7.4
```bash
sudo apt install php7.4 -y
```
```bash
sudo apt install -y php libapache2-mod-php7.4
```
```bash
sudo apt install -y php7.4-fpm php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-gd php7.4-xml php7.4-intl php7.4-mysql php7.4-cli php7.4-ldap php7.4-zip php7.4-curl
```
Seleccioneu la versió de PHP que voleu:
```bash
sudo update-alternatives --config php
```
Activa els mòduls d'apache2 necessaris:
```bash
sudo a2enmod proxy_fcgi setenvif
```
```bash
sudo a2enconf php7.4-fpm
```
Reinicieu l'apache2:
```bash
sudo service apache2 restart
```
# Configuracio d'ownCLoud

# Creació d'usuaris
<p>Per crear usuaris li donem a la part dreta on surt el nostre usuari i li donem.
<p>En aquest lloc es on anem a crear l'usuaris.
<p>Per crear el usuari tenim que posar el nom de l'usuari, un gmail, que pot ser inventat.
<p>En l'espai de dalt del teu usuari que posa el que he dit abans.

  # Assignem rols i permisos

<p> Ara assignarem rols al nostres usuaris creats.
<p> Per crear un rol li tenim que donar on posa "Add group", i tindras ja dos rols creats predeterminats, "Everyone" i "Admin".
<p>I creem dos rols nous, els que vulguis.
<p>Per assignar els rols en un usuari li donem a "Group" en el mateix usuari i l'assignem el rol que acabem de crear.
<p>I ahuria de quedar aixi amb el nom dels rols creats per tu.
<p>Ara assignem permisos al nostres usuaris.
<p>Li donem a "users" que posa d'alt del tot, i aqui li donem a "Archivos"
<p>Ara seleccionem la carpeta a que volem donar permisos als nostres usuaris.
<p>Li donem a "sharing", posem el nom dels rols que volem donar permisos a aquesta carpeta, o el nom de l'usuari al que volem donar permisos en aquesta carpeta.
<p>I amb els teus rols i usuaris ahuria de quedar aixi
<p> Ara li donem al engranatge que hi ha al costat del usuari , podriem posar que pot fer el grup o la persona. 
<p> Una vegada fet tot això hauriem d'haver acabat de configurar rols i permisos als rols.

  # Administració d'arxius.

<p>Per crear arxius, carpetes o pujar fitxers, tenim que dar-li al "+" que posa dalt de les carpetes predeterminades.
<p>Ara tenim que crear una carpeta amb qualsevol nom.
<p> També tenim que cerar un arxiu dins de la carpeta 
<p>I aquest arxiu serveix com un document, pots escriure el que vulguis dins.
<p>També pots pujar un arxiu desde la teva propia maquina.
<p>I dins de l'arxiu com en les carpetes, també pots donar permisos a usuaris d'editar els arxius o pujar mes arxius.



