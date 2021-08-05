---
layout: post
date:   2020-07-27
title: Spectrometer Source Block Settings 
summary:  Settings in spectrometer for different SDR's
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Telescope Hardware Setup'] 
---


The default source block settings in the `spectrometer_w_cal.grc` GNURadio program are for the [Airspy R2](https://airspy.com/airspy-r2) SDR. If a different SDR is used, changes in the source block and the `samp_rate Variable` block may be needed. The settings for some common SDR's used with the horn telescopes are described below.

Options:

+ The [Airspy Mini](https://airspy.com/airspy-r2)

    - Source block: the `osmocom Source` block is used; the "Device Arguments" are the same as for the Airspy R2. So no changes are needed in this block.

    - `samp_rate Variable` block: This block is in the upper left corner of the canvas in the `spectrometer_w_cal.grc` program next to the `Options` block. Open this block by double-clicking it. Change the "Value" to "6e6" (which is 6 MHz).


+ RTL-SDR

    - Source block: change the "Device Arguments" 

    - `samp_rate Variable` block: This block is on the left side of the canvas in the `spectrometer_w_cal.grc` program. Open this block by double-clicking it. Change the "Device Argument" to: rtl=0, bias=1, pack=0

    - `samp_rate Variable` block: This block is in the upper left corner of the canvas in the `spectrometer_w_cal.grc` program next to the `Options` block. Open this block by double-clicking it. Change the "Value" to "2.4e6" (which is 2.4 MHz).

+ Lime 

    - Source block: the Lime uses the `LimeSDR Source (RX)` block. Click on the `osmocom` block and hit Delete. Then in the search window on the tool bar at the top, type "LimeSDR". Grab the `LimeSDR Source (RX)` and drag it onto the canvas where the `osmocom` block was. Connect the blue output of the `LimeSDR Source (RX)` block to the `Stream to Vector` block, the three `Delay` blocks, and the `Complex to Real` one-by-one.
    
    - Open the `LimeSDR Source (RX)` block (by double-clicking) and set the following:
        - On the "General" tab, set "RF frequency" to "freq" [without the quotes], and check that the "Sample rate" is "samp_rate" [without the quotes]. "Channel" should be on "A" [without the quotes].

        - The settings on the Channel A tab should be as shown:
        <img src="/dspira-lessons/images/Lime_channelA.png" align="center" width="500px"/>
        
    - `samp_rate Variable` block: The Lime SDR can use a 10 MHz samp_rate; so no change is needed in this block.

    - POWER TO THE LNA: The Lime SDR does not power the LNA. Therefore, it is necessary that external power is provided to the LNA. This is done through a [bias-T](https://www.minicircuits.com/WebStore/dashboard.html?model=ZFBT-282-1.5A%2B), which is connected to the LNA and Lime as shown:
        
        <img align="center" width="329" height="199" src="/dspira-lessons/images/Bias_T_connections.png">

        An [SMA female to female connector/adapter](https://www.data-alliance.net/sma-female-to-sma-female-adapter-coupler-gender-changer/) will be needed for the connection from the bias-T to the LNA cable, as indicated in the diagram above.

+ ADALM-PLUTO - will need to make a minor change in the source block in the Gnuradio program.

For details on the changes needed in the source block mentioned above, refer to the [spectrometer page here](https://wvurail.org//dspira-lessons/tba??).

Needed for connecting:

+ A [coaxial cable](https://www.coaxrf.com/shop/1-rf-coaxial-cables/times-microwave-lmr240/sma-male-times-microwave-lmr240/lmr240-sma-male-to-sma-male-coaxial-rf-pigtail-cable/) is needed to connect the LNA to the SDR. Typically a 10 ft length is adequate, but any length up to 25 ft should work fine.