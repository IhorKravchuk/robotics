---
layout: post
title: "Variant 3: Radio-Controlled Bot Equipped with a Video Camera"
date: 2009-10-04 05:49:00 -0700
tags: ["early robotics attempts", "computer vision", "rc bot"]
categories: ["early-prototypes"]
original_url: "https://robotics-ingvar-ua.blogspot.com/2009/10/3.html"
---

[← Back to all posts](../index.md)

To achieve autonomy with these prototypes, I needed to write image-processing and self-navigation software.
That required a test robot with a high degree of mobility and the ability to transmit video from an adjustable onboard camera. A standard USB webcam couldn't be used due to USB cable length limits.
Accordingly, I decided to use an analog color PAL camera paired with a video capture card installed in the host PC. I selected a videoconferencing kit consisting of a PAL camera and a BT848-based PCI video capture card. To keep the architecture modular, the camera was modified by replacing its fixed cord with an RJ-45 jack integrated directly into the camera housing.

![Modified PAL camera with integrated RJ-45 jack 1](../assets/images/2009-10-04-variant-3-rc-bot-with-video-camera/sm05.jpg)

![Modified PAL camera with integrated RJ-45 jack 2](../assets/images/2009-10-04-variant-3-rc-bot-with-video-camera/sm07.jpg)

![Camera internals during modification](../assets/images/2009-10-04-variant-3-rc-bot-with-video-camera/sm06.jpg)

Four lines run from the camera to the video capture card: two for power and two for the composite video signal. A 10-meter 4-wire telephone cable was chosen as a test tether. Although it introduced slight image degradation, it gave the robot car plenty of freedom to move around.

![BT848 video capture card and cabling](../assets/images/2009-10-04-variant-3-rc-bot-with-video-camera/sm04.jpg)

The RC car chassis was modified to mount a standard camera tripod head, allowing easy adjustment of the camera's pitch and yaw angles on the vehicle. This resulted in the following setup:

![RC car with tripod-mounted camera 1](../assets/images/2009-10-04-variant-3-rc-bot-with-video-camera/sm02.jpg)

![RC car with tripod-mounted camera 2](../assets/images/2009-10-04-variant-3-rc-bot-with-video-camera/sm03.jpg)

The trials went quite well and yielded valuable insights regarding camera mounting angles, lighting conditions, and the need for additional sensors.

The control software was updated to capture live video and overlay directional arrows on the screen indicating the robot's movement.
I also decided to add joystick support to the control software.
Development of an automatic orientation and fiducial object-recognition system was started to achieve full autonomy, with Variant 3 serving as the primary testbed.

![Control software interface with live video capture](../assets/images/2009-10-04-variant-3-rc-bot-with-video-camera/sm01.jpg)

New control software supporting both joystick and keyboard input was also completed:

![Updated control software with joystick and keyboard support](../assets/images/2009-10-04-variant-3-rc-bot-with-video-camera/sm09.jpg)

---

[← Back to all posts](../index.md)
