# CloneZilla Direct Imaging

First, follow the steps outlined [here](Deploying-Images-using-CloneZilla.md) to get Clonezilla started.

The next step will give you a lot of options. For direct imaging, you'll need to choose ‘device-image’ from the list.

![image_50.png](image_50.png)

Next, choose ‘local-dev’ as we'll be saving to a local device (a.k.a. a portable hard drive). Press 'Enter' when prompted.

![image_51.png](image_51.png)

Make sure that the drive you want the image saved to is plugged into the PC.
The next screen should be black with a list of devices — make sure you can see your drive listed (it will likely start with 'sdb' and have key works like 'SSD' in it).

If you see it, you can press Ctrl-C to close this menu and continue the process.

![image_60.png](image_60.png)

On the next screen you're choosing what drive the image you want is saved on, so choose your portable SSD (usually the bottom option).

![image_52.png](image_52.png)

Choose to skip the file system check (option 'no fsck').

![image_61.png](image_61.png)

The next screen should show the files currently inside your drive. If this looks correct, use the right arrow key to move to select 'done' then press 'Enter'.

![image_62.png](image_62.png)

Next, choose Beginner mode.

![image_63.png](image_63.png)

On the next screen, select 'restoredisk'.

![image_55.png](image_55.png)

Choose the correct image that you want to image the PC with (you should see the name you gave it when you captured the image).

![image_56.png](image_56.png)

Choose the disk that you want the new image to be on. There is usually only one option here so select that.

![image_57.png](image_57.png)

It will then ask you what partition table to use. Choose '-k0', which is the partition table from the image.

![image_58.png](image_58.png)

Choose to skip checking the image before restoring by choosing '-scr'.

![image_59.png](image_59.png)

The last major step is choosing what action should be performed when everything is finished.

![image_53.png](image_53.png)

'Choose' will present you with a list of options in Clonezilla when the imaged is saved.
These options will be shutdown (shuts down the PC), reboot (reboots the PC), and rerun (starts Clonezilla from the beginning).
Choose is always a safe option as the blue on the screen makes it very obvious to people not to use the PC.
'True' will enter a command line prompt. We don't normally use, but you can if you think it will suit your purposes better than other options.
'Reboot' will reboot the PC when the image is captured, leaving it booted into Windows.
'Poweroff' will shut down the PC.

Select whichever option would best suit your needs.

Press enter to confirm, then type y when prompted until the imaging process starts.

Finally, wait until it's done. When it's finished, you'll need to do some things before it's ready for use. 
This process is explained [here](Setting-Up-PC-Post-Imaging.md).
