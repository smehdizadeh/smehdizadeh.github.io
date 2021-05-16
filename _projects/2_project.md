---
layout: post
title: Kool Edit 2020
description: An easy-to-use audio WAV editor made using JUCE
---

**Created by:** Sophia Mehdizadeh, Sandeep Dasari, Yilin Zhang, and Yanchao Liu

*Inspired by [Cool Edit Pro](https://www.techspot.com/downloads/327-cool-edit-pro.html), made using [JUCE](https://juce.com/)*

![Kool Edit 2020](/assets/images/koolEdit2020_logo.png)

*04/2020*

### About the project ###

*Kool Edit 2020* is the result of a semester-long final project for MUSI 6106, a graduate-level audio software engineering course offered through the Music Technology department at Georgia Tech. Our aim was to build a standalone application with audio editing and playback capabilities that was responsive/lightweight, and had an intuitive GUI. We created the application using C++ and JUCE libraries, and as a team utilized an agile/scrum workflow.

[Download and install on GitHub!](https://github.com/sandcobainer/KoolEdit2020)

![Kool Edit screenshot](/assets/images/Capture_KoolEdit.JPG)

### Software features ###

- Compatible on Windows, macOS, and Linux

Playback and visualization:

- Load any WAV file via a file browser
- Audio waveform and spectrogram visualization with time markers
- Zoom in/out
- Play, pause, stop, skip/rewind
- Select portion of waveform by clicking and dragging (I-beam cursor)
- Click and drag on your selection to slide it around (arrow cursor)
- Click anyware on the waveform to disable a selection
- Toggle looping on/off (will loop entire track if no selection enabled)

Editing:

*Note: if no selection is enabled, the following will apply to the entire track*

- Use the editing buttons on the second row of the toolbar, or right click on the waveform
- Mute/silence (does not change length of track)
- Delete (will reduce length of track)
- Cut, copy, paste, or insert
- Fade in/out
- Normalize
- Undo/redo capability
- Save your changes as a new file
