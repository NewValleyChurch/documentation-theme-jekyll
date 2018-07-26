---
title: Check-In Stations Setup and Troubleshooting Guide
layout: page
permalink: check-in-stations-setup-and-troubleshooting-guide.html
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
categories: planning center
toc: false
summary: "Troubleshooting and setup guide for the iPad Check-in Stations and Label Printers"
---

## Overview

The iPads in the Kids area are setup to be event check-in stations for Planning Center events.  They are locked in guided mode to ensure that Check-Ins is the only app open and available.

When someone enters their phone number, they are found in the People database and are given the option to check-in, at which point a name label will be printed.

## Network Connections

Both the printers and the iPads utilize the NewValleyChurch WIFI network.

![](images/network/checkinipads.jpg)

## Configuring the Printers

The printers are configured through a web interface.  The settings for the printers should never need to be changed unless there's a complete loss of settings due to a firmware update or some other anomaly.

### Left Printer - 192.168.9.3

Manufacturer: Brother
Model: QL-710W
Name: Brother QL-710W Check-in Printer 2
IP Address: 192.168.9.3

### Right Printer - 192.168.9.2

Manufacturer: Brother
Model: QL-710W
Name: Brother QL-710W Check-in Printer 1
IP Address: 192.168.9.2

## How to know if the Printers are connected to WIFI

In any web browser, enter the address http://192.168.9.3 or http://192.168.9.2 _while connected to the main WIFI network_.  If you can successfully connect to the printer in the browser, then you know that the printer is online.

## How to know if the iPads are connected to the printer?

- In the Check-In app, enter your phone number as though you are checking in.
- At the next screen, tap the little gear icon on the bottom right corner.
- Tap the Printer button at the bottom of the password keypad.
- Both Brother printers should be available in the list of printers.
- Select the printer that you want that particular iPad to print to. 
- When you are prompted for the type of paper, make sure that you choose the correct type.

{% include important.html content="Note, it's critical that the paper in the cartridge match the type of cartrige in order for the printer to recognize that it has the right type of paper.  The cartridge has a pattern in the bottom that depresses certain buttons in the printer to let the printer know which cartridge is installed.  It is possible to inadvertently select the wrong type of paper for the cartridge." %}

When you select a printer, you're basically telling Check-Ins to send all print jobs on this device to that printer.  This is different than choosing which station will be doing the printing.  Stations can be set to print to other stations, which in turn print to the printer that _that particular station_ has been connected to.  This allows you to have one printer with multiple stations.



{% include links.html %}