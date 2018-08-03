---
title: "How to: Prepare a Video for ProPresenter"
layout: page
comments: true
sidebar: main_sidebar
toc: true
topnav: topnav
image_folder: images
document_folder: documents
keywords: video
summary: "A quick guide to displaying video on the sanctuary screen for Sunday Morning Service"
permalink: peparing-a-video-for-pro-presenter.html
folder: media
---

## Steps:

# When the Video we need to play is smaller than our screen.

## Create the Video Document

1. Obtain highest quality copy of original or rendered original as possible.
2. Save the file to /Volumes/Blue/ProPresenter/Video  
   
   Any video that we download to be presented needs to be organized in this folder, which is a centralized network location.

3. In ProPresenter, create a new document:  

	- Press ⌘ + N.

      {% include image.html file="crashvideos.jpg" %}

    - In `New File Name:` enter the title of the Video.  Omit the word video from the title as that would be redundant.  
	    	a) The video is going to be saved to the /Volumes/Blue/ProPresenter/**Video** folder,  
	    	b) the video will have an extension that indicates that it's a video (*.mov, *.mp4, etc.), and  
	    	c) we're going to categorize it as a video.

    - Click the Template dropdown and select an appropriate video template for the slide.
    - Under Category, select Video.
    - For Size, select 3600 X 1200.

## Set the Slide Cues for the first slide

This will depend on what you want to have happen.

1. Open the cue palette (Shift-CTRL-C) or right click the slide -> Add Cue -> Cue Palette.
1. Clear the appropriate elements from whatever was last displayed by dragging each cue from the cue palette to the first slide in the document.
1. If there are any backgrounds unique to this video, use the Media Cue "Graphic" to browse to the Images folder (/Volumes/Blue/ProPresenter/Images).  If you chose a video template that already has a static background that we use regularly, you don't need additional graphics.
1. Add a stage display cue that's appropriate for this point in the service.
1. Add a timer cue and choose an appropriate timer countdown with the action "Reset and Start Timer"
1. Add any prop cues that apply such as logos, transparent overlays, etc.
1. Add any masks, messages or social media cues that apply.
1. Close the Cue Palette

## Add the Video to the Slide

{% include important.html content="There is a specific way to reference a video in ProPresenter.  Dragging and dropping a video into ProPresenter will cause problems.  Make sure you reference the video as explained here." %}

1. Right click the slide in the document where the video will be displayed.  At this point, it's probably the first and only slide.
1. Click `Edit Slide`.
1. Click the `Add Video to Slide` button on the toolbar above the slide.
1. Choose the video file that was saved to the /Volumes/Blue/ProPresenter/Video folder.
1. Click Select.
1. The video should insert itself dead center on the slide inside of, or directly on top of the frame placeholder in the slide.
1. Click the Object Properties icon in the slide properties inspector on the right.
1. Change the width and height of the element to match the size of the frame on the template.  In this case, 1920X1080 would be a standard aspect ratio.  If the video is rendered at a lower resolution, such as 1280X720, you can still use 1920X1080 as your dimensions.  If you don't know the original dimensions of the video, you can find out by using the Mac Finder to browse to /Volumes/Blue/ProPresenter/Video.  Right click the video file and click `Get Info` then click the arrow next to `More Info.`  This will show you the Dimensions.  The most important aspect of this is making sure that the ratio of length X width remains the same, and that you don't blow up a small video to be too large for it's resolution.
1. Set the X and Y coordinates to be 840 and 60 respectively.
1. Close the slide editor and test your new slide.

