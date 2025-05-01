# Setting Up PC Post-Imaging

After imaging the PCs, there are still some steps to take before the PCs can be used in teaching. These steps need to be  done
on every computer in the lab you've imaged.

## Rename
First, the PC needs to be renamed. When it's first imaged, it will have the generic name of the master 
such as '1A-MASTER-WINDOWS'.

However, we need them all to have individual names based on their desk number. 
So, for desk 6 on row E in 1A running Windows, the name would be '1A-E6-WINDOWS'. 
The room number goes first, then the row and desk number, then the operating system.

There are 2 ways for us to change the name. 
1. Press Windows+I to go into system settings, or find it from the task menu. At the top of the screen underneath
PCs name you'll see the option 'Rename'. Press this, and you'll be prompted with a text box where you can enter the new name for the PC.
Once you've entered it, press 'Next'. It will then prompt you whether you want to restart now or later.
When you restart is up to you, but when it does restart the name will be successfully changed.
2. Open Powershell as admin. Type in the command 'Rename-Computer' and press 'Enter'. 
It will then prompt you to enter the name. Once it's entered, press 'Enter'. 
You can choose to restart the PC now or later, but when you do restart it the name will be successfully changed.

## Boot Order
You will need to check the Boot Order of the PCs in BIOS. 
To enter BIOS, press 'Del' repeatedly as the PC is starting up, and it should take you to the BIOS menu.
Enter advanced mode using 'F7'. Navigate to the 'Boot' tab, and make sure that Boot Priority position 1 is 'Refind'.
If it's not, select position 1 to open a menu with a list of the boot options, and select Refind. 
This will change Refind to be the 1st boot option. 

## Deep Freeze

All the PCs need the program DeepFreeze installed on them. Details of DeepFreeze and how to deploy it on the PCs
can be found in the [DeepFreeze section](DeepFreeze.md).