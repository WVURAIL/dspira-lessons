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

    - Source block: the `osmocom Source` block is used; the Device Arguments are the same as for the Airspy R2. So no changes are needed in this block.

    - `samp_rate Variable` block: This block is in the upper left corner of the canvas in the `spectrometer_w_cal.grc` program next to the `Options` block. Open this block by double-clicking it. Change the "Value" to "6e6" (which is 6 MHz).


+ RTL-SDR - will need to make a minor change in the source block in the Gnuradio program.

+ Lime - will need to make a minor change in the source block in the Gnuradio program.

+ ADALM-PLUTO - will need to make a minor change in the source block in the Gnuradio program.

For details on the changes needed in the source block mentioned above, refer to the [spectrometer page here](https://wvurail.org//dspira-lessons/tba??).

Needed for connecting:

+ A [coaxial cable](https://www.coaxrf.com/shop/1-rf-coaxial-cables/times-microwave-lmr240/sma-male-times-microwave-lmr240/lmr240-sma-male-to-sma-male-coaxial-rf-pigtail-cable/) is needed to connect the LNA to the SDR. Typically a 10 ft length is adequate, but any length up to 25 ft should work fine.