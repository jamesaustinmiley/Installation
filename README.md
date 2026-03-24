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

