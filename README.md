# 3D-LED-Cube-using-Arduino-UNO

## Overview
The 3D LED Cube project aims to create an interactive and visually appealing cube using Arduino and 16 LEDs arranged in a 4x4 matrix. The cube will be controlled using an Arduino board, and the LEDs will light up in different patterns, creating visual effects.

### Components:
- Arduino Uno Rev3+USB Cable: 1
- Cardboard: 1
- Blue Light Emitting Diodes (LEDs): 64
- 100 Ohm Resistors: 4
- Arduino Uno power socket adapter: 1
- Jumper wires (Male-Female and Female-Male)
- Vero Board: 1
- Soldering iron and wire: 1
- Pencil+Eraser+Scissor: 1

### Formula for calculation of Resistor value:
R = V/I

## Working
A safe amount of current can only be sent by the microcontroller, in this example an Arduino Uno, before harm is done due to current sourcing limitations on its output pins. It is 40mA in the case of Arduino Uno. Since an LED consumes 20mA, you may be wondering how we can switch on all the lights at once without damaging the Arduino board. This is due to the fact that just one LED is ever on. An LED that is quickly turned on and off cannot be seen by the human eye. Because the code on the Arduino executes so quickly, numerous LEDs appear to be on to our eyes. As just one LED is on at a time and even if we take the average current over one second, it is much below the danger threshold, this also restricts the current to safe levels. To turn on the LED at the bottom left of the cube, for instance, you would send a positive signal from the microcontroller to layer 0, which would result in a positive voltage being sent to the LED's positive pin. Afterward, you must tell the microcontroller to ground the relevant Column pin of that LED; this will link the LED's negative pin to ground, completing a forward-biased circuit that will illuminate the LED.

### Testing the LEDs:
Connect the LED's positive terminal to the Arduino Uno's 3.3V pin and its negative terminal to ground. Alternately, we could use a resistor and connect it to the Arduino 5V pin while grounding the negative pin.

## Construction
- Take a piece of cardboard and put holes the size of an LED into it.
- Insert 16 LEDs in each row to create the 4x4x4 LED Cube.
- Before setting up the LEDs, make sure the cathode, or the negative terminal, of the LED is slightly bent.
- After inserting the LEDs, bend the anode of the LEDs entirely horizontally in the given direction.
- To create your positive layer, bend every LED's positive leg in such a way that it connects to every LED's positive terminal, after this solder it.
- Solder the anode of one LED to the anode of the LED next to it.
- Once the LEDs have been soldered, remove them from the base.
- Connect the four levels once you have all four with you. Place one level on top of the other, and then solder the upper level's cathode to the lower level's equivalent cathode.
- All 16 Level 1 cathodes should be connected to Level 0.
- Complete the cube.

### Hardware Setup
- Use a cube for connecting the wires to the Arduino Uno pins.
- The code is uploaded to the Arduino.
- Then, link the Arduino cable to the device so that you may supply power and analyze the output.

The 3D LED Cube project offers a fun and educational way to explore electronics and programming concepts. By creating visually stunning light patterns, it demonstrates the principles of microcontroller control and LED technology. With its interactive design and customizable patterns, it can serve as an engaging project for hobbyists and students alike.
