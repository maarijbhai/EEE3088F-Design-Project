# Micro Mouse Power Subsystem

This respository contains the datasheets of components used, schematics and production files of a power subsystem of a Micro Mouse. The power subsystem handles the charging, battery monitoring, motor controll and providing power to the various other subsections of a Micro Mouse.

## Table of Contents
- [Overview](#overview)
- [Subsytem Requirements](#subsystem-requirements)
- [File Structure](file-structure)
- [Usage](#usage)
- [Production](#production)
- [Credits](credits)

## Overview

Designed to navigate and solve a maze by itself, the Micro Mouse is a common project with even competitions made to determine who is able to create the fastest and most efficient Micro Mouse. While not on the competition level this project is undertaken by students in the University of Cape Town to put into practice all the theoretical knowledge learnt in their studies. With the hardware and sensoring subsystem designed by the university, the aim of this project is to design the power subsystem that powers the overall design.

## Subsystem Requirements

- Operate up to 4 motors bidirectionally with the pins available to you (listed in the power pinout table). You will need to control 2x brushed DC motors which could each draw 200mA at the highest voltage of a 1S1P battery (the battery is further specified in the battery section). The other 2x motors are for the auxiliary connection and need to operate 500mA each.
- Place an INA219 for monitoring the battery on the I2C Bus and configure it correctly with respect to the hardware (cannot have BOTH A0 AND A1 on GND)
- Charge the battery from the 9V input pin (listed in the power pinout table).
- Have two charging modes for a higher and lower charging current for the battery (200mA, and approximately 600mA ±100mA from the battery perspective.
- Integrate USB C and get 9V out of the USB Host
- Provide 2x External Load Switching at 1A each (High Side connected to your 5V)
- Provide a 3V3 5% accuracy (300mA max) and 5V Out 5% accuracy (1.5A max)
- Provide an ON/OFF switch. OFF state: battery draw <30uA. ON state: can provide your robot peak current of 2A. The switch needs to shut down 5V and 3V3.

## File Structure

Each of the above mentioned requirements are designed seperately under their own folder name ultimately meeting up in the Main project folder. This was to prevent any clashes or errors arising from outdated revisions of the project being worked on. 

The production files (gerbers) can be found inside the Main project folder under "JLCPCB".

## Usage

# Access schematic or PCB:
To view or modify the schematic and/or PCB:
1. Open KiCad 9 or later
2. Load the Main project (or any other desired)
3. Edit or simulate as needed

# To manufacture the PCB:
1. Navigate to the JLCPCB website
2. Upload the Gerber ZIP file
3. Use the provided BOM and CPL files in the JLCPCB file directory inside the main project folder for assembly

## Credits
- Maarij Alam
- Saeed Solomon

Third-party components from Texas Instruments, ON Semiconductor, and others.
