# CloneZilla P2P Imaging
Another way you can image PCs is using one PC that has already been imaged as the 'source' of the image that can be put onto a 'destination' PC.

However, this can only be done BEFORE DeepFreeze is installed on the source PC. 

## Source Side
First, follow the steps outlined [here](Deploying-Images-using-CloneZilla.md) to get Clonezilla started.

The next step will give you a lot of options. For peer-to-peer imaging on the source PC, you'll want to choose 'remote-source'.

Next, choose 'Beginner' as it is easy to use, and we don't need anything from expert mode.

From the next screen, choose 'disk-to-remote-disk' as we want to image the entire disk and not just a partition.

When asked about network mode, choose 'dhcp'. It may take a few seconds to set up, so wait until you get to the next menu.

Next, choose a local disk as a source. For the purposes of peer to peer imaging, you'll want to choose main disk of the PC.
If you have no drives plugged in, this should be the only option so choose that. If you do have stuff plugged in, it will be the one which
doesn't have anything like 'SanDisk' or 'Portable_SSD' in its name. It is also usually at the top of the list.

We want to skip the checks so choose '-sfsck' to skip checking the source file system.

Then, choose to use the partition table from the source image by choosing '-k0'.

The last major step is choosing what action should be performed when everything is finished.

![image_53.png](image_53.png)

'Choose' will present you with a list of options in Clonezilla when the imaged is saved.
These options will be shutdown (shuts down the PC), reboot (reboots the PC), and rerun (starts Clonezilla from the beginning).
Choose is always a safe option as the blue on the screen makes it very obvious to people not to use the PC.
'True' will enter a command line prompt. We don't normally use, but you can if you think it will suit your purposes better than other options.
'Reboot' will reboot the PC when the image is captured, leaving it booted into Windows.
'Poweroff' will shut down the PC.

Select whichever option would best suit your needs, then press 'Enter' to continue when prompted.

You'll have to wait a little for it to set itself up. You'll know it is done when the bottom of the screen says 'Waiting for the target machine to connect'.

Once it is set up, it will give you an IP address, which you can enter on the destination PC once that side is set up.

Once the imaging is done, you'll get a prompt on the source PC to press enter, and it will bring up a menu where you can choose to
reboot the PC, shut it down, or rerun Clonezilla (for example, to then set it up as a source for another PC).

## Destination Side
First, follow the steps outlined [here](Deploying-Images-using-CloneZilla.md) to get Clonezilla started.

The next step will give you a lot of options. For peer-to-peer imaging on the destination PC, you'll want to choose 'remote-dest'.

When asked about network mode, choose 'dhcp'. 
It may take a minute to set up, but once it is done you should be met with a screen with an IP address in a text box.

Once the source side is set up, you should have an IP address from that screen. 
You now need to enter that IP address into the text box on the destination PC and press 'Ok'.

Press 'enter' or type 'y' when prompted to confirm that you want to continue with the imaging process.

It will then start imaging. Wait until it is done, then it'll do whatever you choose when setting up the source side.

Before it can be used by people in the lab, you'll have to complete some last steps, which are outlined [here](Setting-Up-PC-Post-Imaging.md).




