xinkebot-orca-2-cygnus-marlin-firmware

# Overview

This project is a fork of the Marlin 2.0 Project which adds support for the Xinkebot Orca 2 Cygnus. This requires a hardware conversion using the SKR Mini E3 which is [outlined here](https://github.com/MKronmiler/xinkebot_orca_2_cygnus_marlin_conversion)

## Specific Adjustments

1. Printer axis size properly set
2. Fixed motors being reversed in autohome function
3. Motor steps/mm properly set (specifically important for the Z axis)
4. Adjust motor currents to match the requirements of the motors I could find (they're generic steppers with horrendous documentation and may need adjustment)
5. Added BL touch support
6. Included babystep support
7. Mesh Bed Leveling Support

# Important Notes

1. **You cannot flash the firmware.bin file in the typical manner.** This is because there is a bug somewhere in the SKR mini E3. Attempting to flash with the firmware.bin output of platformio will fail. You must make the filename all caps for it to work (don't ask me why I don't know but it worked for me). firmware.bin --> FIRMWARE.BIN

2. You must compile the non-maple version of the firmware otherwise the print fan won't work (no idea why)