---
layout: post
date:   2020-07-26
title: How to Calibrate the Spectrometer
summary:  The procedure for calibrating the telescope using the spectrometer_w_cal program is outlined.
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Horn Operation'] 
---

[How to Calibrate the Spectrometer video](){: .button}

[![How to Calibrate Spectrometer video](/dspira-lessons/images/CHIME_dishes.jpg | width=100)](https://www.youtube.com/watch?v=dWX0rRU99Z8)

#### Some preliminary pointers: 

   * For the best results, after starting the program, allow the system to warm up for approximately 20 minutes before calibrating.

   * Re-calibrations can be done any time during a viewing session. 

   * For consistency, it is recommended to re-calibrate occasionally during a viewing session.

#### Procedure 

   1. Point the telescope toward the ground at an angle. The video shows how this is done.

   2. Switch the `Spectrum Display` to `Hot Calibration`.

   3. Select the `Time Integration` to `Long Integration`.

   4. Watch the spectrum displayed. You may need to change the `ymax` value to view all of the signal on the graph. Wait for the graph to settle to a steady display. Then switch the `Spectrum Display` to `Cold Calibration`. DO NOT MOVE THE TELESCOPE UNTIL THE SPECTRUM DISPLAYED HAS BEEN CHANGED TO `Cold calibration`.

   5. Switch the display to `Cold Calibration` and the integration to `Short Integration`.

   6. Point the telescope at open sky. Continue to re-direct it until you find a patch of sky that does not show any hydrogen peak near 1420.4 MHz. After doing so, switch to `Long Integration`.

   7. Wait for the graph to settle to a steady display. Then switch the `Spectrum Display` to `Spectrum with Calibration`.  DO NOT MOVE THE TELESCOPE UNTIL THE SPECTRUM DISPLAYED HAS BEE CHANGED TO `Spectrum with calibration`.

   8. The spectrometer is now calibrated, and the graph should now be showing only signals from the galaxy.

#### Some More Things to Note: 

   * After completing a calibration, the signal is in units of Kelvin (K). This sounds odd, but it is how radio astronomers quantify radio signals. 

   * For most amateur applications, it is not necessary to get bogged down trying to understand why the units are Kelvin.

   * After completing a calibration, the baseline signal would theoretically be steady at approximately 10 K, which is the approximate temperature of empty space. However, in reality, the base level after calibration will fluctuate. This is due to several factors, but it is mostly due to the LNA because its temperature will fluctuate some over the span of a viewing session.

   * The background level can actually go negative! No need to worry. Re-calibrating usually takes care of this and brings the base level back up to approximately 20 K.
 
   * The value of the background level will not affect any peak positions or shapes.

   * Even though the background level might not stay the same, the calibrated spectrum can still be used for quantitative analysis by offsetting the data so that the background level is zero. This is typically what is done when analyzing the area of the peaks.
    
