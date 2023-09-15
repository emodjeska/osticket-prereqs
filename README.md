<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Connect to your Virtual Machine with Remote Desktop.
- Install / Enable IIS in Windows.
- Install Web Platform Installer.
- Install osTicket v1.15.8.
- Download and Install HeidiSQL.
- Created database for "osTicket.
- Clean up.
- Change File Permissions. 

<h2>Installation Steps</h2>


![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/6ef4735c-bf21-41f4-8ea6-470984d10d90)


Firstly, we are going to install IIS (Internet Information Dervices) with CGI and common HTTP features. From your Windows search bar go to "programs", then select "uninstall a program" and go to "Turn Windows features on and off". From here, be sure to select CGI and turn on all the common HTTP features.

Now that we have downloaded IIS, we can download Web Platform Installers (Web PI), this program allows a simplifed installation workflow for installing common open source web applications, like osTicket. Once these programs are running on your windows computer, and we have added MySQL 5.5 database, PHP 5.6.31, and the various verisons of between PHP (x86) 7.0 and 7.3, then we are ready to install osTicket.
</p>
<br />

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/9774500a-b229-487d-aaeb-a3d816807f98)

From the downloaded files, we can now install and extract the osTicket file. Extract and copy the “upload”.  reload IIS. Go to sites -> default -> osTicket, from here on the top righthand side of the sreen you will select "restart" and the system will restart with osTicket installed.

 go back to IIS, sites -> Default -> 1. osTicket 2. Double-click PHP Manager 3. Click Enable or disable an extension 1. Enable: php_imap.dll 2. Enable: php_intl.dll 3. Enable: php_opcache.dll -

Assign Permissions: ost-config.php To change the permissions, right-click ost-config --> select 'properties' --> select the 'Security' tab at the top --> select the 'Advanced' button1. Disable inheritance -> Remove All 2. New Permissions -> Everyone -> All

When you have allowed permissions to your computer, you will have to download and install HeidiSQL from google drive using the provided defaults that are provided in the install wizard.

</p>
<br />

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/0af0aba0-e2db-4624-b01e-0ac61a584498)


Open and download HeidiSQL. create a new session and assign it a username and password. Then create a database called "osTicket". Enter your information (username and Password) into osTicket installer and click "Install". Congradulations, hopefully osTicket will be installed correctly into your computer. From here you are able to access the "Staff Contol Panel" to do administative tasks and the "End User Portal" to access and complete tickets. 

From here, you are able to set up osTicket to fit the needs of your business. 

Thank you for joining me today, to install and set up osTicket. 
</p>
<br />
