---
layout: post
title: "Post Production"
date: 2013-08-11 20:40
comments: true
categories: [Guides, Post Processing]
---

## Slides

- Remove all blank slides (if any)
- Remove all separator/title slides (if any)
- Set all transition timings to 0.5s 
	- Inspector > Transition
	- Start Transition: On Click 
	- Delay: 0.5s
- Record Slideshow
	- File > Record Slideshow
- Export to Movie
	- File > Export > Quicktime
	- Playback Uses: Recorded Timing 
	- Formats: Custom
	- Video: Full Size
	- Settings > Compression Type > Apple ProRes 422 (HQ) 
	- Frame Rate: 29.97 FPS
	- Gamma Correction: Automatic
	- Audio: No Audio

## Raw Footage

- Decompress using Rarevision 5DtoRGB
	- Program should auto-detect settings on footage import.
	- Output Format: ProRes 422 (HQ) 
	- Decoding Matrix: ITU-R BT.709
	- Luminance Range: Full Range
	- Chroma Mode: Progressive
	- Post-Processing: Technicolor Cinestyle
- Load into Adobe Premiere Pro. Follow these Sequence Settings
	- Editing Mode: Custom 
	- Timebase: 29.97 frames/second
	- Video
		- Frame Size: 1920 horizontal 1080 vertical (16:9)
		- Pixel Aspect Ratio: Square Pixels (1.0)
		- Fields: No Fields (Progressive Scan)
		- Display Format: 30fps Drop-Frame Timecode
	- Audio
		- Sample Rate: 48000 Hz 
		- Display Format: Audio Samples￼￼￼￼￼￼￼￼￼￼￼
	- Video Previews Width: 1920 Height: 1080
- Open Audio in Adobe Audition
	- Go to "Enhancing Audio"
	- Right click audio track > - Edit Clip in Adobe Audition
- Trim Footage
	- Scrub to desired start and "Mark In" (I- )
	- Scrub to desired end and mark with "Mark Out" (O)
	- Extract Footage (')
	- Select all excess footage (Ctrl/Cmd + A) and delete
	- Move playhead to start and - paste (Ctrl/Cmd + V)
- Insert Exported Slide Footage (See "Slides")
- Sync Both Sets of Footage
Open Footage in Adobe After Effects
	- Go to "Keying Footage" Right click on - footage > Replace with After Effects Composition
- Clean up Useless Tracks
	- Sequence > Delete Tracks
	- Video Tracks
		- Delete Video Tracks > All Empty Tracks
	- Audio Tracks
		- Delete Audio Tracks > All Empty Tracks

## Enhancing Audio

- Remove Noise
	- Select region of room tone
	- Effects > Noise Reduction/Restoration > Capture Noise Print
	- Select entire track (Ctrl/Cmd + A)
	- Effects > Noise Reduction/Restoration > Noise Reduction (Process)
	- Noise Reduction: 100%
	- Reduce by: 4db
- Compress and Normalize
	- Effects > Amplitude and Compression > Single-band Compressor
	- Threshold: -6.0db
	- Ratio: 12.0
	- Attack: 0.0ms
	- Release: 100ms
	- Output Gain: 0.0db
	- Effects > Amplitude and Compression > Normalize
	- Normalize to -6.0db Normalize all channels equally
- Apply EQ
	- Effects > Special > Vocal Enhancer
	- Select male or female accordingly
	- Effects > Special > Mastering
	- Peaking Enable
	- High Shelf Enable
	Adjust accordingly. High shelf point should be above the axis. Peak point should be below the axis.
	- For Guys
		- 2500Hz, +2db
		- 250Hz, -2db
	- For Girls
		- 2500Hz, +2db
		- 250Hz, -5db
- De-Ess Sibilance
	- Effects > Amplitude and Compression > DeEsser
	- Select Male or Female Preset Accordingly

## Keying Footage

- Add Smooth Screen to Composition
- Add Primatte Keyer to Composition
	- Effects and Presets > Primatte > Primatte Keyer
- Configure Primatte Keyer 
	- Keying
		- Tick Adjust Light On/Off
		- Tick Sample On/Off
		- Set Sampling Style to "Rectangle" Tick Smart Sample On/Off
	- Keying > Correction
		- Edge Color Replace: Color
		- Replacement Color: #FFFFFF
		- BG Defocus Layer: None
	- If filming against Chroma-green background Composition Controls > Spill Killer
		- Tick Enable Spill Killer
		- Color Mode: Green
		- Range: Adjust till green cast on person is gone (40-50%)
- Apply Key
	- Keying > Selection
	- Base Color Sample: Eyedrop background color Keying > View
	- View: Matte (To check the accuracy of the mask. Remember to switch back to View: Comp when done so the footage shows up in Premiere Pro)
	- Keying > Selection > Select
	- Use "Clean BG" and "Clean FG" to demarcate areas to be keyed or kept
	- Use "Spill Sponge" to mark areas inside foreground that are accidentally keyed Use "Matte Sponge" on hair edges to regain fidelity
	- Use "Restore Detail" on underarm shadows to create natural gradients
- (Optional) Add Matte Feather Sharp to Composition
	- Effects and Presets > Key Correct > Matte Feather Sharp
	- Useful when the edge of the key shows signs of artifacting or flickering due to the footage being out-of-focus. This tightens the mask by a couple of pixels, removing specks and giving a nice, sharp edge.
	- Known to increase render time significantly - use sparingly or as means of salvaging footage.
- Magic Bullet Colorista II
	- Select Linked After Effects Composition in the Timeline
	- Effects > Magic Bullet Colorista II > Colorista II
	- Effect Controls > Colorista II > Secondary
		- Pop: -10
		- Secondary Key > Key > Edit
	- Move oscilloscope bar up and down till only skintone is selected (Black is not selected, white is selected. All skin areas should be white)
	- Clip highlights and shadows by moving both ends of the horizontal slider bar in a bit.￼￼￼
	- Softness: 5%
	- Click ok
	- Effect Controls > Colorista II > Master
		- RGB Contrast: 0.2 RGB
		- Mid: 0.3
- (Optional) Enlarge Footage
	- The lecturer should fully fill the right third column of the frame.
- Change Composition Background
	- Composition > Composition Settings > Background Color
	- Set to #FFFFFF, white
	- Click ok

## Grading

- Magic Bullet Looks
	- Select Linked After Effects Composition in the Timeline
	- Effects > Magic Bullet Looks > Looks
	- Effect Controls > Looks > Edit Look
	- Mouse hover on left screen edge > Skin Grading 10%
	- Click "Finished"
- Convolution Kernel Sharpen More
	- Select Linked After Effects Composition in the Timeline
	- Effects > Convolution Kernel > Convolution Kernel Sharpen More

## Exporting

- Queue Sequence to Media Encoder File > Export > Media
	- Format: H.264
	- Preset: YouTube HD 1080p 29.97 Export Video and Export Audio
	- Check "Use Previews"
	- Click "Queue"
	- Go to Media Encoder, select the job and press enter
- Save output as <S/N> - <Checkpoint Name>.mp4

## Publishing

- Upload to YouTube
	- Naming Format: <Checkpoint Name>
	- e.g. 'You Demand'
	- Update Google Drive tracking documents with YouTube URL
- Upload to MediaFire <Subject>\⧵<Topic>\⧵<Lesson>
	- Naming Format: <NN> <Checkpoint Name>.mp4
	- e.g. '01 You Demand.mp4'
	- To ensure correct sorting, do not use '1 You Demand.mp4'
- Upload to Youku (Pending)
- Send for Subtitling (Pending)