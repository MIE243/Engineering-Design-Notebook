---
date: 2026-09-30
authors:
  - Mo Zhou
sprint: 1
commits:
  - https://github.com/MIE243/v0-Initial-Chassis/commit/85084e6df45c6b88703ee75f2ed679fd9613c2f1
tags:
  - v0-CAD
  - "#Transfer_Case"
---
## Spec
This tries to CAD the full time transfer case with the added mode sleeve outlined in [[2026-09-30 Full Time Transfer Case with Lockable Differential]] 

The position that the front axle sprocket should sit is already speced in [[2026-09-21 v0 Rear Differential CAD]], so this will build starting from there

## Mode Sleeve
![[Pasted image 20260930215544.png]]
The top rectangle (big one) is the sprocket that is linked to the front shaft. The first smaller rectangle is the dog ring that always spins with the sprocket. The rectangle that is bigger and on top of it is the sleeve gear that slides. The big 2.5mm thick rectangle represents the hub (the spline always stays engaged to it) and the hub always is connected with the main shaft. 

## Center Differential with Lock
![[Pasted image 20260930222849.png]]
The carrier is represented by the construction geometry box around the differential. The two lines represent the pinion gears while the two rectangles are the two side gears of the differential. On top, there is a gear that is locked with the carrier so they spin the same speed and a separate gear that is on the rear shaft. 

The rear shaft and the shaft on the rear side gear of the differential should not spin together. The only time they would spin together would be when the lock connects the two gears. 

## Range Sleeve
![[Pasted image 20260930224306.png]]

The big rectangle is the ring with inner teeth connected to the carrier on the planetary with the dotted lines. The rectangle inside of it represents the gear that is always connected to the main shaft. The small rectangle on the bottom is the gear that is always connected to the input shaft/sun gear in the planetary. The larger rectangle on it is the sleeve that slides. 

## Planetary
![[Pasted image 20260930225049.png]]
The inner most rectangle is the sun gear, followed by the space for the planet gears (and its carrier would be connected to the ring around the range sleeve), and the outer most is the ring gear on the planetary which will be fixed and never move. 

## Full Dimensions
With the distinct shafts as solid lines
![[Pasted image 20260930225438.png]]

## Things to Think About
- On the real v1 draft, it is important to think about the fact that there will be gears very close together yet are not on the same shaft. So there must be ample space left between some of the gears (more than here for sure), and that might make the final gears larger (it is a concern if it will scrape the ground).
- On such a small scale technically speaking the transfer case still takes up quite a lot of space on the chassis, a real demo should be at a larger scale for the transfer case, so it is worth considering how big the chassis should be. 
	- ![[Pasted image 20260930230113.png]]
	- Relatively how big the current transfer case sits on the chassis