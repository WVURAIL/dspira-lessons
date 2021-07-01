---
layout: post
date:  2021-07-01
title: Installing gr-radio_astro
summary:  Details for installing gr-radio_astro
tags: ['School-Teachers', 'Students', 'Hobbyists' ]
categories: ['Telescope Software Setup']
---

*    This will install the spectrometer program *spectrometer_w_cal.grc*.

Complete the following steps:

   1. Open a terminal window in Ubuntu.

   2. Install gnuradio external python dependencies and SDR drivers by typing the following:
      `sudo apt install gnuradio gr-osmosdr airspy python3-h5py python3-ephem`, and hit Enter.

   3. Also install the following package: `sudo apt install git cmake liborc-0.4-dev`
         
   4. To clone the repository: in the terminal, type and Enter: `git clone https://github.com/WVURAIL/gr-radio_astro.git`

   5. Switch to the gr-radio_astro directory: `cd gr-radio_astro`

   6. Switch to the gr-radio_astro 3.8 branch by typing: `git checkout gr38`

   7. Make a build directory: `mkdir build`, and then move to it: `cd build`  
      
   8. Then run the following in the build directory:

      ```
      cmake ..
      sudo make
      sudo make install
      ```
**Additional Steps for setting the proper Python environment:**

   9. Open a terminal window.
   
   10. Make sure you are at the home directory (type and Enter `cd` ). Then type `gedit .bashrc` to open the *.bashrc* file in an editor.
   
   11. Scroll to the very bottom of this file, add a blank line, and then copy and paste the following code: `export PYTHONPATH=/usr/local/lib/python3/dist-packages:/usr/local/lib/python3.8/dist-packages:$PYTHONPATH`

   12. Save and close (x in upper right corner).
   
   13. Go to the following by typing: `cd /usr/local/lib/python3.8/dist-packages`
   
   14. Enter `ls`
   
   15. If the folder `radio_astro` exists, delete it by typing: `sudo rm -rf radio_astro` . If nothing shows up after typing `ls`, then everything is fine.
 
**Check that the Installation was Successful**
 
   16. Run the program in Gnuradio:
         - In a terminal window type `gnuradio-companion`
         - Open the *spectrometer_w_cal.grc* program as follows: 
            
           `File --> Open --> gr-radio_astros --> examples --> *spectrometer_w_cal.grc* `
         - Plug an Airspy radio, with the LNA attached, into the USB port. Run the program by hitting the start triangle ("execute the flowgraph") on the menu bar at top. If no errors occur, you are all set!  
   
#### How to Update files from the gr-radio_astro gr38 Repository

   1. Switch to the *gr-radio_astro* folder on your computer: `cd gr-radio_astro`
      
   2. To check to see if you are in the gr38 branch, enter `git status`. The descriptor "On branch gr38" should appear at the top of the displayed text.
   
      To switch to the gr38 branch, type `git checkout gr38`. Then type `git status` to check. 

   3. Type `git pull`. This should update your gr-radio_astro files on your computer.

   4. Run the *spectrometer_w_cal.grc* program in Gnuradio:
      - In a terminal window type `gnuradio-companion`
      - Close any pre-existing *spectrometer_w_cal.grc* program that may already be loaded in the Gnuradio program.
      - Open the new *spectrometer_w_cal.grc* program that is in the updated gr-radio_astro folder: 
            
         `File --> Open --> gr-radio_astros --> examples --> spectrometer_w_cal.grc`
         
      - Make sure an Airspy radio is plugged into a USB port. Execute the program to check that it is updated successfully.

