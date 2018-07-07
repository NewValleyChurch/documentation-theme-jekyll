---
title: 'Automation: Toe Kick Lights'
layout: page
permalink: automation-toe-kick-lights.html
toc: false
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
summary: Routine for lighting up the floor in the sound booth when motion is detected.
---

## Basic Idea
Light up the floor of the sound booth using an LED light strip when someone walks into the sanctuary, unless the house lights are already on, so nobody trips over the steps.  If neither the house lights go up, nor motion is detected again, the lights will automatically shut off after 5 minutes.  When the house lights are brought up, the light strip will automatically shut off as they will no longer be needed.

Currently there is a single motion sensor that will cover anyone coming in through the front sanctuary doors.  The light sensor and motion sensor are together in the same node.

The toe kick lights are automatic.  They will:

- Turn On:

    When motion is detected by sensor.sn1_pir `and` light levels detected by sensor.sn1_ldr are less than or equal to 85 `and` the light is already currently off.  Otherwise nothing will happen.

- Turn Off:

    When the light level on sensor.sn1_ldr exceeds 300 `or` 5 minutes have passed with no detected light increase nor additional motion sensed.