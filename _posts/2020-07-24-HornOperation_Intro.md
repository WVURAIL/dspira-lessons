---
layout: post
date:   2020-07-24
title: What a Horn Telescope Can Measure
summary:  An overview of what is detected by a horn telescope
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Horn Operation'] 
---

## The Horn Telescope: An Overview

A horn telescope is simply an antenna designed to pick up radio waves. The horn used in DSPIRA is specifically designed to pick up radio waves emitted by neutral hydrogen atoms in the Milky Way Galaxy, which have a frequency of approximately 1420 MHz. 
Because it is an antenna, a horn telescope will pick up all radio waves that are incident on it, regardless of their origin. As a result, the signal that is displayed on the spectrometer output includes signals from outer space as well as those from the local environment here on earth. Some of these signals are inherent in the data processing system. 

Because we are primarily interested in signals that are coming from astronomical objects, such as the galaxy, we need to subtract out any any other signals that the telescope might be picking up. The spectrum_w_cal.grc Gnuradio program enables the user to do just that so that we can view spectra of signals that are only from the astronomical object of interest.

## What a Horn Telescope is Measuring

The graph below shows a typical spectrum of radio waves from neutral hydrogen detected using the DSPIRA spectrometer program with a horn.

![sample spectrum](/dspira-lessons/images/Sample_spectrum.png)


