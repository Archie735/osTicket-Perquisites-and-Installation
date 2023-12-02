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

- Windows 11</b> (21H2)

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


