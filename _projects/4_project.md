---
layout: post
title: Adaptive Filtering
description: Prototype of a real-time adaptive speaker system
---

**Created by:** Sophia Mehdizadeh, Socrates Papageorgiou, Abdulrahman Shehadeh, and Jack Nonnenmacher

*University of Michigan Electrical Engineering senior capstone design project*

![High level diagram](/assets/images/Capture_AdaptiveSpeakers.JPG)

*04/2018*

### About the project ###

EECS 452 is the digital signal processing design lab senior capstone course. For our project, my team decided to make a real-time adaptive speaker system. The prototype used a Raspberry Pi 3 and two STM32 Nucleo microprocessors running a custom C algorithm to analyze the frequency characteristics of room-affected audio and apply a filter to negate these unwanted effects. We were able to create a completely modular system that allowed users to connect their own speakers and microphone, as well as control the processing via a mobile application that could be downloaded to their own device.

![App and signal flow](/assets/images/Capture_AdaptiveApp.JPG)

I mainly worked on designing prototypes of the adaptive filtering algorithm and noise floor algorthm in MATLAB. I then moved on to developing and debugging the communication protocol between the Raspberry Pi and STM32 Nucleo boards. My team and I regularly communicated our progress to our professors through reports and presentations. Our final deliverables included a project poster and IEEE-style technical paper.

The Adaptive Speaker system was demo-ed during the College of Engineering Design Expo.

![Design Expo](/assets/images/DesignExpo.jpg)
