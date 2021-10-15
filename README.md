# minime
3D printer mainboard Minime + Minime_mini, using a Raspberry Pi Pico (RP2040). Can be used on top of a Raspberry Pi or as standalone version.

The main goal of creating this little board was to design a 3D printer mainboard with Raspberry Pi Pico (RP2040) as MCU running Klipper firmware. Because of the limited number of I/O pins and ADC pins the board results in a very minimalistic (only 4 Stepper Driver on minime_mini) but also universal PCB.

Main Features:
- Running Klipper Firmware on Raspberry Pi Pico
- Raspberry Pi Host Version = use the minime and minime_mini as 3D Printer Mainboard with all primary features, like Heat_Bed and Hotend Control, Hotend Fan and Part Fan Control, X/Y/Z Endstop reading, Hotend Temperature and Bed Temperature reading, Probe reading, controlling 4 TMC2209 Stepper Driver
- The minime board can separately be used as standalone sensor board without the need of minime_mini as driver board and can directly be connected via usb to any Raspberry Pi Host
- Switchable between Endswitch and sensorless Homing via Solderjumper
- Switchable between +5V and +24V Probe via Solderjumper
- Switchable between +5V and +24V Fan Supply via Solderjumper
- Hotend Fan (Fan1) uses a 3 pin Header: VCC, GND and tachometer signal for savety reasons
- Fan tachometer signal can be set up in Klipper. If the speed of the Hotend Fan is not detectable, Klipper shuts down the printer
- Part Fan (Fan2, Sunon MF50152VX-1L01C-Q99) uses a 4 pin Header: VCC, GND and PWM signal for directly control the speed, tachometer signal is n.c.
- Integrated bat85 diode (or similar) if using the +24V probe
- Raspberry Pi Pico is used with pin headers to completely exchange the module if broken

Raspberry Pi Pico (with RP2040 Microcontroller):

- Raspberry Pi Host Version --> Raspberry Pi Pico has to be flashed with klipper.uf2 (UART Communication Option)
- Raspberry Pi Pico standalone Version --> Raspberry Pi Pico has to be flashed with klipper.uf2 (USB Communication Option)

![20211009_142807](https://user-images.githubusercontent.com/63971082/136657995-72b43971-b637-41dd-9ba2-68b54d284a6b.jpg)

Has to be continued!
