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

<h2> << Step 1: Using Microsoft Azure Connect to a Windows 10 VM using RDP. >> </h2>
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

<h2> << Step 2: Download and extract the osTicket “Installation Files” zip file. >> </h2>

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

<p>
<img width="689" height="303" alt="Step 2c" src="https://github.com/user-attachments/assets/aca34aa7-c4fd-410d-af56-0453b25d4beb" />


</p>
<p>
  
- At the “Apply a Display filter” bar at the top:
  - Type “icmp” and press enter.
  - All the of traffic flows will disappear. Because it will now only show traffic that is pinged.


</p>
<br />

<p>
<img width="667" height="241" alt="Step 2d" src="https://github.com/user-attachments/assets/cceb643f-f595-477a-ab68-9f2a732a92a1" />


</p>
<p>
  
- Next, minimize the windows VM, go back to your Azure VMs web page to get the Linux VM private ip address.
   - You will find it under the Networking section of your VM's properties tab.
   
</p>
<br />
<p>
<img width="748" height="616" alt="Step 2e" src="https://github.com/user-attachments/assets/2796a37d-ccbf-47a6-ad72-eab71a168d63" />

</p>
<p>

- Next, go back to the Windows VM, go to the windows search bar, search for “PowerShell”.
  - Once you find it open PowerShell as an administrator.

</p>
<br />
<p>
<img width="538" height="268" alt="Step 2f" src="https://github.com/user-attachments/assets/ffc7780c-4adc-4917-8369-ab8d91b38847" />

</p>
<p>

- Once in PowerShell type “ping” then type or paste your Linux private ip number.
  - Example: ping 10.1.0.5 


</p>
<br />
<p>
<img width="592" height="395" alt="Step 2g" src="https://github.com/user-attachments/assets/d5979511-5fb3-4127-84dc-9eda418faa11" />


</p>
<p>

- Next, PowerShell will display the ping statistics of the packets sent by the Linux VM and the packets received by the Windows VM.


</p>
<br />
<p>
<img width="969" height="355" alt="Step 2h" src="https://github.com/user-attachments/assets/af1b77ed-aed8-4761-acab-dbbb2cc65ddc" />


</p>
<p>
  
- Once you ping, Wireshark will capture and display its icmp traffic flow. 
  - Will display ping requests from the Windows VM (10.1.0.4) and replies from the Linux VM (10.1.0.5) within the Wireshark interface.

  
</p>
<br />
