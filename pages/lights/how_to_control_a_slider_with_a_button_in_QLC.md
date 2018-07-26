---
title: How to Control a Slider with a Button in QLC+
layout: page
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
keywords: lights
summary: "Steps to setting the value of a slider in QLC based upon a button."
permalink: how_to_control_a_slider_with_a_button_in_QLC.html
folder: lights
toc: false
---

## Steps

### Setup Loopback

1. In the `Inputs/Outputs` tab in QLC+, Select Universe 2 in the Universe list.
1. Select the `Output` checkbox on the Loopback 1:Loopback 1 plug-in on the right.
1. Select Universe 3 in the Universe list.
1. Select the `Input` checkbox on the Loopback 1:Looback 1 plug-in on the right.

### Create a Fixture (Dimmer)

1. Click the Fixtures tab in QLC+
1. Create a "Fixture" and make it a dimmer with a single channel on Universe 2.

### Create a Scene

1. Click the Functions tab in QLC+
1. Create a new Scene.
1. Add the fixtures to the scene that you want to control, enable the channels for each fixture that you want to set, then pre-set the levels that you want when the scene is fired.
1. Create another scene.  In this scene, attach only the Dimmer you created for Universe 2.  Set the value that you want the dimmer to adopt when you press the button you're going to create.

### Virtual Console Button and Slider

1. Click the Virtual Console tab in QLC+
1. Toggle Live edit mode (upper right toolbar)
1. Add a button.
1. Add a slider.
1. Edit the button and set the function to the scene that changes the dimmer on universe 2.
1. Edit the slider and set the Input Universe to 3: Loopback, Channel (whatever channel you assigned to the fixture you created in `Create a Fixture` above.)
1. Click the playback tab and assign the function you created for the scene that sets your fixtures to the desired settings.

### Test the Button

1. Switch to Operate Mode (green arrow top right)
1. Click your button.  The slider should jump to the value you set.

{% include links.html %}
