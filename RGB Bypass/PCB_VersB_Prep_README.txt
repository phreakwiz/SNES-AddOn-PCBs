###############################  
# Version B (without /CS pad) #  
# File: SNES_RGBAmp           #  
###############################  


Component needed:  
  
1. Common Parts: 
 - U1: [0]
     (THS7373 or THS7374 TSSOP-14 package) OR (THS7314 or THS7316 SOIC-8 package)  
 - R1: 4.99kOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
 - C1: 100nF/50V ceramic capacitor 0603 package    
 - C2: 22uF/6.3V tantalum capacitor type-B package (typical: 3.50mm x 2.80mm) 
  
 - C11, C21, C31:  
     3x 82nF/25V ceramic capacitor 0603 package   
 - R12, R22, R32:  
     3x 3.6MOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
  
2. Special components (read notes):  
a) for 1Chip consoles (not Mini/Jr.)  
 - R11, R21, R31: [1]  
     3x 750Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
   
b) for SNES Mini/Jr.
 - R11, R21, R31: [1]   
     3x 1.2kOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
 - C14, C24, C34: [3]  
     3x 47pF/50V ceramic capacitor 0603 package  
  
3.a) Additional parts for using NTSC-cable schematic or cables with direct wiring [5,6]:  
 - R13, R23, R33:  
     3x 75Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
  
3.b) Additional parts for using PAL-cable schematic [5,7]:  
 - R13, R23, R33:  
     3x 39Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
  
-----------------------------------------------------------------------------------  
  
Notes  
  
[0]  
All four different THS video amplifier are supported. The low pass filters of the THS7373 and THS7374 can be set in bypassed with J1. With the THS7314 and THS7316 J1 has no effect!  
The THS7314 and THS7374 amps have SD-video filters and the THS7316 and THS7373 HD-video filters.  
  
[1]  
These resistors are for correcting the brightness issue on 1Chip consoles. Please take further reading on the 1Chip_README.txt before buying these components.  
 
[3]  
These capacitors and not really needed, but they are present at the outputs of the MultiAV for de-bouncing the MultiAV jack while plugging in and out.  
  
[5]  
Just pic one (i.e. 3.a) OR 3.b) !) and do not buy all parts. 
  
[6]  
If you have a PAL system, you may replace R18 on the SNES mainboard with a 75Ohm resistor 0805 package (0.125W, 1% tolerance should be fine).  
  
[7]  
If you have a NTSC system, you may replace R18 on the SNES mainboard with a 39Ohm resistor 0805 package (0603 package on SNES Mini/Jr.) (0.125W, 1% tolerance should be fine).  
  
-----------------------------------------------------------------------------------  

### Need a PCB? ###  
  
Look at OSHPark: https://oshpark.com/shared_projects/FGz6MoI9
Or look at PCBWay: http://www.pcbway.com/
Or use the affiliate link at PCBway: http://www.pcbway.com/setinvite.aspx?inviteid=10658 (This is an invitation link which gives you $5 discount (10% max.) on your first purchase as well as a $20 discount for my next purchase. Use this link only if you want that!)  
Or use any other PCB service you like :) Make sure that your PCB will be produced on a substrate of 0.8mm or thinner to make installation easier.
