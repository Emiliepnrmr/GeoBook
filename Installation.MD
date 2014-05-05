L'application s'installe en déposant l'ensemble des fichiers du projet sur un serveur web. 

Avec IIS
--------

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
