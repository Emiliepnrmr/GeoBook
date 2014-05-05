L'application s'installe en déposant l'ensemble des fichiers du projet sur un serveur web. L'application nécessitant
l'utilisation d'un e page proxy votre serveur web doit pouvoir exécuter des pages ASP .Net (IIS) ou des pages JSP
(Apache Tomcat, par exemple)

## Installation sous IIS

Si vous souhaitez utiliser IIS 7:
- Copiez les fichiers du projets dans un répertoire de votre serveur IIS, par exemple: c:\Inetpub\wwwroot\GeoBook
- Convertisez ensuite votre répertoire en une application (dans le manager IIS, un clic-droit sur votre répertoire, puis
  "Convertir en application).
- Définissez le pool d'application sur la version la plus récente d'ASP .Net
- Retrouvez et définissez, dans le fichier config.js, la ligne suivante:
  ProxyURL: "/proxy/proxy.ashx",

Si vous disposez d'une version plus ancienne de IIS
- Contactez votre administrateur système pour la configuration et la sécurisation d'un répertoire et l'actvation d'ASP .Net
- Retrouvez et définissez, dans le fichier config.js, la ligne suivante:
  ProxyURL: "/proxy/proxy.ashx",

## Installation sous Apache Tomcat (ou autre)

- Copiez les fichiers du projets dans un répertoire de votre serveur IIS,
- Retrouvez et définissez, dans le fichier config.js, la ligne suivante:
  ProxyURL: "/proxy/proxy.jsp",


###Notes

L'application GeoBook peut être accédée en consultation dans IE 8 et 9 mais la conception de GeoBooks ne peut se faire
qu'avec une version 10 ou supérieure d'Internet Explorer. En revanche, GeoBook est supporté sur Firefox, Chrome et Safari.

Si vous utiliser IIS, vous pouvez modifier le filtrage des URL autorisées par votre page proxy, vous pouvez ouvrir et modifier les URL dans le fichier proxy.config se trouvant dans le répertoire proxy.


## Configurer l'application

Avant de commencer à utiliser GeoBook vous devez configurer quelques paramètres de base. Le fichier de configuration
de GeoBook se trouve à la racine de l'application et se nomme config.js. Ouvrir ce fichier et renseigner les paramètres
suivants:

"ApplicationName":
Il s'agit du titre de l'application, il s'affiche en haut de la page d'accueil.

"PortalURL": 
Il s'agit de l'URL du portail ArcGIS de votre organisation (ArcGIS Online ou Portal for ArcGIS)
Par exemple: http://<mon_organisation>.maps.arcgis.com

"ConfigSearchTag":
Il s'agit de la balise qui sera associée à tous les GeoBooks stocké sur ArcGIS Online. Les GeoBooks sont enregistrés
en tant qu'éléments de type "Application Web" dans votre portail. Cette balise sert à identifier les GeoBooks à afficher
dans l'application. Ne jamais modifier ou supprimer cette balise via votre portail.

"SortField":
Cette propriété permet de trier vos GeoBooks selon différentes méthodes:
- "title" Titre du GeoBook
- "owner" Les noms des auteurs des GeoBooks
- "avgRating" Le nombre de vote sur les GeoBooks
- "numViews" Le nombre de vues des GeoBooks
- "created" La date de création des GeoBooks
- "modified" La date de modification des GeoBooks

"SortOrder":
Permet de spécifier l'ordre de ce tri:
- "asc" Croissant
- "dec" Décroissant



Pour démarrer l'application GeoBook, vous utiliserez l'url suivante:
http://<your server>/GeoBook/default.htm

