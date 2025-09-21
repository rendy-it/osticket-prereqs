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
  - Select “Typical Setup”, then click Next.





</p>
<br />

<p>
<img width="357" height="271" alt="Step 3h1" src="https://github.com/user-attachments/assets/8a2b6bc6-11ca-413b-b13c-d1c22e67cfaa" /> <img width="69" height="271" alt="Right Pointing Arrow for Step 3h 1_2" src="https://github.com/user-attachments/assets/66e054cc-2d13-4456-b2f8-aaee676cb56a" /> <img width="357" height="271" alt="Step 3h2" src="https://github.com/user-attachments/assets/00f1cdf3-2e11-49ef-bf88-032cbcb84987" />







</p>
<p>
  
- Then the “Instance Configuration Wizard” window will appear.
- Select “Standard Configuration”, then click Next.






</p>
<br />
<p>
<img width="358" height="274" alt="Step 3h4" src="https://github.com/user-attachments/assets/b15dc0da-b3d2-4192-9b07-7a50f64bd022" /> <img width="69" height="271" alt="Right Pointing Arrow for Step 3h 1_2" src="https://github.com/user-attachments/assets/eeee5dc0-1d35-4375-ba0e-26da002003ea" /> <img width="358" height="274" alt="Step 3h5" src="https://github.com/user-attachments/assets/f3fb90e7-3d30-4ef3-a080-0fdeb5def206" />






</p>
<p>
  
- Select Next again, then create a username and password and make sure you do not forget it. Then click Next.
- Then, select “Execute”.


</p>
<br />
<p>
<img width="755" height="590" alt="Step 3i" src="https://github.com/user-attachments/assets/1893f77e-7c90-4dda-8e52-ed05b9404fb4" />




</p>
<p>
  
- Next, Open IIS as an Administrator.



</p>
<br />
<p>
<img width="1034" height="415" alt="Step 3i2" src="https://github.com/user-attachments/assets/be704377-40d6-4235-bbbe-0756104c26d7" />





</p>
<p>
  
- Next, double click on “PHP Manager”.



</p>
<br />
<p>
<img width="623" height="527" alt="Step 3i3" src="https://github.com/user-attachments/assets/058f9bf5-7318-4c5c-a42f-b0f111e74ac8" />






</p>
<p>
  
- Then, click on “Register new PHP version”.



</p>
<br />

<p>
<img width="510" height="220" alt="Step 3i4" src="https://github.com/user-attachments/assets/0ee3d8aa-bc8a-4713-bf3a-2d012549bce4" />





</p>
<p>
  
- Then, click on the 3 dots button “…” next to the path bar.



</p>
<br />
<p>
<img width="949" height="572" alt="Step 3i5" src="https://github.com/user-attachments/assets/73a65c30-e1c7-4cc7-a01d-a55a5af3b82a" />





</p>
<p>
  
- Then, go to the “PHP” folder that we created and select the “php-cgi” application file. Click open then click OK.



</p>
<br />
<p>
<img width="1063" height="371" alt="Step 3i6" src="https://github.com/user-attachments/assets/e9f375cb-d3da-4ec3-8eaf-cc6513198257" />




</p>
<p>
  
-	Then go back to the main interface and on the top right, click “Stop” then click on “Start”.



</p>
<br />

<h2> << Step 4: Install osTicket >> </h2>
<p>
<img width="971" height="564" alt="Step 3" src="https://github.com/user-attachments/assets/aed3b5f7-0702-4f80-bd56-f7828852676f" />

</p>
<p>
  
- Head back to the Installation Files folder on your Desktop.
  -	Right click on the “osTicket-v1.15.8” zip file and Extract all.
  -	In which it will create a folder named “osTicket-v1.15.8”.



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
  - Select “Typical Setup”, then click Next.





</p>
<br />

<p>
<img width="357" height="271" alt="Step 3h1" src="https://github.com/user-attachments/assets/8a2b6bc6-11ca-413b-b13c-d1c22e67cfaa" /> <img width="69" height="271" alt="Right Pointing Arrow for Step 3h 1_2" src="https://github.com/user-attachments/assets/66e054cc-2d13-4456-b2f8-aaee676cb56a" /> <img width="357" height="271" alt="Step 3h2" src="https://github.com/user-attachments/assets/00f1cdf3-2e11-49ef-bf88-032cbcb84987" />







</p>
<p>
  
- Then the “Instance Configuration Wizard” window will appear.
- Select “Standard Configuration”, then click Next.






</p>
<br />
<p>
<img width="358" height="274" alt="Step 3h4" src="https://github.com/user-attachments/assets/b15dc0da-b3d2-4192-9b07-7a50f64bd022" /> <img width="69" height="271" alt="Right Pointing Arrow for Step 3h 1_2" src="https://github.com/user-attachments/assets/eeee5dc0-1d35-4375-ba0e-26da002003ea" /> <img width="358" height="274" alt="Step 3h5" src="https://github.com/user-attachments/assets/f3fb90e7-3d30-4ef3-a080-0fdeb5def206" />






</p>
<p>
  
- Select Next again, then create a username and password and make sure you do not forget it. Then click Next.
- Then, select “Execute”.


</p>
<br />
<p>
<img width="755" height="590" alt="Step 3i" src="https://github.com/user-attachments/assets/1893f77e-7c90-4dda-8e52-ed05b9404fb4" />




</p>
<p>
  
- Next, Open IIS as an Administrator.



</p>
<br />
<p>
<img width="1034" height="415" alt="Step 3i2" src="https://github.com/user-attachments/assets/be704377-40d6-4235-bbbe-0756104c26d7" />





</p>
<p>
  
- Next, double click on “PHP Manager”.



</p>
<br />
<p>
<img width="623" height="527" alt="Step 3i3" src="https://github.com/user-attachments/assets/058f9bf5-7318-4c5c-a42f-b0f111e74ac8" />






</p>
<p>
  
- Then, click on “Register new PHP version”.



</p>
<br />

<p>
<img width="510" height="220" alt="Step 3i4" src="https://github.com/user-attachments/assets/0ee3d8aa-bc8a-4713-bf3a-2d012549bce4" />





</p>
<p>
  
- Then, click on the 3 dots button “…” next to the path bar.



</p>
<br />
<p>
<img width="949" height="572" alt="Step 3i5" src="https://github.com/user-attachments/assets/73a65c30-e1c7-4cc7-a01d-a55a5af3b82a" />





</p>
<p>
  
- Then, go to the “PHP” folder that we created and select the “php-cgi” application file. Click open then click OK.



</p>
<br />
<p>
<img width="1063" height="371" alt="Step 3i6" src="https://github.com/user-attachments/assets/e9f375cb-d3da-4ec3-8eaf-cc6513198257" />




</p>
<p>
  
-	Then go back to the main interface and on the top right, click “Stop” then click on “Start”.



</p>
<br />







