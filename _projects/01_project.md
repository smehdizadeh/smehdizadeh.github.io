---
layout: post
title: "Interoceptive Idiophone"
description: An interactive system for interoceptive awareness
---

# An interactive system for interoceptive awareness #

*05/2023*

[![Demo video](/assets/images/Capture_idiophone.jpg)](https://youtu.be/zmnTAz3soPM)

### About the hackathon ###

*Syngeneia* was an interactive sound installation designed and built for the 2023 [SynthUX hackathon](https://www.synthux.academy/events/hackathon-2023).
Teams had four days to design, build, and document a project inspired by this year's theme of "acoustic bytes and artificial nature." For our project, we selected
the sub-prompt "a habitat for coexistence."

### About the project ###

Syngeneia uses two spring-mounted controllers, each with an embedded gyroscope/accelerometer to measure motion, a pulse sensor, and three copper-tape electrodes used to measure galvanic skin response (GSR). The same electrodes are used to determine if the two performers are in contact with each other. Sensor data is amplified by our prototyped circuitry and is read by an Arduino Nano. The motion of each controller, individual heart rates, heart rate similarity, individual GSR, and physical contact are all parameters that are used within MaxMSP to influence both synthesizer parameters and rule-based generative algorithms for the notes played.

![diagram](/assets/images/Syngeneia_diagram.png)

The sound is produced using BEAP synthesizer modules in MaxMSP. We connected and programmed modules to create a modulating drone sound and two melodies (one for each user). All sensor data from the controllers is sent by the Arduino to MaxMSP. Within the Max patch, the control signals are mapped to parameters of the drone (pitches, amplitude, and timbre) and/or parameters of the melodies (rules for melody generation and timbre).

![maxpatch](/assets/images/syngeneia_max.png)

Check out the more detailed, full-length video [here!](https://youtu.be/eGP5dM2umB0)

### More photos ###

![syngeneia1](/assets/images/syngeneia1.png)

![syngeneia2](/assets/images/syngeneia2.png)
