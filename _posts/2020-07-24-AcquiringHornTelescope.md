---
layout: post
date:  2020-07-24
title: Building a Horn Telescope
summary:  Overview of what's needed to build a horn telescope
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Horn Construction']
---
Two different options for building a working system to operate a horn radio telescope are presented below. Links to documentation and instructional videos are provided where applicable.

### How to Assemble a complete system

   - the horn & antenna can assembly – details provided [here](https://drive.google.com/file/d/1_IDQfJlaPI43cPWumYKiKivhqwiIh7C3/view?usp=sharing)

      * the horn
      
      * the antenna can
      
      * the antenna probe
      
      * the antenna feedthrough
      
      * the horn stand

   - a low noise amplifier (LNA)
   
       All of these will work. The DSPIRA LNA is the most stable and long lasting.

      * Best option: the DSPIRA LNA – see information and instructions [link]
      
      * Next best option: [Nooelec SAWbird+ H1](https://www.nooelec.com/store/sdr/sdr-addons/sawbird-h1.html) - Premium SAW Filter & Cascaded Ultra-Low Noise Amplifier (LNA) Module for Hydrogen Line (21cm) Applications
      
      * Next best option: [Radio Astronomy Hydrogen Line Low Noise Amplifier](https://www.tindie.com/products/gpio/radio-astronomy-hydrogen-line-low-noise-amplifier/) 

   - an Airspy Software Defined Radio: [Airspy R2](https://airspy.com/airspy-r2)
   
   - coaxial cable with SMA connectors: from coaxrf.com, [LMR195 SMA MALE to SMA MALE Coaxial RF Pigtail Cable](https://www.coaxrf.com/shop/1-rf-coaxial-cables/times-microwave-lmr195/sma-male-times-microwave-lmr195/lmr195-sma-male-to-sma-male-coaxial-rf-pigtail-cable-2/)
   
   - computer & software needs
   
      * computer with a Linux (Ubuntu) operating system
         + install Gnuradio 3.8
         + install the program spectrometer_w_cal.grc from the Github repository gr-radio_astro

      * computer with Windows operating system - the Gnuradio and spectrometer_w_cal.grc program can be run from a bootable flash drive
   
      * computer with Mac operating system - the Gnuradio and spectrometer_w_cal.grc program can be run from a bootable flash drive
      
