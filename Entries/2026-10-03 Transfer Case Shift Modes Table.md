---
date: 2026-10-03
authors:
  - Mo Zhou
sprint:
commits:
  - https://github.com/MIE243/v0-Initial-Chassis/commit/91f221da4196dbf32fdd99a2036b1aaea57ca8c3
tags:
  - v0-CAD
  - Transfer_Case
---
## Changes since [[2026-10-02 Transfer Case Motion Links Details]] [v0-Initial-Chassis@cba6b21](https://github.com/MIE243/v0-Initial-Chassis/commit/cba6b21e5c7968222faa8d13e6db8d06e76393d7)
- All of the differential mates now gets supressed when differential is locked.
- Added additional gear mate for locked differential so rear shaft spins with the input and main shaft
- Added a 2H Open Suppress folder to suppress a set of mates needed to demonstrate 2H Open on SolidWorks Properly

## Updated Table For Transfer Case Mates Suppression As Of: [v0-Initial-Chassis@91f221d](https://github.com/MIE243/v0-Initial-Chassis/commit/91f221da4196dbf32fdd99a2036b1aaea57ca8c3)
- Note that "Center Differential Gear Mates" refers to the folder of mates with that name.
- Diff Lock Rear Shaft Mate and the folder above cannot both be enabled at the same time, one must be suppressed.
- Note that for 2H Open, you have to suppress a sub folder inside of Center Differential Gear Mates called "2H Open Suppress", this is a SolidWorks only thing because it cannot simulate properly the rear shaft not needing to spin in this case.

| Mode              | Range Sleeve Setting | Mode Sleeve Setting | Differential Lock Setting | Suppressed Mates                                                                                                   |
| ----------------- | -------------------- | ------------------- | ------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| 2H                | 4H                   | RWD                 | Locked                    | Range Sleeve Carrier<br>Mode Sleeve Sprocket<br>Center Differential Gear Mates                                     |
| 4H                | 4H                   | 4WD                 | Locked                    | Range Sleeve Carrier<br>Center Differential Gear Mates                                                             |
| 4L                | 4L                   | 4WD                 | Locked                    | Range Sleeve Input Shaft<br>Center Differential Gear Mates                                                         |
| 4H Open           | 4H                   | 4WD                 | Open                      | Range Sleeve Carrier<br>Diff Lock Carrier<br>Diff Lock Rear Shaft Mate                                             |
| 4L Open           | 4L                   | 4WD                 | Open                      | Range Sleeve Input Shaft<br>Diff Lock Carrier<br>Diff Lock Rear Shaft Mate                                         |
| N                 | N                    | 4WD                 | Locked                    | Range Sleeve Input Shaft<br>Range Sleeve Carrier<br>Diff Lock Carrier<br>Center Differential Gear Mates            |
| Invalid (2H Open) | 4H                   | RWD                 | Open                      | Range Sleeve Carrier<br>Mode Sleeve Sprocket<br>Diff Lock Carrier<br>2H Open Suppress<br>Diff Lock Rear Shaft Mate |
