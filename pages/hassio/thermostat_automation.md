---
title: 'Automation: Thermostats'
layout: page
permalink: automation-thermostats.html
toc: false
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
summary: "Thermostat automation setup for Honeywell WIFI Thermostats"
---

## Goal

- Study cooling and heating patterns so there's hard data to use to make the right decisions regarding lowering overhead.
- Optimize climate control for an organic experience both for staff and congregation.
- Always have the climate set to the right temperature for the occasion.
- Eliminate the _requirement_ to manually control each unit from each thermostat.

## Thermostats and Automation

7 of the WIFI thermostats have been connected to Honeywell's My Total Comfort Connect website and can be accessed remotely via web browser or Honeywell mobile app.

Limitations in Home-Assistant.io prevent direct control of the units through automation, but a workaround is available by bridging the gap between HA and Honeywell Thermostats through IFTTT.com using what's known as a webhook.

Basically, Home Assistant can connect to IFTTT, deliver up to 3 pieces of information (Name of Event, Temperature to set, Time to Hold) to the Applet, and IFTTT will connect to Honeywell My Total Connect to update the thermostat settings remotely.  Those updates are then transmitted to the thermostats and the units will respond accordingly.

## How to Control

