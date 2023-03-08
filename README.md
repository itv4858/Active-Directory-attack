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
- Username = Username Password = Password1
 
 
 ![image](https://user-images.githubusercontent.com/38595857/216215105-1a192bb8-da70-49f9-bf80-6d5dd5aaab43.png)


- Next copy the administrator 
 - Username = SQLService Password = Password123


![image](https://user-images.githubusercontent.com/38595857/216215487-ab34d0ee-0cf2-44b3-855f-0311c7d74647.png)



- Now we will creata a SPN (Serice principal Name) for the SQL service user
 - Open Command prompt as an admin
 - enter the commans
    - setspn -a Messi/SQLService.SOCCER.local:60111 SOCCER\SQLService
    - then type,  setspn -T SOCCER.local -Q */*      *this is to find it*


![image](https://user-images.githubusercontent.com/38595857/216216194-8d6e2f75-7f71-464b-b350-a6d216d72dbd.png)

 ![image](https://user-images.githubusercontent.com/38595857/223738892-ac450cdb-4184-49f6-8229-06ad5f9f3e82.png)

 
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

- We will complete same steps as above, but this time with the windows 10 enterprise iso
- I created 2 users for 2 machines


- hit Domain Join Instead
- We will enter the details of ther users we created in the server machine
- then follow throw with the rest of the install

![image](https://user-images.githubusercontent.com/38595857/216220486-104bd4f9-b5e3-4952-a37c-35e15ad630c2.png)



- Next we donwload vmtools
- then change the name on both pcs
- anyi = user1
- oaklandUni = user2




- We will now join the domain server to both machines 
- We go into the netowrk settings, and add the ip to the ipv4 dns 

![image](https://user-images.githubusercontent.com/38595857/216222173-b777221e-f7f7-42e3-85af-58d88ece0cbf.png)


- next we will add the domain

![image](https://user-images.githubusercontent.com/38595857/216222395-4ae589f2-8433-42a9-8bab-5a484797111a.png)



- We can now see both machines in active directory

![image](https://user-images.githubusercontent.com/38595857/216223011-be780f4f-8e43-49de-868f-71c916d2baba.png)


- we now are adding user under admin

![image](https://user-images.githubusercontent.com/38595857/216223448-59f2c947-518e-4e63-b09f-0b885a934fe9.png)



# Step 10
we will do	LLMNR/NBT-NS Poisoning 





# Step 11

Now lets perform a Kerberoasting attack


- First, we need to make sure we have a user account on the windows server
- go to cmd and type  " net user Username"
- i already know we do, beacuse i added the user, but this is to confirm and output the basic info



![image](https://user-images.githubusercontent.com/38595857/216228590-a4b129d0-8402-4314-83f6-04342de16a14.png)


- We will use a command called 
- Impacket-GetUserSPNs
- (Service principal name)

![image](https://user-images.githubusercontent.com/38595857/216229363-279281f9-1a52-4699-85b0-d1c52b159c5f.png)

- We are now able to Kerberoast the account using the command
- impacket-GetUserSPNs -dc-ip 192.168.11.128 SOCCER.local/SQLService
- Enter the password


![image](https://user-images.githubusercontent.com/38595857/216230121-5c1be911-8998-4fba-afcf-3447e3517482.png)


- We will perform the kerbo attack to get the hash by using the command
- impacket-GetUserSPNs -dc-ip 192.168.11.128 SOCCER.local/Username -request

![image](https://user-images.githubusercontent.com/38595857/216230534-4f1e91c6-a819-4b17-8067-de9c8299d0ab.png)


- We will then use Hash cat to crack the hash of the kerbo attack


![image](https://user-images.githubusercontent.com/38595857/216230865-47c5a65c-9663-4853-9650-e96fe009a72c.png)


- we will use this command to crack the hash.txt
- hashcat -m 13100 -a 0 hash.txt wordlist.txt --force
- -a 0 = dicationary attack

![image](https://user-images.githubusercontent.com/38595857/216353309-df1ce4cb-315a-4070-bd00-a798015a26b3.png)


- PASSWORD IS CRACKED
 
 
 # Step 12
 
 llmnr attack
 
 
 
First we type
- cd into responder directory
- cd /usr/share/responder/


![image](https://user-images.githubusercontent.com/38595857/217105330-1409f606-a609-473f-a50b-c727ecd2b407.png)


- then go into root and run the command below
 - python Responder.py -I eth0 -rdwv
 - We run this becauser it allows us to do this attack by impacket. 


![image](https://user-images.githubusercontent.com/38595857/217105751-e86efd06-5b28-4b0a-8f06-bd8abf22243e.png)


- once into the windows server we apply the repsonders IP to connect inot the netowrk drive and from there we get the hash on our kali machine

![image](https://user-images.githubusercontent.com/38595857/217106760-7029cb3b-1824-4e77-9205-4385cb9a8f58.png)


![image](https://user-images.githubusercontent.com/38595857/217106804-ddbc078a-2b32-4729-bcf4-ca8b963080d7.png)


- now lets crack the hash using hashcat 

- hashcat -m 5600 -a 0 newhash.txt rockyou.txt



![image](https://user-images.githubusercontent.com/38595857/217107201-4d88d352-7d9f-4703-9622-e9a11cacdb1c.png)


![image](https://user-images.githubusercontent.com/38595857/217107289-e0143d80-34fb-4701-9455-7760cf6ad3db.png)



- passwrod is cracked

# Step 13

- smb relay attacks


-go into root
- go into repsinder directory
- - modify .conf folder and turn off smb and http

![image](https://user-images.githubusercontent.com/38595857/217108138-e05dfa86-c5c0-4ca6-ac89-ec646336c05d.png)


![image](https://user-images.githubusercontent.com/38595857/217108207-ead4e397-ee16-43a6-bd0d-d8df5d4778b0.png)



- then run the command below
 - python Responder.py -I eth0 -rdwv
 - We run this becauser it allows us to do this attack by impacket. 



![image](https://user-images.githubusercontent.com/38595857/217109244-1de77152-71d6-4e6b-8ad8-50c74e1b8ea5.png)



![image](https://user-images.githubusercontent.com/38595857/217109414-6c8722a2-8c2f-4bc0-93af-c072b03a226b.png)


- next in the server we just try to connect to some fake foler

![image](https://user-images.githubusercontent.com/38595857/217109553-faf581ca-c3f8-4a2a-96a9-6191828775ec.png)


- the the attack hits and we get the hash

![image](https://user-images.githubusercontent.com/38595857/217109574-72db7f5c-f368-4bce-825b-9e2916e87d4e.png)



![image](https://user-images.githubusercontent.com/38595857/217109609-5dd95f48-53e3-4a4c-8fe6-da2fcc3c2cc4.png)



![image](https://user-images.githubusercontent.com/38595857/217110948-c517fb87-743b-4fb2-bf63-1dcbdd67c6c3.png)















