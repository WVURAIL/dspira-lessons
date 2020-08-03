---
layout: post
date:  2020-07-28
title: Software Required For a Horn Telescope
summary:  Details of software installation required for a horn telescope
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Horn Construction']
---

## Running the Spectrometer on a Computer with Ubuntu 20.04

Complete the following steps as needed:

#### A. How to Partition a Hard Drive for Ubuntu 20.04 Alongside Windows 10

   1. [Download Ubuntu Desktop 20.04 ISO onto hard drive in Windows.](http://releases.ubuntu.com/20.04/)

   2. Install a 32 GB or larger flash drive in the usb port.
      
   3. Download *BalenaEtcher* for Windows and install it if you don’t already have it.
   
   4. Run *BalenaEtcher*. Choose the Ubuntu20.04.iso file as the image and the flash drive as the target.

   5. Before installing Ubuntu on the Windows system, you need to partition the hard disk in Windows. 
      Open a Command Prompt window with admin rights:
         - In the Cortana search field, type in `Command Prompt`, or just CMD.
         - Right click the top result, and select `Run as Administrator`.
         - Click `Yes` on the popup to allow the app to make changes to your device.
         
   6. Enter the command `diskmgmt.msc` to open the Disk Management utility.

   7. Select the Windows partition, usually the C: volume, right-click on this partition and select the `Shrink Volume` option in order to reduce the partition size.

   8. Wait for the system to collect partition size data; then add the desired amount of space you want to shrink, and hit in the 'Shrink' button. The partition size to shrink by (which is the amount that will be allotted to Ubuntu) should be a minimum of 50 GB, and we recommend 100 GB or more, depending on the size of your hard drive.
      
   9. After the shrink process completes, a new unallocated space will be present in your drive. We’ll use this free space to install Ubuntu alongside Windows 10.

#### B. Install Ubuntu 20.04 Alongside with Windows

   1. Place the bootable flash drive in the USB port, and reboot the machine, holding down the bootable key (F12) in order to boot from the Ubuntu USB bootable image.

   2. On the first installation screen, select `Install Ubuntu` and hit Enter to start the installation process.

      This will complete the installation process, unless there is an error message indicating that device encryption (known as Bitlocker) may need to be turned off. If this is the case, complete the following:

      - Refer to the following webpage: [https://www.windowscentral.com/how-enable-device-encryption-windows-10-home](https://www.windowscentral.com/how-enable-device-encryption-windows-10-home)
      
      - If you have Windows 10 Home, there is no Bitlocker easily accessible. Instead, turning off encryption can be done from a command line. In Windows from the `Start Menu`, click the `Windows PowerShell` folder and tap `Windows PowerShell`.

      - A command line window will open up. From the Powershell command line, type `Disable-BitLocker -MountPoint C:` and hit Enter.
      
      Another option is to do the following:
         + In the `Start Menu` search box, type `Services`. Then scroll to `Bitlocker`. 
         + Open it or view its `Properties`, and then `Disable` it.

   3. Then reboot with the bootable flash drive in the USB port, and reboot the machine, holding down the bootable key (F12) in order to boot from the Ubuntu USB bootable image.

   4. On the first installation screen, select `Install Ubuntu` and hit Enter to start the installation process.


#### C. Install Gnuradio 

   1. Open a terminal window.
      
   2. Type `sudo apt install gnuradio`

#### D. Install gr-radio_astro 

   1. Open a terminal window.

   2. Install gnuradio external python dependencies and SDR drivers:
      `sudo apt install gnuradio gr-osmosdr airspy python3-h5py python3-ephem`

   3. Also install the following package: `sudo apt install git cmake liborc-0.4-dev`
      
   4. Open a Terminal window.
   
   5. To clone the repository: in the terminal, type: `git clone https://github.com/WVURAIL/gr-radio_astro.git`

   6. Switch to the gr-radio_astro directory: `cd gr-radio_astro`

   7. Switch to the gr-radio_astro 3.8 branch by typing: `git checkout gr38`

   8. Make a build directory: `mkdir build`, and then move to it: `cd build`  
      
   9. Then run the following in the build directory:

      ```
      cmake ..
      sudo make
      sudo make install
      ```
#### E. Additional Steps for setting the proper Python environment:

   10. Open a terminal window.
   
   11. Make sure you are at the home directory (type `cd` ); type `gedit .bashrc` to open the *.bashrc* file in an editor.
   
   12. Scroll to the very bottom of this file, add a blank line, and then copy and paste the following code: `export PYTHONPATH=/usr/local/lib/python3/dist-packages:/usr/local/lib/python3.8/dist-packages:$PYTHONPATH`

   13. Save and close (x in upper right corner).
   
   14. Go to the folder by typing: `cd /usr/local/lib/python3.8/dist-packages`
   
   15. Type `ls`
   
   16. If the folder `radio_astro` exists, delete it by typing: `sudo rm -rf radio_astro` . If nothing shows up after typing `ls`, then everything is fine.
 
#### F. Check that the Installation was Successful
 
   17. Run the program in Gnuradio:
         - In a terminal window type `gnuradio-companion`
         - Open the *spectrometer_w_cal.grc* program as follows: 
            
           `File --> Open --> gr-radio_astros --> examples --> *spectrometer_w_cal.grc* `

#### G. How to Update files from the gr-radio_astro gr38 Repository

   1. Change to the *gr-radio_astro* folder on your computer: `cd gr-radio_astro`

   2. Type `git status`
      
   3. Check to see if you are in the gr38 branch. To change to gr38 branch, type `git checkout gr38`. Type `git status` to check. 

   4. Type `git pull`

   5. Run the program in Gnuradio:
      - In a terminal window type `gnuradio-companion`
      - Close any pre-existing *spectrometer_w_cal.grc* program that would already be loaded in the Gnuradio program.
      - Open the new *spectrometer_w_cal.grc* program that is in the updated gr-radio_astro folder: 
            
         File --> Open --> gr-radio_astros --> examples --> *spectrometer_w_cal.grc*


##  Running the Spectrometer from a Flash Drive

  INSTRUCTIONS TO FOLLOW
