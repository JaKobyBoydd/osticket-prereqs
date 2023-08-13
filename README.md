<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket Installation</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Computer)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Files</h2>

- PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
- Rewrite Module (rewrite_amd64_en-US.msi)
- PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip
- VC_redist.x86.exe
- MySQL 5.5.62 (mysql-5.5.62-win32.msi)
- osTicket v1.15.8
- Heidi SQL

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/Q9drXaH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/77tarHV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p> 
<p>
The first step is to enable "Internet Information Services" (IIS). That is done by going to the control panel and under the "Turn windows features on and off" tab, 
checking the CGI box under the "Application and development features" tab. Afterwards make sure all the boxes under the "Common HTTP features" tab are checked, then click okay. In order to check if IIS is enabled, go to a web browser and in the browser search bar type, 127.0.0.1, and this should take you to a web page like the one shown in the second image above.  
</p>
<br />


<p>
After enabling IIS, you can now download all the necessary files. It must be noted that in regards to the PHP 7.3.8 file, you need to create a PHP folder in the root of the C drive. After creating that folder, download the file, extract all, and unzip it into the PHP folder. When downloading MYSQL, make sure to choose the "Typical" setup and "Standard" Configuration. Remember the username and password for MySQL because it will be needed when setting up Heidi SQL. Once that is done, open IIS as an Admin by typing IIS in the windows search bar and click on PHP Manager. Register new PHP and choose the highlighted file found in the PHP folder on the C drive as shown in the image below. Reload IIS and stop/start server.
</p>
<br />
<p>
<img src="https://i.imgur.com/0CDzdx3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Install osTicket v1.15.8 and download osTicket from the Installation Files Folder. Extract and copy “upload” folder to c:\inetpub\wwwroot and within c:\inetpub\wwwroot, Rename “upload” to “osTicket” Then within IIs, go to "Sites" in the top left corner, Default, osTicket, in the browse tab on the right click, "Browse*:80". Now there are a few extensions that need to be enabled and those extensions are found within PHP manager in IIS. Click on the "enable or disable extensions" link under PHP Extensions and enable the following: (php_imap.dll) (php_intl.dll) (php_opcache.dll) *See Image Below*  After enabling the extensions, the file, "ost-sampleconfig.php" in the include folder, needs to be renamed to, "ost-config.php". This file can be located by going to the following folders:  C:\inetpub\wwwroot\osTicket\include. 
<p>
<img src="https://i.imgur.com/JTfggby.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
Disable inheritance on the ost-config.php file by; right clicking the file, going to properties, selecting the security tab, choosing advanced and the disable inheritance option will be available there. Be sure to choose the option that removes all inherited permissions. To add permissions for either everyone or selected persons; click on add in the security tab, select principle and in the box you can add whoever needs permissions. Continue setting up OsTicket in the browser.
<br />
<p>
The last step is to download and install Heidi SQL. Once that is downloaded, create a new session and use the same username/password chosen for MySQL. Finally, create a new database by; right clicking unnamed, choosing create new and selecting database. *See Image Below*  Name the database and in the OsTicket browser, under MySQL Database, type that same name. Finally, hit install and you're all done!   
</p>




<p>
<img src="https://i.imgur.com/u7FTfyB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

