# Multiplexed RGB LED Shield
## Introduction
The Multiplexed RGB Shield contains 24 RGB LEDs in a 4x6 matrix and plugs into an Arduino Uno. By controling the state of the pins all LEDs can be individually turned on or off and their colors can be controled.

## Theory
To understand how multiplexing works, it is easiest to start with the theory for a single color multiplexed matrix: 

<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/jLnLXc81mwI?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>
  
  Multiplexing with RGB leds is basically the same as monocrome multiplexing with some small differences:
  <iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/jQYGCGH9bMM?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>
  
## Soldering The Shield
  <iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/OaYhBevXBYk?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>
  
### Materials
  * 12 resistors
  * 24 RGB LEDs
  * male pin header
  
### To solder the shield follow these steps:
  1. Solder the resistors.
  2. Cut the leads on all of the LEDs to 2.5-3mm.
  3. Solder 1 side of each of the LEDs, making sure that the flat side of the LED matches the flat side on the silkscreen. I usually do the Square pin first.
  4. Align the LEDs by remelting the solder and moving the LED into place.
  5. Once aligned, solder the other pins on the LEDs. 
  6. Solder cut and solder the pin header.
  
    Note: Some people like to leave the leads long and bend them to hold them inplace before soldering. Then they trim them after soldering. This is not reccomended for this project because it makes alignment and replacement of LEDs difficult or impossible. 

### Building the Case
1. Glue all sides of the case together except the one with the connector for the arduino (the one with hammes hacks engraved in it). 
2. Wait for glue to dry. Rubberbands can be used to hold the case together while it drys). 
3. Plug the shield into the Arduino. 
4. Slide the shield and arduino into the case.
6. Place transparent plastic between the arduino shield and the top of the case. 
7. Close the case. Friction and the cablesshould hold the unglued side in place. 

### Uploading Code 
<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/ZdOZB8iYkNo?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>
<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/RqE0sPx6IlQ?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>

* Download the [Arduino software](https://www.arduino.cc/en/Main/Software)
* Select Arduino Uno under Tools>Baord in the arduino software
* Select the correct comport under Toold>Port in the arduino software
* Download the code [from github](https://github.com/emilyhammes/8x7charlieplexed/archive/master.zip) and upload it to the Arduino.
