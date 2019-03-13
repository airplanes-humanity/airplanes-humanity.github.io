---
layout: post
title:  "Testing Strategy - Custom vs Purchased Glider Body"
date:   2019-03-01
author: Sasha Hall
---

Building our own glider comes with certain timing challenges. There are 2 main components to the glider: the mechanical body and the glider electronics. Each has a design, development, and testing phase. Since certain electronic components depend on a working mechanical system for testing such as controls and system modeling, delays in mechanical work could lead to severe delays in electrical and programming work. We decided the optimal solution was to obtain a working glider body for electrical testing while working on our own mechanical design in parallel.

The selected glider prototype was a Phantom FPV Flying Wing EPO Airplane kit. It's 1.5 m long, which would work as a fair approximation of our own in-house designed glider. It also has components required for remote control, making it easier to test electronic components not directly involved with controlling the RC aircraft such as servos, GPS, IMU (accelerometer, gyroscope, magnetometer), etc. Once these components are all working, autonomy algorithms can be developed to get the RC glider from point A to point B without direction from the ground.

![Phantom FPV Flying Wing EPO Airplane](/assets/RC_Plane.jpg)

Meanwhile, several glider body prototypes could be developed and free-fall tested without any electronic components to test for aerodynamics and structural integrity. For more information about body development, please see our other blog posts.

Once satisfied with the designed body, the tested electronic components could be fitted to it and integrated system testing could begin, testing control algorithms with the new body to ensure smooth flying with the different aerodynamic properties. Once these are updated, the autonomy could be tested as well, hopefully leading us towards a viable product.
