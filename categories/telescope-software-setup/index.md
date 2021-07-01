---
layout: catpag
category: Telescope Software Setup
---

**Overview Software Needed For the Horn Telescope** 

* The horn telescope uses software defined radio (SDR) for collecting and processing the radio signals collected.

* An SDR dongle is needed for this system. See the [SDR Options page.](https://wvurail.org//dspira-lessons/SDR)

* The "back end" of the telescope is a spectrometer program that runs on the free, open-source software *GNURadio*. Options for acquiring this program are provided below.

* The spectrometer program built and developed by DSPIRA is called *spectrometer_w_cal.grc*. Instructions for installing this program are also provided here. 

* Another option is to build a simple spectrometer program in *GNURadio*. Instructions for doing this are provided here too. Lessons on how to use GNURadio are provided. This is followed by basic lessons in digital signal processing (DSP) that introduce the processes used in the spectrometer. Then the steps on how to build a simple Spectrometer in *GNURadio* are provided.  


**Acquire Necessary Software:**

* [Installation on a Bootable Flashdrive](https://wvurail.org//dspira-lessons/Install_Ubuntu_spectrometer_onFlashdrive) - All of the software needs to operate the telescope are loaded onto a bootable flashdrive, including the operating system Ubuntu, *GNURadio* and the *spectrometer_w_cal.grc* program.

* [Installation of Ubuntu and SDR software on a computer](https://wvurail.org//dspira-lessons/BuildingHorn_SoftwareInfo) - Includes steps for installing the linux Ubuntu OS on a computer, loading *GNURadio*, and installing the *spectrometer_w_cal.grc* program.  

**Build a Simple Spectrometer in *GNURadio*:**

* [**Simple Spectrometer**](https://wvurail.org//dspira-lessons/???) - Includes an introduction to *GNURadio*, some lessons in DSP, and steps on how to build a simple spectrometer in *GNURadio*.