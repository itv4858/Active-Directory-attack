# Active-Directory-attack

In this tutorial, we will be creating a Windows server containg active directory and perfoing attacks to retreince the users account. 


# Possible Attacks

•	SMB Relay attacks       
•	Pass-The-hash       
•	Pass-The-Password       
•	Kerberoasting       
•	Golden Ticket       
•	Token Impersonation         
•	LLMNR/NBT-NS Poisoning 


# Links Used

•	https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html

•	https://www.virtualbox.org/wiki/Downloads

•	https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019

•	https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise

# Instructions

# Step 1
Download the VMware 

- Download VMware Workstation Player
- https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html

# Step 2
 We need to download a few files from Microsoft in order to get the Vmware working correctly. 
 
 - First, Download the Windows Server 2019
 - Go to https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019
 - Select "Download the ISO" 
 
 ![image](https://user-images.githubusercontent.com/38595857/216202044-b08a652f-f602-497d-bf32-fd65f0e602f0.png)

 
 
 
 - Next download the Windows 10 Enterprise
 - Go to https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise
 - Select "Download the ISO" 

![image](https://user-images.githubusercontent.com/38595857/216202843-654ed105-4934-40ad-8bb8-7ea0bc4cb9d2.png)

 
# Step 4
Now open up VMware
We will be adding both ISO files

- Select "Create a New Virtual Machine"
 
 ![image](https://user-images.githubusercontent.com/38595857/216203450-74927c8c-8f8e-4cb2-801a-9b2ddc713779.png)

 
 
 - Select " Installer disc image file (iso):"
 - Then select you Windows server 2019 iso

![image](https://user-images.githubusercontent.com/38595857/216203758-df1c1eaf-2d8d-42ed-8497-0bda0a249faf.png)

 
 
 - Next, in the drop down of  "Version of Windows to install" Press " Windows Server Standard Core"
 - **** You do not need to add a product key****
 - DO NOT ENTER A PASSWORD

![image](https://user-images.githubusercontent.com/38595857/216204086-7d4c315f-166b-4d32-af93-c7929b6fe4b4.png)

 
 - Select next


 ![image](https://user-images.githubusercontent.com/38595857/216204258-0a272de3-56e5-44ea-a798-a383c838281e.png)

 
 - Leave as default disk space and press next


 ![image](https://user-images.githubusercontent.com/38595857/216204375-91f5ad1c-77fb-4ab0-9e2c-726018486046.png)

 
 
 
 - MAKE SURE TO UNCHECK " POWER ON THIS VIRTUAL MACHONE AFTER CREATION
 - Press " Finish" after you're done


![image](https://user-images.githubusercontent.com/38595857/216204490-cb31695a-342c-4271-96cd-adda3bb1325c.png)

 
 
 
# Step 5
We need to fix a few settings for the server

- Press " Edit virtual machine settings"
![image](https://user-images.githubusercontent.com/38595857/216204696-74dab8a5-018d-4ea8-8824-936900243be9.png)


- Adjust memory to fit your ram size on your machine


![image](https://user-images.githubusercontent.com/38595857/216205164-060c41ba-4734-4ad5-918b-1b02f8bc6ed5.png)


 - Next, select the floppy disk and remove it


 ![image](https://user-images.githubusercontent.com/38595857/216205263-bc678a7f-739d-4ea5-8093-ffed197fa027.png)


- Next, make sure the network adapter is set to NAT
- Afterwards, press okay and power on the machine


![image](https://user-images.githubusercontent.com/38595857/216205387-0853e7dd-2409-46cc-9e82-a063dfe2edab.png)


# Step 6
We will finsih the setup for Windows Server 2019

- Press next

![image](https://user-images.githubusercontent.com/38595857/216205838-ec43ded9-8941-4ff7-b87d-195c99049476.png)


-Press Install now

![image](https://user-images.githubusercontent.com/38595857/216205885-02d1fca6-4c3d-4795-bffa-69ed7fbd4101.png)



- Select the " Windows Server 2019 Standad Evaluation (Desktop Expierence)
- Then next

![image](https://user-images.githubusercontent.com/38595857/216206044-1a69a740-c16b-4970-b689-e1669a8d70ad.png)



 - Press accept and select next


![image](https://user-images.githubusercontent.com/38595857/216206190-d3dd0d00-4843-41f9-a889-5a3b4a808598.png)


-Press " Custom windows install"


![image](https://user-images.githubusercontent.com/38595857/216206292-ccddb9c9-3f3e-45f7-95ae-dafa0cc2b9ba.png)


 
 - Next, select "New"


![image](https://user-images.githubusercontent.com/38595857/216206353-917c89f7-a222-4271-9752-d535f55bc0ff.png)


- Next, select "Apply"


![image](https://user-images.githubusercontent.com/38595857/216206421-4e3f64e8-9532-4934-a023-97682e2170f9.png)



- Now press next, it will not install windows


![image](https://user-images.githubusercontent.com/38595857/216206500-c4da746d-0124-401f-8d67-8cc40431d774.png)





# Step 7


 
 
 
 
 
 
 
 
 
 
 
