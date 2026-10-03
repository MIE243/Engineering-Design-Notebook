---
date: 2026-10-02
authors:
  - Mo Zhou
sprint:
commits: []
tags:
  - v0-CAD
  - Transfer_Case
---
## Range Sleeve [v0-Initial-Chassis@19e655e](https://github.com/MIE243/v0-Initial-Chassis/commit/19e655ea713422ab6e021b2050a910ca9c7310d1)
Mode can be selected with the motion controller "Range Sleeve Shifter"
For now you will need to suppress certain mates so motion matches what is in mode

| Mode | Active Mates                                                                       | Image                                |
| ---- | ---------------------------------------------------------------------------------- | ------------------------------------ |
| N    | Range Sleeve Slide Distance<br>Range Sleeve Main Shaft                             | ![[Pasted image 20261002171738.png]] |
| 4L   | Range Sleeve Slide Distance<br>Range Sleeve Main Shaft<br>Range Sleeve Carrier     | ![[Pasted image 20261002171838.png]] |
| 4H   | Range Sleeve Slide Distance<br>Range Sleeve Main Shaft<br>Range Sleeve Input Shaft | ![[Pasted image 20261002171930.png]] |

## Mode Sleeve [v0-Initial-Chassis@8d2e0eb](https://github.com/MIE243/v0-Initial-Chassis/commit/8d2e0eb6a4c91c05214be72800e0737a6435c3f9)
Select with "Mode Sleeve Shifter"

| Mode | Active Mates                                                                 | Image                                |
| ---- | ---------------------------------------------------------------------------- | ------------------------------------ |
| RWD  | Mode Sleeve Slide Distance<br>Mode Sleeve Main Shaft                         | ![[Pasted image 20261002172956.png]] |
| 4WD  | Mode Sleeve Slide Distance<br>Mode Sleeve Main Shaft<br>Mode Sleeve Sprocket | ![[Pasted image 20261002172943.png]] |
## Differential Lock [v0-Initial-Chassis@b319f99](https://github.com/MIE243/v0-Initial-Chassis/commit/b319f99024f48f4e49ea9cb5e311c171d16a72b4)
Select with "Differential Lock Shifter"

| Mode   | Active Mates                              | Image                                |
| ------ | ----------------------------------------- | ------------------------------------ |
| Open   | Diff Lock Rear Shaft                      | ![[Pasted image 20261002175811.png]] |
| Locked | Diff Lock Rear Shaft<br>Diff Lock Carrier | ![[Pasted image 20261002175834.png]] |

## Full Assembly With Mates
![[Pasted image 20261002175945.png]]

## One CAD Change
- The CAD yesterday kept rear shaft and the side gear on the rear shaft side in the differential as separate when they should be connected together 

## To Think About
- The rear shaft thickness then also depends on the thickness of the shaft going into the rear differential, unless you manufacture them separately and figure out a way to lock the two together (which is very possible and helps with 3D printing manufacturability as well)
## NOTE
- ON 2026-10-03 changes were made to the motion links to avoid the assembly not spinning at all in a locking mode because SolidWorks cannot properly simulate the idea of differential gears not spinning while the carrier is rotating at the same time. 
- REFER TO THE ENTRY [[2026-10-03 Transfer Case Shift Modes Table]] FOR UPDATED TABLE OF MATES TO ENABLE FOR EACH TRANSFER CASE MODE