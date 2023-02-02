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


 - Now enter any password, Keep in mind this is a pentest lab so either make it easy or difficult. 
 - I entered "Password1"
 - Press " finsih "


![image](https://user-images.githubusercontent.com/38595857/216207556-50c1dc0f-5da8-42ef-8c9d-0f388c738a19.png)

 
 
 - Search " pc name" and change it to whaterver you want

![image](https://user-images.githubusercontent.com/38595857/216208257-71ac6c79-fe0e-4b42-b6d1-d885b9f0e355.png)


- After you change it, press " restart now"

 ![image](https://user-images.githubusercontent.com/38595857/216208338-7e18fb01-0a73-48be-968e-510ad8e51dc9.png)


- It will now pop up the server dashboard
- press "Manage" then " add roles and features" 

 
 ![image](https://user-images.githubusercontent.com/38595857/216208864-6c04c3bb-6ba4-4a20-a74b-f725ee733d3b.png)

 
 - Select Next until you get to server roles 
 - once there, press " active directory domain services" 
 - afterwards press next all the way then press install
 
 ![image](https://user-images.githubusercontent.com/38595857/216209065-25d2faca-7c18-4bfc-a8af-d351b93ff793.png)

 
 
 - Next hit the flag in th eupper left hand corner
 - Then select promote this server to a domain controller


 ![image](https://user-images.githubusercontent.com/38595857/216210223-bb6fd366-fb40-41da-9213-375a2744f2c1.png)


- press "add a new forest"
- Go ahead and give your domain a name


![image](https://user-images.githubusercontent.com/38595857/216210399-3ab78fa4-6552-4397-b661-c3d61fb7e0ce.png)


- Next give it a password
- i entered " Password1"

![image](https://user-images.githubusercontent.com/38595857/216210566-14cfdd38-238f-47ae-b882-9d9e3f3bf47b.png)


- Now presss next until you get to the pre-req screen.
- Press install and it will reboot aftwards


![image](https://user-images.githubusercontent.com/38595857/216210783-90973e72-99e8-4de4-85d1-fc071b9350ae.png)



- Now after you sign back in,
- Click "manage" then " add roles and features

![image](https://user-images.githubusercontent.com/38595857/216212148-a3d566f6-0869-420a-9335-4d7daa8650ba.png)



- Now click next until you get to  " server roles"
- Now click on " Active directory certificate services"


![image](https://user-images.githubusercontent.com/38595857/216212342-16fe8d20-37d9-4e98-8ff6-10aecbba6aa5.png)


- Now press next until final screen
- Check the box " Restart the destination server automatically if required" 


![image](https://user-images.githubusercontent.com/38595857/216212520-d40c783e-4a60-4df5-8061-e7ba1ee4804e.png)


- Next hit the flag in th eupper left hand corner
 - Then select " Configure active directory certificate services..."

![image](https://user-images.githubusercontent.com/38595857/216212695-2a1bf848-d396-4463-8914-080753deb337.png)


- Check off certification authority

![image](https://user-images.githubusercontent.com/38595857/216212917-34dbe077-83a8-4226-9d21-522efbbd763c.png)


- Finally, leave everything else as deafult and press next then configure
- Press restart then log back in.


![image](https://user-images.githubusercontent.com/38595857/216213105-01ead12e-6144-46bc-a9d2-f961bab5e26b.png)




# Step 8
We will add users, file share, and sharing account


- Press Tools, then active directory users and computers

![image](https://user-images.githubusercontent.com/38595857/216213490-2c16fc58-c61d-472b-b497-d74a650a11a4.png)


- We can see our computer and so much more

![image](https://user-images.githubusercontent.com/38595857/216213608-9f2a7be1-5479-49f4-be7b-2dc1a9e214bf.png)



- Right click on your directory -> then new -> then Organazational unit 


![image](https://user-images.githubusercontent.com/38595857/216213785-21e82743-84a0-4a61-8ce4-15960310d3f9.png)


- Create groups than press ok

![image](https://user-images.githubusercontent.com/38595857/216213840-08da6484-89d6-4304-ad55-a0a00eeff738.png)


- to clean up the "users" folder, we will move all other users excep admin and guest to the groups folder


![image](https://user-images.githubusercontent.com/38595857/216213982-218d905f-5d13-4fe5-8681-87c96f0d3e4d.png)


![image](https://user-images.githubusercontent.com/38595857/216214028-8ec896a4-0a04-49ec-aecc-a72489faefa1.png)



- Now lets create users
- You can creat as many as you want :)


- I will create 3
- Username = anyi Password = Password1
- Username = oaklandUni Password = Iwillhackyou123
- Username = Username Password = Password123

 
 
 ![image](https://user-images.githubusercontent.com/38595857/216215105-1a192bb8-da70-49f9-bf80-6d5dd5aaab43.png)


- Next copy the administrator 
 - Username = SQLService Password = Password123#


![image](https://user-images.githubusercontent.com/38595857/216215487-ab34d0ee-0cf2-44b3-855f-0311c7d74647.png)



- Now we will creata a SPN (Serice principal Name) for the SQL service user
 - Open Command prompt as an admin
 - enter the commans
    - setspn -a Messi/SQLService.SOCCER.local:60111 SOCCER\SQLService
    - then type,  setspn -T SOCCER.local -Q */*      *this is to find it*


![image](https://user-images.githubusercontent.com/38595857/216216194-8d6e2f75-7f71-464b-b350-a6d216d72dbd.png)

 
 
 - for smb atacks we will open ports 149 & 445 open
 
 
 
 - Next lets create a folder called "hackme" in the c drive, for the smb attacks


 ![image](https://user-images.githubusercontent.com/38595857/216216574-bc47ab21-ffb4-40b1-91e9-777faa32285b.png)



- Now go to File storage and servcices
- then click on shares
- then click on tasks
- Then new share

![image](https://user-images.githubusercontent.com/38595857/216216727-060d7436-8f53-4679-b8f3-9e81bb84e20e.png)



- select a custom path and choose the folder you just created

![image](https://user-images.githubusercontent.com/38595857/216216870-afbda3ab-ebed-4f4f-bb65-d78c426818ea.png)


- we now have the port open for this attack

![image](https://user-images.githubusercontent.com/38595857/216216988-aeb49b74-39c1-412d-b38e-74dbe98a1596.png)


- next run a command prompt as an admin
- enter ipconfig  *to grab the ip address of this server*
- mine is 192.168.11.128
![image](https://user-images.githubusercontent.com/38595857/216217075-7087dadd-52d6-4749-9e30-ea15e193a7cc.png)



# Step 9
we will build out user machines







 
 
 
