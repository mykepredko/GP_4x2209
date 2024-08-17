# GP 4x2209 Klipper Optimized 3D Printer Main Controller Board

The GP 4x2209 was designed for new 3D printer users that are new to Klipper.  While being fairly traditional, it has some unique features that make it easier for both new and experienced users to add to their 3D printers.  

The project will not be going forward as the assumptions made at the start of the project regarding the ease of setting up a host with a serial connection was more work and host specific than expected.  

![GP 4x2209 Topside](/photographs/2024_08_17_-_GP_4x2209_Rev_1_10.png)

### Specifications 

- STMG0B1 MCU
- 4x TMC2209 using serial interface with their "diag" pins connected to the MCU
- 1x Board heater
- 1x Nozzle heater
- 3x Two wire fan/LED strip lighting drivers
- 2x Always on fan drivers
- 1x 5V power pins
- 3x Buffered end stops
- BLTouch interface
- Inductive probe interface
- EXP1/EXP2 for a 12864 display
- 2x Neopixel drivers
- SPI port for an ADXL345
- 2x connectors for a BTT smart filament sensor
- Serial connections for Klipper 
- USB C connection for Klipper
- DFU Enabled with "BOOT0" button
- SWD Port

### Unique Features

The board was targeted for new Klipper users and was designed with an eye towards making it as easy as possible for them to setup.  Part of this is reflected above with the multiple endstop interfaces but there are also other features which makes the board attractive to new and experienced users:

- No jumpers. Nothing to select or configure
- "Orthogonal" interfaces.  The circuitry for all the stepper motor drivers and end stops are the same, eliminating the need for wiring specific interfaces to specific devices
- Mounting for Raspberry/Orange Pi zero 2w boards with pogo pin connections which eliminates the need for the user to solder on a connector
- Color coded LEDs for power, MCU status, heaters, fans and endstop sensors 
- Enhanced silk screen information to minimize cross referencing to other sources
- Side access connectors to keep board surface (and status LEDs) visible
- No SD Card slot/No EEPROM
- DFU Enabled for easy and fast Firmware loads and updates

The board works well, has been characterized, and schematics available here on GitHub are correct.  Four are being used with one as a bench unit, two controllering bed slingers and one controlling a CoreXY. USB and Serial connections work with both straight Klipper and with Katapult. 

It should be noted that the unique features do make the GP 4x2209 easier to work with and set up on a 3D printer than other boards.  

Here is the board with a Raspberry Pi zero 2W attached and using the serial interface on a workbench:

![GP 4x2209 Serial Connection](/photographs/2024_08_08_-_GP_on_Test_Fixture.jpg)

Here is a close up of the serial pins and one of the supporting threaded standoffs:

![GP 4x2209 Serial Connection Pogo Pins](/photographs/2024_08_08_-_GP_Closeup_of_Pogo_Pins.jpg)

and a USB connected GP 4x2209 used to control a CoreXY 3D printer.  Note the side access connectors:

![GP 4x2209 USB Connection ](/photographs/2024_08_08_-_GP_in_USB_Operation.jpg)

### Project Conclusion

This project has been very educational and rewarding, however there are no plans on moving foward with it.  The primary reason is that configuring the serial interface is different for each of the various possible hosts as well as being is fairly complex, especially compared to a USB interface.  It is felt that the complexity of implementing the different serial interfaces would be difficult for new users and unduly onerous to support.  

There are no plans for releasing the Gerbers as there was a problem with the SDM1A40CSP-7 diode footprint; the pins are reversed.  Along with that, sections of the silkscreen need to be updated. 
