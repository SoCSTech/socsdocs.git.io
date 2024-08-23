# Creating a Linux Partition

In 2425 we used PopOS as our Linux distribution.

1. Create an empty 250GB partition in Windows Disk Manager.
2. Boot into PopOS Live environment.
3. Resize the EFI partition to be 1GB.
   * Use GParted to move all of the partitions to the right of the EFI partition over to give space to expand into.
   * Back up the contents of the EFI partition.
   * Resize the EFI partition to 1GB. This will wipe it.
   * When resizing is complete, copy the backed up EFI files back to the EFI partition.
   * Move the other partitions back over to the left adjacent to the EFI partition.
4. Create a new ext4 partition in the empty 250GB space you made earlier.
5. There should now be 5 partitions, EFI, Windows Recovery, Windows Reserved Space, Windows NTFS, and the new ext4 for the Linux file system.
6. Follow prompts in the PopOS installer. Make sure to choose a custom installation.
7. When choosing the partitions to install PopOS on, select the EFI partition you just resized, and make sure that 'Format' is NOT checked. If you leave the format box checked all your hard work will be lost.
8. Select the 250GB ext4 partition as the main install location for PopOS.
9. Done!