Part 1 - Buidling VMs

1.) The first step to setting up a guest OS on your host machine should be to download a virtual machine software on your host OS. In this case I installed Virtual Box. Since I am operating Windows as my guest host I will be downloading the Windows host platform package. That can be found here https://www.virtualbox.org/wiki/Downloads  

2.) Got to UBUNTU's website and download the latest ISO file (unless you prefer a certain version. Make sure to download Ubuntu desktop version in order to perfrom certain actions. This can be found at https://ubuntu.com/download/desktop

3.) Once you have passed the last two steps, open Virtual Box and you will be taken to the main menu. Once there select the "New" button. This will take you through a prompt to setup your guest OS. 
	
	a.) When allocating RAM only allocate the amount of RAM your host can allocate. So if you have 8GB of RAM do not allocate more than that in the Virtual Box. 
	b.) Next it will ask how you want your storage optimized. Would you like it Dynamically allocated or fixed? I choose Dynamically because it only uses storage on what is needed. Fixed is as it sounds, there is a set amount of storage set aside and stays the same no matter if you use it or not, but will not expand past the fixed amount you set it at.
	c.) Now that we have gone through the prompts to create your virtual machine, you should now see it on the left side whatver name you gave it. Now click on the machine and then select the "Settings" button. Once in the settings page select the "Storage" option on the left side. Here you will need your Ubuntu ISO file you downloaded earlier. Under the sotrage devices tab select the disk Icon that says "Empty". Then on the right select the dropdown CD icon and select "Choose a disk file" Locate where you downloaded your ISO file, click on it and click on open. 
	d.) I have no use for 3D acceleratioin for this Virtual Machine so, no I will not be enabling it. If I was using my gaming desktop I would have plenty of GPU resources, but since I am using my laptop I do not have the resources for it, nor like I said earlier I won't have any use for it. 
	e.) Some guest addtions I decided to add to my virtual box was Shared Clipboard (Biderectional), and Drag n' Drop (Biderctional). This allows me to share my files between my Host machine and my Virtual machine and the ability to copy and paste vice versa. 

Part 2 - Exploring Virtualization 

1.) My guest OS is saved on my Host machine found in this directory, C:\Users\south\VirtualBox VMs\Ubuntu 20.04

2.) No you are unable to directly access your Guest files from the virtual machine image folder. 

3.) Snapshots is a cool feature that allows you save a particular state of a virtual machine and revert back to that state if you need to. If something goes wrong, such as problems after installing software or infecting the guest with a virus, you can easily switch back to a previous snapshot and avoid the need of frequent backups and restores.
	
	a.) My first snapshot was 660MB in size. 
	b.) A VM template is a master copy image of a virtual machine that includes VM disks, virtual devices, and settings.

 Part 3 - Networking with Style

 1.) The Networking method I tried that was not NAT was, bridged adapter. 