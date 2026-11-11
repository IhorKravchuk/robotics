---
layout: post
title: "Variant 2: LPT Port Radio Transmitter"
date: 2009-10-04 05:22:00 -0700
tags: ["early robotics attempts", "LPT port", "radio control"]
categories: ["early-prototypes"]
original_url: "https://robotics-ingvar-ua.blogspot.com/2009/10/2-lpt.html"
---

*All the material below was originally written around 2004 and is posted here as backstory.*

In this version of the robot, I decided to integrate the radio control transmitter directly onto the LPT port connector itself, similar to a hardware HASP dongle. Once again, a classic Chinese no-name radio-controlled toy car was used as the base. Its remote control transmitter operated on the same frequency as the previous model and used compatible command signals, making it possible to control both cars with a single unit. The remote control was disassembled, and the transmitter board was carefully extracted.

![RC toy car used for Variant 2](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm02.jpg)

![Extracted RF transmitter board](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm01.jpg)

Next, I found the smallest possible enclosure suitable for plugging directly into an LPT port. The transmitter board, with modified control and power circuits, was mounted inside.

![Compact enclosure for LPT transmitter](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm04.jpg)

![Transmitter board fitted inside enclosure](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm03.jpg)

The stock power source (a 9V battery) was replaced with direct power from the PC's power supply. For this, a custom power cable with a standard PC Molex connector was routed out of the PC case through a modified expansion slot bracket.

An LPT connector, power toggle switch, and status LED were installed in the enclosure, allowing the transmitter to be switched on at any time while the computer is running.

![Power cable and toggle switch assembly](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm05.jpg)

The driver IC (`ULN2803A`) and its supporting components were mounted on a board and wired to the LPT connector and the command inputs of the radio transmitter.

![Driver IC wiring inside the LPT dongle 1](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm06.jpg)

![Driver IC wiring inside the LPT dongle 2](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm08.jpg)

All that remained was to mount the antenna, and the LPT radio transmitter was complete:

![Completed LPT radio transmitter dongle](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm07.jpg)

Testing showed how easy it was to plug into any PC case, as well as its compactness and convenience when operating both RC car models.

![LPT radio transmitter plugged into the back of a PC](../assets/images/2009-10-04-variant-2-lpt-port-radio-transmitter/sm09.jpg)

No software changes were needed at this stage, as the existing control program was fully compatible with both transmitter variants.
The next step in evolving this setup was mounting a video camera onto the vehicle.
