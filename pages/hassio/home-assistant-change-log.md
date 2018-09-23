---
title: Home Assistant Change Log
layout: page
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
permalink: home-assistant-change-log.html
categories: [changelogs]
toc: false
summary: "Home Assistant is a powerful automation system that runs on a small micro-computer.  It integrates with almost any electronic device that is connected to the network, whether it be the WIFI network, or a Zwave network.  It is responsible for automating the A/C units in the Sanctuary, lighting, presence detection, etc."
---
## 9-22-2018

-	// Added the `feedreader` component to Home Assistant to monitor RSS feeds on `newvalleyresources.com`.  Home Assistant checks each feed every 15 minutes for new content.  If there is new content, an event is logged which can be used to trigger any automation in the system.  Primarily, this will be used to trigger messaging systems such as Slack.com to notify subscribers of the updates to the website.

## 9-21-2018

-	// Added the Sonoff 4ch WIFI Relay to Home Assistant configuration.  Relay switches are `switch` components and are named after the type of lighting fixture and the position of the light.  In HA, the lights are as follows:  

    - switch.375Z_IRC_Stage_Right | switch.375Z_IRC_Stage_Right | switch.Wash_Zoom_450_IRC_v2_stage_left | switch.Wash_Zoom_450_IRC_v2_stage_right

-	// Rewired the Sonoff 4CH relay.  Circuit breaker 27 controls the power to these 4 fixtures through 10 AMP relays.  The circuit is a 20AMP circuit but each relay can handle 10A.  Each fixture draws a maximum of approximately 250 Watts, so there's plenty of head-room on the circuit to handle all four fixtures simultaneously.
-	// 

## 9-19-2018

-	// Configured Home Assistant to recognize Sonoff 4CH Relay Switch.  Device can now be controlled remotely and scripted for automation.
-	// Flashed Tasmoto firmware to Sonoff 4CH Pro 2 Relay Switch.  This relay switch will be used to remotely control and automate the power source to the moving head lighting fixtures in the sanctuary.
-	// Tested Slack notification integration.  :thumbsup:
-	// Added Slack integration to Home Assistant to enable automation of status messages and updates to change logs.
-	// Added the DarkSky component to Home Assistant to track local weather conditions in preparation to better automate the cliate control system in the sanctuary.
-	// Added two sensors to the dashboard in Home Assistant.  1) Outside Temperature, 2) Outside Humidity.

## 9-4-2018

-	// Renamed Sanctuary N2 thermostat to Main Foyer (mytotalconnectcomfort.com)
-	// Renamed Main Foyer thermostat to Sanctuary N2. (mytotalconnectcomfort.com)
-	// Swapped Thermostats from Sanctuary to the Main Foyer.
-	// Reprogrammed automation to know the difference.  Foyer thermostat WIFI card may be defective.	  

## 8-24-2018

-	// Installed DB Browser for SQLite to report on and access Home Assistant Data

## 7-31-2018

-	// Installed ArtNet support for HASS.IO and connected to new Enttec ODE Mk2 Ethernet to DMX device.
-	// Programmed Home Assistant to automatically turn house lights on when motion is detected at the center doors at the back of the sanctuary...

## 7-30-2018

-	// Added Meagan's iPhone to the sensors and uploaded avatar.

## 7-14-2018

-	// Reconfigured Raspberry Pi3 to use Ethernet port as primary connection.
-	// Disconnected RPi3 from Wireless connection and attached to port 4 of the 8-port Ethernet Switch.
-	// Tested connection good.
-	// Added [configuration information](raspberry-pi-network-configuration.html) to site for future reference.
-	// Updated programming for A/C Units (WIFI only).
	-	// At Midnight, every night, all temperatures will be re-set to 85 degrees.
	-	// Prior to Sunday Morning Service, all thermostats will fire up at 8AM.

## 7-13-2018

-	// Configured and installed Sonoff switch for desk-lamp behind iMac.

## 7-12-2018

-	// Adjusted automations to handle the toe kick light strip in FOH.
-	// Mounted NODEMCU Sensor logic board with Motion, Temperature, and Light Level sensor between the Sanctuary Stage display and the Exit sign.  Power is provided by the same source as the TV.
-	// Tested and adjusted the sensors.

## 7-7-2018
- // Updated HASS.IO to latest version from 0.72.1 to 0.73.

## 7-5-2018
- // Configured NODEMCU1.0 sensor with Temperature, Motion, Humidity, and Light sensors.
- // Installed LED light strip under cabinets at FOH (toe kick)
- // Added SONOFF inline WIFI switch for Toe Kick lights.
- // Created automation for Toe Kick lights.

## 6-15-2018
### 1:27 PM
Hass.io is installed and ready for configuration