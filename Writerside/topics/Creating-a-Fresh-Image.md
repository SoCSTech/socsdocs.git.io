# Creating a Fresh Image

## Aim
Every summer, a fresh lab image needs to be created ready for the start of the academic year in September.

## Procedure
We create our Lab Machine images on the Master machines in INB1201. The following procedure outlines how we create and 
deploy a new image to the lab machines.

Before this procedure can be followed, a full list of software requirements must be collected from academics by sending
an all school email well in advance with multiple reminders.

* Locate the SATA Master Machine
* Install a fresh copy of Windows 11
* Create a partition for Linux
* Install Linux on this partition
* Update Windows, configure Windows settings, and set wallpapers
* Install all required software for Windows
* Update Linux, configure Linux settings, and set wallpapers
* Install all required software for Linux
* Set up GRUB
* Test the image
* Capture both the SATA and NVME images
* Deploy the images to the labs using CloneZilla
* Install DeepFreeze on all machines
