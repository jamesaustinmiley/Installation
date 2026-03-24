<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket. OsTicket is used to manage both internal and external requests via e-mail, phone, or the company website. These requests are then converted into tickets that can be tracked and completed. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure 
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11 Pro</b> (25H2)

<h2>Installation Steps</h2>

<p>
Create a Microsoft Azure Resource Group.
</p>
<p>
<img src="https://imgur.com/xmznU8l.png" alt="Resource Group Creation"/>
</p>
<p>
Create a Microsoft Azure Virtual Machine.
</p>
<p>
<img src="https://imgur.com/zdRJFdN.png" alt="Virtual Machine part 1"/>
</p>
<p>
Ensure that the VM Region is the same as the Resource Group Region. 
</p>
<p>
<img src="https://imgur.com/dBtlAHj.png" alt="Virtual Machine part 2"/>
</p>
<p>
Pick a Windows Image (Windows 11 Pro, version 25H2). When choosing the Size of the VM, make sure that it has 2 vcpus and 8 gb (Standard _D2s_v3-2 vcpus, 8 GB Memory).
</p>
<p>
<img src="https://imgur.com/NMIVfY7.png" alt="Virtual Machine part 3"/>
</p>
<p>
Enter a Username and Password that will be used for Remote Desktop access. 
</p>
<p>
<img src="https://imgur.com/VzXo0eC.png" alt="Virtual Machine part 4"/>
</p>
<p>
Check the box that confirms that you have an eligible Windows license.
</p>
<p>
<img src="https://imgur.com/XNCaU9N.png" alt="Virtual Machine part 5"/>
</p>
<br />

<p>
Find the Public IP Address for the Virtual Machine. 
</p>
<p>
<img src="https://imgur.com/hmDqnOP.png" alt="Public IP Address"/>
</p>
<p>
Open the Remote Desktop Connection program and use VM's Public IP Address to start the connection. 
</p>
<p>
<img src="https://imgur.com/vP6CB44.png" alt="Remote Desktop Connection part 1"/>
</p>
<p>
Enter the VM Username and Password to complete the Remote Desktop connection. 
</p>
<p>
<img src="https://imgur.com/Lv9lOHs.png" alt="Remote Desktop Connection part 2"/>
</p>
<br />

<p>
Download the osTicket Installation Files zip folder. 
</p>
<p>
<img src="https://imgur.com/R3g0vCT.png" alt="osTicket Installation Files zip folder"/>
</p>
<p>
Open Downloads Folder 
</p>
<p>
<img src="https://imgur.com/m34P0fj.png" alt="Downloads Folder"/>
</p>
<p>
Drag the osTicket Installation Files zip folder to the Home Page.
</p>
<p>
<img src="https://imgur.com/lJqHTon.png" alt="Home Page"/>
</p>
<p>
Right click the osTicket Installation Files zip folder and click Extract All. This will copy all of the items from the zip folder to a regular folder on the Home Page named osTicket Installation Files. 
</p>
<p>
<img src="https://imgur.com/aByZnd2.png" alt="Extracting osTicket Installation Files"/>
</p>
<p>
Open the osTicket Installation Files folder to view its contents. 
</p>
<p>
<img src="https://imgur.com/z6JuZUW.png" alt="osTicket Installation Files folder content"/>
</p>
<br />

<p>
Open the Control Panel.
</p>
<p>
<img src="https://imgur.com/odzF9hP.png" alt="Control Panel"/>
</p>
<p>
Uninstall a Program. 
</p>
<p>
<img src="https://imgur.com/fFqGhVm.png" alt="Programs"/>
</p>
<p>
Turn Windows features on or off. 
</p>
<p>
<img src="https://imgur.com/9ojp16Z.png" alt="Windows Features"/>
</p>
<p>
Check the Internet Information Services box and the CGI box to turn them on. IIS is the primary web server for Windows and enables the osTicket app to run by serving its files and executing its scripts. To find CGI, expand World Wide Web Services and then Application Development Features. CGI is a dependency that osTicket needs to operate. 
</p>
<p>
<img src="https://imgur.com/HeYlMUV.png" alt="Turn Windows Features On"/>
</p>
<br />

