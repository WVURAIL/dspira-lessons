---
layout: post
date:  2021-07-01
title: Installing gr-radio_astro
summary:  Details for installing gr-radio_astro
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Telescope Software Setup']
---

This will install the spectrometer program *spectrometer_w_cal.grc* as well as other useful radio astronomy GNURadio programs.

**NOTE:** The instructions on this page will install gr_radio_astro files for Ubuntu 22.04. If you are using Ubuntu 20.04 LTS, click [here](https://wvurail.org//dspira-lessons/gr_radio_astro_Installation_Ubuntu20) for the installation.

Complete the following steps:

   1. Open a terminal window in Ubuntu.

   2. If you have not already done so in the Install GNURadio step, install the gnuradio external python dependencies and SDR drivers by typing the following and hit enter:
   ```
      sudo apt install gnuradio gr-osmosdr airspy python3-h5py python3-ephem git cmake liborc-0.4-dev -y
   ```
   3. In the terminal type and Enter: `git clone https://github.com/WVURAIL/gr-radio_astro.git`

   4. Switch to the gr-radio_astro directory: `cd gr-radio_astro`

   5. Type and enter: `git branch` to verify that you are on the "main" branch. If you are NOT on the main branch, then type and enter: `git checkout main`.

   6. Make a build directory: `mkdir build`, and then move to it: `cd build`  
      
   7. Then run the following in the build directory:

      ```
      cmake ..
      make
      sudo make install
      ```
 
   8. To check that the installation was successful, type and enter `cd` to get to the home directory. Run the program in Gnuradio:
   * In a terminal window type `gnuradio-companion`
   * Open the *spectrometer_w_cal.grc* program as follows from the File menu:
            
           `File --> Open --> gr-radio_astros --> examples --> DSPIRA --> *spectrometer_w_cal.grc* `
   * Plug an Airspy radio, with the LNA attached, into the USB port. Run the program by hitting the start triangle ("execute the flowgraph") on the menu bar at top. If no errors occur, you are all set!

Occasionally the files in gr_radio_astro may change. Complete the following to update these files.

#### How to Update files from the gr-radio_astro Repository

   1. Open the terminal window.
      
   2. From your home directory (cd ), go to the gr-radio_astro folder: `cd gr-radio_astro`
   
   3. Type `git status`. Check the "On branch ..." statement at the top. You want to be in the "main" branch. To get there, type `git checkout main`.

   4. Type `git pull`. 
      - If a warning message shows up about local changes made that could overwrite files, type `git stash`. 
      - Then type `git pull` again.

   5. Change to the `build` directory: `cd build`

   6. Type `rm -rf *`. **NOTE:** Make sure you are in the `build` directory before typing `rm -rf *`!

   7. Then run the following:
         ```
      cmake ..
      make
      sudo make install
      ```

   8. The update is complete.

   
   **To Run the __spectrometer_w_cal.grc__ program in Gnuradio After Updating:**
   
   1. In a terminal window type `gnuradio-companion`.

   2. Close any previous version of `spectrometer_w_cal.grc` that might be open in Gnuradio.
   
   3. Open the new version of `spectrometer_w_cal.grc` from the folder `/gr-radio_astro/examples/DSPIRA/`
            
      - under `File` select `Open`; 
      - Navigate to the` gr-radio_astro` folder.
      - Under `examples` open `DSPIRA`; then select `spectrometer_w_cal.grc`.

   4. Connect an Airspy SDR to a USB port, and start the program running (Hit the black triangle at the top middle ribbon bar.)
         
   
