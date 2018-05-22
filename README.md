# Homepage
Cette page d'accueil a été réalisée par [Benjamin SECLIER](http://generation-linux.fr) à partir du template [AdminLTE](https://almsaeedstudio.com/preview).
Ce projet est disponible sous licence [CC BY-CA](http://creativecommons.org/licenses/by-sa/3.0/deed.fr).

![Screenshot](https://github.com/bseclier/homepage/raw/master/pages/inc/images/screenshot.jpg)

## Démo
Une page de démo est disponible à [cette adresse](http://generation-linux.fr/homepage) (login : demo ; Mot de passe : !demo!).
**Il s'agit des mêmes identifiants à entrer quand vous installez le projet chez vous.**

<b> Installation </b>
------
</br>

Install it doesn't require SQL Database to use Homepage. I recommand to install PHP7.1 + Apache2 with the last requirements.To install it, please use the next console. Only on Ubuntu 16.04 LTS for the moment.
**/!\ Please use these commands on root.**

</br>

##### Requirements
> $ apt-get update && apt-get -y dist-upgrade </br>
> $ apt-get -y install dialog unzip zip dirmngr unattended-upgrades needrestart </br>
> $ dpkg-reconfigure unattended-upgrades </br></br>
> $ apt-get install apt-transport-https lsb-release ca-certificates</br>
> $ wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg </br>
> $ "deb https://packages.sury.org/php/ $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/php.list </br>
> $ apt-get update </br>
> $ apt-get install php7.2-cli </br>
</br>

##### PHP7.1
> $ apt-get -y install apt-transport-https lsb-release ca-certificates nano curl git </br>
> $ add-apt-repository ppa:ondrej/php </br>
> $ apt-get update && apt-get -y dist-upgrade </br>
> $ apt-get -y install --no-install-recommends php7.1 php7.1-fpm php7.1-curl php7.1-json php7.1-gd php7.1-mcrypt php7.1-msgpack php7.1-memcached php7.1-intl php7.1-gmp php7.1-geoip php7.1-mbstring php7.1-redis php7.1-xml php7.1-zip </br>
> $ mkdir -p /var/lib/php7.1-fpm/ </br>
> $ service php7.1-fpm restart </br>
</br>

##### Apache2
> $ apt install --no-install-recommends php7.1 libapache2-mod-php7.1 php7.1-curl php7.1-json php7.1-gd php7.1-mcrypt php7.1-msgpack php7.1-memcached php7.1-intl php7.1-gmp php7.1-geoip php7.1-mbstring php7.1-redis php7.1-xml php7.1-zip </br>
> $ service php7.1-fpm restart && service apache2 restart </br>

</br>
</br>

<b> How to use Homepage </b>
------
</br>

Afin de vous aider dans l'adoption de cet outil, voici quelques conseils et remarques :

##### Site entier
- Vous pouvez faire en sorte que la sidebar ne soit pas minimaliste en supprimant le mot "sidebar-collapse" de la balise body du fichier "pages/inc/header.php".
- Pour désactiver l'authentification, supprimez les 5 premières lignes du fichier "pages/inc/header.php".
- Pour changer le login et/ou le mot de passe, modifier la ligne correspondante (troisième) dans le fichier "pages/login.php".

##### Première page
- Vous pouvez mettre une icône sur les boutons (voir la liste ici) ou mettre un favicon récupéré sur le site en question (dans le répertoire inc/images).
- Il est très simple de remplacer le moteur de recherche du formulaire, il suffit de modifier l'URL dans la page "pages/index.php".

##### Calendrier
- Le fichier ics à afficher est à mettre dans le répertoire "plugins/ics-parser". Il est possible d'afficher plusieurs ics au sein du même calendrier, avec différentes couleurs, une simple boucle PHP est nécessaire.


**Si vous avez des questions ou des remarques, vous pouvez me contacter à [cette adresse](http://blog.elob.fr/index.php?contact).**
