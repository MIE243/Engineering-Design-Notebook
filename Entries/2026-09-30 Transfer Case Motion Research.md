---
date: 2026-09-30
authors:
  - Mo Zhou
sprint:
commits: []
tags: []
---
## Transfer Case Type
Researched a NP231 style transfer case that features a planetary gearset driven by the input shaft from the transmission.

## Vocab
- Range Sleeve 
	- A sliding splined collar (dog clutch) on the mainshaft that either leaves the mainshaft free (neutral), locks the mainshaft directly to the input shaft, or locks the mainshaft to the carrier output from the planetary gearset
- Mode Sleeve
	- A sliding splined collar on the mainshaft that either stays disengaged (drive sprocket free spins) or locks the drive sprocket to the mainshaft to drive the front output
- Chain Drive
	- The drive sprocket free spins on the mainshaft. When the mode sleeve locks it to the mainshaft, the mainshaft drives the sprocket, which drives the front output through the chain
- Planetary
	- A planetary gearset with a sun gear, 3 planet gears that spin the carrier, and a ring gear
	- The ring gear is always fixed and never spins
	- The sun gear is part of the input shaft, so it is powered directly by the transmission
	- The carrier's center is a hole and lets the input shaft run through it. The carrier's actual output is a set of internal dog teeth around the range sleeve that it can engage. 
## How It Works

### N
- Range sleeve sits in the middle/neutral position, not connected to the input shaft or the carrier. 
- Mode sleeve stays engaged (N is between 4H and 4L on the lever), so the front and rear outputs are linked to each other but free from the input.
- The input shaft spins the sun gear and the planetary gears, but none of it drives anything. Both front and rear outputs can free spin
### 2H
- The range sleeve locks the input shaft directly to the mainshaft/rear output. 
- The mode sleeve disengages the front output 
- Only RWD in this case, direct from transmission

### 4H
- The range sleeve is locked to the input shaft (planetary gets skipped)
- The mode sleeve engages the sprocket that drives the front output
- This case front and rear outputs spin direct from the input
### 4L
- The range sleeve gets locked to the carrier output 
- Mode sleeve is engaged to the sprocket
- The input shaft spins the sun gear, which drives the planetary gearset. The input shaft does not drive the mainshaft directly. The carrier drives the mainshaft/rear output. 

## To-Do
- Need to investigate how adding a center locking differential may change how this whole setup works. 
- Need to figure out the exact math behind input vs output speed and torque in these configurations