<p>
Install PHP Manager for IIS from the osTicket Installation Files folder. PHP is the backend scripting language that osTicket runs on.    
</p>
<p>
<img src="https://imgur.com/3nFthaO.png" alt="PHP Manager"/>
</p>
<p>
Install the IIS URL Rewrite Module from the osTicket Installation Files folder. 
</p>
<p>
<img src="https://imgur.com/lZFiGgX.png" alt="Rewrite Module"/>
</p>
<br />

<p>
Open File Explorer
</p>
<p>
<img src="https://imgur.com/dWzRbNA.png" alt="File Explorer"/>
</p>
<p>
Expand This PC to gain access to the Windows C Drive and its contents.
</p>
<p>
<img src="https://imgur.com/bGO0GyU.png" alt="Windows C Drive"/>
</p>
<p>
Create a new folder in Windows C Drive named PHP. Right click in the C Drive, click New, and click Folder. 
</p>
<p>
<img src="https://imgur.com/6ojs6za.png" alt="PHP folder"/>
</p>
<p>
Unzip the php 7.3.8 zip folder in the osTicket Installation Files folder. Right click the php 7.3.8 folder and select Extract All. 
</p>
<p>
<img src="https://imgur.com/do4tz9t.png" alt="php 7.3.8 zip folder"/>
</p>
<p>
Click Browse to find a destination where the files will be extracted to. 
</p>
<p>
<img src="https://imgur.com/vGZZPUR.png" alt="Browse"/>
</p>
<p>
Select the PHP folder in Windows C Drive. 
</p>
<p>
<img src="https://imgur.com/3hGnjlK.png" alt="Select Folder"/>
</p>
<p>
Extract the php 7.3.8 zip folder files to the PHP folder in Windows C Drive. 
</p>
<p>
<img src="https://imgur.com/3SApW02.png" alt="Extraction"/>
</p>
<br />

<p>
Install the Microsoft Visuall C++ Redistributale (x86) file from the osTicket Installation Files folder. 
</p>
<p>
<img src="https://imgur.com/34PL8lo.png" alt="VC"/>
</p>
<p>
Start the installation of MYSQL 5.5.62 from the osTicket Installation Files folder. MYSQL is the database management system that will store and manage all osTicket help desk data.
</p>
<p>
<img src="https://imgur.com/uf62zVJ.png" alt="MYSQL 5.5.62"/>
</p>
<p>
Choose Typical Setup.
</p>
<p>
<img src="https://imgur.com/i4qmx9o.png" alt="Typical"/>
</p>
<p>
Launch the MySQL Instance Configuration Wizard. 
</p>
<p>
<img src="https://imgur.com/YGxOuHH.png" alt="Instance Configuration Wizard"/>
</p>
<p>
Choose Standard Configuration. 
</p>
<p>
<img src="https://imgur.com/2I7WBkO.png" alt="Standard Configuration"/>
</p>
<p>
Install as Windows Service. 
</p>
<p>
<img src="https://imgur.com/IclqORy.png" alt="Windows Service"/>
</p>
<p>
Enter a password for MYSQL. 
</p>
<p>
<img src="https://imgur.com/gFCXc63.png" alt="MYSQL Password"/>
</p>
<br />

