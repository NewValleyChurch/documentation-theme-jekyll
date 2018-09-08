---
title: How to Modify SK for Ableton to Utilize MIDI Notes for Patch Selection
keywords: [ableton,tracks,sunday keys]
summary: "Steps to set up the template correctly."
sidebar: main_sidebar
permalink: modifying-sunday-keys-ableton-midi-note-selection.html
folder: worship_band
toc: true
categories: ableton
---

1. Set up IAC Driver and create IAC Bus.
1. Configure Live Preferences under MIDI tab.  Input for IAC Driver should be Remote ON.  Output should be Track ON.  That's all that's needed.
1. Open Sunday Keys for Ableton
1. Save As to preserve your current set and give the new set a new name.  Keep it in the same project folder.
1. Insert a new MIDI track to the left of Pianos 1.
1. Name it `Pianos 1 Selector`
1. Set the `MIDI From` to your piano.
1. Select input channel 10 (arbitraty, but important.  You don't want any other devices sending the same signal unintentionally.)
1. Set your piano's global MIDI channel to 10.
1. Set the `Monitor` setting in the track to `IN`
1. Under `MIDI To` select `IAC Driver (IAC Bus 1)` or whichever you created when you setup your IAC bus.
1. Select Channel 10 for the MIDI output.
1. Drag a `MIDI Effect Rack` from MIDI Effects into the device editor on `Pianos 1 Selector`.
1. Show the chain list in the new MIDI Effect Rack.
1. Click the `Key` button next to `VEL`.
1. Right click the area the reads `Drop MIDI Effects Here` and click `Create Chain`.
1. Press Command-D to duplicate the chain.
1. Select both chains and press Command-D to duplicate again.
1. Select all 4 chains.
1. Drag the Key range for one of the chains all the way to the right to G8.  You should now have 4 little slivers all the way on the right.
1. Deselect the first chain, keeping the next 3 selected.
1. Move the key range indicator on the 2nd chain one slot to the left.  All three should move.
1. Deselect the second chain.
1. Move the key range indicator on the 3rd chain on slot to the left.
1. Repeat this on the 4th chain until each chain has a key range indicator in its own key, from E8 to G8.
1. Select all 4 chains.
1. Press Command-D to duplicate them.
1. Grab the key range indicator on the 5th chain at G8 and drag it one to the left of E8, continuing the staircase pattern.
1. Press Command-D to duplicate again.
1. Repeat the process until you have 28 Chains.
1. Scroll to the top chain.
1. Rename the first chain to `OFF`.
1. Transcribe the names of the instruments in Pianos 1 to each chain in order from top to bottom by renaming each chain.
1. After you get to `Dream Keys`, rename the remaining chains below to `Custom`
1. Right click one of the chain names and check off `Show Names in MIDI Editor`.
1. Click the Title of the `MIDI Effect Rack` and rename it to `Pianos 1 Selector`.
1. Click the Title on the `Piano 1 Selector` _TRACK_ header to select the entire track.
1. Duplicate the track.  Command-D.
1. Rename the duplicated track to `Pianos 2 Selector`
1. Rename the MIDI Effects Rack in the device editor to `Pianos 2 Selector`.
1. Select all chains in the `Pianos 2 Selector` MIDI Effects Rack.
1. Scroll to the top chain (the "OFF" chain).
1. Click and drag the Key range indicator in position G8 to the left until you get to D#6.  Release.  Now your staircase should span from C4 to D#6 for the `Pianos 2 Selector` key-range.
1. Click the `Pianos 2 Selector` track title to select the entire track.
1. Duplicate the track.  Command-D.
1. Rename the new track to `Pads 1 Selector`
1. Rename the MIDI Effects Rack in the new track to `Pads 1 Selector`.
1. Change the color of the track to match the SK Pads 1 track.  All of the chains in the MIDI Effects Rack should also change color.
1. Starting with the 2nd chain in the `Pads 1 Selector` chain list, begin renaming your chains in order to match the names of the Pads in Pads 1, starting with Warm Pad.
1. Select all chains in `Pads 1 Selector` MIDI Effects Rack.
1. Drag the key range indictators by clicking and dragging D#6 on the "OFF" chain to the left until you drop it on B3.  Your starting and ending key range for all of the chains should now be G#1 to B3.
1. Click the `Pads 1 Selector` Track heading.
1. Duplicate the `Pads 1 Selector` track.
1. Rename the new track to `Pads 2 Selector`.
1. Rename the MIDI Effects Rack in the device editor to `Pads 2 Selector`.
1. Select all chains in the MIDI Effects rack.
1. Click and drag the key range indicator in the "OFF" chain from B3 to G1.  Your starting and ending key range for all chains should now be E1 to G1.
1. Select all 4 Selector Tracks so they are all highlighted.
1. Duplicate all 4 tracks.
1. Set all 4 tracks `MIDI To` and `MIDI From` to channel 11.
1. Rename the first duplicated track and MIDI Effects Rack to `Synths 1 Selector`.
1. Change the color of the `Synths 1 Selector` track to match `Synths 1` that came with SK for Ableton.
1. Repeat this process for the remaining 3 duplicated tracks.
1. In each track's MIDI Effect rack, you'll need to rename each chain in order to match the instruments in the corresponding instrument track, just like we did for the pianos and pads.
1. Double-click the `Pianos 1` track title.  The instrument track that came with SK for Ableton.
1. Click the `Show/Hide Macros` button.
1. Click the `Chain` button so it is activated.
1. Click the `Map` button in the Pianos 1 device in the device editor.  The chain selector should turn green.
1. Click the green area of the chain selector range.
1. Choose a Macro knob and click `Map`.
1. In the `Macro Mappings` window, change the MIN/MAX settings to `0` and `28`.
1. Click the green `Map` button to deactivate mapping mode.  The macro knob will now move the chain left and right when adjusted with your mouse.  It will also be limited to a value of 28.
1. Repeat this process for each of the remaining 7 SK tracks.
1. Select the `Pianos 1` instrument track.
1. Click the MIDI map button in the upper right hand corner of Ableton.
1. Click the Macro button that you previously mapped in the device editor.
1. Press a key on your piano and note which value is stored in the MIDI mappings.  You'll need to transpose your keyboard _at the keyboard_ until you find E6.  Once the MIDI mapping value is E6, hold down E6 and press G8.
1. You should see something like, Channel - 10 / Note Control - Notes E6:G8 with a min and a max value of 0 and 28 in the MIDI mapping list.
1. Reverse the two values.  Change 0 to 28, and 28 to 0.
1. Deselect the MIDI mapping button.
1. Repeat this process on each Macro button that you mapped in each instrument track that came with SK for Ableton.  **Note: the second piano track has a different key range for the mapping.  You can find that range by looking at the key range selector in the selector track MIDI Effect Rack for that track.** Or reference the values at the end of this list.
1. Select all of your new Selector tracks and change the MIDI From to `No Input`.

**Note: You will also need to make sure that you change your keyboard global MIDI channel to channel 11 before you start mapping the MIDI settings on the Synth and Aux tracks, which should already be set to send and receive on channel 11.**

Here are the values:

MIDI Channel 10:

- Piano 1 Selector: E6:G8
- Piano 2 Selector: C4:D#6
- Pad 1 Selector: G#1:B3
- Pad 2 Selector: E1:G3

MIDI Channel 11:

- Synths 1 Selector: E6:G8
- Synths 2 Selector: C4:D#6
- Auxiliary 1 Selector: G#1:B3
- Auxiliary 2 Selector: E1:G3

Why separate everything into so many selector tracks?  To stay organized.  You could easily put all of the chains for all of the instruments in SK for Ableton in a single selector track, but you would chew up nearly every one of your 127 notes for that channel, leaving you with room for only 15 custom instruments.  The way I have it set up now, we use two MIDI Channels for 8 tracks each containing 13 instruments with a single OFF track and a bunch of custom place-holders.  So, each track, if divided up evenly, gets a total of 27 instruments, including the ones that came pre-configured.

{% include links.html %}
