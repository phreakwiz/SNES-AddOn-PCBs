##################################################################################  
# SNES_RGBAmp: for all 3Chip boards                                              #  
# SNES_RGBAmp_wCSYNC: possible on 3Chip boards (but not tested / described here) #  
##################################################################################  
  
  
INTSTALLATION MAY DIFFER FROM MAINBOARD VERSION TO MAINBOARD VERSION!  
  
The presented installation methods here are either  
- reported: I haven't done the modification by myself but it is reported to work in that way, or  
- checked: I have done the modification by myself and have measured the output with an oscilloscope.  
If I have a reference url, I will give it.  
  
-----------------------------------------------------------------------------------  
  
### Jumper J1 - Low Pass Filter of the THS7373 / THS7374 ###  

Both ICs are supported. The THS7373 has one SD-video low pass filter (used for /CSYNC) and three HD-video filters (used for R, G and B). The THS7374 has four SD-video filters.  
At the THS7373 the HD-video LPFs can be bypassed and at the THS7374 all four SD-video filters can be bypassed (using J1).  
  
The Jumper 1 is for bypassing the internal low pass filters.  
- leave J1 open: internal filters are NOT bypassed  
- close J1: internal filters are bypassed (not effective for the SD-video channel of the THS7373)   
  
It is not possible to set the three HD-video (THS7373) or four SD-video (THS7374) low pass filters independently!  
  
Note: This jumper has no effect if you use a THS7316 or THS7314!  
  
-----------------------------------------------------------------------------------  
  
### SNSP-CPU-01/02 (checked) ###  
  
additional components needed for the SNES mainboard:
  - 3x 750Ohm resistor 0805 package (0.125W, 1% tolerance should be fine)  
  - 3x 1.87kOhm resistor 0805 package (0.125W, 1% tolerance should be fine)   
 
how to install:  
  - remove R8, R9, R13, R14, R18, R19 and Q4, Q6, Q8 from the SNES mainboard  
  - solder the three 1.87kOhm resistors to R8, R13 and R18  
  - solder the three 750Ohm resistors to R9, R14 and R19  
  - solder the directly beneath the MultiAV  
  - connect pad 'R' with the pad where the base of Q4 was  
  - connect pad 'G' with the pad where the base of Q6 was  
  - connect pad 'B' with the pad where the base of Q8 was  
  
reference url: (German)  
https://circuit-board.de/forum/index.php/Thread/20199-SNES-RGB-Bypass-für-PAL-3-Chip-SNES-SNSP-CPU-01-02/  
  
-----------------------------------------------------------------------------------  
  
### SHVC-CPU-01 (reported) ###  
  
additional components needed for the SNES mainboard:
  - 3x 750Ohm resistor 0805 package (0.125W, 1% tolerance should be fine)  
  - 3x 1.87kOhm resistor 0805 package (0.125W, 1% tolerance should be fine)   
  
how to install:  
  - cut traces for R', G' and B' right before the MultiAV (but behind C44, C46 and C47)  
  - solder the three 1.87kOhm resistors to R8, R13 and R18  
  - solder the three 750Ohm resistors to R9, R14 and R19  
  - solder modding board to the MultiAV  
  - connect pad 'R' with the point (R8,R9)  
  - connect pad 'G' with the point (R13,R14)  
  - connect pad 'B' with the point (R18,R19)  
  
reference url: (English)  
http://assemblergames.com/l/threads/attempted-to-rgb-bypass-shvc-cpu-01-super-famicom-picture-too-bright.63581/  
  
-----------------------------------------------------------------------------------  

### SNS-CPU-GBM-01/02 (---) ###

It likely the same procedure as for the SHVC-CPU-01. Yet, I haven't tested it and it was never reported! Please keep that in mind if you decide to install the bypass board into your SNES and please report the result to me.
  
-----------------------------------------------------------------------------------  
  
### SNS-CPU-RGB-01/02 (---) ###  
  
The installation on these mainboards should be similar to the one presented for the SNS-CPU-APU-01; but it was never reported so far.  
If you do the modification (on your own risk), please report the result to me.  
  
-----------------------------------------------------------------------------------  
  
### SNS-CPU-APU-01 (checked) ###  
  
how to install:  
  - remove R56, R57 and R58 from the SNES mainboard  
  - solder modding board to the MultiAV  
  - connect pad 'R' with the point (R6,R7,C6)  
  - connect pad 'G' with the point (R8,R9,C7)  
  - connect pad 'B' with the point (R10,R11,C8) 

reference url: (German)  
https://circuit-board.de/forum/index.php/Thread/20199-SNES-RGB-Bypass-f%C3%BCr-PAL-3-Chip-SNES-SNSP-CPU-01-02/?postID=537811#post537811  