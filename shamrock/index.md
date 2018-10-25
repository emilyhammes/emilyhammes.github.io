Tiny Heart
<iframe id="ytplayer" type="text/html" width="640" height="360" src="https://www.youtube.com/embed/GyDOj3QPB-8?autoplay=0&origin=http://hammeshacks.com" frameborder="0" allowfullscreen></iframe>
Introduction
The Tiny Heart is a PCB shaped like a heart with 20 LEDs. The LEDS are intependantly controlled by an ATTINY 13 using charlieplexing. Code is uploaded to the device with AVR dude using a Bus Pirate, a AVRisp mk II or similar. It is not arduino compatable. It comes pre-programmed in the kit.

Theory
<iframe id="ytplayer" type="text/html" width="640" height="360" src="https://www.youtube.com/embed/Bx5GLyJSWPk?autoplay=0&origin=http://hammeshacks.com" frameborder="0" allowfullscreen></iframe>
Soldering The Heart
Materials
5 110 Ohm resistors
1 0.1 uF capacitor
20 LEDs
1 ATtiny13A
3 to 5v power source (USB, batteries, etc.)
To solder the heart follow these steps:
Front of SnowflakeBack of Snowflake

Solder on all 20 LEDS paying attention to the LED orientation on the silkscreen.
The LEDs are paired, so as long as all the LEDs have the same orientation (cathode down or annode down) it will not really matter.
Solder the capacitor onto the PCB.
Solder the ATtiny13A onto the PCB.
Solder the Resistors onto the PCB.
Solder the power cable onto the PCB.
(Optional) Chain them together by soldering cables onto eachother.
Uploading Code
Code comes pre-uploaded to the ATtiny. The source can be found on github.
Whats Inside the PCB?
schmatic

This is the schematic of the PCB, showing how all the components are connected.

PCB

This is a transparent view of the PCB. Green lines are wires on one side and red lines are wires on the other side of the PCB. The text that will be printed on the board is in magenta on one side and teal on the other. The yellow line is the edge of the board. The gold circles are drilled through the board and have copper on both sides.
