L'application s'installe en déposant l'ensemble des fichiers du projet sur un serveur web. L'application nécessitant
l'utilisation d'un e page proxy votre serveur web doit pouvoir exécuter des pages ASP .Net (IIS) ou des pages JSP
(Apache Tomcat, par exemple)

Installation sous IIS
---------------------

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

Installation sous Apache Tomcat (ou autre)
------------------------------------------

- Copiez les fichiers du projets dans un répertoire de votre serveur IIS,
- Retrouvez et définissez, dans le fichier config.js, la ligne suivante:
  ProxyURL: "/proxy/proxy.jsp",


Note
----

L'application GeoBook peut être accédée en consultation dans IE 8 et 9 mais la conception de GeoBooks ne peut se faire
qu'avec une version 10 ou supérieure d'Internet Explorer. En revanche, GeoBook est supporté sur Firefox, Chrome et Safari.

Si vous utiliser IIS, vous pouvez modifier le filtrage des URL autorisées par votre page proxy, vous pouvez ouvrir et modifier les URL dans le fichier proxy.config se trouvant dans le répertoire proxy.

Pour démarrer 
Begin using Briefing Book by browsing to the URL. http://<your server>/BriefingBook/default.htm
