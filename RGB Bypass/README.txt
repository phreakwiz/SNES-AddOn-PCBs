SNES_RGBAmp: for 1Chip-01/02 boards  
SNES_RGBAmp_1Chip03+: for 1Chip-03 boards and for SNES Mini/SFC Jr.  
  
-----------------------------------------------------------------------------------  
  
Solder Joints:  
  
  R - red image component from S-CPUN pin156  
  G - green image component from S-CPUN pin157  
  B - blue image component from S-CPUN pin158  
  /CS - composite sync from S-CPUN pin151  
  
Look for appropriate Vias and other equivalent solder joints ;)  
  
solder PCB directly beneath the MultiAV  
deactivate the RGB-output of S-RGB by lifting pin20, 22 and 24 from mainboard or simply by removing R15, R16 and R17 from the SNES mainboard (not SNES mini / SFC Jr.).  
  
equivalent installation guides: http://retrorgb.com/snes.html  
(with this version, there is no need to adjust any brightness issues ;)  
  
While modding some components on the PCB may vary depending on your RGB cable you want to use.  
See the notes related to the components!    
  
-----------------------------------------------------------------------------------  
  
Component needed:  
  
1. Common Parts:  
 - 1x THS7314 SOIC-8 package [board SNES_RGBAmp only]  
 - 1x THS7374 TSSOP-14 package [board SNES_RGBAmp_1Chip03+ only]  
  
 - 1x 22uF/6.3V tantalum capacitor type-C package  
 - 1x 100nF/50V ceramic capacitor 0805 package  
  
 - 2x 1.3kOhm resistor 0805 package (0.125W, 1% tolerance should be fine) [1]  
 - 2x 8.45kOhm resistor 0805 package (0.125W, 1% tolerance should be fine) [1]  
 - 1x 806Ohm resistor 0805 package (0.125W, 1% tolerance should be fine) [1]  
 - 1x 9.53kOhm resistor 0805 package (0.125W, 1% tolerance should be fine) [1]  
  
 - 1x 4.99kOhm resistor 0805 package (0.125W, 1% tolerance should be fine) [board SNES_RGBAmp_1Chip03+ only]  
 - 1x 4.30kOhm resistor 0805 package (0.125W, 1% tolerance should be fine) [board SNES_RGBAmp_1Chip03+ only]  
 - 1x 47pF/50V ceramic capacitor 0805 package [board SNES_RGBAmp_1Chip03+ only], [2]  
 - 3x 47pF/50V ceramic capacitor 0805 package [board SNES_RGBAmp_1Chip03+ in SNES Mini / SFC Jr. only], [2]  
  
 - 1x (between 75Ohm and 300Ohm [3]) resistor 0805 package (0.125W, 1% tolerance should be fine)  
 - 1x 330uF/6.3V tantalum capacitor type-D package  
  
2.a) Additional parts for using NTSC-cable schematic [4,5]:  
 - 3x 75Ohm resistor 0805 package (0.125W, 1% tolerance should be fine)  
  
2.b) Additional parts for using PAL-cable schematic [4,6]:  
 - 3x 39Ohm resistor 0805 package (0.125W, 1% tolerance should be fine)  
 - 3x 330uF/6.3V tantalum capacitor type-D package  
  
2.c) Additional parts for a cable with direct wiring RGB [4,5]:  
 - 3x 75Ohm resistor 0805 package (0.125W, 1% tolerance should be fine)  
 - 3x 330uF/6.3V tantalum capacitor type-D package  
  
-----------------------------------------------------------------------------------  
  
Notes  
  
[1]  
You may want to replace them with 3x 750Ohm (R4, R5, R6) and 3x 7.5kOhm (R7, R8, R9) resistors for simplicity. This gives a 'warmer' image.  
  
[2]  
These capacitors and not really needed, but they are present in 1Chip-01/02/03 consoles for de-bouncing the MultiAV jack while plugging in and out.  
  
[3]  
depending on your TV: 75Ohm matches impedance, 300Ohm matches standard for sync. Personally I use 75Ohm. My TV does not have any problems with all values between 75Ohm and 300Ohm!  
  
[4]  
Just pic one (!) and do not buy all parts. If you use NTSC-cable schematic you have to short the three jumpers on the PCB.  
  
[5]  
If you have a PAL system, you may replace R18 on the SNES mainboard with a 75Ohm resistor 0805 package (0.125W, 1% tolerance should be fine).  
  
[6]  
If you have a NTSC system, you may replace R18 on the SNES mainboard with a 39Ohm resistor 0805 package (0.125W, 1% tolerance should be fine).  
