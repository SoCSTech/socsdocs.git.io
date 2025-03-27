# Capturing the Images

- Update master PC for the lab in question (kept in the office) with everything needed for the Semester (e.g., new software, updates, etc.)
- Boot into the USB by pressing F12 until boot menu opens then choosing the option for USB (this is normally second from last, starting with UEFI and containing something like ‘Sandisk’ or ‘USB’)
- Once the Clonezilla menu opens, press the second option that says ‘Clonezilla live (VGA 800 x 600 & To RAM)’
- Choose English
- Keep the default keyboard layout
- Press start Clonezilla
- Choose ‘device-image’ from the list
- Choose ‘local-dev’
- Press Ctrl+C
- Choose where the image will be saved, normally portable SSD (PSSD)
- Press ‘done’ (have to use the right arrow key to get to this option)
- Choose Beginner mode
- Choose ‘savedisk’
- Name the image (for naming conventions see [this page](Image-Revision-History.md))
- Choose the compression option ‘-zip’
- Choose to skip the check of source file system
- Choose to skip checking the saved image
- Choose not to encrypt the image
- Choose the option ‘choose’ when everything is finished. This could be different depending on the purpose, but it’s always a safe option as it shows people not to use them until we’re ready to finish it up.
- Press enter to continue.
- Wait for Clonezilla to save the image
- Press Y
- Press enter
- Select reboot or power off

Your image is now saved to your Portable SSD! Yay!


