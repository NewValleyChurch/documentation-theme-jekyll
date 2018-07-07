---
title: OSC Reference for DMXIS
layout: page
categories: general
permalink: osc-reference-for-dmxis.html
toc: false
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
---

The following OSC Reference can be found on page 35 of the DMXIS.pdf file that's loaded from the Help menu from within DMXIS.  Surprisingly, I couldn't find it anywhere on the webbernets, so here it is.

## General

| Command | Trasmit (TX) or Receive (RX) | Description |
|---|---|---|
| /dmxis/master [level] - [level] = float from 0.0 to 1.0 | TX+RX | Sets the master level, e.g. /dmxis/master "0.35" |
| /dmxis/master/label [string] - [string] = the current master level represented as a percentage.|TX|A string representing the master level. e.g. /dmxis/master/label "35.1%"|
|/dmxis/tempo [tempo]
[tempo] = float representing tempo (e.g. 120.0 = 120bpm)|TX+RX|Sets the master tempo. Note this is overriden by any MIDI clock signal.
e.g. /dmxis/tempo “145”|

## Tap Tempo

|Command|Transmit (TX) or Receive (RX)|Description|
|---|---|---|
|/dmxis/tap|RX|When received, the DMXIS master tempo will synchronize to the timing of these commands.|
|/dmxis/resync|RC|When received, the DMXIS oscillators will restart. Use this to manually resync your oscillators effects if they drift during a performance.|

## Direct Control

|Command|Transmit (TX) or Receive (RX)|Description|
|---|---|---|
|/dmxis/ch/x [level] x = DMXIS channel number (1-512) [level] = float representing the channel level (0.0-1.0)|TX+RX|Sets a single DMX channel fader to the specified level.|
|/dmxis/ch/list [level] list = a list of DMXIS channel number (1-512) separated by forward slashes [level] = float representing the channel level (0.0-1.0)|RX|Sets a list of channels to a single value. Allows you to control many DMXIS faders with one OSC slider. e.g. /dmxis/ch/1/3/12/24 0.3 (set DMXIS channels 1, 3, 12 and 14 to 0.3)|
|/dmxis/ch/list [levels] list = a list of DMXIS channel number (1-512) separated by forward slashes [levels] = a list of floats (0.0-1.0) representing the level of each channel defined in list.|RX|Sets a list of channels to individual values. This is useful for OSC controls which transmit multiple values (e.g. XY Pads in TouchOSC) e.g. /dmxis/ch/10/20 0.2 0.4 (set channel 10 to 0.3 and channel 20 to 0.4)|
|/dmxis/ch/val/x [string] x = DMXIS channel number (1-512) [string] = a string representing the current channel value.|TX|Sends a readable string representing the current DMX channel value. This will be identical to the value displayed on the DMXIS fader (i.e. if a fixture definition is loaded, sensible labels like “Red”, “Gobo 3”, Dim 50%” etc will be sent).|
|/dmxis/ch/name/x [string] x = DMXIS channel number (1-512) [string] = a string representing the current channel name|TX|Sends the name of the specified channel, as specified in the fixture definition (e.g. “Dimmer”, “Gobo”)|
