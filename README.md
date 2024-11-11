# Dell-Optiplex-1070-Hackintosh-Nvidia-GTX-1050Ti

PC Specs:
1. Processor i7-3770 3.4 Ghz
2. dGPU Nvidia GeForce GTX 1050 Ti
3. RAM 32 GB
    
This config plist and kext compilations divided into 3 stages:
1. macOS High Seara - Stage 1
    - This EFI still need 2 or 3 Security Updates from Apple before you can update your Nvidia Web Driver. After 1st update you can update your Nvidia Web Driver and goes the same until the last update of High Seara and giving you Nvdia Web Driver 387.10.10.10.40.140 version.

   - Don't forget to backup your work when you reach the last updates of High Seara in case you have trouble then you can go back to Time Machine with High Seara as your foundation.

   - Don't forget to copy this macOS High Seara EFI files to your EFI partition when you are done with High Seara final updates so you don't have to boot with USB Flash Disk.
   
2. macOS Monterey - Stage 2
   - Still in the High Seara OS, download the latest OCLP.
     
   - Prepare your USB Flash Disk (size 32 gb minimum to avoid lack of space when creating installer).
     
   - Plug you Flash Disk and open OCLP.
   
   - on OCLP app go to setting first. Choose Target as "Host Model" if the chosen target cannot make the option "Build and Install Opencore" button ready then chage the target to whatever you want and make it back again to "Host Model" until that "Build and Install Opencore" button ready to be used.
   
   - Still in the OCLP app - Setting, go to Security - Kernel Security, checklist "Disable Library Validation" and "Disable AMFI".
   
   - Next on the same page go to System Integrity Protection and checklist "ALLOW_UNTRUSTED_KEXTS", "ALLOW_UNRESTRICTED_FS", "ALLOW_UNAPPROVED_KEXTS" AND "ALLOW_UNAUTHENTICHATED_ROOT".
   
   - Next return to front page app and click "Create macOS Installer" and follow the instruction that given in OCLP website to create Disk Installer.
     
   - Meanwhile you wait your intaller ready you can try to replace the macOS High Seara EFI with macOS Monterey EFI on your EFI partition (assuming you already have macOS High Seara EFI on your EFI partition - Stage 1)
     
   - When the installer ready - OCLP macOS Monterey finishing dowloaded - and you already install "OpenCore" on the USB Flask Disk, now you ready for reboot with holding "Option" (ALT) button.
     
   - When you already in the Recovery Mode go to Disk Utility and make sure the disk where you want to install macOS Monterey exist, if its not then reboot your PC - still using hold ALT as per OCLP instruction.
   
   - Assuming everything run normal, now you have macOS Monterey on your Dell Optiplex 7010.
    
   - Now back to OCLP app - go to Setting - check your Target (remember to make checklist "Disable Library Validation" and "Disable AMFI" and "ALLOW_UNTRUSTED_KEXTS", "ALLOW_UNRESTRICTED_FS", "ALLOW_UNAPPROVED_KEXTS" AND "ALLOW_UNAUTHENTICHATED_ROOT").
    
   - Back to main menu and click "Post-Install Root Patch". Install the Root Patch provided to your EFI partition (it will be merged with your "macOS Monterey EFI" that you installed before.
   
   - Plug-out your USB Flash Disk then reboot your PC to make some changes.
  
   - When you get back, update your Post-Install Root Patch from OCLP app once again. Then try to update what macOS Monterey offer.
     
   - Reach the last update of macOS Monterey and then make a backup.
     
3. macOS Monterey
   - The macOS Monterey EFI that has been patched in previous stage  Reach the last update of macOS Monterey and then make a backup.
