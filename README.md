# What is the T-COMPUTER?
The T-COMPUTER is a new micro computer platform supported and powered by the MCUME project.
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
- the T-COMPUTER is a DIY project, you can build it yourself and contribute to it!

https://youtu.be/jb_A_36Tv24 <br>
https://youtu.be/ADHyYO1vjXU <br>
https://youtu.be/OZnFfMv9jf4 <br>
<br>

# News
June 2022: Initial release<br>
- After testing the Rev3 PCB from Aisler, I can finally release everything...
- Repository created with schematics, Gerber files and binaries
- How to build the T-COMPUTER video published! 

# BOM

Computer systems supported and status on various MCU platforms<br>

| System | Teensy3.6 | Teensy 4.0 | Teensy4.0 +PSRAM | Teensy4.1 +PSRAM | ESP32 | ESP32-Wrover | Pico |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Zx81        | X | X | X | X | X | X | X |
| Zx spectrum | X | X | X | X | X | X | X |
| Atari 800   | X | X | X | X | X | X | X |
| C64         | X | X | X | X | X | X | X |
| VIC20       |   |   |   | X |   |   | X |
| Apple2      |   |   |   | X |   |   |   |
| Atari 520ST | - | full speed! | X | X (640x400!) | - | slow | - |
| 8086 XT PC  | - | full speed! | X | X | - | slow | - |
| MSX1/2      | - | full speed! | X | X | - | - | - |
| Amiga       | - | - | exp only! | X (640x240!) | - | - | - |
| Doom        | - | - | - | x | - | - | - |

<p align="center">
  <img width="640" height="480" src="/images/diybom.jpg">
</p>
