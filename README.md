<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This walkthrough provides an overview of the prerequisites and installation steps for osTicket, an open-source help desk ticketing system.
.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11

<h2>List of Prerequisites</h2>

- Resource group named seasons
- Windows 11 virtual machine named Summer

      Use the same resource group and region
      Size: Standard_D4s_v3 – 4 vcpus, 16 GiB memory
      Username: Summerfield
      Password: Summerfestival2
- Use Remote Desktop to login to the Summer virtual machine

<h2>1. Install and Enable IIS with CGI</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/e6fe64c9-33f1-4a41-aa5b-926153ae3bdb width="50%" height="auto" alt="IIS CGI"/>

Make sure IIS Management Console is checked

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/f5948f57-6c88-47d8-b41a-a9a71a46b09b width="50%" height="auto" alt="IIS Managment Console"/>


Check all common HTTP Features


<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/e49d2a91-d0e9-4bcd-8b5e-fb789a0ac141 width="50%" height="auto" alt="IIS HTTP"/>

Test local host (127.0.0.1)

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/10f21212-20dc-4cf1-a455-ec3e1e8f6cfa width="50%" height="auto" alt="local host"/>

<h2>2. Download and install PHP manager</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/68fe43ba-c567-4118-a890-b2b1e2d81541 width="50%" height="auto" alt=PHP Manager/>

<h2>3. Download and install Rewrite Module</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/372bc66d-fb50-4884-b0b7-099d02a4428b width="50%" height="auto" alt="Rewrite Module"/>

<h2>4. Create C:\PHP directory</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/6da19523-eaf4-4c7f-86b7-fc12ccb65ecc width="50%" height="auto" alt="C:\PHP"/>

<h2>5. Download PHP 7.3.8 and unzip into C:\PHP</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/1b8868d9-f578-4b70-93e9-427126ee6484 width="50%" height="auto" alt="new folder C:"/>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/890cf7e0-d2f6-4b1f-a473-97be06222150 width="50%" height="auto" alt="Extract all PHP"/>


<h2>6. Download and Install VC_redist.x86.exe</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/f402e671-1af5-421d-98bd-3d9f25c3c510 width="50%" height="auto" alt="Visual C++"/>

<h2>7. Download and Install MySQL 5.5.62</h2>

Choose a typical setup

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/d03d0406-4cde-4c63-8efb-e8cee779316c width="50%" height="auto" alt="typical setup"/>

Launch Configuration and select Standard

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/a46dda4b-4ca9-43cd-a44d-d525e72f0f58 width="50%" height="auto" alt="standard configuration"/>

The username will be root. The password will be SunDown1

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/b7f3547a-fa1a-408d-903d-7a401f87b12f width="50%" height="auto" alt="root password"/>

<h2>8.Open IIS as an Admin and register PHP</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/ad22e29a-cddd-46b3-a562-b939030ff6d4 width="50%" height="auto" alt="ISS Admin"/>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/6faea20b-4cb0-44e5-be43-f8eeaf39ca46 width="50%" height="auto" alt="register PHP"/>

<h2>9. Download osTicket</h2>

Extract and copy "upload" folder to c:\inetpub\wwwroot

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/746c46f2-53dd-41e3-803f-7f74bea4dafc width="50%" height="auto" alt="upload folder"/>

Rename upload as "osTicket"

<h2>10. Reload IIS (restart server)</h2>

<h2>11. On IIS go to sites → Default → osTicket</h2>

Click on "Browse *:80"


<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/cf25e7bd-ce86-45cb-8925-a4c061f3c6f0 width="50%" height="auto" alt="Browse *:80"/>

<h2>12. On IIS→ Sites→ Default Web Site→ osTicket→ PHP Manager, Enable these PHP Extensions</h2>

      Enable: php_imap.dll
      Enable: php_intl.dll
      Enable: php_opcache.dll

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/d4b44fb9-159f-4e85-bf0c-559d0a219719 width="50%" height="auto" alt="php enable"/>


Refresh osTicket Browser

<h2>13. Rename: ost-sampleconfig.php to ost-config.php</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/1fbc1948-c33b-4f7f-852a-e1c4390f9b82 width="50%" height="auto" alt="rename os-sampleconfig"/>

Assign permission to everyone

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/5002b315-686d-4d9c-9391-1a4ca824de10 width="50%" height="auto" alt="allow permission"/>

<h2>14. Click Continue on the osTicket browser and complete system settings and admin user</h2>

Password is Summerfestival2

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/f33aa738-4a2c-47bb-8290-e4392614384d width="50%" height="auto" alt=" Sytem settings and Admin User"/>


Download and install HediSQL

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/e2c37072-40c0-4149-98c5-ac904cfabada width="50%" height="auto" alt="install heidi"/>

Make sure the check mark for launch is on then click finish. Add new and enter the password for root then click open.

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/87867d99-60cc-4416-84c0-c40c20e5c20e width="50%" height="auto" alt="Session manager heidi"/>

<h2>15. Create a database on HeidiSQL named osTicket</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/fede1a7a-0394-4b50-b2a7-b367c3031b34 width="50%" height="auto" alt="new database"/>

<h2>16. Fill in the database, username, and password</h2>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/25e06fb7-fc61-4f2f-9d79-68dad0902634 width="50%" height="auto" alt="Database Settings"/>

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/1016bb85-479b-4e30-9680-ce68a4c81252 width="50%" height="auto" alt="osTicket installed"/>

<h2>17. Tighten up</h2>

Delete: C:\inetpub\wwwroot\osTicket\setup

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/7d5fc7a4-3950-4c32-a5a0-b945405ddd44 width="50%" height="auto" alt="delete setup"/>

Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<img src=https://github.com/Archie735/osTicket-Perquisites-and-Installation/assets/150314129/1b6c3e0c-8025-42f3-9e0b-479f053b3f65 width="50%" height="auto" alt="Read only permission"/>


Now we are done installing osTicket :)

