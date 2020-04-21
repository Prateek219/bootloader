# BOOTLOADER
The common method to program a microcontroller is to use a programmer for that particular
microcontroller. An alternative is to write a small program (a bootloader) into the flash memory of the
microcontroller which allows code and EEPROM data to be transmitted over a serial cable and written
to the microcontroller.

A bootloader has to written to the flash memory just once using a conventional programmer. The
bootloader is programmed such that when bootloader start condition is satisfied it receives data via a
predetermined interface (eg, UART) and writes these into the program memory at predetermined
locations.

We would be using the AVR Butterfly Bootloader. For programming using the
Bootloader we would be using AVRDude which is part of the WinAVR package.
Instructions for setting up the main.c and makefile are also given in the readme file. 

1. Select the MCU type to be used.

2. Keep the bootloader size t its default 512 words.

3. Set the baudrate making sure it’s the same as the one set for the PORT used.

4. Set the CPU frequency for eg, #define F_CPU 8000000 for 8MHz.

5. Now select the startup mode. 
