---
title: "Configuring the Raspberry Pi Resin OS Network Settings"
layout: page
toc: false
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
permalink: raspberry-pi-network-configuration.html
categories: automation
summary: "Network configuration details for the RPi3 running Home Assistant"
---

All of the configuration settings for automation at New Valley Church are stored on a memory card that's installed in the Raspberry Pi3.  If this card is damaged, lost, corrupted, etc., all automations and automation configurations will be lost and will need to be rebuilt.

There is an operating system on the card that boots the RPi3.  In order for the operating system to be able to communicate on the network, a single file must be configured before starting the system for the first time (and/or reconfiguring the network connection.)

{% include note.html content="To adjust these settings, you will need to remove the flash card from the RPi3 and use a USB card reader to access the contents of the card on another computer.  The configuration file is a basic text file and can be edited with just about any text editor."

## File Name and Location

The name of the file that needs to be edited is `resin-wifi` and it is located in the `system-connections`.  Simply open the file, make a copy of the file to your local desktop before changing it (to preserve the already working setup just in case), and edit the settings.

## WIFI or Ethernet?

The RPi3 can connect via WIFI, but in our environment, having the system hard wired to the network switch is more stable and reliable.

## WIFI Configuration Settings

To configure the RPi3 for WIFI, the file should look like this:

~~~
[connection]
id=resin-wifi
type=wifi

[wifi]
hidden=true
mode=infrastructure
ssid=NewValleyChurch (or whatever the name of the WIFI network is)

[ipv4]
address1=192.168.1.1/20,192.168.0.1
dns=8.8.8.8;8.8.4.4;
method=manual

[ipv6]
addr-gen-mode=stable-privacy
method=auto

[wifi-security]
auth=alg=open
key-mgmt=wpa-psk
psk=<your wifi password here>
~~~

## Ethernet Configuration Settings

To configure the RPi3 for WIFI, the file should look like this:

~~~
[connection]
id=ethernet
type=ethernet
interface-name=eth0 (this name is dependent upon which actual network connector you plug into.  The RPi3 only has one, so there's no questiona bout it.)
permissions=
secondaries=

[ethernet]
mac-address-blacklist=

[ipv4]
address1=192.168.1.1/20,192.168.0.1
dns=8.8.8.8;8.8.4.4;
method=manual

[ipv6]
addr-gen-mode=stable-privacy
dns-search=
method=auto
~~~
