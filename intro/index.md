# Intro to Arduino Shield

<iframe id="ytplayer" type="text/html" width="640" height="360" src="https://www.youtube.com/embed/vzUWGo-a7EA&list=PLOODSiZqm-6Vm45pemXBhKMmCtVTKruHoautoplay=0&origin=http://hammeshacks.com" frameborder="0"></iframe>

<iframe id="ytplayer" type="text/html" width="640" height="360" src="https://www.youtube.com/embed/YMQ2k3mRRPE?autoplay=0&origin=http://hammeshacks.com" frameborder="0"></iframe>

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
Digital outputs allow us to tell a pin to be high or low. High is sometimes called 1 and low is sometimes written as 0. In the Intro to Arduino shield, we use digital outputs to turn on or blink lights, act as a power source or act as a ground pin. 
To set a pin as digital somewhere in the code we need to write "pinMode (redLED, OUTPUT);" and then "digitalWrite(redLED, LOW/HIGH/0/1);",  where redLED could be a pin number or a variable name we defined previously. 
### Analog Output
If digitial outputs are like an on off switch, analog outputs are like dimmers. They work by switching a pin between high and low much faster than you can see. The ratio of on to off is defined by a number between 0 and 255, 0 being low all the time and 255 being high all the time. Just like with digital outputs, we need to write "pinMode (redLED, OUTPUT);" however, next we need to write  "analogWrite(redLED, 0-255);" where 0-255 is any number in that range. 
### Digital Input
Digital inputs are things that can be either on or off with nothing inbetween like a button or a switch. Similar to digital outputs we need to set the pinMode but this time we set the pinmode to input: "pinMode(button, INPUT);". Alternatively, if we are using a button, sometimes we need to use an integrated pullup resistor. If this is the case, we set pinmode to input pullup "pinMode(button, INPUT_PULLUP);". When we want to read the state of the button, the code will read digitalRead(button), where button is a previously defined variable.
### Analog Input
Analog inputs are things that can be in any state between high and low. One example is a Light Dependand Resistor (LDR). The resistance in an LDR changes based on how much light hits the sensor surface. Using Ohm's Law (V=IR), we can translate the change in resistance to a change in voltage. The Arduino can approximate what the voltage on the pin is. To do this we need to include the following lines of code: "pinMode (LIGHT, INPUT);" followed by "analogRead(LIGHT);" where LIGHT is a variable which defines which pin the LDR is on.  
### Non-Blocking State Machiene
Normal computers (and human brains) can think about more than one thing at once, but Arduinos (and other microcontrollers) cannot. That means that if you want to do two things at the same time (like blink a light once every 2 seconds and check if a button was pressed), and you do not know which will happen first or when one will happen, you cannot use the delay command. This is because when delay is called, the microcontroller just stops and will not notice if a button is being pressed. The user could wait 2 seconds (1 second light on 1 second light off) before the microcontroller got to the line of code where the button state is being read. This is too slow!

To fix this we use a non-blocking state machiene. This is a simple technique where you replace the delay function with a variable which tells you when an event, like turning the light on or off, should happen. The microcontroller then goes through the loop much faster because it only asks is it time yet? and is the button pushed?. When the desired amount of time has passed, the state of the LED (on or off) is switched and a new time is assigned. Reading the button state (pushed or not pushed) is no longer blocked by blinking the LED.
  
## Soldering The Shield
  
### Materials
  * 3 220 ohm resistors
  * 1 10K ohm resistor
  * 1 RGB LED
  * 1 Light Dependant Resistor (LDR)
  * 1 Button
  * Male pin header
  
### To solder the shield follow these steps:
  1. Solder the 220 ohm resistors to the R-red R-green and R-blue pads.
  2. Solder the 10K ohm resistor on the R-LDR pad
  3. Cut the leads on the LED to 2.5-3mm.
  3. Solder one pad on the LED, making sure that the flat side of the LED matches the flat side on the silkscreen. I usually do the Square pin first.
  4. Align the LED by remelting the solder and moving the LED into place.
  5. Once aligned, solder the other pins on the LED.
  6. Solder cut and solder the pin header.
  7. Solder the LDR so that the leads are long enough that you can bend the sensor away from the LED (if soldered on top) or away from the board if soldered on bottom.
  8. Solder the button.
  
  Note: Some people like to leave the leads long and bend them to hold them in place before soldering. Then they trim them after soldering. If you do this, make sure that the LED has the correct orientation before you start soldering!

### Uploading Code 
* Download the [Arduino software](https://www.arduino.cc/en/Main/Software)
* Select Arduino Uno under Tools > Baord in the Arduino software
* Select the correct comport under Tools > Port in the Arduino software
* Copy the code from the bottom of each video and paste into the Arduino IDE
* Click on the arrow symbol in the Arduino IDE
