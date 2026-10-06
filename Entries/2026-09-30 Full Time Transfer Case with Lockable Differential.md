---
date: 2026-09-30
authors:
  - Mo Zhou
sprint: 1
commits: []
tags:
  - "#Transfer_Case"
---
## Difference from Part Time
- Input side stays the same, from planetary, input shaft,  range sleeve and also the fixed ring gear on the planetary. 
- The drive sprocket now is always connected to the front side gear of the differential (through a hollow shaft around the mainshaft) instead of having a mode sleeve.
- The mainshaft is always connected to the carrier of the center differential. The front side gear drives the sprocket. 
- The rear side gear in the differential is connected to the rear output shaft.
- The rear output shaft has a lock collar on it that can lock the rear output shaft with the differential carrier so the two spin at the same speed.

## Locking Differential
The lock on the differential exists because now with the center differential, if the front wheels are stuck on ice or some not grippy surface, without the lock the front spins and the rear only gets the same small torque the front can hold, so the vehicle would be stuck. 
### Carrier
- The carrier has the cross pin that the pinions of the differential spin on
- The pinions always orbit at carrier speed. 
- When both of the side gears spins at the same speed, the carrier will also spin at the same speed as them since neither pinion spins and their orbit speed matches the speed of the two side gears
- When the side gears spin at different speeds, the pinions will also spin on their rotation axis, the carrier still rotates, but now at the average of the two side gear speeds, so it is not the same speed as either side gear. 
### Lock Collar
- The lock collar is always connected to the rear output shaft and always spins with it.
- When locking, it will slide over outward facing dog teeth on the back of the carrier using its own inward facing teeth so the carrier and the rear output shaft is forced to spin at the same speed. In practice, this stops the pinions from spinning (they still orbit), and thus both side gears will spin at the same speed (and the same speed as the mainshaft).
- In N, the lock collar is locked to the carrier
### Torque Split
- With differential open, the front and rear outputs both get the same torque
- With differential locked, the torque distribution between front and rear outputs depends on traction

## Why Differential?
The center differential fixes wheel slip between the front vs rear axle because during a turn the front axle will travel a bigger circle than the rear axle. 

## To Think About
- It may be possible to showcase both part time and full time transfer cases by adding a mode sleeve between the front side gear of the center differential and the sprocket, exactly how it would work would be like the following table:

| Showcase                | Range | Lock collar | Mode sleeve | Result                                                                 |
| ----------------------- | ----- | ----------- | ----------- | ---------------------------------------------------------------------- |
| Part-time 2H            | H     | On          | Off         | Rear only                                                              |
| Part-time 4H            | H     | On          | On          | Front + rear locked                                                    |
| Part-time 4L            | L     | On          | On          | Front + rear locked, low range                                         |
| Full-time 4H            | H     | Off         | On          | Front + rear through open differential                                     |
| Full-time 4L (optional) | L     | Off         | On          | Open differential in low range                                             |
| **Invalid**             | any   | **Off**     | **Off**     | **Nothing driven**: the front side gear freewheels, and the rear gets zero torque |
- The combined build has three shifts (range, mode and lock collar). A possible interlock may be needed to prevent the invalid situation from happening. But keeping the invalid situation could still be used for teaching as it can be very easy to see the differential in action. 