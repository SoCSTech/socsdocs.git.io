# Understanding Imaging and Master Machines

Imaging simply means installing an operating system that already has all the software and settings pre-installed. In
our case, we create a dual boot Windows-Linux image, with required software for teaching, as well as other settings such
as desktop wallpapers pre-configured.

We do this by creating the image manually on a master machine. This is simply done by installing Windows and Linux
normally, and installing software from online just as you would do for any other computer.

There are 3 master machines at the time of writing. A master machine for labs 1A and 1B which has a SATA drive, a master machine for labs 1C and 2B
which has an NVME drive, and a master machine for lab 2C. The 2C master isn't used very frequently so the rest of this
documentation will focus on the 1A/1B and 1C/2B masters.

When creating the master, we usually first do this on the SATA machine, then copy the image over to the NVME machine, and then
capture the image from the NVME machine.
