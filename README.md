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

- Azure Virtual Machine Windows 10, 4 vCPUs
- osTicket Installation Files
- Admin User Credentials (for database and osTicket setup)
- PHP 7.4 - 8.0 (Latest stable version recommended)
- MySQL 5.5+ or MariaDB 10.0+

<h2>Installation Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/e7bbd916-aaab-4319-ba99-b71104f8a810" />
</p>
<p>
Start by creating a virtual machine using Microsoft Azure.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/453a8391-73ac-4bd9-92b3-734f5498693e" />

</p>
<p>
Rename resource group to osticket, virtual machine renamed to myVm, and set region to East US (happens to be the only one available for the East coast).
<br />

<p>
<img src="https://github.com/user-attachments/assets/bd2ddfae-4046-41f9-a90b-b7931b542b4e" />
</p>
<p>
Select applicable region for VM size and select Windows 10 Pro version 22H2 x64 Gen2 as the image. Create login, confirm licensing, and click next until you reach review + create.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/5cf8b52f-ff83-4ff4-9946-b1f7c6f05cc3" />
</p>
<p>
Review to confirm and click create.
</p>

<p>
<img src="https://github.com/user-attachments/assets/d95163e7-6162-4617-814b-37b323324aec" />
</p>
<p>
After deployment, return to Virtual Machines, copy and paste public IP address to Remote Desktop and login.
</p>

<p>
<img src="https://github.com/user-attachments/assets/8c0bdd73-2b8f-4d26-8c62-364d6e7837ff" />
</p>
<p>
Download osTicket installation files and extract the zip file.
</p>

<p>
<img src="https://github.com/user-attachments/assets/afab5c7a-4173-48b9-9b51-a68465ad8e79" />
</p>
<p>
Confirm that the loopback address isn't responding before installing IIS with CGI enabled.
</p>

<p>
<img src="https://github.com/user-attachments/assets/61c16cf5-df9c-4b57-97a8-9d2a8ac44b9c" />
<img src="https://github.com/user-attachments/assets/ae817770-7abb-4bc7-9cdc-6d4f69372d37" />
</p>
<p>
Launch Control Panel and navigate to click "uninstall a program" under Programs
</p>

<p>
<img src="https://github.com/user-attachments/assets/ce78044f-c73b-40f5-be17-c7082675c0db" />
</p>
<p>
Check the "Internet Information Services" box, click the "+" next to the IIS folder to drop down to World Wide Services. Expand WWS to the Application Development Features and expand folder, check CGI box and click OK 
</p>

<p>
<img src="https://github.com/user-attachments/assets/8296ca4c-553c-4436-b151-c9498430987f" />
</p>
<p>
After completing changes and closing the window, refresh the loopback address of 127.0.0.1 and see that IIS has been installed successfully.
</p>

<p>
<img src="https://github.com/user-attachments/assets/cd105dd7-5c4c-4724-a1a7-50392bdaba37" />
<img src="https://github.com/user-attachments/assets/abca6951-b8b4-4b08-9e9f-6b4bda4bb4ec" />
</p>
<p>
Go to the extracted osTicket installation files and launch the PHP Manager installation. Click next, select "I agree" to Licensing Agreement, then click next to install
</p>

<p>
<img src="https://github.com/user-attachments/assets/63d1ae97-b2e7-4f31-a007-862686a65349" />
<img src="https://github.com/user-attachments/assets/e4c1a348-5760-41fa-950c-28c6436c2c45" />
</p>
<p>
Navigate to the C drive and right-click in Windows folder screen to create a new folder. Rename the folder to PHP.
</p>

<p>
<img src="https://github.com/user-attachments/assets/0f0d30bc-b350-41ef-85bf-f35c9ddb2cd0" />
</p>
<p>
Back within the osTicket Installation files on the desktop, right-click the php file and click Extract All.
</p>

