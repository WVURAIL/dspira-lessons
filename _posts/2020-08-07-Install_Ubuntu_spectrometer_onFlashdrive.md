---
layout: post
date:   2020-08-07
title: Installing Ubuntu 22.04 with spectrometer_w_cal.grc on Bootable Flashdrive
summary:  Instructions for copying the Ubuntu/spectrometer_w_cal image on a bootable flashdrive
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Telescope Software Setup'] 
---

#### Image the Flashdrive:

1. Before starting, you will need the program *balenaEtcher*, which is an easy-to-use cross-platform tool for burning images to SD cards, USB drives and other removable devices. It can be downloaded from <https://www.balena.io/etcher/>.

2. Download the file [ubuntu_radio_astro08_2022_2.zip](https://drive.google.com/file/d/1qAk6Z-XyFaoyRFH1mHWrmuKy9UBirV1s/view?usp=sharing) while in either Windows or Ubuntu.

3. Unzip this file in a folder of your choice.

4. Install a 32 GB or larger flash drive in the usb port. [We recommend a Samsung 32 GB flash drive.]

5. Run *balenaEtcher*. Choose the file *ubuntu_radio_astro08_2022_2.img* as the image and the flash drive as the target.


6. The *Ubuntu with spectrometer_w_cal.grc* image should now be on this bootable flashdrive.

#### How to Run Gnuradio and the spectrometer_w_cal.grc program from the flashdrive. 

1. To run Gnuradio and the *spectrometer_w_cal.grc* program, place the bootable flash drive in a USB port. 

2. Start or reboot the computer. While it is starting, hold down the bootable key (F12) to pull up a menu of boot options.

3. Scroll down to the flashdrive and hit enter.

4. On the first installation screen, choose **run Ubuntu persistent live** (the choice at the top). IT MAY TAKE A FEW MINUTES FOR THE SYSTEM TO BOOT UP, DEPENDING ON THE FLASHDRIVE USED. BE PATIENT!

5. Open a Terminal by selecting the terminal icon on the left menu bar. 

6. Type and enter `gnuradio-companion` at the prompt. 

7. The *spectrometer_w_cal.grc* program should open. 

8. Before you hit the Play button at the top of the program window, you will need to adjust the gains for the AIRSpy in the OSMOCOM block. The nominal gain values for the AIRSpy are 17 12 10. 

9. NOTE: When the save/write to file buttons are hit, the data files are written to the Spectra folder. Before you run GNURadio, you will need to create the Spectra folder. Click on the Files icon on the left side of the screen. Create the Spectra folder at this level.

10. NOTE: The system clock time defaults to UTC/London. Change it if needed.

11. Enjoy radio astronomy observations!
