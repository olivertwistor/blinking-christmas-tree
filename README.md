# Blinking Christmas Tree
**Update 2024-08-30:** I don't have the necessary equipment to compile and develop this project on hardware anymore, so I'll just leave this repository up as a public archive. Feel free to clone it and do something fun and exciting!

This is a program for a blinking Christmas tree encoded onto an ATmega88 microchip. The Christmas tree offers four light patterns for eleven LEDs, controlled by a variator.

In 2013, I built this Christmas tree as a gift for a friend. She later discovered a bug relating to switching between light patterns. Unfortunately, I couldn't fix it for her, because my design didn't include a USB port and I didn't want to tear apart the whole tree to get to the microchip. A lesson learned; to always design a way to update the code. It was so long ago she discovered the bug so I don't remember how to reproduce it.

## Installation
It was a long time ago I built this, and my memory is vague around how. However, I can say that the source code must be compiled into a HEX file (using [Atmel Studio][2] for example) and written to ATmega88's EEPROM.

### Hardware
Component | Value(s) | Comments
:--- | :---: | :---
1x [ATmega88 microchip][1] | |
1x battery | 9&nbsp;V | Will power both the ATmega88 and the LEDs.
1x four-state variator | |
11x LEDs | ? | The colour(s) of your choice.
Material in the form of a Christmas tree | | Plastic or other non-conducting material on which to attach the LEDs and resistors
[Perfboard][4] | | To hold all the components except the LEDs and their resistors.
1x resistor | 1.4&nbsp;kΩ&ndash;2.6&nbsp;kΩ | For the ATmega88 microchip's power supply, since the maximum operating voltage is 2.7&nbsp;V&ndash;5.5&nbsp;V.
11x resistors | ? | Resistance dependent on the configuration; the goal is to not fry the LEDs.
Wires | | To connect the components.

Since microchips and LEDs are very sensitive things, please make sure that you do your own calculations and research for which resistors you need. Do not rely solely on what I have written here. That is from my hazy memory, after all. :wink:

In future updates to this project, I will probably take the time to design schematics detailing the exact values for all components and how to connect them.

### Software
* [Atmel Studio][2] (or any other compiler capable to write the C source code onto the ATmega88's EEPROM)
* [TinyCAD][3] (for reading the schematics; note that no schematics are available at this time)

## Usage
When the hardware is connected, and the software has been written to ATmega88's EEPROM, the user can choose between light patterns on the LEDs, using the variator. To stop the Christmas tree from emitting light, the user has to remove or unplug the battery.

## Licenses
This application is distributed under an *MIT License*. For detailed license terms, please read [LICENSE][5].

[1]: http://www.microchip.com/wwwproducts/en/ATmega88
[2]: https://www.microchip.com/mplab/avr-support/atmel-studio-7
[3]: https://sourceforge.net/projects/tinycad/
[4]: https://en.wikipedia.org/wiki/Perfboard
[5]: LICENSE
