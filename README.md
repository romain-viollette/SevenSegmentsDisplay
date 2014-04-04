SevenSegmentsDisplay
====================

description: Autonomous 3 seven-segments display powered by an Atmega328P.

author: Romain VIOLLETTE romain.viollette@gmail.com

https://github.com/romain-viollette/SevenSegmentsDisplay

http://www.oshpark.com/profiles/RomainViollette


features:
  - small form factor
  - communication: Serial, I2C, SPI, (bitbanging possible if you want to) 
  - SDM components, soldering by hand is not too difficult.
  - 5 volts only
  - Arduino IDE compatible
  - programmable via ISP by default (or maybe via serial lines with a different bootloader)
  - crystal 16Mhz, 20MHz (or whatever or internal if you want to) 
  - 2 support holes for 3 mm screws
  
  
partlist: (See complete file in /version_xx/partlist.txt)
  - PCB at OSHpark.com see http://www.oshpark.com/profiles/RomainViollette
  - 3 x TDSO 5151 - Seven Segments displays with common anode (any common anode 7 seg display would fit)
  - 2 leds, any basic ones would fit, adapt R5 and R6 for current limiting.
  - SMD discrete parts form factor 0805:
      - C1 & C3 - 100nF - unpolarized decoupling capacitor
      - C4 & C5 - 12-22pF - unpolarized capacitor for quartz
      - ATMEGA328P-AU - TQFP32 - http://bit.ly/1gV6cmJ
      - QUARTZ - MULTICOMP HC49SM-20-30-50-60-16-ATF - http://bit.ly/1i76kLW
      - R2, R3 & R4 - 150 Ohms - current limiting resistor for 7 seg displays (adapt them to your display specs)
      - R5 & R6 - 150-2200 Ohms  - current limiting resistor for LED (adapt them to your LED specs)
      - R1 - !!!ERROR!!! - do not put anything - R1 could be used as a reset switch (I set R1 as pulldown instead of pullup)
	  
notice:
	- If you beggin in SMD, consider buying http://bit.ly/1ikUmQc and the equivalent for capacitor: you  will save a lot of money at the end.
	- R1 is wrong, see in Partlist.
	- Connectors should be placed on the same side than led display. If you want to put the connector on the other side like I did in the photos (http://bit.ly/1hbSIUK), keep in mind that the pinning is inverted.
	- There is not power regulator, nor overvoltage protection, so nerver power with more than 5V. (Maybe 3.3 could works?).
 
