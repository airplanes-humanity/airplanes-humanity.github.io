---
layout: post
title:  "Arduino Prototype"
date:   2019-02-20
cover:  "/assets/SoftwareCover.jpg"
author: Kiran Rao
---

In order to expedite the software development, we will be testing using an Arduino Prototype. That way, we can interface with sensors before moving to the custom PCB.

## Protoshield

![Protoshield Schematic](/assets/Protoshield.jpg)

We will be using a protoshield for our prototyping with the Arduino. Protoshields also allow us to:
 - Keep cables organized
 - Ensure components are securely attached while remaining modular
 - Keep the IMU upright and stable

## Sensor Testing

Sensor testing was fairly straightforward. Adafruit provides drivers for all their breakout boards, as well as example code.

### IMU

The IMU worked flawlessly. It is able to output the exact orientation with no drift.

![IMU Serial Output](/assets/IMUSignal.png)


### GPS

The GPS had several unexpected issues. The GPS was unable to locate a satellite signal whenever indoors. It will therefore be much more difficult to test.

![GPS Serial with No Signal](/assets/GPSNoSignal.png)

Once outside, the GPS took about 1 minute to locate a satellite. This was far longer than the expected 5 seconds. To resolve this, we can use a coin cell battery to maintain a real time clock. This dropped the time to lock, but we were still unable to locate satellites indoors.
