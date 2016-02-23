SNES_RGBAmp: for PAL 3Chip-SNES boards (SNSP-CPU-01/02)  
  
-----------------------------------------------------------------------------------  
  
Installation:  
  
  - remove R8, R9, R13, R14, R18, R19 and Q4, Q6, Q8 from the SNES mainboard  
  - solder the three 1.87kOhm resistors to R8, R13 and R18  
  - solder the three 750Ohm resistors to R9, R14 and R19  
  - solder the directly beneath the MultiAV  
  - connect pad 'R' with the pad where the base of Q4 was  
  - connect pad 'G' with the pad where the base of Q6 was  
  - connect pad 'B' with the pad where the base of Q8 was  
  
While modding some components on the PCB may vary depending on your RGB cable you want to use.  
See the notes related to the components!    
  
-----------------------------------------------------------------------------------  
  
Components needed:  
  
1. Parts for the PCB:  
 - 1x THS7314 SOIC-8 package   
  
 - 1x 22uF/6.3V tantalum capacitor type-C package (typical: 6.00mm x 3.20mm)  
 - 1x 100nF/50V ceramic capacitor 0805 package  
  
 - 3x 82nF/50V ceramic capacitor 0805 package  
 - 3x 3.6MOhm resistor 0805 package (0.125W, 1% tolerance should be fine)   
  
2.a) Additional parts for the PCB for using NTSC-cable schematic [1]:  
 - 3x 75Ohm resistor 0805 package (0.125W, 1% tolerance should be fine)  
  
2.b) Additional parts for using PAL-cable schematic [1]:  
 - 3x 39Ohm resistor 0805 package (0.125W, 1% tolerance should be fine) [2]  
 - 3x 220uF/6.3V or 330uF/6.3V tantalum capacitor type-D package (typical: 7.30mm x 4.30mm)  
  
2.c) Additional parts for a cable with direct wiring RGB [1]:  
 - 3x 75Ohm resistor 0805 package (0.125W, 1% tolerance should be fine)  
 - 3x 3x 220uF/6.3V or 330uF/6.3V tantalum capacitor type-D package (typical: 7.30mm x 4.30mm)  
  
3. Parts for the SNES mainboard:  
 - 3x 750Ohm resistor 0805 package (0.125W, 1% tolerance should be fine)  
 - 3x 1.87kOhm resistor 0805 package (0.125W, 1% tolerance should be fine)   
  
-----------------------------------------------------------------------------------  
  
Notes  
  
[1]  
Just pic one (!) and do not buy all parts. If you use NTSC-cable schematic you have to short the three jumpers on the PCB.  
  
[2]  
You could also use 6x 75Ohm resistor (0805 package (0.125W, 1% tolerance should be fine)) and stack two of them on each pad pair.  