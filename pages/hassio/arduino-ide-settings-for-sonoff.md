---
title: "Arduino IDE Settings for Sonoff Switches"
layout: page
toc: false
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
permalink: arduino-ide-settings-for-sonoff.html
categories: automation
summary: "Sonoff WIFI Switches and Relays"
---

New Valley has installed WIFI switches in various locations throughout the building.  These are in-line switches that can either be hidden behind the wall, or found directly between the wall-outlet and a plugged in device.

Each of these is flashed using the Arduino IDE Utility with specific code and the following settings in Arduino IDE Tools:

- Board: Generic ESP8266 Module
- Flash Mode: "DOUT"
- Flash Size: "1m (no SPIFFS)"
- Debug Port: "Disabled"
- Debug Level: "None"
- IwIP Variant: "v2 Lower Memory"
- Reset Method: "nodemcu"
- Crystal Frequency: "26 MHz"
- Flash Frequency: "40MHz"
- CPU Frequency: "80 MHz"
- Builtin Led: "2"
- Upload Speed: "115200"
- Erase Flash: "All Flash Contents"
- Port: "COM[X]" whichever lights up when you connect the device.