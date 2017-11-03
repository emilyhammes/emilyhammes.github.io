# Intro to Arduino Shield
## Introduction
The Intro to Arduino shield is a simple kit which plugs into an Arduino Uno or similar. It includes a button, light sensor (LDR) and red green blue LED. The LED can be controlled as a digitial or an analog output, the button is a digitial input and the sensor is an analog input. 

## Theory
### How Arduino Code is Organized
Arduino codes are often organized in the following way:
1. At the top of the file is an explanation of what the code does. This is written so that people can quickly understand what you are trying to do without reading the whole file. So that the computer does not get confused by this text, the programmer needs to tell the computer to ignore it. We do this by putting it in a comment. Single line comments in the Arduino IDE (Arduino software) begin with //. Multiline comments begin with /* and end with */. Comments are also used within the code to explain confusing parts in words so that they are easy to understand a year later. 
2. Next globally defined variables are declared. Global variables allow us to define something in a place where it can be accessed by the whole program. They allow us to give abstract ideas names instead of numbers. For example, in the intro shield pin 6 always has a red LED on it. By creating the global variable redLED and assigning it a value of 6 we do not need to remember which pin redLED is on, we just need to remember that it is called redLED. 
3. After the global variables there is always a setup function. This looks like:
void setup () {
... 
}
where the elipsis is replaced by any command which is only run once at the begining of the program. For example, if you wanted a red light to turn on whenever the device is powered then you would tell the light to turn on in this section. 
4. Last, there is a loop function. This looks like: 
void loop () {
...
}
where the elipsis is replaced by code which is run in a loop forever, this is known as an infinite loop. For example, lets say that you wanted to change what the red light was doing when the device was powered: instead of being on, you now want it to blink. To do that you would need to tell the light to turn on in this section and then wait for some time and turn off and wait for more time. After waiting, the loop would run out of instructions and would start over at the begining ... the light would turn back on... time would pass... the light would turn off.... forever (or until the battery died).

Note: to see the difference between setup and loop compare the code in redOn to redBlink.
### Digital Output
### Analog Output
### Digital Input
### Analog Input
### State Machienes

  
## Soldering The Shield
  //<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/OaYhBevXBYk?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>
  
### Materials
  * 3 220 ohm resistors
  * 1 10K ohm resistor
  * 1 RGB LED
  * 1 Light Dependant Resistor (LDR)
  * male pin header
  
### To solder the shield follow these steps:
  1. Solder the 220 ohm resistors to the R-red R-green and R-blue pads.
  
  2. Cut the leads on all of the LEDs to 2.5-3mm.
  3. Solder 1 side of each of the LEDs, making sure that the flat side of the LED matches the flat side on the silkscreen. I usually do the Square pin first.
  4. Align the LEDs by remelting the solder and moving the LED into place.
  5. Once aligned, solder the other pins on the LEDs. 
  6. Solder cut and solder the pin header.
  
  Note: Some people like to leave the leads long and bend them to hold them in place before soldering. Then they trim them after soldering. This is not recommended for this project because it makes alignment and replacement of LEDs difficult or impossible.

### Uploading Code 
* Download the [Arduino software](https://www.arduino.cc/en/Main/Software)
* Select Arduino Uno under Tools > Baord in the Arduino software
* Select the correct comport under Tools > Port in the Arduino software
* Copy the code from the bottom of each video and paste into the Arduino IDE
* Click on the arrow symbol in the Arduino IDE
