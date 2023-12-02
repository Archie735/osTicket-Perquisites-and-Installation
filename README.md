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
