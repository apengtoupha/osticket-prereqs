<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- osTicket Prerequisites/Installation Walkthrough https://www.youtube.com/watch?v=FyZaUnCpqPc

<h2>Environments and Technologies Used</h2>

- Microsoft Azure Virtual Machine
- Remote Desktop Connection
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro

<h2>List of Prerequisites</h2>

- Within the virtual machine, download the osTicket-Installation-Files.zip and unzip it onto the desktop. The folder should be called “osTicket-Installation-Files.”
 The files in this folder are used to install osTicket and some of the dependencies.

- Install / Enable Internet Information Services (IIS) in Windows, along with CGI
World Wide Web Services -> Application Development Features -> enable CGI

- Install the Web Server (PHP Manager) from within the “osTicket-Installation-Files” folder (PHPManagerForIIS_V1.5.0.msi). Followed by installing the Rewrite Module (rewrite_amd64_en-US.msi). Create a new folder on the C drive and rename it PHP. Extract all PHP files into to the new PHP folder onto the C drive.
 

- From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) and HeidiSQL to create the database. Rename to osTicket.  
Typical Setup ->
Launch Configuration Wizard (after install) ->
Standard Configuration ->
Set credentals 

- Open IIS as an Administrator... Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe). Reload IIS (Open IIS, Stop and Start the server)

- Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”

- Install HeidiSQL for database configuration

<h2>Installation Steps</h2>

<p>

 ![sc](https://github.com/user-attachments/assets/7e265625-d5d8-4986-9df0-9c95b348119b)

</p>
<p>
From the start menu, open control panel and click on "uninstall or change a program". Next, click "turn Windows features on or off". Check Internet Information Services followed by expanding the folder to also check CGI. This feature is important to ensure that the web server is properly installed. 
</p>
<br />

<p>

 ![image](https://github.com/user-attachments/assets/bfd7ff86-3571-4065-8b2b-3dfb87dd681f)

</p>
<p>
 PHP Manager is a tool used for managing PHP installations on a Windows server, particularly with Internet Information Services (IIS). PHP Manager helps administrators manage multiple PHP versions and configure various PHP settings without manually editing configuration files or performing complex command-line operations. The Rewrite Module (rewrite_amd64_en-US.msi) is a dependency for installation followed by creating the new PHP folder on the C drive and extracting all PHP files into the new folder to ensure osTicket is properly installed. 

</p>
<br />

<p>

 ![image](https://github.com/user-attachments/assets/5aa0e194-5c93-4076-9c33-8a4a81a69b8e)

</p>
<p>
MySQL is an open-source, relational database management system (RDBMS). MySQL is used to store, retrieve, and manage data in structured formats using SQL (Structured Query Language).  
</p>
<br />


<p>

 ![image](https://github.com/user-attachments/assets/1b0b9a9c-a76f-4968-8bb1-8170c1e3125a)

</p>
<p>
Registering PHP Manager from within IIS is required for making the web server aware of the existence of PHP on the computer. Be sure to restart Internet Information Services after PHP Manager has been registered. 
</p>
<br />

<p>

 ![image](https://github.com/user-attachments/assets/a79a4808-c7c6-4237-9732-115db357d10c)

</p>
<p>
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip”. A new folder will appear named upload. Copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket." This ensures that osTicket is successfully installed on the computer. 

</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/ab35a793-8626-44e4-b050-dab275a83014)


</p>
<p>

Note that not all extensions are enabled. For osTicket to work properly, we must check some boxes to enable the following extensions... "php_imap.dll", "php_intl.dll", and "php_opcache.dll". This can be done through PHP Manager from within Internet Information Services (IIS)
  

</p>
<br />

<p>

<p>

![image](https://github.com/user-attachments/assets/3485f7bb-1aa4-4e62-a993-4f88ff96b489)

</p>
<p>

HeidiSQL is an application that is required for allowing us to make a connection to the database and perform configurations. HeidiSQL is one of the dependencies for osTicket.   

</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/2f8f2683-5199-41a7-8443-592b12f6b87d)

</p>
<p>

Start a new session from within HeidiSQL in order to establish a connection to the database and rename it osTicket. Right click the blue fin icon next to "Unnamed" and select create new, then click database. Name the database osTicket.  
  
</p>
<br />

<p>

<p>

![sc5](https://github.com/user-attachments/assets/79bdbc68-dab7-42f6-a237-24949c807afd)

</p>
<p>

osTicket has been successfully installed! 
  
</p>
<br />

<p>
