<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Installation</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket. OsTicket is used to manage both internal and external requests via e-mail, phone, or the company website. These requests are then converted into tickets that can be tracked and worked to completion. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure 
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11 Pro</b> (25H2)

<h2>Installation Steps</h2>

<p>
On Microsoft Azure, create a Resource Group named osTicket. Next, create a Virtual Machine named osticket-vm that will be a part of the osTicket Resource Group. Select the same Region from the creation of the Resource Group. Under Image, you will select the operating system that will be utilized by the Virtual Machine (Windows 11 Pro, version 25H2). Under Size, you should select an option that has 2 vcpus so that there will be plenty of processing power, memory, and storage capacity to utilize (Standard_D2s_v3 - 2 vcpus, 8 GB Memory). Set up a Username and Password that will be associated with the VM and confirm that you have an eligible Windows license. 
</p>
<p>
<img src="https://imgur.com/WitlT1o.png" alt="Resource Group Creation"/>
</p>
<p>
<img src="https://imgur.com/FOYHMDy.png" alt="Virtual Machine Creation 1"/>
</p>
<p>
<img src="https://imgur.com/OE6jg9X.png" alt="Virtual Machine Creation 2"/>
</p>
<br />

<p>
Use the Virtual Machine's public IP address, Username, and Password to log into it with Remote Desktop. Before installing OsTicket onto the VM, you must enable Internet Information Services on the VM. The IIS is the primary web server used by Windows and will allow the osTicket app to run by serving its files and executing its scripts. Without IIS, osTicket can't be accessed from a browser due to lack of HTTPS service. 
</p>
<p>
<img src="https://imgur.com/rMG5n5U.png" alt="Remote Desktop"/>
</p>
<p>
<img src="https://imgur.com/t27Gwhs.png" alt="IIS Enabling"/>
</p>
<br />

<p>
The next step is to install PHP, which is a backend scripting language that osTicket runs on. Install the PHP Manager for IIS. Install the IIS URL Rewrite Module. Create a new directory on the Windows C Drive titled PHP. Unzip and extract the contents, such as the binaries and language files, from the PHP file and move them to your PHP folder in the C Drive for osTicket installation. Install VC_redist, which implements runtime components required by PHP within IIS. 
</p>
<p>
<img src="https://imgur.com/ImGrHPw.png" alt="osTicket Installation Files"/>
</p>
<p>
<img src="https://imgur.com/9eHghjE.png" alt="PHP Folder Contents"/>
</p>
<br />

<p>
Another important step is to install MySQl, a database management system which will store and manage all of the osTicket help desk system's data. During installation of MySQL, choose Typical Setup, which will install the most common program features. Launch the MySQL Instance Configuration Wizard. Choose Standard Configuration and to Install as a Windows Service. When setting the security options, type ROOT as the password. 
</p>
<p>
<img src="https://imgur.com/ImGrHPw.png" alt="osTicket Installation Files"/>
</p>
<p>
<img src="https://imgur.com/zJO0qZk.png" alt="Typical Setup"/>
</p>
<p>
<img src="https://imgur.com/ylioDKN.png" alt="Configuration wizard"/>
</p>
<p>
<img src="https://imgur.com/0uhz7Wg.png" alt="Standard Configuration"/>
</p>
<p>
<img src="https://imgur.com/ayQA0WK.png" alt="Password"/>
</p>
<br />

<p>
Open Internet Information Services as an Administrator. Register PHP from within IIS using the PHP Manager, which will allow PHP to run within the server. To enable PHP, you must click Register new PHP version, which will allow you to provide a path to php-cgi, a PHP executable file located in the PHP folder you created in the Windows C Drive. Reload IIS by stopping and starting the server to implement the changes. To install osTicket, unzip and extract the files from the osTicket folder. Move the upload folder from within osTicket to wwwroot in the Windows C Drive. Rename the Upload folder to osTicket. Once again, reload IIS by stopping and starting the server. Go to the osTicket website by clicking Browse *:80 on the osTicket Home Page within IIS. You will notice that there are some extensions that haven't been enabled. to enable these extensions, go back to the osTicket Home Page within IIS, click PHP Manager, and click Enable or disable an extension. Once you've enabled the necessary extensions, you can refresh the osTicket site and observe the changes. Rename the ost-sampleconfig.php file, located in the osTicket folder in the Windows C Drive, to ost-config.php.
</p>
<p>
<img src="https://imgur.com/mCPHnUq.png" alt="IIS Administrator"/>
</p>
<p>
<img src="https://imgur.com/K2lJ0Uv.png" alt="IIS Manager"/>
</p>
<p>
<img src="https://imgur.com/YucpG3z.png" alt="Register new PHP version"/>
</p>
<p>
<img src="https://imgur.com/1d4tXHH.png" alt="php-cgi"/>
</p>
<p>
<img src="https://imgur.com/ImGrHPw.png" alt="osTicket Installation Files"/>
</p>
<p>
<img src="https://imgur.com/21WUj2a.png" alt="wwwroot osTicket"/>
</p>
<p>
<img src="https://imgur.com/LTPmqq4.png" alt="Browse 80"/>
</p>
<p>
<img src="https://imgur.com/uzcXpxj.png" alt="Missing Extensions"/>
</p>
<p>
<img src="https://imgur.com/hTfN2nf.png" alt="PHP Manager"/>
</p>
<p>
<img src="https://imgur.com/G2WyaqA.png" alt="PHP Extensions"/>
</p>
<p>
<img src="https://imgur.com/lBd5ERo.png" alt="Enabled Extensions"/>
</p>
<p>
<img src="https://imgur.com/EDhaY6f.png" alt="Rename File"/>
</p>
<p>
<img src="
