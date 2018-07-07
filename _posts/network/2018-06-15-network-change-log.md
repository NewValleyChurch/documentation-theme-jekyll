---
title: Network Change Log
layout: post
permalink: 2018-06-15-network-change-log.html
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
categories: network
---

## 8:45AM
- Changed guest network IP settings to the 192.168.20.xxx range with 254 available leases for guest devices.  Leases last 2 hours before they're released for a new device to connect.

- Changed primary router subnet from 255.255.255.0 to 255.255.255.240, opening up the ability to have over 4,000 assignable IP Addresses.  (Excessive?  Probably, but easy to segment hardware types across multiple IP ranges.)

- Updated [this page](/network.html) to reflect the current network setup.
- All SSID wireless names have been re-written with no spaces.
- Renamed both access points from their gnarly networky names to `Access Point 1` and `Access Point 2`
- Changed MediaOne IP address and re-routed SSH and Remote Access in port forwarding for screen sharing.
- Updated Sound Booth iPad with new IP address and tested connection to QU-32.
- Changed QU-32 IP address and confirmed availability on the network through remote access on the iPad.
- Renamed iPads to MobileOne and MobileTwo
- Set static IP's on both iPads to 192.168.3.xxx
- Confirmed Stage Display connectivity with MediaOne ProPresenter
- Configured VPN IPSec access for remote management.
- Installed Raspberry Pi3 with HASS.io (Home Assistant) automation server.