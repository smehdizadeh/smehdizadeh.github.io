---
layout: post
title: Theremin Bot
description: A Theremin-playing robotic musician
---

**Created by:** Sophia Mehdizadeh and Neha Rajagopalan

[![Video coming soon]()

*04/2022*

### What is the Theremin? ###

<img src="/assets/images/rockmore.jpg" width="365" height="247">

*Thereminist Clara Rockmore (from WNYC.org)*


The Theremin is an electronic musical instrument first developed around the 1930s. It has two RF oscillators and antennas that are affected by the proximity of the thereminist’s hands. One antenna controls the volume of the sound and the other controls the pitch of the sound, resulting in a smooth, ghostly tone.

The thereminist hovers their hands near the antennas, making minute and precise learned movements in space to play the instrument. Unlike more traditional instruments like the violin or the trombone, the thereminist does not rely on any tactile feedback from the instrument. This makes the Theremin a notoriously difficult instrument for humans to learn, which is why we thought it is the perfect instrument for a robotic musician!

### About the project ###

Our Theremin-playing robot (nicknamed "Terry") is the result of a semester-long final project for the Music Technology special topics course Robotic Musicianship. Robotic musicians are not just robots that are designed to play an instrument but they may also embody traits of human musicians, such as expressivity, improvisation, and group collaboration and communication with other robotic or human musicians.

![System Diagram](/assets/images/Terry_Diagram.jpg)

Our aim was to design, build, and perform with a Theremin-playing robot that was embedded within a biofeedback loop. Human input (physiological signals) is mapped to the Terry's playing style (staccato or legato notes); what Terry plays may then influence the physiology of the human collaborator. In the current implementation, we use EMG (muscle activity) from two sites on the face to capture the human collaborator's facial expression/emotion. This directly controls Terry's playing style, while the notes and timings themselves are pre-composed and streamed to Terry live as MIDI over Ethernet. In future work, we would like to expand the biofeedback implementation to include EEG (brainwaves) and map these signals to real-time music generation algorithms.

### Technical details ###

We first designed the structure for the robot in CAD (Solidworks) and then constructed it by hand using basic shop tools and 3D printers at Georgia Tech's [Invention Studio](https://inventionstudio.gatech.edu/). The [OpenBCI](https://openbci.com/) platform was used for recording physiological signals, which we then streamed to [MaxMSP](https://cycling74.com/products/max) through Open Sound Control (OSC) protocol. We streamed MIDI notes as well as play style commands calculated from the incoming EMG data from MaxMSP to Terry's on-board Raspberry Pi via Ethernet. Python code running on the Raspberry Pi translated these notes and commands to motor positions and PID settings. Two [Dynamixel](https://emanual.robotis.com/docs/en/dxl/x/xl430-w250/) servo motors were tuned and used for Terry's pitch and volume arms.

### Challenges ###

The relationship between sound frequency and distance between the thereminist's hand and the pitch antenna is non-linear. Furthermore, the Theremin's antennas are known to be highly sensitive to environmental variables such as humidity, room size, and number of surrounding objects/people. This means that the Theremin's tuning and pitch characteristics may vary significantly day to day, or if the instrument is moved to a new space. The hand positioning you use to play a melody must be adjusted, or it may even be impossible to play if the frequency output of the instrument has been significantly compromised. For a robotic musician with no real-time pitch detection, this presents a big problem.

We needed to implement a quick, efficient way of tuning the system prior to a performance. We researched [other thereminist robots](https://ieeexplore.ieee.org/document/5723333) that had been developed by other research groups, and were able to implement the parametric tuning model presented by [Mizumoto et al. (2009)](https://ieeexplore.ieee.org/document/5354473). This greatly increased Terry's performance and ability to play more than an octave in tune! See the video above to hear Terry in action, and check out the parametric tuning MATLAB script, EMG and MIDI Max patch, and Python code on the project's GitHub.

[View the project on GitHub](https://github.com/smehdizadeh/ThereminBot)

### More photos ###

![design progress](/assets/images/terry1.jpg)
![construction progress](/assets/images/terry2.jpg)
![3d prints](/assets/images/terry3.jpg)
