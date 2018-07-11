---
title: "How To Set The Thermostats"
layout: page
comments: true
permalink: how-to-set-the-thermostats.html
categories: building
toc: false
search: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
summary: "A brief overview of how and when to control the thermostats."
---

{% include important.html content="The ultimate goal is to automate the climate control system to synchronize with the schedule of events at New Valley Church.  At some point, we won't need to manually control the thermostats." %}

[Facilities Map](thermostats.html)

## Non-WIFI Thermostats

Standard control applies.  Simply use the thermostat to set the temperature and/or program the schedule.

## WIFI Thermostats

Nobody likes walking around the room adjusting each thermostat individually.  There are currently 7 WIFI thermostats that can be controlled through a web or mobile interface.

### How to Control The WIFI Thermostats

- Point your browser to http://72.216.245.116:8123/lovelace and login.  Password is not disclosed on this site.
- Once you're logged in, find the `Climate Control` tab at the top and click or tap it.

![](images/climate-control-1.jpg)

- You will see a page with Thermostat Settings.

![](images/thermostat-settings-1.jpg)

{% include note.html content="At present, only 5 of the 7 WIFI controls are visible, along with two additional settings.  One setting is to change all thermostats at the same time, and the other setting tells the thermostats how long to hold that temperature before returning to regular climate control schedules." %}

#### Sanctuary Thermostats

- You can either adjust individual A/C units in the Sanctuary, or you can adjust all of them at the same time.
- Choose the length of time to hold the temperature you're about to set.
- Set each A/C unit, or set the master and all other thermostats will follow.

Within moments, you should experience a result.  The settings you just adjusted were sent through Home Assistant, to Honeywell's MyTotalConnectComfort.com control center, and back to the thermostats.
