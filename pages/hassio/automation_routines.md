---
title: 'Automation Routines'
layout: page
permalink: automation-routines.html
toc: true
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
categories: [automation, hassio]
summary: "A basic overview of the automation routines that are currently active at New Valley Church Chandler."
---

The following are the currently configured automations.

{% include note.html content="Conditions must be true for an automation to run.  If the condition is not true, the automation will stop." %}

# Lights

1. House lights automatically turn on when motion is detected.
  - **Name**: "House Lights On Motion"
  - **Trigger**: Motion sensor. 
  - **Conditions**:  Lights must be off, and light sensor level above sanctuary center doors must not exceed 40 LUX.
  - **Action**: Script runs - `script.house_lights_on`
  - **Sensor Location**: Above the Exit sign, center doors, at the back of the sanctuary.  Sensor tracks light level, motion, humidity, and temperature.

2. A timer begins to countdown when the lights are triggered.
  - **Name**: "Start House Lights Timer"  
  - **Trigger**: When the house lights are turned on manually or automatically.
  - **Conditions**: No conditions.
  - **Action**: Script runs - `script.house_lights_timer`
  - **Timer Length**: The length of the timer can be set with an input slider from the dashboard.
  - **Purpose**: Facilitate automatic light shut-off when the timer runs out if certain conditions are met.  

3. Automatic Timer Restart.  
  - **Name**: "Restart House Lights Timer" 
  - **Trigger**: Motion sensor.
  - **Condition**: The house lights timer must already be running.
  - **Action**: Script runs - `script.house_lights_timer`.  Timers that are triggered while they're already running simply restart.
  - **Purpose**: We don't want the house lights to turn off inadvertently.  This restarts the timer if motion is sensed during the countdown.

4. House lights automatically turn off when timer expires.
  - **Name**: "House Lights Timer Expired"  
  - **Trigger**: House lights timer expires.
  - **Conditions**: No conditions.
  - **Action**: Script runs - `script.house_lights_off`

  {% include note.html content="The action script in this automation contains a condition that prevents the lights from being shut off if the system detects that someone is still in the building." %}

5. Shut off house lights if nobody is in the building.
  - **Name**: "House Lights Timer Start When Nobody Home"
  - **Trigger**: When the system detects that all registered tracking devices are no longer connected to the WIFI network.
  - **Conditions**: House lights must already be on.
  - **Action**: Script runs `script.house_lights_timer`

# HVAC / Air Conditioning System

1. Set Thermostat Timer to 5 Hours for Sunday Morning
  - **Name**: "Set Thermostat Timer to 5 Hours"
  - **Trigger**: Time.  At one second past midnight.
  - **Conditions**: Only happens on Sunday
  - **Action**: Sets the input slider for the thermostat timer to 5.

2. Start Thermostat Timer
  - **Name**: "Start Thermostat Timer"
  - **Trigger**: Any time the master Sanctuary input slider is adjusted.
  - **Conditions**: None.
  - **Actions**: Script runs `script.thermostat_timer`

