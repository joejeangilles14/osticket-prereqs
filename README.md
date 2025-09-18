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
Go to the extracted osTicket installation files and launch the PHP Manager installation. Click Next, select "I agree" to Licensing Agreement, then click Next to install
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

<p>
<img src="https://github.com/user-attachments/assets/e5635f9b-cd0a-408d-9aee-f2ae1e42d124" />
</p>
<p>
Browse to the PHP folder within the Windows folder on the C drive and extract the files to the PHP folder.
</p>

<p>
<img src="https://github.com/user-attachments/assets/be11db9e-1a27-4c09-b8b8-e5935849f7da" />
</p>
<p>
Go to the osticket installtion folder and launch the mysql installer. In order, click Next, click "accept terms" and click Next, choose Typical installation and install.  
</p>

<p>
<img src="https://github.com/user-attachments/assets/5c11221e-5fbb-4d54-bc5c-02986e7430c8" />
</p>
</p>
After the installation is complete be sure "Launch the MySQL Instance Configuration Wizard" is checked and click Finish.
<p>

<p>
<img src="https://github.com/user-attachments/assets/e0efc8e2-fdb9-4a90-8b94-b19860a45be6" />
</p>
<p>
Click Next and select Standard Configuration 
</p>

<p>
<img src="https://github.com/user-attachments/assets/dcfc2540-a04d-4523-9d27-e2941f4794a3" />
</p>
<p>
Leave this page as is and click Next. 
</p>

<p>
<img src="https://github.com/user-attachments/assets/db41c205-107d-4627-b433-e4d8c903852a" />
</p>
<p>
For the sake of this lab, I created my username and password as "root" (all lowercase) but I recommend against this in a live workplace environment. Click Next then Execute
</p>

<p>
<img src="https://github.com/user-attachments/assets/e49618c9-76e3-4be1-a2e8-9777bf29e93e" />
</p>
<p>
After all configuratons are done processing, click Finish.
</p>

<p>
<img src="https://github.com/user-attachments/assets/02ae61dd-75d3-4a0a-b2b3-b6f5b24e2ea3" />
</p>
<p>
Type IIS in the search bar and launch IIS.
</p>

<p>
<img src="https://github.com/user-attachments/assets/02f2a2ce-23c3-4e31-af65-7477658371cd" />
</p>
<p>
Navigate to the PHP Manger and launch the application
</p>

<p>
<img src="https://github.com/user-attachments/assets/425e018d-896e-4c44-81ef-10ff2562d791" />
<img src="https://github.com/user-attachments/assets/58612f39-eae9-421c-8147-71ea53ad5648" />
</p>
<p>
Here, a path for the php executable is being provided by registering a new PHP
</p>

<p>
<img src="https://github.com/user-attachments/assets/a32b0ee1-b169-489b-b766-e89548e78402" />
<img src="https://github.com/user-attachments/assets/28d94fa5-1293-4b26-83fb-0de06a4a8586" />
</p>
<p>
Browse to the Windows C drive and open the PHP folder. Then, open the php-cgi application.
</p>

<p>
<img src="https://github.com/user-attachments/assets/f6b392c9-b451-4282-8edc-57a7b1cec441" />
</p>
<p>
Click OK
</p>

<p>
<img src="https://github.com/user-attachments/assets/def26adf-949b-4be4-870b-60cd8ae2494a" />
</p>
<p>
Within IIS, right click and stop the connection.
</p>

<p>
<img src="https://github.com/user-attachments/assets/8a9c390f-f0df-4f38-9e69-54eab736f50a" />
</p>
<p>
Right click again and start the connection.
</p>

<p>
<img src="https://github.com/user-attachments/assets/aabe906f-f32b-4386-a617-95d3ef7edf35" />
</p>
<p>
Go to the osTicket installation files, right click on the osTicket-v1.15.8 file and click Extract All.
</p>


<p>
<img src="https://github.com/user-attachments/assets/b753abdc-c8ef-48aa-9574-d791dbffc906" />
<img src="https://github.com/user-attachments/assets/597d9236-a821-4eb6-9808-19244c47e338" />
</p>
<p>
Extract files within the OSTicket Installation folder and copy the "upload" folder into "c:\inet\pub\wwwroot". Within "c:\inet\pub\wwwroot", rename "upload" to "osTicket"
</p>

<p>
<img src="https://github.com/user-attachments/assets/2d59bfea-c30f-4935-b68d-318e3d9e2c57" />
<img src="https://github.com/user-attachments/assets/e301a88c-c1e5-4896-90a2-46406c683f41" />
</p>
<p>
Reload IIS by right clicking and stopping the service. Then, start the service back up.
</p>

<p>
<img src="https://github.com/user-attachments/assets/990a0482-4048-4fdd-aa3a-cba979b5af87" />
</p>
<p>
Within IIS, click the drop arrow on Application Pools, Default Site and click on osTicket. On the right hand side, click "Browse *.80"
</p>

<p>
<img src="https://github.com/user-attachments/assets/781c0ae7-75b0-4486-a944-69dba23368b8" />
</p>
<p>
osTicket installer has been launched and now certain features can be enabled.
</p>

<p>
<img src="https://github.com/user-attachments/assets/c60dae43-b46a-49b3-9ce0-7812795322ee" />
<img src="https://github.com/user-attachments/assets/a4c56b5b-d303-4515-85ca-195f6bff092b" />
</p>
<p>
Go back to IIS and double-click on PHP Manager. Then click on "Enable or disable an extension".
</p>

