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


Welcome to this tutorial on how to install and set up OS Ticket, a common ticketing system used in many Help Desk senarios. This lab will help us get a greater sense of how ticketing system work from an admin position to being a customer. Let's get into it.

First things first, Go into Azure and set up a virual Machine that is running Windows 10. Then use remote desktop to log into the newly generated PC.

Now that we are all set up, we are going to install IIS (Internet Information Dervices) with CGI and common HTTP features. From your Windows search bar go to "programs", then select "uninstall a program" and go to "Turn Windows features on and off". From here, be sure to select CGI and turn on all the common HTTP features.

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/934a6ea6-26c7-4eb3-a1bb-90744c2a97ee)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/9bb534cb-34fd-4ff7-bc19-9cd170f3f87d)


Now that we have downloaded IIS, we can download PHP Mangager and Rewrite Module, these programs allow a simplifed installation workflow for installing common open source web applications, like osTicket. Once these programs are running on your windows computer, and we have added MySQL 5.5 database, PHP 5.6.31, and the various verisons of between PHP (x86) 7.0 and 7.3, then we are ready to install osTicket. Download osticket onto your system. All these downloads can be found on the simple list found here.

https://docs.google.com/document/d/12QH7yrsaiUfYNOgZK7KgTSZQSJ-HYTSVcGFildWMRig/edit#bookmark=id.cajb4ktub1km
</p>
<br />

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/e1490b73-3fa1-4fee-9b79-0e324eb4351f)

From the downloaded files, we can now install and extract the osTicket file. Extract and copy the “upload” file and drag it into the c inetpub wwwroot folder, found in the windows c folder at the bottom of the downloads.  You must then rename the new "upload" file as "osTicket". Then we will reload IIS and restart the system. Then OS Ticket should be downloaded.

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/1e2daf2c-d845-49dc-8bf5-d5f5c0523c7e)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/2346de50-2e9f-4cb0-a254-8073d679ff0d)

 go back to IIS, sites -> Default -> osTicket -> Double-click PHP Manager -> Click Enable or disable an extension
 

Assign Permissions: ost-config.php To change the permissions, right-click ost-config --> select 'properties' --> select the 'Security' tab at the top --> select the 'Advanced' button
1. Disable inheritance -> Remove All
2.  New Permissions -> Everyone -> All

When you have allowed permissions to your computer, you will have to download and install HeidiSQL from google drive using the provided defaults that are provided in the install wizard.

</p>
<br />

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/0af0aba0-e2db-4624-b01e-0ac61a584498)


Open and download HeidiSQL. create a new session and assign it a username and password. Then create a database called "osTicket". Enter your information (username and Password) into osTicket installer and click "Install". Congradulations, hopefully osTicket will be installed correctly into your computer. From here you are able to access the "Staff Contol Panel" to do administative tasks and the "End User Portal" to access and complete tickets. 

From here, you are able to set up osTicket to fit the needs of your business. 

Thank you for joining me today, to install and set up osTicket. 
</p>
<br />
