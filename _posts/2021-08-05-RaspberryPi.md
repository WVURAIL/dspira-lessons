---
layout: post
date:  2021-07-01
title: Raspberry Pi
summary:  Details for setting up Raspberry Pi for Radio Astronomy
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Telescope Software Setup']
---

Raspberry Pi's are inexpensive and the more modern Pi's are powerful enough to keep up with the level of signal processing on GNURadio associated with Radio Astronomy applications. 

- [Supported Raspberry Pi Devices](#supported-raspberry-pi-devices)
- [Operating system requirement](#operating-system-requirement)
- [Installing Ubuntu on Raspberry Pi](#installing-ubuntu-on-raspberry-pi)
  - [Prerequisites](#prerequisites)
- [Post Installation actions:](#post-installation-actions)
  - [Interacting with the Raspberry Pi](#interacting-with-the-raspberry-pi)
- [Installing `gr-radio_astro`: Installing gr-radio_astro{:target="_blank"}](#installing-gr-radio_astro-installing-gr-radio_astro-sitebaseurl-gr_radio_astro_installationtarget_blank)
- [Installing Ubuntu image with radio astronomy preinstalled  on a Raspberry Pi](#installing-ubuntu-image-with-radio-astronomy-preinstalled--on-a-raspberry-pi)


## Supported Raspberry Pi Devices

1. Raspberry Pi 4 Model B
2. Raspberry Pi 400

## Operating system requirement

1. Ubuntu for Raspberry Pi [Click here for more Info](https://ubuntu.com/raspberry-pi)

_Note_: The custom `gr-radio_astro` [software]({{ site.baseurl }}/gr_radio_astro_Installation)  is now only supported for `GNURadio 3.8` only. The Raspberry Pi OS by default installs `GNURadio 3.7` which is not longer supported. 

## Installing Ubuntu on Raspberry Pi

### Prerequisites

1. Support Raspberry Pi
2. A microSD card (9GB minimum, 16GB recommended)
3. A computer with a microSD card drive
4. A micro USB-C power cable

Optionally:    
1. A monitor with an HDMI interface
2. A micro HDMI cable
3. A USB keyboard


[Instructions from Ubuntu to install the OS on the Raspberry Pi 4](https://ubuntu.com/tutorials/how-to-install-ubuntu-on-your-raspberry-pi#1-overview){:target="_blank"}

_NOTE_: Raspberry Pi is built on an ARM based architecture  any version of Ubuntu will not work. The OS has to specific to the Pi. If you do not want to access the full desktop interface of ubuntu and only interact via command line interface you can install Ubuntu Server [instruction for Ubuntu server installation here](https://ubuntu.com/tutorials/how-to-install-ubuntu-on-your-raspberry-pi#1-overview){:target="_blank"}

## Post Installation actions: 

### Interacting with the Raspberry Pi

1. Using a moniter and mouse and keyboard like any other desktop. 
2. Using SSH:
   1. This method can be used on any machine with ssh server enabled.
   2. Install X server on your computer. [VcXcrv]{https://sourceforge.net/projects/vcxsrv/}{:target="_blank"} on windows and [XQuartz](https://www.xquartz.org/){:target="_blank"}for macOS. 
   3. Power up the Raspberry Pi and connect your computer via ethernet cable
   4. First we need to determine the IP address of the raspberry PI. [How to determine Raspberry PI IP address](https://www.raspberrypi.org/documentation/remote-access/ip-address.md){:target="_blank"}
   5. If the determined IP address is `<IP address>` then in the terminal type `ssh -Y pi@<IP address>`
   6. More info on SSH [here](https://www.raspberrypi.org/documentation/remote-access/ssh/){:target="_blank"}
3. Using PuTTy on Windows: 
   1. [DownloadPuTTy](https://www.putty.org){:target="_blank"}.
   2. Add IP address in
4. Using VNC: More info [here](https://www.raspberrypi.org/documentation/remote-access/vnc/README.md){:target="_blank"} 
    
    

## Installing `gr-radio_astro`: [Installing gr-radio_astro]({{ site.baseurl }}/gr_radio_astro_Installation){:target="_blank"} 


## Installing Ubuntu image with radio astronomy preinstalled  on a Raspberry Pi