<p>
<img src="https://github.com/user-attachments/assets/7c65f3d7-06bf-4802-8cee-a90186f990b0" />
<img src="https://github.com/user-attachments/assets/7bd83457-2ac0-4002-b516-f16f02640b57" />
<img src="https://github.com/user-attachments/assets/3b958718-9b19-428c-b0f6-4576c4c2fca2" />
</p>
<p>
Right click and enable php_imap.dll then repeat the same for php_intl.dll and php_opcache.dll
</p>

<p>
<img src="https://github.com/user-attachments/assets/9bcd92a7-b900-4b4f-8ef7-768b86b80913" />
</p>
<p>
Reload browser and features are now enabled!
</p>

<p>
<img src="https://github.com/user-attachments/assets/9a338de9-4cc1-4631-87d7-745c4c0f5730" />
</p>
<p>
Navigate to C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, rename it to ost-config.php, right click and go to Properties
</p>

<p>
<img src="https://github.com/user-attachments/assets/850e42cd-b410-41a2-80ac-a7a971bb1065" />
</p>
<p>
Go to the Security tab and click on Advanced.
</p>


<p>
<img src="https://github.com/user-attachments/assets/f8d2b65a-3f47-4975-a6b0-a1b85314af02" />
</p>
<p>
Click on "Disable inheritence" and "Remove all inherited permissions from this object"
</p>

<p>
<img src="https://github.com/user-attachments/assets/d6ee95bc-792e-4a77-b1bd-434c49859db9" />
<img src="https://github.com/user-attachments/assets/5335e465-b19d-43e4-bc18-1725f9fea608" />
<img src="https://github.com/user-attachments/assets/50928559-954d-4dad-8c7e-2476774772b9" />
</p>
<p>
Click Add, Select a principle, then type Everyone in the box, click "Check names" and click OK
</p>

<p>
<img src="https://github.com/user-attachments/assets/c73b029b-63e8-40c6-9d99-37c094ec10b0" />
</p>
<p>
Check Full control to allow all permissions and click OK
</p>

<p>
<img src="https://github.com/user-attachments/assets/3450ed16-4435-4f2c-92c4-546c1c0a04e8" />
</p>
<p>
Click Apply and then OK
</p>

<p>
<img src="https://github.com/user-attachments/assets/e7cba3aa-d6f7-4f23-9038-1057e1bf2701" />
</p>
<p>
On osTicket browser, click Continue then fill out basic information for the installer.
</p>

<p>
<img src="https://github.com/user-attachments/assets/4bfc25da-664a-4a4b-8ad6-bd89fa393485" />
</p>
<p>
Navigate to osTicket installation folder and launch HeidiSQL
</p>

<p>
<img src="https://github.com/user-attachments/assets/c262725f-2d21-4dab-9371-11786121d759" />
</p>
<p>
After reviewing the terms, accept terms and click Next
</p>

<p>
<img src="https://github.com/user-attachments/assets/79cd18ac-e95b-41b5-bb2e-a877b9fe4a65" />
<img src="https://github.com/user-attachments/assets/3a1737c8-7456-426e-ad7c-e70617087eb0" />
<img src="https://github.com/user-attachments/assets/a5eaf7c6-aa73-4789-9eda-2472ac3e019c" />
</p>
<p>
Continue to click Next until you see a list of checked boxes, make sure all are checked, click Next
</p>

<p>
<img src="https://github.com/user-attachments/assets/b92f60e2-a8e8-4205-8f98-3a7a7597afb3" />
</p>
<p>
Click Install
</p>

<p>
<img src="https://github.com/user-attachments/assets/5777f5e9-a057-4385-b810-2177cbeef505" />
</p>
<p>
Make sure "Launch HeidiSQL" is checked and click Finish
</p>

<p>
<img src="https://github.com/user-attachments/assets/bf9bb3b3-e048-47b0-8715-a181ccb1f1c6" />
<img src="https://github.com/user-attachments/assets/bd38526b-26ea-4e33-a8e7-94325d33ce1d" />
</p>
<p>
Once Heidi is launched, click New. The username and password will be root, then click Open
</p>

<p>
<img src="https://github.com/user-attachments/assets/7d719000-2292-4422-91ca-117df929abb0" />
</p>
<p>
Right click Unnamed, hover over Create new and click Database to create one
</p>

<p>
<img src="https://github.com/user-attachments/assets/a0f4bf9a-5635-4422-8145-dff1c5b1d42d" />
</p>
<p>
Name the database "osTicket"
</p>

<p>
<img src="https://github.com/user-attachments/assets/4cac537c-c282-4f1d-a7d4-7d9d6189f9a5" />
</p>
<p>
The information used to create our database will be used for the configuration settings for the osTicket installer.
</p>

<p>
<img src="https://github.com/user-attachments/assets/57ad948d-fbdc-45b1-95d2-a228297b0a21" />
</p>
<p>
osTicket has been successfully installed!
</p>

<p>
<img src="https://github.com/user-attachments/assets/3aff10da-902e-48ec-8f94-3809df1e798e" />
</p>
<p>
Refresh the osTicket database.
</p>

<p>
<img src="https://github.com/user-attachments/assets/663e6469-1494-4493-b8a8-dcf19ebc7ea7" />
</p>
<p>
On the internet browser, navigate to http://localhost/osTicket/scp/login.php and use login credentials to log into osTicket
</p>

<p>
<img src="https://github.com/user-attachments/assets/ec024326-78c2-43ef-a277-3ece9c13ec4d" />
</p>
<p>
Congratulations! osTicket login has been successful!
</p>
