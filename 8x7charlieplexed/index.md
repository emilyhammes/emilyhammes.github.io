# 8x7 Charlieplexed LED Shield
## Introduction
The 8x7 Charlieplexed Shield contains 56 LEDs in a 8x7 matrix and plugs into 8 adjacent pins on a microcontroller such as an Arduino Pro Mini or an Arduino Nano. By controlling the state of the pins all LEDs can be individually turned on or off.

## Theory
<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/Bx5GLyJSWPk?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>

## Soldering The Shield
<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/YMQ2k3mRRPE?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>
  
### Materials
  * 8 resistors
  * 56 LEDs
  * 8 pin female pin header
  
### To solder the shield follow these steps:
  1. Solder the resistors.
  2. Cut the leads on all of the LEDs to 2.5-3mm.
  3. Solder 1 side of each of the LEDs, making sure that the flat side of the LED matches the flat side on the silkscreen.
  4. Align the LEDs by remelting the solder and moving the LED into place.
  5. Once aligned, solder the other side of the LEDs. 
  6. Solder the female pin header.
  
    Note: Some people like to leave the leads long and bend them to hold them in place before soldering. Then they trim them after soldering. This is not recommended for this project because it makes alignment and replacement of LEDs difficult or impossible. 
    
## The Laser Cut Case 
### Soldering the Arduino Nano
1. Solder the pin headers onto the Arduino Nano so that the pins point up on the same side as the USB. 

Note: this is the opposite side to what is normally shown on the internet.

### Building the Case
1.	Glue the front and sides together leaving the back panel unglued. It is often useful to use the back to make sure all parts are aligned, but be very careful not to get glue on the back panel!
2.	Wait for glue to dry.
3.	Once glue is dry, place the offset angles into the case.
4.	Plug pins 2-9 of the Arduino into the shield.
5.	Place the shield and Arduino into the case.
6.	Assemble the T-shaped offset, and place it into the case.
7.	Close the case. Friction should hold the back in place.

### Uploading Code for Snakes
<iframe id="ytplayer" type="text/html" width="640" height="360"
  src="https://www.youtube.com/embed/YZnQFtUXSJo?autoplay=0&origin=http://hammeshacks.com"
  frameborder="0"></iframe>

* Download the [Arduino software](https://www.arduino.cc/en/Main/Software)
* Select Arduino Nano under Tools > Baord in the Arduino software
* Select the correct comport under Tools > Port in the Arduino software
* Download the code [from github](https://github.com/emilyhammes/8x7charlieplexed/archive/master.zip) and upload it to the Arduino.
