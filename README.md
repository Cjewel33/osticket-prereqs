<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
This is an easy guide to installing a help desk ticketing system called osTicket.<br/>


<h2> Files You Need to Download</h2>

- ### [Download Now](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

<h2> Software & Technologies  Used</h2>

- Windows 10 (Build 19044)
- Microsoft Azure (Virtual Machines)
- Remote Desktop (RDP)
- Internet Information Services (IIS)

  <h2> Prerequisites </h2>

- Create a Virtual Machine in Azure
- Install osTicket v1.15.8
- Install HeidiSQL
- Install MySQL
- Install PHP
- install Microsoft Visual C++ Redistributable
  <h2>Steps</h2>
<h3 align="center">Create Virtual Machine in Azure</h3>
<br />
<p>
<h3 align="center">First, start by creating a Resource Group inside Azure.</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/eBi5k2l.png" height="75%" width="100%" />
</p>
<p>
<h3 align="center">Now, create a Windows 10 Virtual Machine (VM), typically with 2-4 Virtual CPUs. For username and password, it can be anything as we'll be using this info to remote in with our main computer. When creating the Virtual Machine (VM), allow Azure to create a new Virtual Network (Vnet):</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/dEF1c7h.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Open your Remote Desktop Connection app on your computer and connect to your Virtual Machine that was created in Azure. </h3>
<br />
<p>
	<img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/2e71fd86-4198-47aa-aa1a-d0aed1b8e0eb"/>
	

</p>
<br />
<br />
<h3 align="center">Now we need to install / Enable IIS in Windows. Go to your Search Bar > Type "Control Panel" > Click "Programs" > "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS).</h3>
<br />
<p>
	<img src="https://i.imgur.com/iB0DDRd.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Once clicked, find the "Internet Information Services" expand it and then expand the "World Wide Web" tab. Afterward, expand the application Developer tab. Finally check the "CGI" button & press Ok. You will need CGI to download the PHP Manager. The PHP manager is a back-end web programming language that allows osTicket to run off a web browser.</h3>
<br />
<p>
  <img src="https://github.com/Cjewel33/osticket-prereqs/assets/50834280/a6af9c35-e10c-4d7e-b2c8-30ffbe128f08" height="75%" width="100%"/>
</p>
<br />
<h3 align="center">Install PHP Manager</h3>
<br />
<p>
<h3 align="center">Download the PHP manager file, and agree with all the terms. We've now downloaded the PHP manager into our operating system.</h3>
<p>
       <img width="860" alt="Screenshot 2025-03-11 114627" src="https://github.com/user-attachments/assets/e3a4db57-9c32-486a-8543-259c0c3a7d41" />

</p>
<br/>
<h3 align="center">Install Rewrite Module</h3>
<br />
<p>
<h3 align="center">Download the Rewrite Module file, agree with all the terms and it should now be installed onto the Computer.</h3>
<p>
  <img src="https://github.com/Cjewel33/osticket-prereqs/assets/50834280/28cf2dd0-d39e-45f8-a01b-61aec6657228"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<br />
<p>
<h3 align="center"> Open File Explorer, type, "C:\" in the search bar, Right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from<a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> Files You Need to Download</a>, Extract it by going to where you download the file, Right-click the PHP 7.3.8 file and press extract to the PHP Folder you just created.
</h3>
<p>
  <img <img width="719" alt="Screenshot 2025-03-11 122349" src="https://github.com/user-attachments/assets/e07feb0c-c673-4125-af69-d622c89a87ad" />

</p>
<br/>
<h3 align="center">VC_REDIST DOWNLOAD</h3>
<br/>
<h3 align="center"> Download and install VC_Redist, Agree with any terms and agreements and finish installing.
</h3>
<p>
  <img src="https://i.imgur.com/Gx8ryBV.png"75%" width="100%"/>
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Download and install MySQL, Agree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket. 
</h3>
<p>
  <img width="790" alt="Screenshot 2025-03-11 121744" src="https://github.com/user-attachments/assets/9049aa12-6542-4a79-a134-a3461d6fd55b" />
>
<br/>
  <img src="https://i.imgur.com/zdhWXNx.png" height="75%" width="100%" />
</p>
<br/>
<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket (download from within lab files: link).
</p>
<p>
	Extract and copy the “upload” folder INTO c:\inetpub\wwwroot:
</p>
	<img src="https://i.imgur.com/0MUJLMU.png" height="75%" width="100%" />
	<img width="714" alt="Screenshot 2025-03-12 213039" src="https://github.com/user-attachments/assets/a4d55255-9c8e-488b-93b7-51b4a08afccd"/>
 />
<p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
	<img width="674" alt="Screenshot 2025-03-12 212728" src="https://github.com/user-attachments/assets/2ba74771-a26e-482f-806d-aa9e7a73cd55"/>
 />
</p>
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
<br />
<p>
	Go to sites -> Default -> osTicket:
</p>
<p>
	<img src="https://i.imgur.com/QeWNlG3.png" height="75%" width="100%" />
</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img src="https://i.imgur.com/3iXhNbi.png" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
<br />
<p>
	Go back to IIS, sites -> Default -> osTicket.
</p>
<p>
	Double-click PHP Manager:
</p>
<p>
	<img src="https://i.imgur.com/LFKo5Hs.png" height="75%" width="100%" />
</p>
<p>
	Click “Enable or disable an extension”.
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<p>
	<img src="https://imgur.com/a/nrQo0kz" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<p>
	<img src="https://i.imgur.com/6iSNd4H.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img width="773" alt="image (1)" src="https://github.com/user-attachments/assets/8ea6b13c-dc9a-409f-aeb4-e78463dde598"/>
 />
</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:
</p>
<p>
	<img src="https://i.imgur.com/1QtRWEF.png" height="75%" width="100%" />
</p>
<p>
	New Permissions -> Everyone -> All:
</p>
<p>
	<img src="https://i.imgur.com/YzsMXNX.png" height="75%" width="100%" />
</p>
<p>
	<img src="https://i.imgur.com/k7x9yGR.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Name Helpdesk.
</p>
<p>
	Default email (receives email from customers):
</p>
<p>
	<img src="https://i.imgur.com/rvMvlNC.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/YszhIpl.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/AEg0b2P.png" height="75%" width="100%" />
</p>
<p>
	Create a new session, root/Password1.
</p>
<p>
	Connect to the session:
</p>
<p>
	<img src="https://i.imgur.com/9t51ApR.png" height="75%" width="100%" "/>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/vXzmQqg.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: Password1:
</p>
<p>
	<img src="https://i.imgur.com/akDyber.png" height="75%" width="100%" />
</p>
<p>Click “Install Now!”</p>
<p>Congratulations, hopefully it is installed with no errors!</hp>
<p>
	<img src="https://i.imgur.com/J5omRoE.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Clean up</h3>
<br />
<p>
	Delete: C:\inetpub\wwwroot\osTicket\setup:
</p>
<p>
	<img src="https://i.imgur.com/eg0ZPG3.png" height="75%" width="100%" />
</p>
<p>
	Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/n6k46XL.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/8wvWH0H.jpg" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
