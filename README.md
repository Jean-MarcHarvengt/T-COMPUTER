# What is the T-COMPUTER?
The T-COMPUTER is a micro computer platform supported and powered by the MCUME project.
- It is based on the powerful Teensy4.1 MCU (800+ MHz ARM based, 1MB internal + 8MB QSPI RAM)
- It features: 
  - a 42 keys basic keyboard (including D-PAD controls + 3 buttons)
  - a built-in 320x240 TFT display
  - VGA output 
  - 16 bits stereo DAC output
  - USB host input (for keyboard, mouse, midi devices...)
  - a DB9 digital joystick input (Atari 2600 style joystick)
  - 2 general purpose buttons    
  - 8+6 shared I/O pins for GP usage
  - a SD card slot (from the Teensy 4.1)
- it can be powered over micro USB or can be used as a takeaway system powered by a 1000mA/H lipo.   
- the T-COMPUTER is a DIY project, you can build it yourself and contribute to it!<br>

<p align="center">
  <img width="640" height="480" src="/images/tcomputer.jpg">
</p>

# News
June 2022: Initial release<br>
- After testing the Rev3 PCB from Aisler, I can finally release everything...
- Repository created with schematics, Gerber files, stl files and binaries
- How to build the T-COMPUTER video(in 3 parts) below<br> 

https://youtu.be/jb_A_36Tv24 <br>
https://youtu.be/ADHyYO1vjXU <br>
https://youtu.be/OZnFfMv9jf4 <br>

# BOM

All the components needed are listed below.<br>
SMD resistors and ceramic capacitors are of type 805.<br>

<p align="left">
  <img width="960" height="640" src="/images/diybom.jpg">
</p>
<p align="left">
<img src="/images/bottom.png" width="480" />  
<img src="/images/top.png" width="480" />  
</p>

<br>

| | Category | Item | Amount | Link |
| --- | --- | --- | --- | --- |
| 1 | resistors| 1KOhms | 2 | --- |
| 2 | | 2.2KOhms | 2 | --- |
| 3 | | 470Ohms | 2 | --- |
| 4 | | 390Ohms | 1 | --- |
| 5 | | 820Ohms | 1 | --- |
| 6 | | 82Ohms | 2 | --- |
| 7 | | 330Ohms | 1 | --- |
| 8 | | 10Ohms | 1 | --- |
| 9 | electolytic capa | 4.7uF | 3 | --- |
| 10| ceramic capa | 100nF | 1 | --- |
| 11| IC| Teensy4.1 | 1 | --- |
| 12| IC| PT8211 | 1 | --- |
| 13| switches| classic | 42 | --- |
| 14| switches| high | 2 | --- |
| 15| TFT| ST7789 | 1 | --- |
| 16| VGA| DB15 female | 1 | --- |
| 17| JOYSTICK| DB9 male | 1 | --- |
| 18| USB| ? | 1 | --- |
| 19| AUDIO| Jack female | 1 | --- |
| 20| Battery| lipo 1000mAh | 1 | --- |
| 21| USB micro lipo charger| pcb | 1 | --- |
| 22| power switch| 3 pins, mini | 1 | --- |
| 23| LED| green or yellow | 1 | --- |
| 24| ST7789 HEADER| 1x8 | 1 | --- |
| 25| ILI9341 HEADER| 1x9 | 1 | --- |
| 26| JOYEXT HEADER| 1x8 | 1 | --- |
| 27| USB HEADER| 1x5 | 3 | --- |


# Assembly
Location and values for the components are printed on the PCB.<br>
Respect the polarity for of electrolytic capacitors (dot indicates the +) and the IC (dot is pin 1).<br>
Follow the step procedure below and test between the steps:
- before starting anything, 
  -  solder the PSRAM chip on the teensy 4.1 board and test it
     - use the sketch provided by the PJRC project
  - solder the header pins of the teensy (classic male header pins), including the 1x5 usb header pins (I use female low profile personally)
  - after that, program the teensy with one of the VGA emulator in /bin
- step 1: VGA out + keys
  - solder all smd resistors
  - solder the 4 switches of the direction D-PAD at the right of the keyboard
  - solder the VGA connector
  - solder the Teensy 4.1 (use female header as socket, don't solder directly!!!)
  - power the teensy over micro usb and test
- step 2: sound out + keyboard
  - solder the PT8211 IC
  - solder all smd capacitors (respect polariry for the electrolytes)
  - solder all keys of the keyboard + the 2 user keys 
  - solder the audio connector
  - power the teensy over micro usb and test
- step 3: USB + joystick
  - solder the joystick DB9 connector
  - solder the ST and ILI header pins (female pins)
  - solder the joyext header pins (female pins)
  - solder the USB connector + USB header pins on the PCB (2 females pins on top of each other)
  - connect the Teensy USB header to the PCB USB header pins using wires
  - power the teensy over micro usb and test
- step 4: TFT display
  - connect the TFT display
  - program the teensy with one of the TFT emulator in /bin
  - power the teensy over micro usb and test
- step 5 (optional):  
  - solder the power switch
  - solder the battery to the USB charger PCB kit
  - glue the USB charger PCB kit at the back of the T-COMPUTER board and solder the power pins
  - glue the battery at the back of the T-COMPUTER board
  - Always DISCONNECT the teensy micro usbcable when powering up the system via the battery.
  - power switch down = battery powered
