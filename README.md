# GP 4x2209 Klipper Optimized 3D Printer Main Controller Board

I’ve designed a board that I was thinking about selling that was targeted to new users. It’s major selling point was that it would be easy and cheaply for new users to add a Klipper specific main controller board with an attached Raspberry/Orange Pi zero 2W to their printers.

2024.06.23 - GP 4x2209 PCB Topside
2024.06.23 - GP 4x2209 PCB Topside
1920×1342 410 KB
The board is working and, I’ve been characterizing it (partially along side the BTT SKR Mini E3 V3.1).

From a specifications point of view, the board is fairly traditional:

- STMG0B1 MCU
- 4x TMC2209 with serial connections
- 1x Board heater
- 1x Nozzle heater
- 3x two wire fans
- 3x end stops
- BL Touch interface
- Inductive probe interface
- EXP1/EXP2 for a 12864 display
- 2x Neopixel drivers
- SPI port for an ADXL345
- 2x connectors for a BTT smart filament sensor
- BTT Pico serial compatible connector along with the ability to mount a built in mounting for Raspberry/ Orange Pi zero 2w boards with pogo pin connections 
- USB C connection for Klipper
- No SD Card slot (this is ONLY for Klipper so why include it and the hassle of including a bootloader when there’s one built into the MCU)
- No jumpers. Just plug in the peripherals and away you go

The board works well and schematics are correct.  I'm not releasing the Gerbers as there was a problem with the SC40A diode footprint - the pins are reversed - and, along with that, I would want to redo sections of the silkscreen. If you are interested in the board as is, I’m really pleased with how it works. There are a number of features that I’ve put in that I think are really useful and attractive in a product. The only PCB issue is a result of an error in the parts library that I used that resulted in the surge protection diodes being put in the wrong way - they’ve been taken off the boards that you see below.

I am running three right now on a couple of old bed slingers and an old CoreXY. It works fine on both USB and serial. Here is a serial setup on a workbench and connected to the CoreXY:

2024.08.08 - GP in USB Operation
2024.08.08 - GP in USB Operation
1920×1440 413 KB
Here’s the bench unit that you’ve been seeing the SSH responses for serial-arksine and serial-ttyAMA0:

2024.08.08 - GP on Test Fixture
2024.08.08 - GP on Test Fixture
1920×1440 298 KB
The leads on the bottom are the serial port interface that I’ve connected to my oscilloscope. You can see my ST-Link peeking in on the right side of the image.

This is what the pogo pins for the 'zero 2W boards look like:

2024.08.08 - GP Closeup of Pogo Pins
2024.08.08 - GP Closeup of Pogo Pins
1920×1440 179 KB
