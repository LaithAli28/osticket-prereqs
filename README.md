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

- Within the VM, download "osTicket-Installation-Files.zip" and extract to desktop. 
 The files in this folder are used to install osTicket and its dependencies.

- Install / Enable Internet Information Services (IIS) in Windows, along with CGI
Start at World Wide Web Services, navigate to Application Development Features, click enable CGI.

- Install the web server (PHP Manager) from within the osTicket-Installation-Files folder (PHPManagerForIIS_V1.5.0.msi), then install the rewrite module (rewrite_amd64_en-US.msi). Create a new folder on the C drive and rename it PHP. Extract all PHP files into our new folder.
 

- Once again from the osTicket-Installation-Files folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi) and HeidiSQL to create the database. We will name the database "osTicket".
Typical Setup, then Launch Configuration Wizard (after install), then Standard Configuration and set credentals 

- Open IIS as an administrator, register PHP from within IIS (PHP Manager to C:\PHP\php-cgi.exe). Reload IIS (Open IIS, Stop and Start the server)

- Install osTicket v1.15.8
From the osTicket-Installation-Files folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”.
Now within “c:\inetpub\wwwroot”, rename “upload” to "osTicket”

- Install HeidiSQL for database configuration

<h2>Installation Steps</h2>

<p>

![image alt](https://github.com/LaithAli28/osticket-prereqs/blob/main/P1.png?raw=true)

</p>
<p>
From the start menu, open Control Panel and click on "uninstall or change a program". Next, click "turn Windows features on or off". Check both IIS and CGI. This is important to ensure that the web server is properly installed. 
</p>
<br />

<p>

![image alt](https://github.com/LaithAli28/osticket-prereqs/blob/main/P2.png?raw=true)

</p>
<p>
 PHP Manager manages PHP installations on a Windows server, particularly with IIS. PHP Manager simplifies the configuration of PHP settings without the need of the command line. The Rewrite Module (rewrite_amd64_en-US.msi) is a dependency for installation followed by creating the new PHP folder on the C drive and extracting all PHP files into the new folder to ensure osTicket is properly installed. 

</p>
<br />

<p>

![image alt](https://github.com/LaithAli28/osticket-prereqs/blob/main/P3.png?raw=true)

</p>
<p>
MySQL is an open-source, relational database management system (RDBMS). MySQL is used to store, retrieve, and manage data in structured formats using SQL (Structured Query Language).  
</p>
<br />


<p>

![image alt](https://github.com/LaithAli28/osticket-prereqs/blob/main/P4.png?raw=true)

</p>
<p>
Registering PHP Manager from within IIS is required for making the web server aware of the existence of PHP on the computer. Be sure to restart IIS after PHP Manager has been registered. 
</p>
<br />

<p>

![image alt](https://github.com/LaithAli28/osticket-prereqs/blob/main/P6.png?raw=true)

</p>
<p>
From the osTicket-Installation-Files folder, unzip “osTicket-v1.15.8.zip”. Copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket." This ensures that osTicket is successfully installed.

</p>
<br />

<p>

![image alt](https://github.com/LaithAli28/osticket-prereqs/blob/main/P7.png?raw=true)


</p>
<p>

You'll notice that not all extensions are enabled. For osTicket to work properly, we must enable the following extensions: "php_imap.dll", "php_intl.dll", and "php_opcache.dll". This can be done from PHP Manager through IIS.
  

</p>
<br />

<p>

<p>


</p>
<p>
 

</p>
<br />

<p>

![image alt](https://github.com/LaithAli28/osticket-prereqs/blob/main/P9.png?raw=true)

</p>
<p>
HeidiSQL is an application that is required to connect to the database and perform configurations, and is one of the dependencies for osTicket. Start a new session within HeidiSQL in order to establish a connection to the database and rename it "osTicket". To do this, we right click the blue fin icon next to "Unnamed" and select create new, then click database and name it osTicket.  
  
</p>
<br />

<p>

<p>

![image alt](https://github.com/LaithAli28/osticket-prereqs/blob/main/P10.png?raw=true)

</p>
<p>

With this, osTicket has been successfully installed! 
  
</p>
<br />

<p>
