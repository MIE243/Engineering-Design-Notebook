---
date: 2026-09-29
authors:
  - Mo Zhou
sprint: 1
commits:
  - https://github.com/MIE243/v0-Initial-Chassis/commit/91ea6e1b1a4317ff8e64f1192d00af37e2547f1b
tags:
  - "#v0-CAD"
---
## Summary
Created a rough draft of a rear open differential design with motion links and mates built into SolidWorks. This should give a reference for when designing the real differential about how the motion works precisely. 

## Details
The ring gear and input is at a ratio of: **4.1 : 1**
The side gears and pinion gears have a ratio of: 7:6
## CAD
Sketch showing the rough schematic outline for the v0 chassis (on the top plane). 
![[Pasted image 20260929143916.png]]

Rear differential skeleton setup schematic (each square represents a bevel gear)
![[Pasted image 20260929144032.png]]

Built assmebly in SolidWorks
![[Pasted image 20260929144239.png]]

## To Do
- Worth considering adding in a few more detalis so it is easier to tell which direction the gears are spinning in. Even though the motion links all work properly it is very hard to tell what way the gear is actually spinning. s
## Notes for Future CAD
- The ring gear at a ratio of 4.1:1 is quite large, and its size directly affects how large the overall differential assembly is. So it is worth considering running a different ratio from the common 4.1 : 1 or making the drive wheels at a larger size so that the differential will not scrape the ground. Alternatively we will have to do some complex setup where the differential sits above the rear drive axle. 
- Similar thing applies to the side vs pinion gears. In the real design the side gear should be larger than the pinion gears as that is more common, but the larger size again takes up vertical space so it is something that should be considered before the v1 CAD. 