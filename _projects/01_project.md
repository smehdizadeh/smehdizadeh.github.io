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



### More photos ###


