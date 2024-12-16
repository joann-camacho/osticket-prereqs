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

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Create and Log Into the Azure VM
- Download and Prepare the osTicket Files
- Install IIS and Enable CGI
- Install File Dependencies
- Install and Configure MySQL
- Install osTicket and Configure Settings
- Complete osTicket Set Up

<h2>Installation Steps</h2>


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>

<p>
  
![image](https://github.com/user-attachments/assets/799ee796-80a5-4151-b74e-f6d1b9c187ff)
</p>
<p>
Within the VM, download the https://tinyurl.com/y68yenz5, and unzip it onto the desktop. The folder should be called "osTicket-Installation-Files".
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/3393574b-cc80-43d3-8f01-99d4cd6d628e)

</p>
<p>
From the Control Panel> Programs> Turn Windows feature on and off. Install/ Enable IIS in Windows, with CGI selected.
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/66291ab9-aa61-4db0-babf-d888ecde566c)

</p>
<p>
From the “osTicket-Installation-Files” folder, Install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />

<p>

  ![image](https://github.com/user-attachments/assets/8ea4d5fe-a3b7-45ce-800c-cbd6e945e6e5)

</p>
<p>
From the “osTicket-Installation-Files” folder, Install the Rewrite Module (rewrite_amd64_en-US.msi)

</p>
<br />

<p>
  
![image](https://github.com/user-attachments/assets/d2765821-4e15-4b83-bd57-e635dc22fd65)
</p>
<p>
Create the directory C:\PHP. (Open File Explorer and create a new folder named PHP at C:\PHP)
From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/8489004b-254b-44ce-8477-3e4e42d01da0)
</p>
<p>
From the “osTicket-Installation-Files” folder, Install VC_redist.x86.exe.
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/9d7467b6-20fb-441a-8589-e0287f6ff2df)
</p>
<p>
Install MySQL:
From the osTicket-Installation-Files folder, double-click mysql-5.5.62-win32.msi to install MySQL.
Select Typical Setup and launch the Configuration Wizard after installation.
Set Standard Configuration, and for Username, enter root and for Password, enter root.
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/5f411fff-1c8e-45b9-a7ae-b869a3f6d38c)

</p>
<p>
Open IIS as an Admin
Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
Reload IIS (Open IIS, Stop and Start the server)
</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/dfa06715-ab2e-4b9b-b0b8-91c2be414fa5)

</p>
<p>
Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>
<br />

<p>
  
![image](https://github.com/user-attachments/assets/a416fef9-5605-4039-9602-a5d8017ecaaf)
![image](https://github.com/user-attachments/assets/d0f6c25d-1ecf-4bbf-b9af-ae447b5357fe)
![image](https://github.com/user-attachments/assets/df36ef58-7f6a-4b07-84e0-fec3437af989)


</p>
<p>
Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

</p>
<br />

<p>

![image](https://github.com/user-attachments/assets/a2c51788-7d4d-4c60-86f7-1baaf4bcde9a)
![image](https://github.com/user-attachments/assets/652e1fd2-fc95-4c7a-a25a-7f1209be4584)

</p>
<p>

Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
