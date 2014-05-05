L'application s'installe en déposant l'ensemble des fichiers du projet sur un serveur web. L'application nécessitant
l'utilisation d'un e page proxy votre serveur web doit pouvoir exécuter des pages ASP .Net (IIS) ou des pages JSP
(Apache Tomcat, par exemple)

Installation sous IIS
---------------------

Si vous souhaitez utiliser IIS 7:
- Copiez les fichiers du projets dans un répertoire de votre serveur IIS,
- Convertisez ensuite votre répertoire en une application
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
  ProxyURL: "/proxy/proxy.ashx",



he application is published by moving the application files to a web server, converting them to an application, and defining 
the application pool using Microsoft Internet Information Services (IIS). This workflow uses Microsoft IIS 7. If you are 
using a different version, modify the workflow as necessary. Contact your server administrator for information about setting 
up the application on a virtual directory, server security, or installing and configuring ASP.NET.

Note
Briefings and reports can be viewed with Internet Explorer 8 and 9 but can only be authored with these Internet Explorer versions if the application is published with a SSL Certificate. Briefing and report authoring is fully supported on Firefox, Chrome and Safari.
To publish Briefing Book as an application, complete the following steps:

Using Windows Explorer, browse to the BriefingBook\Proxy folder and open the proxy.config file in Microsoft Notepad or another text editor. Enter the URL for your ArcGIS Online organization and Portal for ArcGIS site, then save the file and exit.
Copy the BriefingBook folder to your web server so it can be accessed as a website or virtual directory. In Microsoft Internet Information Services (IIS), the default web server directory is <your directory>\Inetpub\wwwroot\.
Browse to Start > Control Panel > Administrative Tools > Internet Information Services (IIS) Manager.
Click <your server> > Sites > Default Web Sites.
Right-click the web server directory folder for the application and choose Convert to Application.
Choose the ASP.NET v4.0 application pool.
Note
If you do not see ASP.NET v4.0 as an option in the menu, install and configure it with your web server.
Click OK.
Begin using Briefing Book by browsing to the URL. http://<your server>/BriefingBook/default.htm
