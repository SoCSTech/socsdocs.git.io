# CloneZilla Server Imaging

## Server Side
Choose a PC that you want to use as the server. This can be any PC, though the PC you use won't be imaged during this process so if it's not already been done beforehand, it will have to be done afterwards.
So, if there is a PC that's already been done it is better to use that. 

First, start up Clonezilla as outlined [here](Deploying-Images-using-CloneZilla.md).

Once Clonezilla is started, you'll have a list of options. Choose the option 'lite-server'. Then, press start.

![image_71.png](image_71.png)

![image_72.png](image_72.png)

Next, choose local-boot-media as the client PCs will be booted locally (using the Clonezilla bootable USB outlined [here](Deploying-Images-using-CloneZilla.md)).

![image_73.png](image_73.png)

Next, choose DHCP.

On the next options screen, choose 'local-dev' as we'll be using a portable SSD locally as the source of the image.
Press “Enter” to continue when prompted.

![image_74.png](image_74.png)

Make sure that the drive you want the image saved to is plugged into the PC.
The next screen should be black with a list of devices — make sure you can see your drive listed (it will likely start with 'sdb' and have key works like 'SSD' in it).

If you see it, you can press Ctrl-C to close this menu and continue the process.

![image_60.png](image_60.png)

On the next screen you're choosing where the image you'll be using is saved, so choose your portable SSD (usually the bottom option).

![image_52.png](image_52.png)

Choose to skip the file system check (option 'no fsck').

![image_61.png](image_61.png)

The next screen should show the files currently inside your drive. If this looks correct, use the right arrow key to move to select 'done' then press 'Enter' to continue.

![image_62.png](image_62.png)

Next, choose Beginner mode.

![image_63.png](image_63.png)

From the next option screen, select 'massive-deployment'.

![image_75.png](image_75.png)

Next, choose 'from-image' as we're deploying an image to the client PCs.

![image_76.png](image_76.png)

Then, select 'restoredisk' as we're restoring an image onto the whole computer disk rather than just a partition.

![image_55.png](image_55.png)

On the next screen, you'll need to choose the correct image for the lab you're imaging ((you should see the name you gave it when you captured the image).

![image_56.png](image_56.png)

Choose the disk that you want the new image to be on. There is usually only one option here so select that.

![image_57.png](image_57.png)

It will then ask you what partition table to use. Choose '-k0', which is the partition table from the image.

![image_58.png](image_58.png)

Choose to skip checking the image before restoring by choosing '-sc0'.

![image_77.png](image_77.png)

Next, we need to choose what all the client PCs will do once the imaging is done.

![image_53.png](image_53.png)

'True' will enter a command line prompt. We don't normally use, but you can if you think it will suit your purposes better than other options.
'Reboot' will reboot the PC when the image is captured, leaving it booted into Windows.
'Poweroff' will shut down the PC.
'Choose' will present you with a list of options in Clonezilla when the imaged is saved.
These options will be shutdown (shuts down the PC), reboot (reboots the PC), and rerun (starts Clonezilla from the beginning).
Choose is always a safe option as the blue on the screen makes it very obvious to people not to use the PC. 

Choose 'multicast' from the next list.

![image_78.png](image_78.png)

Then, you'll need to choose either time-to-wait or clients-to-wait. Generally, we use time to wait as it is easy to get the count wrong with clients-to-wait and if you get it wrong it can mess up the whole thing.

With time to wait, just make sure you put in enough time for you to get round the entire lab and press enter on every PC (why you'll be doing this will be explained in the next section).
After that time is up, the imaging process will start on the client PCs. You'll just need to wait for it to be done.

![image_79.png](image_79.png)

The screen will have a lot of text on it. It can seem daunting, but we only need one bit of information from this wall of text.

The line above the lowest row of asterisks, there is a line where at the end of the line there is an IP address.
This is the IP address that you need to type into all the client PCs when they are on the IP input screen.

![image_80.png](image_80.png)

Once you have all the client PCs set up, you can then start pressing enter on them all and after the time you specified is over,
the machines will start imaging.

Once the imaging is done, you'll get a prompt on the server PC to press enter, and it will bring up a menu where you can choose to
reboot the PC, shut it down, or rerun Clonezilla (for example, to then set it up as a source for another PC).

![image_81.png](image_81.png)

![image_82.png](image_82.png)

Once everything is imaged, if the PC you've been using as a server has not already been previously imaged, 
you'll have to image it using [direct imaging](CloneZilla-Direct-Imaging.md).

## Client Side
On the PCs that you want to be imaged over the server (the client PCs), the process is quite simple.

First, start up Clonezilla as outlined [here](Deploying-Images-using-CloneZilla.md).

Once Clonezilla has started, you'll have a list of options. Choose the option 'lite-client'.

It may check if you want to continue — if prompted, type 'y' and press enter.

Next, choose DHCP. You may have to wait for a minute for the next step.

It will then show you a box with an IP address. You'll need to check the server that you've set up to see the IP address you'll need to put in.
Put in that IP address on the PC you want to image (normally you'll only have to change the last number or 2), but DO NOT PRESS ENTER YET.

Once all the PCs you want to be imaged are set up with the right IP address, then you need to go around and press enter on all the PCs.
You'll have as much time as you set on the server to do this.

Once that time is done, the imaging will start whether you've got round to all of them or not so make sure you gave yourself enough time to get round an entire lab.

Once the time runs out, the imaging process will start. Then, you just have to wait! Once it's done, it will do whatever you specified on the server side. So either reboot, shutdown or go to a menu with options.

Before the PCs can be used, you'll have to complete some last tasks, which are outlined in [this article](Setting-Up-PC-Post-Imaging.md).
