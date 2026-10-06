---
date: 2026-10-05
authors:
  - Mo Zhou
sprint: 1
commits:
  - https://github.com/MIE243/v0-Initial-Chassis/pull/10/changes/076be431fb8e4f3cbd832c5ff8f87a7e6e425d8c
tags:
  - "#v0-CAD"
---
The front differential will share parts and reference the rear differential (for now) as they are more or less the same. 

## Differences from Rear Differential
The pinion is not placed on the center axis, and it is offset 
![[Pasted image 20261005005223.png]]

### Changes from Rear Differential
RD L Gear Left (Rear Differential Left Wheel) --> FD L Gear Left (Front Differential Left Wheel): 35mm shorter axle. ![[Pasted image 20261005010356.png]]

RD L Gear Right (Rear Differential Right Wheel) --> FD L Gear Right (Front Differential Right Wheel): 35mm longer axle
![[Pasted image 20261005010443.png]]

### Reused Parts from Rear Differential
The following parts were reused parts from Rear Differential **without** renaming:
- Ring Gear
- Pinion
- Pinions inside of the differential (smaller gears)

## Changes to carrier case
Added an extrude so the back of the carrier sits flush with the gear in front
![[Pasted image 20261005010633.png]]


## Front Differential
![[Pasted image 20261005010657.png]]

## Full Chassis (So Far)
![[Pasted image 20261005010727.png]]

## Near Future
- Steering will probably be implemented on the front axle, therefore the differential's shafts to the wheels are still subject to change
