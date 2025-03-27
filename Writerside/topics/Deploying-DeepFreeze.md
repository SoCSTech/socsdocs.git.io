# Deploying DeepFreeze

Deploying DeepFreeze is as simple as running an installer. The installer can be downloaded from the
main dashboard by clicking the 'Install Cloud Agent' button.

![InstallCloudAgent.png](InstallCloudAgent.png)

![DownloadInstaller.png](DownloadInstaller.png)

From this page, a group should be selected, which will have an enforced policy. In this case, the 1A
group is selected which has the 'Computing' policy enforced.

When you first install this time it will be named something generic,
so make sure to name it something simple like that, so '1a' for lab 1A,'1b' for lab 1B, etc.
It makes it easier to keep track of which installer is for what lab.

This installer can be used in Lab 1A to deploy DeepFreeze. Usually we also create a batch script
which copies the installer from a memory stick to the computer, and then runs the installer. This way,
we don't need to wait for the installer to finish before we unplug the memory stick.

## Batch Script
As mentioned previously, we usually create a batch script to help us when installing DeepFreeze. 
This script copies the installer over to the desktop of the computer from the memory stick, and then runs it.
This means that as soon as the script is run, we can remove our memory stick and move onto the next PC. 
This is incredibly useful when you need to deploy DeepFreeze to every PC in a large lab, and saves a lot of time. 

The script looks like this: 

"COPY 1a.exe C:\Users\Student\1a.exe
C:\Users\Student\1a.exe"

It's only 2 lines, so nice and easy. 
The '1a.exe' refers to the installer file you've downloaded. You'll need to change this part so it works on the installer you're using,
so if you're installing DeepFreeze in 1B, your installer file should be named '1b' and you'll change the batch file so it says that instead of '1a'.

Once you've made the batch script, make sure it and the installer are on a USB stick, then click to run the script.
This will copy over the file and start the installation. Once the installation has started (so the DeepFreeze box is up), you can unplug the USB stick
and move onto the next PC. And that's it!

