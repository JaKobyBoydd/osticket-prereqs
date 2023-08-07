<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket Installation</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

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
After enabling IIS, you can now download all the necessary files. It must be noted that in regards to the PHP 7.3.8 file, you need to create a PHP folder in the root of the C drive. After creating that folder, download the file, extract all, and unzip it into the PHP folder. When downloading MYSQL, make sure to choose the "Typical" setup and "Standard" Configuration. Once that is done, open IIS as an Admin by typing IIS in the windows search bar and click on PHP Manager. Register new PHP and choose the highlighted file found in the PHP folder on the C drive as shown in the image below. Reload IIS and stop/start server.
</p>
<br />
<p>
<img src="https://i.imgur.com/0CDzdx3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />


Install osTicket v1.15.8 and download osTicket from the Installation Files Folder. Extract and copy “upload” folder to c:\inetpub\wwwroot and within c:\inetpub\wwwroot, Rename “upload” to “osTicket” Then within IIs, go to "Sites" in the top left corner, Default, osTicket, in the browse tab on the right click, "Browse*:80". Now there are a few extensions that need to be enabled and those extensions are found within PHP manager in IIS. Click on the "enable or disable extensions" link under PHP Extensions and enable the following: (php_imap.dll) (php_intl.dll) (php_opcache.dll) 
*See Image Below*
<p>
<img src="https://i.imgur.com/JTfggby.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>



<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
