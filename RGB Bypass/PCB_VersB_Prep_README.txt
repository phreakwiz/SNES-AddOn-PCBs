###############################  
# Version B (without /CS pad) #  
# File: SNES_RGBAmp           #  
###############################  


Component needed:  
  
1. Common Parts: 
 - U1: THS7374 TSSOP-14 package  
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
   3x 1.2kOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
   
b) for SNES Mini/Jr.
 - R11, R21, R31: [1]   
   3x 750Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
 - C14, C24, C34: [3]  
   - 3x 47pF/50V ceramic capacitor 0603 package  
  
3.a) Additional parts for using NTSC-cable schematic or cables with direct wiring [5,6]:  
 - R13, R23, R33:  
   3x 75Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
  
3.b) Additional parts for using PAL-cable schematic [5,7]:  
 - R13, R23, R33:  
   3x 39Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
  
-----------------------------------------------------------------------------------  
  
Notes  
  
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
  
Look at OSHPark: https://oshpark.com/shared_projects/wA0RQ7FC
Or look at PCBway: http://www.pcbway.com/setinvite.aspx?inviteid=10658 (This is an invitation link which gives you $5 discount on your first purchase as well as a $20 discount for my next purchase. Use this link only if you want that!)  
Or use any other PCB service you like :) Make sure that your PCB will be produced on a substrate of 0.8mm or thinner to make installation easier.
