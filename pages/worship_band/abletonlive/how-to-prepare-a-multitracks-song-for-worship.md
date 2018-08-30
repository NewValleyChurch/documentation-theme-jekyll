---
title: Preparing a MultiTracks Song for Worship with Ableton Live
keywords: [multitracks, ableton live]
summary: "A step by step account from MultiTracks to Performance"
sidebar: main_sidebar
permalink: preparing-multitracks-songs-for-worship-in-ableton-live.html
folder: worship_band
toc: true
categories: ableton
---

# Part 1: Modify Original Multi-Tracks Download

MultiTracks songs come with a few basic ingredients, saved as an Ableton Project file with a single Ableton Set.  That set contains each track of the song as published along with a click track and a band cue track.  

There are a few characteristics of each MultiTracks song that need to be adjusted in order to optimize your ability to stay organized.  Unfortunately, each MultiTracks song share the same name for each track.  Drums are always labeled `Drums` and keys are always labeled `Keys`.  As a result, the underlying audio files included have the same names.

{% include note.html content="If you plan on building a master Ableton Set with multiple songs from MultiTracks, you will find that Ableton will incrementally name duplicated wave files.  When you combine them, tracks like `Drums` which are based upon an audio file called `Drums.wav` will share the same clip name, but the underlying audio file will be named to `Drums-1.wav` and `Drums-2.wav` and so on.  It becomes difficult to know, by looking at your audio samples, which `Drums` audio file belongs to which song." %}

## Steps:

### Duplicate the Original

1. Open the MultiTracks Set File in Ableton Live.
1. Immediately `Save Live Set As`.  Give the set a new name and save it in this song's project folder.  This is to ensure the original remains untouched, just in case.  You'll even have a backup ZIP file that you downloaded from MultiTracks.  **Make your edits to _this new set_.**

### Add the Follow Track

1. In the set, switch to Arrangement View.
1. Insert a new MIDI track above the Click Track.  Name it "Follow"
1. Drag the Follow SCENE Max 4 Live Device to the Follow track. (Presets -> MIDI Effects -> Max MIDI Effect -> Follow SCENE 4.0.4.amxd)
1. In the device window at the bottom, click the "Next" and "Clip End" buttons.
1. In Arrangement View, create a blank MIDI clip in the Follow track (Shift-CMD-M) and ensure that it is as long as the MultiTrack arrangement.

### Warp the Audio

1. One at a time, click each track's clip, then click the Warp button in the Sample box in the clip editor at the bottom of the screen.  If you don't see the sample box, click the little circle with the squiggly wave icon in the bottom left corner of Ableton Live.

### Rename the Clips

We do this to ensure that the underlying audio files have names that make sense if we ever need to locate them.

1. Click on a track, press CMD-R, rename the track.  If the song's name is Amazing Grace, then rename the Drums track to Amazing Grace - Drums.  If you anticipate multiple versions of Amazing Grace, come up with a more unique name, like Amazing Grace - Jon Bon Jovi - Drums.
1. Select all clips in Arrangement View, right click, Consolidate.  This renames all of the audio files and puts them into the Samples -> Processed -> Consolidate folder.  **It also adds a time-stamp to the clip name**

### Move the Clips to Session View

{% include alert.html content="If you intend to do any automation to the arrangement, such as individual track volume control, muting or unmuting a specific section of a part, etc., do it now so the clips will carry over to your template." %}

{% include note.html content="When you consolidate a single clip or multiple clips into single clips, Ableton writes a new version of the audio file to the current project's Samples folder.  That means that if you were to consolidate any split tracks from this set in your own template, new samples will be created and you'll find that your set has samples from both the original MultiTracks project _and_ your project.  This can get messy, so be intentional about consolidation of clips." %}

1. Split the Clips at their locators.  Select all clips in Arrangement view, click the first locator, then press CMD-E.  Click the next locator and do the same, and so on until you've split all tracks into multiple clips for each section.
1. In Arrangement View, select from the first measure to the first locator (probably Intro.)
1. Press CMD-L to place the loop brace over this section.
1. Click the loop brace to select all clips within this range.
1. Click the clip title bar in the first track (Follow) and hold.  While holding, press the TAB key to switch to session view.
1. Drag to the first scene of the Follow track to drop all of the clips for this section into the first scene.
1. Switch back to Arrangement View (Tab).
1. Move the start of the loop brace to the next locator and make sure the loop brace length matches the length of the next section.  
1. Click and drag the clips again.  Do this until the entire song is stacked one scene on top of the next in session view.
1. Save your set.

### Bring all of your work into your custom layout.

1. Open your Master Template.  I'm assuming you have a master template with all of the songs the way you play them in a template that has all of your additional controls, etc.
1. Switch to Arrangement View.  Select all and clear it out so you have a fresh workspace.
1. In the Ableton browser, go to the MultiTrack project you just edited and expand the project and set that contains the clips you just created.
1. One by one, expand each track so all of the clips are in the browser.  Select the first through the last clip of a given track and drag it to the appropriate track in your template.  You'll notice that the clips will be laid out in sequence with lines where the song sections were in the MultiTracks file.
1. 



{% include links.html %}
