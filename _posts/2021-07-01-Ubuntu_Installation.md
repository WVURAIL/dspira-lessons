---
layout: post
date:  2021-07-01
title: Installing Ubuntu
summary:  Details for partitioning and installing Ubuntu OS
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Telescope Software Setup']
---

  *Ubuntu versions 20.04 LTS onwards are supported*

Complete the following steps:

A. Partition a Hard Drive and Ubuntu 20.04 Alongside Windows 10

   1. [Download Ubuntu Desktop 20.04 ISO onto hard drive in Windows.](http://releases.ubuntu.com/20.04/) You want to choose the Desktop version. It will take some time to download this file. [Latest versions can be downloaded from](https://ubuntu.com/download/desktop). Our software is tested to work up to 21.04.

   2. Install a 32 GB or larger flash drive in the usb port.
      
   3. Download *BalenaEtcher* for Windows and install it if you don’t already have it.
   
   4. Run *BalenaEtcher*. Choose the Ubuntu20.04.iso file as the image and the flash drive as the target. It will take some time for this to run.

   5. Before installing Ubuntu on the hard disk, you need to partition the hard disk in Windows.
   
      Open a Command Prompt window with admin rights:
         - In the Cortana search field, type in `Command Prompt`, or just CMD.
         - Right click the top result, and select `Run as Administrator`.
         - Click `Yes` on the popup to allow the app to make changes to your device.
         
   6. Enter the command `diskmgmt.msc` to open the Disk Management utility.

   7. Select the Windows partition, usually the C: volume. Right-click on this partition and select the `Shrink Volume` option in order to reduce the partition size.

   8. Wait for the system to collect partition size data; then add the desired amount of space you want to shrink, and hit in the 'Shrink' button. The partition size to shrink by (which is the amount that will be allotted to Ubuntu) should be a minimum of 50 GB, and we recommend 100 GB or more, depending on the size of your hard drive.
      
   After the shrink process completes, a new unallocated space will be present in your drive. We’ll use this free space to install Ubuntu alongside Windows.  
     

B. Install Ubuntu 20.04 Alongside with Windows

   1. Place the bootable flash drive in the USB port, and reboot the machine, holding down the bootable key (F12) in order to boot from the Ubuntu USB bootable image.

   2. On the first installation screen, select `Install Ubuntu` and hit Enter to start the installation process. This will complete the installation process, unless an error message appears.

   3. IF AN ERROR APPEARS REGARDING DEVICE ENCRYPTION, you probably need to disable device encryption in Windows. This is known as Bitlocker. To disable it, complete the following:

      - For most Windows systems, the following can be followed to turn off encryption:
          + Boot up the computer in Windows.
          + Open `Settings`.
          + Click on `Update & Security`.
          + Click on `Device encryption`.
          + Under the "Device encryption" section, click the `Turn off` button.
          + Wait until Windows 10 has completed un-encrypting the hard drive before you turn off Windows 10 and start the disk boot and Ubuntu install.
      
      - For some Windows 10 Home system, the Bitlocker or Device encryption is not visible. Complete the following to turn off encryption from a command line.
      
         +  In Windows from the `Start Menu`, click the `Windows PowerShell` folder and tap `Windows PowerShell`.

         + A command line window will open up. From the Powershell command line, type `Disable-BitLocker -MountPoint C:` and hit Enter.
      
      - Another option for systems with Windows 10 Home is the following:
         + In the `Start Menu` search box, type `Services`. Then scroll to `Bitlocker`. 
         + Open it, or view its `Properties`, and then `Disable` it.

       - After disabling the encryption in Windows, repeat steps 1 and 2 above. Be sure to wait until Windows 10 has completed un-encrypting the hard drive before you turn off Windows 10 and start the disk boot and Ubuntu install.
