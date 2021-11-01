# BiquB1MarlinFirmware
Biqu B1 Marlin Firmwares - stock, BLTouch, UBL

in this repository you can find Marlin firmwares for Biqu B1 3D printer.

the firmwares are based on Marlin 2.0.7.2 and the source code is from BigTreeTech Biqu B1 github page.

the firmwares are for SKR 2 board.
changes I have made in the firmwares:

configuration_adv.h - the original ADVANCED_PAUSE_FEATURE parameters from Biqu were wrong - the extruder went too fast when loading filament and that caused a skipping stepps and very small amount of purge.
with my version you have to press purge more 1 time (or more) before continue. 
(total of 2 extruding processes in a filament change [m600])

in the BLTouch firmwares I have changed from JUNCTION_DEVIATION_MM to CLASSIC_JERK,
because of a problem that made the travel movement pause mid-travel
(probably because of the Z axis compensation between araes on the print bed). now everything works fine.
In addition, I used safe Z homing (home in the center of the bed) 
and use probe instead of Z endstop (as it should be)
the Probe offset is set to Biqu's documents - 24, -47, -1.5

there are 4 BLTouch firmwares - BLINIEAR 3x3 , 4x4, 5x5 - this is the grid of probing points, the higher - the better, but also time consumer.
I am using 4x4 grid and it is just fine.
The last BLTouch firmware is UBL - Unified Bed Leveling. I am not a fan of that but it is also an option. it is 7 probe points each axis (XY)

before considering updating to my firmware, please backup your current firmware. (if it is a stock, you have it in Biqu's github, if it is modified, it probably sitting in your SD card as "FIRMWARE.CUR")

Please use at your own risk, and in the first homing process I advise you to be with hand on the power switch in case something goes wrong.
the firmwares have been tested on 2 printers of Biqu B1 and didn't go into any trouble so it should be all good.

Please let me know if you install a firmware and how it went. I would love to get feedbacks. 
Have Fun! 
