############################  
# Version A (with /CS pad) #  
# File: SNES_RGBAmp_wCSYNC #  
############################  
  
  
Component needed:  
  
1. Common Parts: 
 - U1: [0]  
     THS7373 or THS7374 TSSOP-14 package  
 - R1: 4.99kOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
 - C1: 100nF/50V ceramic capacitor 0603 package    
 - C2: 22uF/6.3V tantalum capacitor type-B package (typical: 3.50mm x 2.80mm) 
  
 - C11, C21, C31:  
     3x 82nF/25V ceramic capacitor 0603 package   
 - R12, R22, R32:  
     3x 5.1MOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
  
2. Special components (for 1Chip and SNES Mini/Jr.)  
   (!!! combine a), b) and c) AND read notes!!!)  
  
a) for 1Chip-0x consoles (not Mini/Jr.)  
 - R11, R21, R31: [1]  
     3x 750Ohm resistor 0603 package (0.125W, 1% tolerance should be fine) 
  
b) for SNES Mini/Jr.
 - R11, R21, R31: [1]  
     3x 1.2kOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
 - C14, C24, C34:  
     3x 47pF/50V ceramic capacitor 0603 package [4]  
  
c) for both 1Chip-03 AND SNES Mini/Jr.  
 - C44: 1x 47pF/50V ceramic capacitor 0603 package [2,4]  
 - R41: [2]  
     TTL compatible:    4.99kOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
     75Ohm termination: 9.53kOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
 - R42: [2,2a]  
     TTL compatible:    4.30kOhm resistor 0603 package (0.125W, 1% tolerance should be fine)  
     75Ohm termination: 620Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
 - C43: [2,3]  
     TTL compatible:    no component (short J2)
     75Ohm termination: 220uF/6.3V or 330uF/6.3V tantalum capacitor type-D package (typical: 7.30mm x 4.30mm)  
 - R43: [2,2a,2b]  
     TTL compatible:    0Ohm
     75Ohm termination: 75Ohm resistor 0603 package (0.125W, 1% tolerance should be fine) [2,3]  
  
3.a) Additional parts for using NTSC-cable schematic or cables with direct wiring [5,6]:  
 - R13, R23, R33:  
     3x 75Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
  
3.b) Additional parts for using PAL-cable schematic [5,7]:  
 - R13, R23, R33:  
     3x 39Ohm resistor 0603 package (0.125W, 1% tolerance should be fine)  
  
-----------------------------------------------------------------------------------  
  
Notes  
  
[0]  
Both ICs are supported. The THS7373 has one SD-video low pass filter (used for /CSYNC) and three HD-video filters (used for R, G and B). The THS7374 has four SD-video filters.  
At the THS7373 the HD-video LPFs can be bypassed and at the THS7374 all four SD-video filters can be bypassed (using J1).  
  
[1]  
These resistors are for correcting the brightness issue on 1Chip consoles. Please take further reading on the 1Chip_README.txt before buying these components.  
    
[2]  
These components are for csync restoration. The R41 (common components) is needed on all boards to leave the connected pin 1 of the THS7373 / THS7374 not floating.  
However, buffering csync can also be used on other consoles like 1Chip-01/02 (also PAL version). To do so you have to ensure that pin 3 of the MultiAV is freed before starting the installation. 
  
With R41, R42 you can adjust the output level of the /CSYNC in accordance with your setup (termination of your receiving device).  
  
[2a]  
Be carefull, if you have a 75Ohm termination setup AND use a PAL SNES RGB cable, which has an additional 75Ohm load at the sync connection inside the SCART plug.  
In this case you have to EITHER remove the load resistor inside your cable OR adjust R42 to 953Ohm OR adjust R43 to 39Ohm. I would prefere the first option.  
  
[2b]
If you use a cable with /CSYNC wiring, please note that these cable should not have any components within or at the sync wire! This fact doesn't matter whether you have a TTL-setup or a 75ohm terminated setup.  
  
[3]  
Under C43 there is the jumper J2. This cap is meant to remove the DC component out of the /CS signal. If your end-device does not like that, remove the cap and just short the underlying jumper.  
Resistor R43 can also be soldered on the PCB in any case. If you do not wish to use the buffered /CS, just leave C43 and the underlying jumper open. R43 has then no influence on the rest of the circuit.  
  
[4]  
These capacitors and not really needed, but they are present at the outputs of the MultiAV for de-bouncing the MultiAV jack while plugging in and out.  
  
[5]  
Just pic one (i.e. 3.a) OR 3.b) !) and do not buy all parts. 
  
[6]  
If you have a PAL system, you may replace R18 on the SNES mainboard with a 75Ohm resistor 0805 package (0.125W, 1% tolerance should be fine).  
  
[7]  
If you have a NTSC system, you may replace R18 on the SNES mainboard with a 39Ohm resistor 0805 package (0603 package on SNES Mini/Jr.) (0.125W, 1% tolerance should be fine).  
  
-----------------------------------------------------------------------------------  

### Need a PCB? ###  
  
Look at OSHPark:   https://oshpark.com/shared_projects/hMAav8Ju
Or look at PCBWay: http://www.pcbway.com/
Or use the affiliate link at PCBway: http://www.pcbway.com/setinvite.aspx?inviteid=10658 (This is an invitation link which gives you $5 discount (10% max.) on your first purchase as well as a $20 discount for my next purchase. Use this link only if you want that!)  
Or use any other PCB service you like :) Make sure that your PCB will be produced on a substrate of 0.8mm or thinner to make installation easier.