---
title: Network Overview
layout: page
comments: true

sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
keywords: media
summary: A brief overview of the Network Layout at New Valley Church
permalink: network.html
folder: network
toc: false
---

## Topology Overview

### Static IP Organizational Structure

All devices at New Valley that are permanent fixtures are assigned a static IP address.  This is to accomodate not only better organization, but the ability to remotely control some of those devices.  If we automatically assigned everything, we would be inefficiently chasing numbers around.

### IP Ranges for Specific Types of Devices

Each type of device will be found on a different segment of the network.  Since we have a range of IP addresses starting at `192.168.0.xxx` through `192.168.15.xxx` we can afford to assign static IP addresses with a logical layout. 

#### Ranges and Hardware Assignments

- 192.168.0.xxx - Servers / Routers

#### Details

Subnet Mask: `255.255.255.240`  
Available IP Addresses: 4,094  
Starting IP Address Range: `192.168.10.1`  
Ending IP Address Range: `192.168.10.201`     

200 of the 4,094 addresses have been made available for anyone connecting to the primary SSID network: `NewValleyChurch`.

### What This Means
When your computer or mobile device connects to the WIFI network at New Valley Church, it is assigned a temporary 72 hour IP address on the network.  That IP Address is leased to your device from the Starting and Ending ranges above.  If more than 200 devices are ever concurrently connected to the network within a 72 hour window, the number of available IP addresses will need to be increased.

The subnet we're on allows us to have 4,094 hosts (that's your phone or computer, a TV, projector, sensor, etc.)  That's plenty.

### Guest Network
The guest network is called `NewValleyGuest`.  
Subnet Mask: 255.255.255.0  
IP Limit: 254 concurrent devices.  
IP Range: 192.168.20.1 - 192.168.20.254  
Lease Length: 2 Hours  

{% include links.html %}