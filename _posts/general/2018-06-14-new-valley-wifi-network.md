---
title: New Valley WIFI Network
layout: post
permalink: 2018-06-14-new-valley-wifi-network.html
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
categories: network
---

## Important Update
The network SSID has changed.  This is the name that you see when you browse for WIFI networks when you're at the church.  The old name used to be `New Valley Church` with spaces.  It is now `NewValleyChurch`.  This is true for both 2.4 and 5Ghz bands.  There are technical reasons for this that aren't important.

What is important is that you'll need to make sure you re-connect your device(s) when you're at the church if you connect to the primary network.

## Guest Network
If you prefer, you can simply connect to the guest network which is called `NewValleyGuest`.  Keep in mind that if you operate a device that needs to work in tandem with another piece of hardware on the primary network, you'll run into a problem because both of the subnets are isolated from one another.

## Repeater
There's a third network ID that you can ignore.  It's called NewValleyChurch_RPT.  This is a repeater used solely to connect the Toshiba Printer/Copier to the network.

## Planned Changes
(**Note: Lot's of technical mumbo jumbo to follow**)

Tomorrow, Friday, June 15th, I will be reconfiguring the network to utilize an alternate subnet mask which will add the ability to segment the network and organize our hardware more efficiently and add the ability to host a few thousand devices instead of only 254.

### What does this mean?
Every device that connects to the network is "tuned into" subnet 255.255.255.0.  No need to worry about the numbers.  What's important is to know that this subnet mask is limiting, and I'm adding more room to grow.

So, we're adjusting to the following:

Subnet Mask: 255.255.255.240
This gives us room for over 4,000 hosts on the network.

#### Static IP Addresses
Devices that stay on site are being configured with a static address that never changes.  Devices that come and go, like your iPad, or your iPhone, etc., will be automatically assigned an address from a pool of available addresses.

The static devices will now be more organized.  I will be able to group them.  For example:

- Servers and Routers can occupy 192.168.**1**.xxx.
- Mobile Devices can use: 192.168.**2**.xxx
- TV's and Projectors can use 192.168.**3**.xxx