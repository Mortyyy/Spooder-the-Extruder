# Mission Statement

This is a repository of code I've modified for use with an Anycubic Kossel Plus 3D printer. Built in code based on the Marlin 1.1.8 framework.

While this printer is very good mechanically (the quality and speed of the prints are astounding), there is a lot to be desired in the firmware available online. Additionally, there are some physical modifications that can be made to improve the machine.

# Marlin 3D Printer Firmware

The majority of this code is modified from the general [Marlin 3D Printer Firmware](https://github.com/MarlinFirmware/Marlin code.) At this point, Marlin 2.0.x has been released but is unpolished, so I've decided to make changes in an older, more stable release. Additional documentation can be found at [The Marlin Documentation Project](https://www.marlinfw.org/).


# Custom Functions and Features
## Filament Change: Work in Progress

Function to heat the extruder and reverses motor on the filament intake. Prompts user to manually retract the loaded filament as well during this process. Click the control knob when displayed prompt has been completed. The filament intake motor will now drive forwards to help feed new filament in. Click once for cooldown procedures at this point. Click twice at any time to end function.

## Emergency Stop: NOT YET

Either a special click sequence on the knob or a specialized button.

## Detailed Print Progress: NOT YET

On print pause or manual stop, the printer will display the line number the print was aborted at. This will allow one to better troubleshoot or restart a particular print job.

## Networking Features and Monitoring: NOT YET

I plan on adding an ESP01 ESP8266 wifi module to the Trigorilla board. Thingiverse [resource](https://www.thingiverse.com/thing:2798147).

## UI Optimization on the LCD Display: NOT YET


# Machine Mods
- [ ] [Rubber Feet](https://www.thingiverse.com/thing:2654983) for vibration dampening
- [x] Low-profile print surface clamps
- [ ] Stepper motor heat sinks
- [ ] Stabilizers for the LCD screen
- [x] Tool holders
- [ ] Camera mount
- [ ] LED light strips
- [ ] TPU filament extruder and software settings
- [x] Knob for manual filament feeding/retracting.

# Technical documentation
## Control Board
The Anycubic Kossel Plus utilizes a Tri-Gorilla board. Requires a CP2102 driver for the associated communication chip.
- Main control chip: ATMEGA256016AU, programmable using ICSP.
- Input Voltage: 10V to 30V
- Standby Current: 35mA ±5mA
- Supports five stepper motors.
- Dimensions: 125 x 82 mm

##G-Code Commands Reference List
- [Wikipedia](https://reprap.org/wiki/G-code#M500:_Store_parameters_in_EEPROM)
