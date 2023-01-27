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

- Set up an Azure Windows 10 Virtual machine.
- Install / Enable IIS in Windows WITH CGI
- Install PHP Manager for IIS, Install Rewrite Module, download PHP, install C++ redistributable, and install MySQL.
- Set up MySQL
- Register PHP from within IIS

<h2>Installation Steps</h2>

<p>
<img src="https://i.ibb.co/f8bzPn2/lab3-1.png" height="70%" width="70%" alt=""/>
</p>
<p>
1. The first step was to create a new resource group and VM in Azure. I created a resource group named "osTicket" and inside that group I created a Windows 10 VM and named it "VM-osTicket".
</p>
<br />

<p>
<img src="https://i.ibb.co/fkcpLg0/lab3-2.png" height="70%" width="70%" alt=""/>
</p>
<p>
2. Next, I opened VM-osTicket and enabled IIS with CGI using the following steps: open the Control Panel, then click Programs, next click "turn windows features on or off", next find "Internet Information Services", enable it and expand it, then expand "World Wide Web Services", next expand "Application Development Features", find CGI and enable it, then click ok.
</p>
<br />

<p>
<img src="https://i.ibb.co/LZ7VMMW/lab3-5.png" height="70%" width="70%" alt=""/>
</p>
<p>
<img src="https://i.ibb.co/mT5tY0H/lab3-6.png" height="70%" width="70%" alt=""/>
</p>
<p>
<img src="https://i.ibb.co/Nr1WnLd/lab3-7.png" height="70%" width="70%" alt=""/>
</p>
<p>
3. Next, download and install prereq files. 1. "PHP Manager"(https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view). 2. "Rewrite Module"(https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link). 3. "PHP 7.3.8"(https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link) - download this entire folder, create a new folder in the windows C drive and name is PHP. Once "PHP 7.3.8" is downloaded, right click it and extract the contents into that C:\PHP folder that you created. (example above). 4. "C++ redistributable"(https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link). 5. "MySQL" (https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link) - be sure to click "Typical" install(example above). 
</p>
<br />

<p>
<img src="https://i.ibb.co/q5JBkmB/lab3-8.png" height="70%" width="70%" alt=""/>
</p>
<p>
4. Next, set up MySQL. Launch MySQL, press next then press standard configuration, press next again, create a password then press next, finally press execute. A database is now installed on the VM which is used for osTicket.
</p>
<br />
<p>
<img src="https://i.ibb.co/db6YVtz/lab3-9.png" height="70%" width="70%" alt=""/>
</p>
<p>
5. Next, register PHP from within IIS. Go to the start menu, search IIS and run it as an admin. Double click PHP manager, click "register new PHP version", browse for the PHP folder we created in the C drive earlier, open the folder and click "php-cgi", next press ok. Finally, restart the server, click on the name of the server then click restart in the right hand corner.
</p>
<br />
