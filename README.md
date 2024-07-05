# biodata sonofication midi data over USB

**a fork of biodata sonification project that allows arduino to send midi signals to PC via using midi.h library. i helped a friend create an interactive art installation.**

instructions:
1. build the hardware using the PDF from original repo
2. determine if your board can run [midi.h library](https://github.com/FortySevenEffects/arduino_midi_library?tab=readme-ov-file#documentation) by loading the sketch onto the board. if it runs okay, yay!

*if it doesn't run (like mine - third party uno board) you can turn your arduino into a midi device by flashing custom firmware.*

if your board is official arduino:
- follow this tutorial to make your arduino a class compliant midi device https://www.youtube.com/watch?v=-bCz2I9SMAA by flashing mocoLUFA. load sketch as normally with pins shorted as shown in tutorial, and replug into pc with pins unshorted.

*important* if your board is third party:
- you will need to replace the firmware for the main chip, atmega328P. i use dfu-programmer. follow the instructions in the video tutorial on how to install it and use it. instead of flashing moculufa, flash the appropriate .hex file from here https://github.com/arduino/ArduinoCore-avr/tree/master/firmwares/atmegaxxu2/arduino-usbserial
- you can then now flash mocoLUFA as per the video instructions
- if you do not follow the above step, you will soft-brick your arduino (ask me how i know). to unbrick your arduino, you will need a 'clean' original arduino and hook it up to the 'unclean' one to reset its bootloader. god sent tutorial here https://arduino.stackexchange.com/questions/13292/have-i-bricked-my-arduino-uno-problems-with-uploading-to-board

good luck friends. may this help anyone who gets lost.



