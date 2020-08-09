---
layout: post
date:  2020-07-28
title: Software Needs for Runing the Horn Telescope
summary:  Details of software installation needed for a horn telescope
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Horn Construction']
---

## Installing the Software Needed to Run the Spectrometer on a Computer That is Using Ubuntu 20.04

Complete the following steps as needed:

#### A. How to Partition a Hard Drive for Ubuntu 20.04 Alongside Windows 10

   1. [Download Ubuntu Desktop 20.04 ISO onto hard drive in Windows.](http://releases.ubuntu.com/20.04/)

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
      
   After the shrink process completes, a new unallocated space will be present in your drive. We’ll use this free space to install Ubuntu alongside Windows

#### B. Install Ubuntu 20.04 Alongside with Windows

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


#### C. Install Gnuradio 

   1. Open a terminal window.

   2. Type and enter `sudo apt update`
   
   3. Type and enter `sudo apt upgrade`
      
   2. Type `sudo apt install gnuradio`

   3. You may need to respond 'Y' to a few prompts before installation is complete.

#### D. Install gr-radio_astro 

   This will install the spectrometer program *spectrometer_w_cal.grc*.

   1. Open a terminal window in Ubuntu.

   2. Install gnuradio external python dependencies and SDR drivers by typing the following:
      `sudo apt install gnuradio gr-osmosdr airspy python3-h5py python3-ephem`, and hit Enter.

   3. Also install the following package: `sudo apt install git cmake liborc-0.4-dev`
         
   4. To clone the repository: in the terminal, type and Enter: `git clone https://github.com/WVURAIL/gr-radio_astro.git`

   5. Switch to the gr-radio_astro directory: `cd gr-radio_astro`

   6. Switch to the gr-radio_astro 3.8 branch by typing: `git checkout gr38`

   7. Make a build directory: `mkdir build`, and then move to it: `cd build`  
      
   8. Then run the following in the build directory:

      ```
      cmake ..
      sudo make
      sudo make install
      ```
**Additional Steps for setting the proper Python environment:**

   9. Open a terminal window.
   
   10. Make sure you are at the home directory (type and Enter `cd` ). Then type `gedit .bashrc` to open the *.bashrc* file in an editor.
   
   11. Scroll to the very bottom of this file, add a blank line, and then copy and paste the following code: `export PYTHONPATH=/usr/local/lib/python3/dist-packages:/usr/local/lib/python3.8/dist-packages:$PYTHONPATH`

   12. Save and close (x in upper right corner).
   
   13. Go to the following by typing: `cd /usr/local/lib/python3.8/dist-packages`
   
   14. Enter `ls`
   
   15. If the folder `radio_astro` exists, delete it by typing: `sudo rm -rf radio_astro` . If nothing shows up after typing `ls`, then everything is fine.
 
**Check that the Installation was Successful**
 
   16. Run the program in Gnuradio:
         - In a terminal window type `gnuradio-companion`
         - Open the *spectrometer_w_cal.grc* program as follows: 
            
           `File --> Open --> gr-radio_astros --> examples --> *spectrometer_w_cal.grc* `
         - Plug an Airspy radio, with the LNA attached, into the USB port. Run the program by hitting the start triangle ("execute the flowgraph") on the menu bar at top. If no errors occur, you are all set!

#### E. How to Update files from the gr-radio_astro gr38 Repository

   1. Switch to the *gr-radio_astro* folder on your computer: `cd gr-radio_astro`
      
   2. To check to see if you are in the gr38 branch, enter `git status`. The descriptor "On branch gr38" should appear at the top of the displayed text.
   
      To switch to the gr38 branch, type `git checkout gr38`. Then type `git status` to check. 

   3. Type `git pull`. This should update your gr-radio_astro files on your computer.

   4. Run the *spectrometer_w_cal.grc* program in Gnuradio:
      - In a terminal window type `gnuradio-companion`
      - Close any pre-existing *spectrometer_w_cal.grc* program that may already be loaded in the Gnuradio program.
      - Open the new *spectrometer_w_cal.grc* program that is in the updated gr-radio_astro folder: 
            
         `File --> Open --> gr-radio_astros --> examples --> spectrometer_w_cal.grc`
         
      - Make sure an Airspy radio is plugged into a USB port. Execute the program to check that it is updated successfully.

