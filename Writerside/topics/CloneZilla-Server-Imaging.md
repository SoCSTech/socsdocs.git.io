# CloneZilla Server Imaging

## Server Side
- Boot into USB stick (press F12 as PC boots up)
- Start up Clonezilla (option 2 VGA 800 x 600 & To RAM)
- Wait until it starts
- Take out USB stick
- Choose English
- Keep default keyboard layout
- Press start Clonezilla
- Choose option 'lite-server'
- Choose start
- Choose local boot
- Choose DHCP (auto-detect)
- Choose local-dev
- Choose the portable hard drive from the options
- Choose beginner
- Choose 'massive-deployment'
- Choose 'from-image'
- Choose the correct image
- Choose to skip the checks
- Choose what the PC will do when the image is done- either reboot, or choose.
  Choose is useful when in a lab where you want the PC to look unusable after the imaging if you don't want students to use it.
  However, reboot will just reboot the PC and leave it on the Windows log in screen.
- Choose 'multicast'
- Choose either time-to-wait or clients-to-wait. 
- Wait until it's done
- After everything is imaged, you'll have to image the server PC using [direct imaging](CloneZilla-Direct-Imaging.md).

## Client Side
- Boot into USB stick (press F12 as PC boots up)
- Start up Clonezilla (option 2 VGA 800 x 600 & To RAM)
- Wait until it starts
- Take out USB stick
- Choose English
- Keep default keyboard layout
- Press start Clonezilla
- Choose option 'lite-client'
- Choose DHCP (auto-detect)
- IP screen will come up. See the server PC 
- Wait until it's done