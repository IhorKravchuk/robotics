---
layout: post
title: "First Attempts: The Prototype"
date: 2009-10-04 04:28:00 -0700
tags: ["early robotics attempts", "prototype", "ULN2803A", "LPT port"]
categories: ["early-prototypes"]
original_url: "https://robotics-ingvar-ua.blogspot.com/2009/10/blog-post.html"
---

*All the material below was originally written around 2004 and is posted here as backstory.*

**In the beginning, there was an idea…**

One day, while playing a flight simulator, a thought crossed my mind: *"Wouldn't it be great to sit in front of the PC and use a joystick to control a REAL model airplane… or at least a car…"*
Getting a toy car wasn't a problem, and I already had a computer—all that remained was to connect the two. The LPT (parallel) port was chosen as the interface because it is the simplest port for building custom hardware interfaces. Controlling external devices from an LPT port only requires buffering the port pins using simple transistor switches.

##### The Prototype

Soldering arrays of discrete transistors is tedious and takes up a lot of space. After a brief search, I settled on the `ULN2803A` Darlington transistor array IC. This chip has excellent current-handling capabilities, allowing it to sink relatively high currents directly. This meant it could be wired directly into the control circuits of standard radio-controlled toys without needing bulky electromagnetic relays—making it possible to integrate the interface into almost any handheld remote control.

First, to verify the concept, a test circuit was assembled on a breadboard using LEDs and 12V electromagnetic relays as test loads.

![Breadboard prototype with ULN2803A and relays 1]({{ '/assets/images/2009-10-04-first-attempts-prototype/sm3.jpg' | relative_url }})

![Breadboard prototype with ULN2803A and relays 2]({{ '/assets/images/2009-10-04-first-attempts-prototype/sm2.jpg' | relative_url }})

![LPT interface test setup]({{ '/assets/images/2009-10-04-first-attempts-prototype/sm1.jpg' | relative_url }})

This circuit lived up to every expectation.
It reliably drove both electromagnetic relays and DC motor power circuits directly.
In parallel, a Windows program was developed to control the LPT port. Working under Windows 2000 posed a particular challenge because the OS blocks user-space applications from accessing hardware I/O ports directly. After some searching online, I found the `IO.DLL` library, which enables direct hardware port access under Windows 2000/XP. This library formed the foundation of our control software.