<p>
Open Internet Information Services Manager as an Administrator. 
</p>
<p>
<img src="https://imgur.com/wj9mxmQ.png" alt="Administrator"/>
</p>
<p>
Register PHP within IIS by opening PHP Manager. 
</p>
<p>
<img src="https://imgur.com/y1IhZ0U.png" alt="PHP Manager"/>
</p>
<p>
Click Register new PHP version and provide a path to the php executable file (php-cgi) by clicking Browse (...).
</p>
<p>
<img src="https://imgur.com/qNMMJOr.png" alt="Register new PHP version"/>
</p>
<p>
Open the PHP folder, within Windows C Drive, where you will find php-cgi.
</p>
<p>
<img src="https://imgur.com/ZSrofcN.png" alt="php-cgi"/>
</p>
<p>
Double-click php-cgi which will result in PHP being registerd within IIS. 
</p>
<p>
<img src="https://imgur.com/DNYqC2r.png" alt="Register PHP within IIS"/>
</p>
<p>
Reload IIS by stopping and starting the server to implement the changes.
</p>
<p>
<img src="https://imgur.com/Qaz5zyG.png" alt="Stopping and Starting"/>
</p>
<br />

<p>
Right-click the osTicket-v1.15.8 zip folder within the osTicket Installation Files folder and click Extract All. 
</p>
<p>
<img src="https://imgur.com/OhmUSLe.png" alt="osTicket v1.15.8 zip folder"/>
</p>
<p>
Click Extract which will result in the files being extracted to a new folder, also named osTicket-v1.15.8, located within the osTicket Installation Files folder. 
</p>
<p>
<img src="https://imgur.com/oqGBXJQ.png" alt="Extract"/>
</p>
<p>
<img src="https://imgur.com/lXrsQG6.png" alt="New Folder"/>
</p>
<p>
Open the new osTicket-v1.15.8 folder to find the Upload folder. Open File Explorer in another window where you will click on Windows C Drive, click on inetpub, and finally wwwroot. 
</p>
<p>
<img src="https://imgur.com/V44x5hY.png" alt="wwwroot"/>
</p>
<p>
Drag the Upload folder from the osTicket-v1.15.18 to wwwroot and rename it osTicket. 
</p>
<p>
<img src="https://imgur.com/8PM1IOa.png" alt="osTicket"/>
</p>
<br />

<p>
Open IIS and stop and start the server. Expand osticket-vm, Sites, and Default Web Site to get to osTicket Home. 
</p>
<p>
<img src="https://imgur.com/ITLPrS4.png" alt="osTicket Home"/>
</p>
<p>
In IIS, click on Browse *:80 (http) on the far right of the page to load the osTicket Installer page. Scroll down to view a list of extensions, including some that haven't been enabled. 
</p>
<p>
<img src="https://imgur.com/iIA5mbJ.png" alt="osTicket Installer"/>
</p>
<p>
<img src="https://imgur.com/c4mfhxY.png" alt="Extensions"/>
</p>
<p>
Go back to IIS (osTicket Home), open PHP Manager, and click on Enable or disable an extension.
</p>
<p>
<img src="https://imgur.com/2eTpY7S.png" alt="osTicket Home PHP Manager"/>
</p>
<p>
<img src="https://imgur.com/x5tj4AV.png" alt="Enable Extensions"/>
</p>
<p>
Enable three extensions (php_imap.dll, php_intl.dll, and php_opcache.dll) by right-clicking each one and clicking Enable.
</p>
<p>
<img src="https://imgur.com/3NCGKO0.png" alt="php_imap.dll"/>
</p>
<p>
<img src="https://imgur.com/DT6cVAt.png" alt="php_intl.dll"/>
</p>
<p>
<img src="https://imgur.com/9NECEWa.png" alt="php_opcache.dll"/>
</p>
<p>
<img src="https://imgur.com/BEWpuM2.png" alt="PHP Extensions"/>
</p>
<p>
Reload the osTicket Installer page to view the extensions again. Disregard the APCu and Zend OPcache extensions.
</p>
<p>
<img src="https://imgur.com/UYWXXA4.png" alt="Extensions part 2"/>
</p>
<br />

