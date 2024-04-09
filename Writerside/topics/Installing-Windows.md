# Installing Windows

OK, this bit is straight forward, but due to how we get our licences, there are a few differences. They'll be outlined here.

## The ISO

We use an ISO downloaded using the Windows Media Creation Tool - however, we need to _slipstream_ our key into the ISO 
in order for it to activate.

The University uses a KMS key to activate Windows, as we use the Enterprise SKU. The Key is common knowledge as it 
relies on a local server to work.

The key is: `NPPR9-FWDCX-D2C8J-H872K-2YT43` - and can also be found on the shared 1Password vault. Unless making a 
new ISO, you won't need to worry about this too much. 

If you do need to make a new ISO - download the Windows Media Creation Tool, and open a terminal in the folder you downloaded it to. 
In that terminal run `.\MediaCreationTool.exe /Eula Accept /Retail /MediaArch x64 /MediaLangCode en-GB /MediaEdition Enterprise`, the executable will run and ask you 
for the above key. From there, you can create the ISO image and burn a USB using Rufus.

### Rufus
Rufus will appear with a prompt regarding some configuration options it can slipstream in for you. Have it automatically
deny any permissions - it will save you a load of time in the setup.

## Installing 
From here, installing Windows is how you would now expect it, however - for older machines, you will need a few more 
steps which will be outlined in a later revision of these docs. 

## Windows Setup (OOBE)
Once the installation has completed, you will need to make an account. We make an account called SoCSTech Admin as it means 
we can have some network volumes mounted away from the Computing user.

When it asks for you to sign in, click "Domain Join", and create an account using the following details:

Username: `SoCSTech Admin`

Password: Check what the current password rotation is and use that

Reset Questions: Check rotation answers

From there, the installation will automatically configure privacy settings (if you set them up above) and dump you onto
a desktop after a little while.
