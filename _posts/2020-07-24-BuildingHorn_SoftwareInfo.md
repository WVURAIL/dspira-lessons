---
layout: post
date:  2020-07-28
title: Software Needs to Run Horn Telescope
summary:  Details of software installation needed for a horn telescope
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Horn Construction']
---


### If You Want to Use a Computer with the Ubuntu 20.04 Operating System

Complete the following steps as needed:

   * #### How to Partition a Hard Drive for Ubuntu 20.04 Alongside Windows 10 

      1. [Download Ubuntu Desktop 20.04 ISO onto hard drive while in Ubuntu.](http://releases.ubuntu.com/20.04/)

      2. Install a 32 GB or larger flash drive in the usb port.
      
      3. Run *balenaEtcher*. Choose the Ubuntu20.04.iso file as the image and the flash drive as the target.

      4. Before installing Ubuntu on the Windows system, you need to partition the hard disk in Windows. Open a Command Prompt window with admin rights, and execute the command `diskmgmt.msc` to open the Disk Management utility.

      5. Select the Windows partition, usually the C: volume, right-click on this partition and select the **Shrink Volume** option in order to reduce the partition size.

      6. Wait for the system to collect partition size data; then add the desired amount of space you want to shrink, and hit in the **Shrink** button.
      
      7. After the shrink process completes, a new unallocated space will be present in your drive. We’ll use this free space to install Ubuntu alongside Windows 10.


   * #### Install Ubuntu 20.04 Alongside with Windows 

      1. Place the bootable flash drive in the USB port, and reboot the machine, holding down the bootable key (F12) in order to boot from the Ubuntu USB bootable image.

      2. On the first installation screen, select Install Ubuntu and hit Enter to start the installation process.

      This will complete the installation process, unless there is an error message indicating that device encryption (known as Bitlocker) may need to be turned off. If this is the case, complete the following:

      - Refer to the following webpage: [https://www.windowscentral.com/how-enable-device-encryption-windows-10-home](https://www.windowscentral.com/how-enable-device-encryption-windows-10-home)

      - Alternately, boot up in Windows. From the **Start** Menu, click the **Windows Administrative Tools**, then **Windows PowerShell** folder and tap **Windows PowerShell**.
      
        A command line window will open up. From the Powershell command line, type `Disable-BitLocker -MountPoint C:`

        Then reboot with the bootable flash drive in the USB port, and reboot the machine, holding down the bootable key (F12) in order to boot from the Ubuntu USB bootable image.

        On the first installation screen, select Install Ubuntu and hit Enter to start the installation process.


   * #### Install Gnuradio 

      1. Open a terminal window.
      
      2. Type `sudo apt install gnuradio`

   * #### Install gr-radio_astro 

      1. Open a terminal window.

      2. Install gnuradio external python dependencies and SDR drivers:
      `sudo apt install gnuradio gr-osmosdr airspy python3-h5py python3-ephem`

      3. Also install the following package: `sudo apt install git cmake liborc-0.4-dev`
      
      4. Clone the repository: From the terminal, type: `git clone https://github.com/WVURAIL/gr-radio_astro.git`

      5. Switch to the gr-radio_astro directory: `cd gr-radio_astro`

      6. Switch to the GNURadio 3.8 by typing: `git checkout gr38`

      7. Make a build directory: `mkdir build`, and then move to it: `cd build`  
      
      8. Then run the following in the build directory:

        ```
               cmake
               make
               sudo make install
        ```
     

