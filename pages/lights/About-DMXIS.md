---
title: About DMXIS
layout: page
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
keywords: DMXIS
summary: Information on the DMXIS lighting control.
permalink: About-DMXIS.html
folder: lights
categories: lighting
---

{% include important.html content="The DMXIS interface and technology has been removed from the system and no longer applies." %}

# Hardware

The [DMXIS](/DMXIS.html) is a hardware interface that connects to the media computer via USB.  It allows transmission of DMX512 protocol data without the need for a dedicated lighting console.  The computer becomes the lighting console.

<p align="center">
<img src="https://github.com/NewValleyChurch/Infrastructure-docs/blob/master/images/dmxis.jpg">
</p>

(_Note: Tactile control of the lights with faders and bank selections can still be achieved with external USB MIDI controllers of which there are many available on the market._)

# Software

[DMXIS](/DMXIS.html) Software controls all of the aspects of the DMX Universe.  The [DMXIS](/DMXIS.html) software can control up to 512 channels of lighting functions.  Each light has one or more channels that can be addressed.

## Standalone Mode

[DMXIS](/DMXIS.html) can be launched independently of any other DAW software.  It can then be mapped to a midi controller, or you can use the mouse to design your lighting scenes.

## Plug-in Mode

[DMXIS](/DMXIS.html) can also be dropped into a DAW, like Ableton Live.  When operating inside of a DAW, the midi mappings are unique to the DAW and are not directly connecting to the [DMXIS](/DMXIS.html) software.  Inside of Ableton, we map functions on the [DMXIS](/DMXIS.html) to Ableton, then we assign those functions to MIDI signals.

**Note: [DMXIS](/DMXIS.html) will only operate in one of those modes at a given time.  The first instance of [DMXIS](/DMXIS.html) that is opened is the one that takes control.  If you open [DMXIS](/DMXIS.html) from the OSX Dock at the bottom of the screen you lose the ability to control the lights with the MIDI mapped faders on the QU-32.**  

**Only ONE instance of [DMXIS](/DMXIS.html) can actually be used, and it's the first one that gets loaded.**
