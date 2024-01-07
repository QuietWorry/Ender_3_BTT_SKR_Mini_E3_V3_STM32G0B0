# Custom Firmware for Ender 3 V2 Neo with BTT SKR Mini E3 V3.0

This README outlines the steps for setting up a custom firmware for the Ender 3 V2 Neo 3D printer, specifically tailored for the BTT SKR Mini E3 V3.0 mainboard equipped with a STM32G0B0 processor, Sprite Pro Extruder, CR Touch, and dual Z motors.

## Overview

This guide is for a printer running clipper and a pi running mainsail

The BTT SKR Mini E3 V3.0 mainboard provided for the Ender 3 V2 Neo comes with a STM32G0B0 processor, instead of the commonly used STM32G0B1. This requires a custom firmware setup using Klipper. The following steps will guide you through creating a custom firmware, modifying the printer configuration, and setting up the CR Touch sensor.

*Start with BTT's official page for the board: https://github.com/bigtreetech/BIGTREETECH-SKR-mini-E3/tree/master
and this guys stuff: https://github.com/LeeOtts/Ender3v2-Klipper-Configs

## My Hardware

- Ender 3 V2 Neo 3D Printer
- BTT SKR Mini E3 V3.0 with STM32G0B0 processor
- Sprite Pro Extruder
- CR Touch
- Dual Z Motors

## Firmware Setup

1. **Creating Custom Firmware with Klipper:** 
   - Access the Klipper folder and run the `make menuconfig` command.
   - Specify the correct processor (STM32G0B0) in the configuration.

2. **Modifying Printer Configuration:**
   - Use the `ls /dev/serial/by-id/*` command to identify the MCU's correct serial ID.
   - Modify the provided Klipper `printer.cfg` file, replacing the MCU details with the correct serial ID from the previous step.

3. **Setting up CR Touch:**
   - Change the BLTouch sensor pin in the `printer.cfg` file to `^PC14` to ensure proper functioning of the CR Touch.

## Conclusion

Following these steps should successfully set up your Ender 3 V2 Neo with the custom configuration required for the BTT SKR Mini E3 V3.0 mainboard with a STM32G0B0 processor. Ensure all connections and configurations are double-checked before initiating the printer.

---

*Note: This guide assumes a basic understanding of 3D printer firmware and configuration. Proceed with caution and at your own risk.*
