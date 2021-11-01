# BiquB1MarlinFirmware
Biqu B1 Marlin Firmwares - Stock, BLTouch, UBL

in this repository you can find Marlin firmwares for Biqu B1 3D printer.

The firmwares are based on Marlin 2.0.7.2 and the source code is from BigTreeTech Biqu B1 github page. <br />
The firmwares are for SKR 2 board. <br />
Changes I have made in the firmwares: <br />

configuration_adv.h - the original ADVANCED_PAUSE_FEATURE parameters from Biqu were wrong - the extruder went too fast when loading filament and that caused a skipping stepps and very small amount of purge. <br />
With my version you have to press purge more 1 time (or more) before continue. <br />
(total of 2 extruding processes in a filament change [m600]) <br />

in the BLTouch firmwares I have changed from JUNCTION_DEVIATION_MM to CLASSIC_JERK,
because of a problem that made the travel movement pause mid-travel
(probably because of the Z axis compensation between araes on the print bed). now everything works fine.
In addition, I used safe Z homing (home in the center of the bed) 
and use probe instead of Z endstop (as it should be) <br />
The Probe offset is set to Biqu's documents - 24, -47, -1.5

There are 4 BLTouch firmwares - BLINIEAR 3x3 , 4x4, 5x5 - this is the grid of probing points, the higher - the better, but also time consumer. <br />
I am using 4x4 grid and it is just fine. <br />
The last BLTouch firmware is UBL - Unified Bed Leveling. I am not a fan of that but it is also an option. it is 7 probe points each axis (XY) <br />
Please notice that in order to use BLTouch each power cycle of the printer, <br />
you need to write in your Start Gcode script the command 'M420 S1' to activate and use the bltouch that saved on the EEPROM <br />
If you are using the bed leveling command G29, it is automatically activating and use (no need for M420 S1) <br />


Before considering updating to my firmware, please backup your current firmware. (if it is a stock, you have it in Biqu's github, if it is modified, it probably sitting in your SD card as "FIRMWARE.CUR")

Please use at your own risk, and in the first homing process I advise you to be with hand on the power switch in case something goes wrong. <br />
The firmwares have been tested on 2 printers of Biqu B1 and didn't go into any trouble so it should be all good.

Please let me know if you install a firmware and how it went. <br />
I would love to get feedbacks. <br />
Have Fun! 

<p align="center">
  <img src="https://res.cloudinary.com/echoshare/image/upload/c_scale,q_auto:good,w_630/v1635757779/9_aczzrd.jpg">
</p>

![BiquB1](https://res.cloudinary.com/echoshare/image/upload/c_scale,q_auto:good,w_630/v1635757779/9_aczzrd.jpg)


