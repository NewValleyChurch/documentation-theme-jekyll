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

1. Set Sanctuary Thermostat when Jon's iPhone is detected in the building.  
  - **Name**: "Set Thermostat iPhone"
  - **Trigger:** State.  The state of the device.  Either `home` or `away`.  When the state changes `to` the value `home`.
  - **Condition**: No conditions.
  - **Action**: Set the main Sanctuary A/C input value to 73.

1. Set Thermostat Timer to 6 Hours for Sunday Morning  
  - **Name**: "Set Thermostat Timer to 6 Hours"
  - **Trigger**: Time.  At one second past midnight.
  - **Conditions**: Only happens on Sunday
  - **Action**: Sets the input slider for the thermostat timer to 6 for the following morning's service activities.

1. Start Thermostat Timer
  - **Name**: "Start Thermostat Timer"
  - **Trigger**: Any time the master Sanctuary input slider is adjusted.
  - **Conditions**: None.
  - **Actions**: Script runs `script.thermostat_timer`
  - **Purpose**: To start a countdown timer for the A/C system shut-down routine.

1. Track Thermostat timer Expiration
  - **Name:**: "Thermostat Timer Expired"
  - **Trigger**: When the timer `timer.thermostat_timer` reaches zero.
  - **Condition**: Any day but Sunday (Day 6 when counting from zero to 6)
  - **Action**: Run Script.  `script.reset_thermostats`
  - **Purpose**: To make sure that the A/C isn't running when nobody is here.

1. Reset Thermostats every Day Except Sunday
  - **Name:** Reset Thermostats Daily
  - **Trigger**: 10PM.
  - **Condition**: Every day but Sunday.
  - **Action**: Reset the thermostats to the default value.
  - **Purpose**: To ensure that the units are set to the default value every day.

1. Start Thermostat timer automatically when nobody is here.
  - **Name**: "Thermostat timer Start When Nobody Home"
  - **Trigger**: When the system detects that all registered devices are no longer in the building.  Dependent up on whether or not someone's phone has been added to the system.
  - **Condition**: Only happens if the Main Sanctuary Thermostat setting isn't already 85.
  - **Action**: Script runs.  `script.thermostat_timer`.
  - **Purpose**: To ensure that the A/C will be reset to default values when the timer reaches zero.  In order for that to happen, the timer must be running, so this automation ensures the timer starts for a full cycle.

1. Sunday Morning Cooldown
  - **Name**: "Sunday Morning Cooldown"
  - **Trigger**: There are two triggers.  
      - Trigger 1: 6AM in the morning.
      - Trigger 2: When the system detects that someone is in the building through mobile device tracking.  
  - **Condition**: It must be Sunday.  
  - **Action**: Two scripts.  
      - Script 1: `script.sunday_morning_ac`
      - Script 2: `script.thermostat_timer`  
  - **Purpose**: To ensure that we have adequate cooling for the duration of rehearsal and both services on Sunday morning.

1. Set Sanctuary AC Level
  - **Trigger**: Manual input of the Sanctuary Master A/C temperature slider.
  - **Condition**: No conditions.
  - **Action**: When the value is changed, two scripts are run.
      - Script 1: Set all sanctuary thermostats to the same level as the input value selected. `script.set_all_sanctuary_thermostats`  
      - Script 2: Start the thermostat countdown timer.  `script.thermostat_timer.`  
  - **Purpose**: A single control to set all 5 of the thermostats rather than setting each one.

1. The following 7 automations are what run when the temperature settings are adjusted in Home Assistant.
  - Sanctuary NE
  - Sanctuary N1
  - Sanctuary N2
  - Sanctuary SE
  - Sanctuary W
  - Living Room
  - Main Foyer
  - **Trigger**: When the main sanctuary input number is changed.
  - **Action**: The temperature setting is transmitted to IFTTT and then to MyTotalComfortConnect.com for EACH thermostat.  MyTotalComfortConnect.com then remotely sets the thermostats in the building.

