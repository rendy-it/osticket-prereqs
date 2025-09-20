<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Windows and Linux Virtual Machines on Microsoft Azure
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro </b> (21H2)

<h2>List of Prerequisites</h2>

•	osTicket: [Installation Files](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)

<h2>Steps</h2>

-	Step 1: Using Microsoft Azure Connect to a Windows 10 VM using RDP.
-	Step 2: Download and extract the osTicket “Installation Files” zip file.
-	Step 3: Install all of the osTicket requirement files. 
-	Step 4: Install osTicket.


<h2>Installation Steps</h2>

<h2> << Step 1: Using Microsoft Azure Connect to a Windows 10 VM using RDP >> </h2>
<p>
<img width="1351" height="394" alt="Step 1" src="https://github.com/user-attachments/assets/feb3a155-5afd-4a9e-8108-e38824cf5332" />


</p>
<p>
  
- On the Virtual Machines page of your Azure Resource Group, make sure that both the Windows and Linux virtual machines have a status of “Running”.

</p>
<br />

<img width="1126" height="391" alt="Step 1a" src="https://github.com/user-attachments/assets/913906cc-6e19-466f-a7dd-827bc8acfe8c" />


<p>
  
- Click on your Windows VM.
- On the page of your Windows VM:		
  - Copy the “Public IP address” number.

  
</p>
<br />

<img width="338" height="210" alt="Step 1b" src="https://github.com/user-attachments/assets/96cac9e1-0bda-435e-a54e-3011fb98f997" /> <img width="88" height="210" alt="Right Pointing Arrow for Step 1b" src="https://github.com/user-attachments/assets/af5e210f-1d60-45b5-92f7-09e49326b75a" /> <img width="343" height="235" alt="Step 1b1" src="https://github.com/user-attachments/assets/71fbeb04-ba76-4150-bd18-f524641089ed" />



</p>
<p>
  
- Open the Remote Desktop App:
  - Paste the Windows VM ip address that you copied. Then click on Connect.
  - Then, enter the Windows VM username and password that you created and click on Ok to login.


</p>
<br />

<h2> << Step 2: Download and extract the osTicket “Installation Files” zip file >> </h2>

<p>
<img width="1303" height="352" alt="Step 2" src="https://github.com/user-attachments/assets/6af6d5ec-fa7b-4646-8748-36e313e7e6cd" />


</p>
<p>
  
- Once inside the Windows-VM.
  - Open up your web browser.
  - Then download the osTicket: [Installation Files](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)



</p>
<br />

<img width="1200" height="985" alt="Step 2a" src="https://github.com/user-attachments/assets/58432d75-9f43-49ba-a079-cd0ed92f02d6" />


<p>
  
- Once downloaded, Click on “Open File” and extract the zip onto your desktop for easy access.
   
</p>
<br />

<h2> << Step 3: Install all of the osTicket Requirement Files >> </h2>
<p>
<img width="971" height="564" alt="Step 3" src="https://github.com/user-attachments/assets/aed3b5f7-0702-4f80-bd56-f7828852676f" />



</p>
<p>
  
- Enable IIS (Internet Information Services) in Windows.
  - Go to "Control Panel". 
  - Then click on “Uninstall Program” under Programs.


</p>
<br />

<p>
<img width="971" height="564" alt="Step 3a" src="https://github.com/user-attachments/assets/d8ed245c-c01e-41c1-911e-998393b3c7fb" />


</p>
<p>
  
- Then click on "Turn Windows features on or off".


</p>
<br />

<p>
<img width="420" height="718" alt="Step 3b" src="https://github.com/user-attachments/assets/f95537f5-e3d0-4a10-8010-e31eee7ea15e" />





</p>
<p>
  
- Inside IIS (Internet Information Services), you want to expand “World Wide Web Services”.
-	Then expand “Application Development Features”.
- Then check the “CGI” folder and click Ok.



</p>
<br />

<p>
<img width="1004" height="676" alt="Step 3c" src="https://github.com/user-attachments/assets/1ee9f1fd-78b2-4b51-8742-9dc942e91db3" />




</p>
<p>
  
- From the Installation Files folder on your Desktop:
  - Install the PHP Manager (PHPManagerForIIS_V1.5.0.msi).




</p>
<br />

<p>
<img width="1004" height="676" alt="Step 3d" src="https://github.com/user-attachments/assets/8c5efad0-d48e-4eb6-a669-606419bf90b9" />




</p>
<p>
  
- Next, in the installation files folder:
  -	Install the Rewrite Module (rewrite_amd64_en-US.msi).





</p>
<br />

<p>
<img width="792" height="394" alt="Step 3e" src="https://github.com/user-attachments/assets/ea59a03c-41f3-4e41-832d-7afb4b33ca86" />





</p>
<p>
  
- Next, we are going to create the directory C:\PHP :
  -	Go to your Windows (C:) drive and create a folder named “PHP”.






</p>
<br />

<p>
<img width="1185" height="751" alt="Step 3f" src="https://github.com/user-attachments/assets/9ea1a96a-ca47-4711-bfa6-ad6a71d73da9" />





</p>
<p>
  
- Now go back to the installation files folder and unzip the “php-7.3.8-nts-Win32-VC15-x86” zip file in to the PHP folder.



</p>
<br />
<p>
<img width="989" height="605" alt="Step 3g" src="https://github.com/user-attachments/assets/fb30b596-963f-4296-8a53-f114f5050c69" />



</p>
<p>
  
- Next, in the installation files folder:
  -	Install "VC_redist.x86".




</p>
<br />
<p>
<img width="1012" height="668" alt="Step 3h" src="https://github.com/user-attachments/assets/c50ecce9-952c-44f0-a691-f21b7909bbcb" />



</p>
<p>
  
- Next, in the installation files folder:
  - Install “MySQL 5.5.62” (mysql-5.5.62-win32.msi).





</p>
<br />

<p>
<img width="416" height="318" alt="Step 3h1" src="https://github.com/user-attachments/assets/23f1c36a-19d2-4cfd-8f5b-25dad9f471e3" /> <img width="48" height="318" alt="Right Pointing Arrow for Step 3h 1_2" src="https://github.com/user-attachments/assets/a641b16d-3a64-4db6-8a6b-22b7253b9f6b" /> <img width="416" height="318" alt="Step 3h2" src="https://github.com/user-attachments/assets/d184b37a-b402-479a-8f70-668c1efe0b58" />






</p>
<p>
  
- Select “Typical Setup”, then click Next.
- Then the “Instance Configuration Wizard” window will appear.
- Select “Standard Configuration”, then click Next.






</p>
<br />




