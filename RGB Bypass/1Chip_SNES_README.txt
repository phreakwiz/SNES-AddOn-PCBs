############################################################################  
# SNES_RGBAmp: mainly for 1Chip-01/02 boards                               #  
# SNES_RGBAmp_wCSYNC: mainly for 1Chip-03 boards and for SNES Mini/SFC Jr. #  
############################################################################  
  
  
### Jumper J1 - Low Pass Filter of the THS7373 and THS7374 ###  

Both ICs are supported. The THS7373 has one SD-video low pass filter (used for /CSYNC) and three HD-video filters (used for R, G and B). The THS7374 has four SD-video filters.  
At the THS7373 the HD-video LPFs can be bypassed and at the THS7374 all four SD-video filters can be bypassed (using J1).  
  
The Jumper 1 is for bypassing the internal low pass filters.  
- leave J1 open: internal filters are NOT bypassed  
- close J1: internal filters are bypassed (not effective for the SD-video channel of the THS7373)   
  
It is not possible to set the three HD-video (THS7373) or four SD-video (THS7374) low pass filters independently!  
  
-----------------------------------------------------------------------------------  
  
### Solder Joints: ###  
  
  R - red image component from S-CPUN pin156  
  G - green image component from S-CPUN pin157  
  B - blue image component from S-CPUN pin158  
  /CS - composite sync from S-CPUN pin151 (SNES_RGBAmp_wCSYNC only)  
  
Look for appropriate Vias and other equivalent solder joints ;)  
  
solder PCB directly beneath the MultiAV  
deactivate the RGB-output of S-RGB by lifting pin20, 22 and 24 from mainboard or simply by removing R15, R16 and R17 from the SNES mainboard (not SNES mini / SFC Jr.).  
  
equivalent installation guides: http://retrorgb.com/snes.html   
(some words about the brightness issue are given below)  
  
While modding some components on the PCB may vary depending on your RGB cable you want to use.  
See the notes related to the components!    
  
-----------------------------------------------------------------------------------  
  
### Want to use /CSYNC on PAL or on 'earlier' NTSC 1Chip systems? ###  
> Of course, there is no problem to do that. Just make sure that MultiAV pin 3 is free.  

On PAL systems:  
- remove R28 from the bottom side of the SNES mainboard  
- remove C46 from the SNES mainboard, too, iff you have C44 (47pF) installed on the RGB bypass board  
- optionally also remove D1  

On NTSC systems:
- remove R11 and R12  
- remove also C46 from the SNES mainboard, too, iff you have C44 (47pF) installed on the RGB bypass board  
- optionally remove also Q1, R9 and R10  
  
-----------------------------------------------------------------------------------  
  
### BRIGHTNESS ISSUE ###  

The S-CPUN overdrives the outputs of R, G and B. This has the effect that R', G' and B' (signals going to your TV set) have higher peak-to-peak voltage values than the standard defines. In simple word, the brightness is to high.

RetroRGB suggest to increase the load on the R, G and B lines (wires coming out of the S-CPUN) to correct that. Measurements were taken by Ultron (http://assemblergames.com/l/threads/snes-mini-rgb-measurements.53053/). Thanks for that btw.
RetroRGB summarizes the final solution:
- for the 'regular' 1Chip model: http://retrorgb.com/snes1chip.html (using 750 Ohm resistors)
- for the SNES Mini/Jr.: http://retrorgb.com/snesminipremade7314.html (using 1.2k Ohm resistors)
The resistors, which are soldered to the SNES mainboard, got a place on the modding PCB (R11, R21 and R31). You may want to the SMD 0603 footprints for the resistors correcting the brightness, here.

Personally, I use an ALTERNATIVE method.
I reduce the current driving the internal DAC of the S-CPUN. This can be done by
- lifting pin 155 of the S-CPUN (which is the analog voltage supply AVCC) and
- reconnect pin 155 to VCC over a 20 Ohm resistor.
This reduces the outputs of R,G and B AND also reduces the GHOSTING issue (just google it - most S-CPUNs have that problem) to a non-noticeable level.
If you decide to use that method, no additional resistors as presented above are needed.
But please be aware: Pin 155 shows to the cartridge slot of the SNES. The space is quite tight. The risk to damage your SNES (e.g. break the pin) is quite high if you have careful enough.
  
-----------------------------------------------------------------------------------  