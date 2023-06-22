---
layout: post
title: "Interoceptive Idiophone"
description: An interactive system for interoceptive awareness
---

# An interactive system for interoceptive awareness #

*05/2023*

[![Demo video](/assets/images/Capture_idiophone.jpg)](https://youtu.be/zmnTAz3soPM)

### What is interoception? ###

Interoception, or interoceptive sensing, is the perception of signals internal to the body (from both central and autonomic nervous systems) that may reveal aspects of physiological, cognitive, and emotional state [[1]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8054704/). Examples include one’s ability to perceive their own heart rate, breathing, body temperature, hunger, etc. For the most part (when the body is in homeostasis), interoception is a subconscious process. The act of being consciously aware of and interpreting these internal states/signals is called interoceptive awareness/attention [[1]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8054704/). Ability for interoceptive awareness varies between individuals [[1]](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8054704/), [[2]](https://doi.org/10.1111/j.1469-8986.1981.tb02486.x), [[4]](https://doi.org/10.3389/fpsyg.2018.00798), and it may also fluctuate within individuals, depending on environmental factors/external stimuli, such as stress [[4]](https://doi.org/10.3389/fpsyg.2018.00798). Multiple studies have linked the ability for interoceptive awareness with greater cognitive-affective processing– for example, perception of emotional states [[2]](https://doi.org/10.1111/j.1469-8986.1981.tb02486.x), [[3]](https://doi.org/10.1177/0956797610389191) and emotion regulation [[4]](https://doi.org/10.3389/fpsyg.2018.00798).

### Interoception and interactive systems... ###

Technologies and interactive systems have been developed which aim to guide a user’s interoceptive awareness outside of a clinical setting (some examples: [[5]](https://ieeexplore.ieee.org/abstract/document/10049707?casa_token=nbSnY0fJggcAAAAA:mzeSkasgKCWO2oxGjq34Q-YVIxT5b_Rdva8lFZ78rFQSQo1AnTC7IbjMSKDGXn9z7wAvkNQ), [[6]](https://doi.org/10.1145/3411764.3445137), [[7]](https://doi.org/10.1145/2948910.2948922), [[8]](https://doi.org/10.1145/3139131.3139134)). These systems are typically designed to be accessible, easy to use, and to effectively communicate the signal of interest to the user. My goal was to design and build such a system, which could guide users' interoceptive awareness of their heart rate using sound. I aimed to make the heart rate-to-sound mappings appear intuitive, such that the system could guide users to slow their heart rates and the user felt like they could actually control the system. 

### What are idiophones? ###

Idiophones are a category of self-resonating/"self-sounding" musical instruments-- instruments that produce sound without air columns, membranes, electricity, or strings. Chimes are a type of idiophone. The chime body itself is what vibrates and resonates to produce sound. In this work, I use idiophones (in this case, chimes) as a physical metaphor/representation of humans' internal, yet expressive, physiological rhythms and resonances. From both an interaction-design and artistic perspective, the sound design was a key component of this project. I wanted the system and its sounds to be versatile enough such that it could potentially be "performed" by someone with high interoceptive awareness and accuracy.

![photo1](/assets/images/intero-1.jpg)

### How it works... ###

I manufactured three chimes out of 1/4" thick aluminum rod, carefully cut and tuned such that their resonant frequencies all fit the key of A minor. I then built a wooden frame from which I could suspend the chimes and also mount three mini solenoid motors. The solenoids are positioned such that when they are turned "on" and "off" the pistons will strike the chimes to produce sound.

![photo2](/assets/images/intero-2.jpg)

The solenoid "on" and "off" signals are sent from an Arduino Mega along with a small circuit that I made to power and drive the motors. The timing of these solenoid signals is directly based on the user's heart rate. The user's heart rate is measured from a light-based pulse (PPG) sensor that can be secured to the finger. The PPG signal is sent to the Arduino, which detects the peaks ("pulses") and calculates and updates the heart rate in real time.

![photo3](/assets/images/intero-3.jpg)

The user can start and stop the system using a laptop interface that I designed in MaxMSP. MaxMSP is connected via serial interface to the Arduino. The real-time heart rate is sent from the Arduino to MaxMSP so that it can also be diplayed on the screen for additional visual feedback. After the user puts on the pulse sensor, they can select one of two different "modes" of operation (self guidance or system guidance). The mode selection is sent from MaxMSP to the Arduino. Upon selecting one of the two modes, the user's baseline/starting heart rate is saved so that any subsequent changes in heart rate can be measured against the user's unique baseline.

![photo4](/assets/images/intero-4.jpg)

![photo5](/assets/images/intero-5.jpg)

The two modes offer two different mappings of the heart rate to sound. Under the system guidance mode, the middle chime will always sound at the tempo of the user's heart rate. The right chime will start out by sounding at every fourth strike of the middle chime (4:1 ratio of tempos between middle:right). As the user's heart rate slows down, this tempo ratio will decrease. When the user's heart rate drops by 2%, the right chime will begin sounding at every third strike of the middle chime (3:1 tempo ratio). When the user's heart rate drops by 4%, the right chime will sound at every other strike of the middle chime (2:1 ratio). The "goal" of this mode is for the user to get the middle and right chimes to begin sounding in unison (1:1 ratio), which will happen if they are able to decrease their heart rate by 7% of their baseline/starting heart rate.

Under the self guidance mode, the right chime will always sound at the tempo of the user's heart rate. The other two chimes remain silent to start. Once the user's heart rate drops by 3% the middle chime will begin sounding, forming a 3:2 polyrhythm with the right chime. The "goal" of this mode is for the user to "unlock"/activate all possible layers of the sound (all three chimes), which will happen when their heart rate drops by 5% of their baseline.

### More photos ###


