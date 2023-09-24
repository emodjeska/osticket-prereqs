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


Welcome to this tutorial on how to install and set up OS Ticket, a common ticketing system used in many Help Desk senarios. This lab will help us get a greater sense of how ticketing system work from an admin position, an agent, and a end-user Let's get into it.

First things first, Go into Azure and set up a virual Machine that is running Windows 10. Then use remote desktop to log into the newly generated PC. Use the IP address found in the azure portal to connect to it.

Now that we are all set up, we are going to install IIS (Internet Information systems) with CGI and common HTTP features. From your Windows search bar go to "programs", then select "Turn Windows features on and off". From here, be sure to select CGI and turn on all the common HTTP features.

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/934a6ea6-26c7-4eb3-a1bb-90744c2a97ee)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/9bb534cb-34fd-4ff7-bc19-9cd170f3f87d)

Now that we have downloaded IIS, we can download PHP Mangager, Rewrite Module, along with a few other downloads. These programs allow a simplifed installation workflow for installing common open source web applications, like osTicket. We are going to install PHP Mangaer, Rewrite Admin, and VC_redist, mysql5.5.62, and the various versions of PHP from a folder found in the simple list below. Note, when you install the PHP folder, you will have to unzip the folder by right clicking it and exporting its contents into the C:/ PHP folder (Create directory by creating a PHP folder within the Windows C folder). Finally, download osticket onto your system. All these downloads can be found on the simple list found here.

https://docs.google.com/document/d/12QH7yrsaiUfYNOgZK7KgTSZQSJ-HYTSVcGFildWMRig/edit#bookmark=id.cajb4ktub1km
</p>
<br />

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/e1490b73-3fa1-4fee-9b79-0e324eb4351f)

From the downloaded files, we can now install and extract the osTicket file. Extract and copy the “upload” file and drag it into the c inetpub wwwroot folder, found in the windows c folder at the bottom of the downloads.  You must then rename the new "upload" file as "osTicket". Then we will reload IIS and restart the system. Then OS Ticket should be downloaded.
After we go back to IIS, sites -> Double-click PHP Manager -> Click Enable or disable an extension, we will be ready to open OS Ticket.

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/1e2daf2c-d845-49dc-8bf5-d5f5c0523c7e)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/2346de50-2e9f-4cb0-a254-8073d679ff0d)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/0d058043-5949-419e-a394-49166c05bc8a)

 When you click on Browse *80, you should see this screen pop up, letting you know that you have successfully downloaded OS Ticket.

 ![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/b1a51bc5-9586-4a80-89f0-8fb82a6f8e6a)

 Now go back to IIS -> Sites-> default -> osTicket -> double click "Enable or disable extention" -> Enable php_imap.dll, php_intl.dll, and php_pocache.dll.

 ![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/d45a5eeb-f26b-4011-a844-18feaa53fbd1)

 Now you should be able to go back into osTicket and observe the changes.

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/71d78b1b-b3fe-476a-89e0-5f66f96353c8)

Go into wwwroot folder and rename "ostsample-config" "folder to ost-config" 

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/de3d2192-9c1a-420b-9f82-31a92798d9ce)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/688693f2-ad98-44de-acfa-bf7ff7fbd278)

Assign Permissions: ost-config.php. To change the permissions, right-click ost-config -> select 'properties' -> select the 'Security' tab at the top -> select the 'Advanced' button
1. Disable inheritance -> Remove All
2.  New Permissions -> Everyone -> All

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/05e9a2ed-0677-461a-8abd-1869644e3d87)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/66ec4849-7352-4b3e-bb48-4c38dd4bbb35)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/ae278fcf-4427-4964-8e3a-07a460a2dc92)

We will now hit continue on the OS Ticket installation page and fill out our basic information.

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/46047cca-6338-4017-abf6-3673e733de5b)

When you have allowed permissions to your computer, you will have to download and install HeidiSQL from google drive using the provided defaults.

Open and download HeidiSQL. create a new session and assign it a username and password. Then create a database called "osTicket". Enter your information (username and Password) into the osTicket installer and click "Install".

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/fd0c9159-df92-491a-ad3f-36a414885414)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/161b641e-e0c2-43d1-87e5-3fc595211142)

We now have a Hiedi databased named osTicket. Go back to the osTicket installer and input the information you just created in the SQL server.

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/ffe22b4f-ba35-4c80-8d11-ba2de5c06127)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/33bdd80a-4cec-4956-a908-3e95b791f42a)

Now that we have OS Ticket successfully installed on our computer, we are going to clean up by deleting the "setup" folder within our "wwwroot" folder. We will also go back into the "ost-config.php" file and set it to read only. If you do not remember where that is, it is in our "include" folder found within the "wwwroot" folder.

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/e4f44acd-30ba-473c-8cc2-2a09b5689c93)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/cf944cc2-0334-473f-884a-8e7d52bf97bc)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/d0dd6539-7161-4bd7-b93b-dafdbcc0c0ec)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/1b22d5e1-4d1f-4f4f-8d12-f020f3f2fd8c)

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/7350be71-16a5-431c-8c49-ee8594043fd6)

Congradulations! You succesfully downloaded OS Ticket!

![image](https://github.com/emodjeska/osticket-prereqs/assets/143763072/a3c390e5-cf94-4d31-a88a-522791f523af)

From here, on your VM, You may access the staff portal through this link.
http://localhost/osTicket/scp/login.php

and you may access the End-User portal through this link.
 http://localhost/osTicket/ 

From here, you are able to set up osTicket to fit the needs of your business. 

Thank you for joining me today, to install and set up osTicket. 

