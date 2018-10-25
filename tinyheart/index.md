# Tiny Snowflake
<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/Tw_KlINMhWY?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0" allowfullscreen></iframe>


## Introduction
The Tiny Snowflake is a PCB shaped like a snow flake with 19 LEDs. The LEDS are intependantly controlled by an ATTINY 13 using charlieplexing. Code is uploaded to the device with AVR dude using a Bus Pirate, a AVRisp mk II or similar. It is not arduino compatable.

## Theory
<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/Bx5GLyJSWPk?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0" allowfullscreen></iframe>
  
## Soldering The Snowflake
  
### Materials
  * 5 110 Ohm resistors
  * 1 0.1 uF capacitor
  * 19 LEDs
  * 1 ATtiny13A
  * 5v power source (USB, batteries, etc.)
  
### To solder the snowflake follow these steps:
<img alt="Front of Snowflake" src="snowflake_front.jpg" width="45%" /><img alt="Back of Snowflake" src="snowflake_back.jpg" width="45%" />

1. Solder on all 19 LEDS paying attention to the LED orientation on the silkscreen.
    - The center LED is the only one that is not paired so it is very important that it is in the correct orientation. For the rest it is ok to have them all inverse (or just the spokes or just the ring) because this is charlieplexed so these 18 LEDs are in groups of 9 opposing pairs.
2. Solder the capacitor onto the PCB.
3. Solder the ATtiny13A onto the PCB. 
4. Solder the Resistors onto the PCB. 
5. Solder the power cable onto the PCB.
6. (Optional) Chain them together by soldering cables onto eachother.

### Uploading Code 
* Code comes pre-uploaded to the ATtiny. [The source can be found on github](https://github.com/emilyhammes/snowflake-firmware).

### Whats Inside the PCB?

<img alt="schmatic" src="snowflake-schmatic.jpg" width="100%" />

This is the schematic of the PCB, showing how all the components are connected.

<img alt="PCB" src="snowflake-pcb.jpg" width="45%" />


This is a transparent view of the PCB. Green lines are wires on one side and red lines are wires on the other side of the PCB. The text that will be printed on the board is in magenta on one side and teal on the other. The yellow line is the edge of the board. The gold circles are drilled through the board and have copper on both sides. 
