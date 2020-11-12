---
layout: catpag
category: Horn Construction
---

### OVERVIEW

A horn telescope consists of 3 major parts: the **antenna**, the **support stand**, and the **back-end electronics**, as illustrated in the picture below. 

{picture to come}

The radio signals that reach the antenna on the horn surface are guided into the can and picked up by the wire probe. These signals are then immediately amplified by the **low noise amplifier (LNA)**. 

From there the amplified signal is passed into the software defined radio (SDR), which digitizes the signal to be fed into the computer. These signals are input to the GnuRadio **spectrometer program** which processes the signals and outputs a graph showing the signal strength vs. radio frequency. 

These horn telescopes are designed specifically to detect the 1420.4 MHz radio signal that is emitted by cold hydrogen atoms that permeate the Milky Way Galaxy. These spectra contain information that enables us to determine the relative amounts of hydrogen atoms in the galaxy and their relative motions.

A complete horn telescope system can be built for a few hundred dollars, the actual cost depending on the options you choose and whether or not you have a computer. No building experience is needed, as we have tried to provide enough details for anyone to build the telescope. The tools needed include a drill, an electric screwdriver (or screwdriver drill bit), a saw, and a soldering iron.

The parts needed are listed under each section described below.

### The Antenna

The antenna consists of the horn panels, a metal can, the wire probe, and a low noise amplifier.

The horn panels and metal can are assembled as a single unit. For detailed instructions on assembling the horn panels, metal can, and stand, click [here.](https://drive.google.com/file/d/1qdc5lhKErFyIsc8b52ZIkCPJLi-XykSb/view?usp=sharing) More complete details on assembling the metal can apparatus are found [here.](http://wvurail.org/dspira-lessons/AssemblingtheCAN)

A low noise amplifier (LNA) connects to the antenna probe through a standard SMA connector that is part of the can assembly. (See diagram above??) The DSPIRA LNA is designed for a 1420 MHz radio telescope by Professor Kevin Bandura at WVU. The total cost to build this LNA circuit is approximately $60. Details on ordering the parts and instructions on how to solder the circuit are provided [here.](http://wvurail.org/dspira-lessons/DetailedLNAInstructions) 
	
If you prefer not to solder together a circuit, other options for obtaining a low noise amplifier include the following. All of these will work with the dSPIRA horn telescope and software.
+[Nooelec SAWbird+ H1](https://www.nooelec.com/store/sdr/sdr-addons/sawbird-h1.html) - Premium SAW Filter & Cascaded Ultra-Low Noise Amplifier (LNA) Module for Hydrogen Line (21cm) Applications; $44.95.

+ [Radio Astronomy Hydrogen Line Low Noise Amplifier](https://www.tindie.com/products/gpio/radio-astronomy-hydrogen-line-low-noise-amplifier/); $49.50.

### The Support Stand

The support stand described here is intended to be simple and affordable to anyone. It can be constructed out of standard lumber that can be found at any home improvement store.

The support stand consists of a cradle that holds the horn/can assembly and a base to support the cradle. The cost of the parts is under $50. Details on how to construct the stand shown in the picture above are provided in the document [here.](https://drive.google.com/file/d/1qdc5lhKErFyIsc8b52ZIkCPJLi-XykSb/view?usp=sharing)

### The Back-end Electronics and Spectrometer

The radio signals detected by the horn telescope are digitized by a **software defined radio (SDR)** and then processed by digital signaling processing software. The SDR comes with a cable that connects to a USB port on the computer.

+ The SDR we prefer is the [Airspy R2](https://airspy.com/airspy-r2), $169. This operates in a 10 MHz bandwidth and is the SDR that the DSPIRA software is coded for.

+ A less expensive option is the [Airspy Mini](https://airspy.com/airspy-r2), $99. It operates in a 6 MHz bandwidth. Only a minor adjustment to the software is needed if this SDR is used. Contact us for more information about the changes that would need to be done.

+ A coaxial cable [link??] is needed to connect the LNA to the SDR. Refer to the diagram above.

The spectrometer program on the computer is run in GnuRadio, which is a free and open source software program. Information about setting up the computer with the necessary software can be found [here.](http://wvurail.org/dspira-lessons/HornOperation_computerSystems)
