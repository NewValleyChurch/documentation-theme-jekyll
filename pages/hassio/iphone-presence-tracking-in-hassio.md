---
title: "About iPhone Presence Tracking"
layout: page
toc: false
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
permalink: iphone-presence-tracking-in-hassio.html
categories: hassio
summary: "More information about how Home Assistant tracks iPhones..."
---

Home Assistant repeatedly scans the  IFI network at regular 5 minute intervals to see which devices are connected to the network and which devices are not.  **Only devices that have been configured will be recognized.**

Due to the fact that iPhones tend to sleep to save battery power, they sometimes appear to be away when in fact they are here.  At the moment, there are only a few ways to _automatically_ track if someone is here or not.  At present, none of them are 100% accurate...but close.

## Why Track if Someone is Here

Aside from being able to see if someone is in the building, various functions can be automated based upon someone being here or not.  Since accuracy isn't 100%, basing mission critical systems automations on presence detection could easily lead to undesired results.

So, while it may show you as not here, that may not actually be true.