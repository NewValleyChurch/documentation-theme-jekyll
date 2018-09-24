---
title: How To\: Display Rotating Slide Show on Sharp Aquos TV in Cafe
layout: page
categories: [media,audiovisual]
permalink: how-to-display-images-on-the-sharp-tv-in-the-cafe.html
toc: false
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
summary: "This How To document will explain how to display images on the Aquos TV in the Cafe area in a rotating slide show without using a USB stick."
---

Using a free program called Serviio, which has been installed on MediaOne, we can now point to any network shared folder to create a repository that the TV can access.

## Pre-Requisites

- Serviio server must be up and running.  To test this, point your browser to http://192.168.4.1:23423/console/.  If you see the management console, it's up and running. Serviio is running as a service on MediaOne, which means it _should_ auto-start when the computer is powered up.  If it doesn't, it will need to be manually started at the MediaOne workstation.
- The file repository must be accessible on the network.  Currently the files are located on an external USB drive.  A network drive will eventually replace this to provide centrallized access to media.
- The TV must be on and the input source must be set appropriately.  Instead of using USB, use the network server setup.  The TV should see the Serviio media server in the list of available media servers.


There is a media browser that gives you access to the media served by Serviio.  Simply point your browser to http://192.168.4.1/mediabrowser.  You know the password.  This media browser is a tool that can be used on any device to display the contents of the media server's repositories.

## How To Manage Files:

-  Create your media in the proper aspect ratio using whatever you use (Photoshop, Illustrator, Skitch, etc.)  Images must be in JPG format. Music must be either MP3 or LPCM formats.  Videos are limited to AVI, ASF, MP4, WMV, and MPG formats.
-  Publish your final image to the following folder:  `/Volumes/Blue/ProPresenter/Images/Photo Galleries/TV Loop`.  If you don't have access to this folder from your computer's `Finder`, you'll need to connect to the share through your network browser in finder and the location will become an available volume on your computer.  If you have trouble doing this, it may be due to permissions on the repositories files.  Contact your network admin for help.
-  On the TV, if it's not automatically playing, select the appropriate input and media source, and then drill down to the `TV Loop` folder until you find the content you want to cycle through.  
-  Start the slide show (Press 'C' on the remote's screen.)

{% include tip.html content="The images in this folder should not be considered originals.  This is an endpoint for images that are created from masters that should be stored in a different location to preserve the original.  Following that practice, you'll know that it's safe to delete images permanently from the TV Loop folder when it's time to retire them, unless they need to be archived for future TV Loop usage." %}

