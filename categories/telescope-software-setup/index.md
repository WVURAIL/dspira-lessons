---
layout: catpag
category: Telescope Software Setup
---

**Overview Software Needed For the Horn Telescope** 

* The horn telescope uses software defined radio (SDR) for collecting and processing the radio signals collected.

* An SDR device (dongle) is needed for this system. See the [SDR Options page.](https://wvurail.org//dspira-lessons/SDR)

* Data from SDR is fed into a computer and processed in a *spectrometer* program at the "back end" of the telescope.

* The spectrometer program called *spectrometer_w_cal.grc* runs on the free, open-source software *GNURadio* on the *Ubuntu* operating system. Information for acquiring *Ubuntu*, *GNURadio*, and *spectrometer_w_cal.grc* are provided in the *Installation of Ubuntu and SDR software on a Windows-based computer* instructions below.

* Instructions on how to use the *spectrometer_w_cal.grc* program can be found [here](https://wvurail.org//dspira-lessons/spectrometer_w_cal_Instructions){:target="_blank"}. 

* Another option is to build a simple spectrometer program in *GNURadio*. Instructions for doing this are provided below under *Build a Simple Spectrometer in GNURadio*. These instructions include lessons on how to use *GNURadio* followed by basic lessons in digital signal processing (DSP) that introduce the processes used in the spectrometer. Then steps on how to build a simple spectrometer in *GNURadio* are provided.  

**Warning-Novice Computer Users - Does *UBUNTU* or *Command Line Interface* sound new to you?**
You may wish to read the following intro to the UBUNTU environment. [**What is UBUNTU?**](https://docs.google.com/document/d/14U9ANGS9YM3PnQY-n2ykO4uKVwVDf8NeHfauRmGDmw0/edit?usp=sharing) before you start downloading and setting up software.

**Acquire Necessary Software:**

* [**Installation on a Bootable Flashdrive**](https://wvurail.org//dspira-lessons/Install_Ubuntu_spectrometer_onFlashdrive) - This is the DSPIRA-preferred method to have all the needed softwware for operating the horn telescope.  By having simple 32G flashdrives that can be put in any Windows based computer, the user doesn't need to have dedicated PCs to run the software. All of the software needed to operate the telescope are loaded onto a bootable flashdrive, including the operating system Ubuntu, *GNURadio* and the *spectrometer_w_cal.grc* program.

* [**Installation of Ubuntu and SDR software on a Windows-based computer**](https://wvurail.org//dspira-lessons/BuildingHorn_SoftwareInfo) - Includes steps for installing the linux Ubuntu OS on a computer, loading *GNURadio*, and installing the *spectrometer_w_cal.grc* program.  APPLE COMPUTERS - DSPIRA has had no success with running GNURadio on Apple computers, so we have no support material here for Apple products. 

**Build a Simple Spectrometer in *GNURadio*:**

* [**Simple Spectrometer**](https://wvurail.org//dspira-lessons/Simple_Spectrometer) - Includes an introduction to *GNURadio* with some basic lessons in DSP, and steps on how to build a simple spectrometer in *GNURadio*.
