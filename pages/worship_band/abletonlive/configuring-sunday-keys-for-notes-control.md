---
title: Preparing Sunday Keys for Ableton for Note Value Control
keywords: [sunday keys, ableton live]
summary: "Step by step instructions to enhance Sunday Keys for MIDI Note Patch selection"
sidebar: main_sidebar
permalink: configuring-sunday-keys-for-notes-control.html
folder: worship_band
toc: true
categories: ableton
---

- Open the original Sunday Keys ALS file.
- Save As a new name.
- Using File Manager (View -> File Manager), click Manage Project and ensure that all external PROJECT files are collected and saved into this project.  **LEAVE FACTORY PACK FILES IN PLACE**
- Enable the IAC Driver bus on your computer.
- Set IAC Driver Preferences in LIVE.  Input = Remote ON.  Output = Track ON.
- Determine in advance what MIDI channel(s) and number of MIDI channels you will use to complete this task.
- Make sure your piano or keyboard is connected and configured for use in LIVE.


## What do we know about the current setup?

Each track contains an instrument rack with 14 chains pre-populated.  The first position in the chain (zero) is empty which is reserved for the OFF setting.  The remaining 13 are pre-configured and ready to use.  There are 27 additional place-holder chains ranging from 14 - 40 that you can use for your custom instruments.  You can add even more than that.

MIDI channels have 127 note values from C - 2 through G8.  This setup reserves a single note value for every instrument chain that you need to be able to switch between.  You have the option of using one MIDI channel, and controlling the chain selectors on all 8 SK Ableton tracks, or you can use more than one MIDI channel.

If you use one MIDI channel, since each track already contains 13 pre-set sounds, and an OFF chain, you have a total of 14 per track * 8 tracks = 112 notes.  With only 127 available on a single channel, this limits your total selection of additional instruments for these 8 tracks combined to 15. (127 - 112 = 15).

If you use TWO MIDI channels, you can split this process in half and setup tracks 1-4 on one channel and 5-8 on another.  This will give you double the amount of 

- Create a new MIDI track.
- Drag it to the left of the Piano 1 track. (arbitrary location)
- Set the MIDI From to your piano.
- Choose Channel 10. (arbitrary, but must be available and not used by any other device)
- 





{% include links.html %}