<p>
Navigate to ost-sampleconfig.php, which is located in the Windows C Drive (inetpub/wwwroot/osTicket/include).
</p>
<p>
<img src="https://imgur.com/UitJVze.png" alt="ost-sample.config"/>
</p>
<p>
Rename ost-sampleconfig.php to ost-config.php.
</p>
<p>
<img src="https://imgur.com/hRwMc05.png" alt="ost-config.php"/>
</p>
<p>
Right-click ost-config.php, click Properties, click Security, and click Advanced under Permissions for SYSTEM. 
</p>
<p>
<img src="https://imgur.com/zAxARkq.png" alt="Advanced"/>
</p>
<p>
Click Disable Inheritance to remove all of the inherited permissions. 
</p>
<p>
<img src="https://imgur.com/3pSh8HW.png" alt="Disable Inheritance"/>
</p>
<p>
<img src="https://imgur.com/lonOrQp.png" alt="Remove all inherited permissions"/>
</p>
<p>
Add new permissions. 
</p>
<p>
<img src="https://imgur.com/ZMXvhpZ.png" alt="Add New Permissions"/>
</p>
<p>
Select a Principal that the new permissions will apply to. 
</p>
<p>
<img src="https://imgur.com/aJvqrO2.png" alt="Select a Principal"/>
</p>
<p>
These new permissions will be applied to Everyone. Click Check Names.
</p>
<p>
<img src="https://imgur.com/pNjMVd9.png" alt="Everyone"/>
</p>
<p>
Check Full Control to give Everyone access to the basic permissions. 
</p>
<p>
<img src="https://imgur.com/2BtAoVA.png" alt="Full Control"/>
</p>
Observe that Everyone now has permissions with regards to ost-config.php.
</p>
<p>
<img src="https://imgur.com/3rdXiAf.png" alt="Properties"/>
</p>
<br />

<p>
Go back to the osTicket Installer page to begin the osTicket Basic Installation. Provide a Helpdesk name and a Default Email under System Settings.
</p>
<p>
<img src="https://imgur.com/5i5EPtv.png" alt="System Settings"/>
</p>
<p>
Provide a name, email, username, and password under Admin User.
</p>
<p>
<img src="https://imgur.com/eueOQWL.png" alt="Admin User"/>
</p>
<br />

<p>
Install HeidiSQL 12.3.0.6589 from the osTicket Installation Files folder. HeidiSQL is the database for osTicket. 
</p>
<p>
<imgs src="https://imgur.com/NJgFkqp.png" alt="HeidiSQL"/>
</p>
<p>
Select a location where HeidiSQL will be installed. The location will be a folder named HeidiSQL.
</p>
<p>
<img src="https://imgur.com/gS3LFMN.png" alt="Select Destination Location"/>
</p>
<p>
The HeidiSQL folder will be located on the Home Page. 
</p>
<p>
<img src="https://imgur.com/5R1x9m1.png" alt="Start Menu Folder"/>
</p>
<p>
Select all of the listed tasks to ensure they are performed. 
</p>
<p>
<img src="https://imgur.com/1nWhcPx.png" alt="Additional Tasks"/>
</p>
<p>
Open HeidiSQL on the Home Page. Click New in the bottom left to create a new session. Enter your MySQL password from earlier. 
</p>
<p>
<img src="https://imgur.com/1SQKVDP.png" alt="New Session"/>
</p>
<p>
Create a new database named osTicket. Right-click Unnamed to start the process.
</p>
<p>
<img src="https://imgur.com/KNOuZHQ.png" alt="New Database"/>
</p>
<p>
<img src="https://imgur.com/DKhVh5J.png" alt="New Database part 2"/>
</p>
<p>
Return to the osTicket Basic Installation page to fill in the Database Settings section.
</p>
<p>
<img src="https://imgur.com/O1xh33V.png" alt="Database Settings"/>
</p>
<p>
View the osTicket Installer page after successful installation. 
</p>
<p>
<img src="https://imgur.com/yMa16hM.png" alt="Success"/>
</p>






