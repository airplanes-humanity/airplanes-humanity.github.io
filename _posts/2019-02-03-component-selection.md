---
layout: post
title:  "PCB Design"
date:   2019-02-03
author: Paul George
preview: "/assets/schematics/Main.png"
---

## Overall board design

It was decided to manufacture the boards at the University of Waterloo’s Rapid Prototype Center as this would allow for fast turnaround to debug and create new revisions quickly. To do this, the board would have to comply with the larger tolerances of the Center due to the different manufacturing process (milling).

Components with larger footprints were selected to fit these tolerances. However, the IMUs selected (the BNO055 and BNO080) only come in an LGA-28 footprint which cannot be manufactured at Waterloo. In order to be able to maintain fast turnaround, it was decided to manufacture a separate daughter board for the IMU elsewhere, while the rest of the components were manufactured locally. It was also decided to place the MCU on a daughter board to allow for easier debugging and to allow to swap microcontrollers easily into a pin-compatible socket.

## Main Board

![Motherboard Layout](/assets/schematics/Main.png)

The main board handles power delivery, as well as having sensors and connectors to interface with servos. A fuse is placed in between the lithium polymer battery and the power on switch to be able to deal with short circuits. A linear regulator was used to produce the voltage that powers the sensors and other logic circuitry, while the power rail (that powers the servos) can be run directly from the battery voltage. Electrolytic capacitors are used on both power lines to handle any abrupt changes in voltage.

[Motherboard Schematic](/assets/schematics/Main.pdf)


## IMU Board

![IMU Layout](/assets/schematics/IMU.png)


The IMU circuitry is based on the reference design found in the IMU datasheets. It was then sent to OSH Park to be manufactured with the tighter tolerances required by the LGA-28 package.

[IMU Schematic](/assets/schematics/IMU.pdf)


## MCU Boards

![ATmega Layout](/assets/schematics/ATmega.png)

Two microcontrollers boards were designed: One board for the EFM8 microcontroller, and another for an Atmega328PB (similar to the microcontroller found in the Arduino UNO but with more pins available). This would allow for easier initial development (as there are many more libraries and pins available on the Atmega chip) but would also let users have hardware closer to what we would eventually want to use (the EFM8). Both of the boards are pin compatible with the socket on the main board, allowing for easy on the fly swaps with each other.

[ATmega Schematic](/assets/schematics/ATmega.pdf)
[EFM8 Schematic](/assets/schematics/EFM8.pdf)
