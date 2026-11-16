---
date: 2026-11-16
authors:
  - Mo Zhou
sprint: 2
commits:
  - https://github.com/MIE243/v1-chassis/commit/fd4187921e635e04f3c8b2109aee30e688d462d7
tags:
  - "#v1-CAD"
---
This entry is the current position and spec of every gear in the v1 drivetrain. It replaces the table in [[2026-10-30 v1 Chassis Initial Position Spec]]. The v1 master geometry sketch has not been kept up to date, so the positions below were read straight from `v1 Chassis Assembly.SLDASM` as of [v1-chassis@fd41879](https://github.com/MIE243/v1-chassis/commit/fd4187921e635e04f3c8b2109aee30e688d462d7). 

## Changes since [[2026-10-30 v1 Chassis Initial Position Spec]]
- Centre diff moved 10 mm forward, from Z -151.5 to **Z -141.5**. The chassis uses `v1_CenterDiff_Assem`.
- Centre diff front side gear is now `v1_CD_SideF`: same 18T m2.5 gear with a Ø14 bore so it sits around the mainshaft.
- Added the centre diff lock: lock dog, lock collar and lock hub, all 20T m1.25.
- Added the transfer case dog clutches, hubs and sleeves (range and mode) to the table.
- Front and rear axle side gears and spiders are **m1.75** (18T / 12T). The old table listed m2.5. Each diff has **2 spiders**, not 4.
- Chain plane is at Z -91.9. The old table had -92.5.
- Added Y and the axis direction of each gear, since spider and planet positions aren't in the Y = 0 plane.

## Coordinate frame
Same origin as before: the centre of the input shaft (chassis assembly origin).
- **+Z** forward, toward the front axle
- **+X** vehicle left
- **+Y** up
- All shafts lie in the Y = 0 plane.

The position of each gear is its **centre**:
- **Spur gears, dogs, sleeves and hubs:** the middle of the toothed face.
- **Bevel gears:** the centre of the mean pitch circle, on the gear's axis. The diff centre (cone apex) is the shared point all of a diff's bevel axes pass through:
	- Centre diff: (0, 0, -141.5)
	- Front diff: (-63.5, 0, 133.25)
	- Rear diff: (0, 0, -252.75)

**Axis** is the direction the gear's axis points from that apex or face, toward the gear. Planet and spider positions depend on how far the carrier or diff case has turned, so treat their angle around the shaft as arbitrary.

## Gear positions
Specs for each part are in [[#Gear specs]] at the bottom.

### Transfer case

| Gear | SolidWorks part | X (mm) | Y (mm) | Z (mm) | Axis |
| --- | --- | --- | --- | --- | --- |
| Sun (input shaft) | `Gear_m1.25_N29-1` | 0 | 0 | 10.5 | +Z |
| Planet 1 | `Gear_m1.25_N13-1` | -22.996 | 12.658 | 10.5 | +Z |
| Planet 2 | `Gear_m1.25_N13-2` | 0.536 | -26.245 | 10.5 | +Z |
| Planet 3 | `Gear_m1.25_N13-3` | 22.461 | 13.586 | 10.5 | +Z |
| Ring (fixed to range box) | `Ring_m1.25_N55-1` | 0 | 0 | 10.5 | +Z |
| High-range dog (input shaft) | `v1_InDog-1` | 0 | 0 | -32 | +Z |
| Low-range dog (carrier) | `v1_LoDog-1` | 0 | 0 | -17 | +Z |
| Range hub (mainshaft) | `v1_RangeHub-1` | 0 | 0 | -45.5 | +Z |
| Range sleeve (two-band) | `v1_RangeSleeve-1` | 0 | 0 | -42.5 | +Z |
| Mode hub (mainshaft) | `v1_ModeHub-1` | 0 | 0 | -80 | +Z |
| Front dog (drive sprocket face) | `Dog_m1.25_N20-1` | 0 | 0 | -88 | +Z |
| Mode sleeve | `Sleeve_m1.25_N20-1` | 0 | 0 | -85.5 | +Z |

### Chain drive

| Gear | SolidWorks part | X (mm) | Y (mm) | Z (mm) | Axis |
| --- | --- | --- | --- | --- | --- |
| Drive sprocket (mainshaft) | `v1_Sprocket_Drive-1` | 0 | 0 | -91.9 | +Z |
| Front output sprocket | `v1_Sprocket_Front-3` | -63.5 | 0 | -91.9 | +Z |

### Centre diff

| Gear | SolidWorks part | X (mm) | Y (mm) | Z (mm) | Axis |
| --- | --- | --- | --- | --- | --- |
| Side gear, rear output | `v1_CD_Side-1` | 0 | 0 | -154.004 | -Z |
| Side gear, front output | `v1_CD_SideF-2` | 0 | 0 | -128.996 | +Z |
| Spider 1 | `v1_CD_Spider-1` | -17.467 | -6.833 | -141.5 | (-0.931, -0.364, 0) |
| Spider 2 | `v1_CD_Spider-2` | 17.467 | 6.833 | -141.5 | (0.931, 0.364, 0) |
| Lock dog | `v1_LockDog-1` | 0 | 0 | -169.75 | +Z |
| Lock collar | `v1_LockCollar-1` | 0 | 0 | -172.25 | +Z |
| Lock hub | `v1_LockHub-1` | 0 | 0 | -177.75 | +Z |

### Front axle

| Gear | SolidWorks part | X (mm) | Y (mm) | Z (mm) | Axis |
| --- | --- | --- | --- | --- | --- |
| Front pinion | `v1_FD_Pinion-1` | -63.5 | 0 | 104.867 | -Z |
| Front ring (on diff case) | `v1_FD_Ring-1` | -49.308 | 0 | 133.25 | +X |
| Front side gear, left | `v1_AX_Side-1` | -54.664 | 0 | 133.25 | +X |
| Front side gear, right | `v1_AX_Side-2` | -72.336 | 0 | 133.25 | -X |
| Front spider 1 | `v1_AX_Spider-1` | -63.5 | 8.708 | 143.242 | (0, 0.657, 0.754) |
| Front spider 2 | `v1_AX_Spider-4` | -63.5 | -8.708 | 123.258 | (0, -0.657, -0.754) |

### Rear axle

| Gear                     | SolidWorks part  | X (mm)  | Y (mm)  | Z (mm)   | Axis               |
| ------------------------ | ---------------- | ------- | ------- | -------- | ------------------ |
| Rear pinion              | `v1_FD_Pinion-1` | 0       | 0       | -224.367 | +Z                 |
| Rear ring (on diff case) | `v1_FD_Ring-1`   | -14.192 | 0       | -252.75  | -X                 |
| Rear side gear, left     | `v1_AX_Side-3`   | 8.836   | 0       | -252.75  | +X                 |
| Rear side gear, right    | `v1_AX_Side-2`   | -8.836  | 0       | -252.75  | -X                 |
| Rear spider 1            | `v1_AX_Spider-1` | 0       | -13.139 | -251.008 | (0, -0.991, 0.131) |
| Rear spider 2            | `v1_AX_Spider-4` | 0       | 13.139  | -254.492 | (0, 0.991, -0.131) |

Range sleeve is shown at **H** (travel H = -5, N = 0, L = +5 mm). Mode sleeve is shown at **4WD** (2WD = 0, 4WD = -5 mm). The chain is ANSI #25 with 40 links (20 roller + 20 connecting), and the sprocket centres are 63.5 mm apart (10 pitches).

## Ratios

| Stage | Ratio (in : out) | Calculation |
| --- | --- | --- |
| Transfer case, high range (2H / 4H) | 1 : 1 | Sleeve locks mainshaft to input shaft |
| Transfer case, low range (4L) | 2.897 : 1 | 1 + 55/29 (ring fixed, sun in, carrier out) |
| Chain to front output | 1 : 1 | 20T / 20T |
| Centre diff | 1 : 1 | Bevel diff, averages front and rear |
| Final drive, front and rear | 2 : 1 | 30T / 15T |
| **Overall, high range** | **2 : 1** | 50 rpm at the wheels from a 100 rpm input |
| **Overall, low range** | **5.793 : 1** | 17.3 rpm at the wheels from a 100 rpm input |

Checks:
- Sun–planet centre distance is (36.25 + 16.25)/2 = 26.25 mm, which matches the carrier pin radius.
- (29 + 55)/3 = 28 is a whole number, so the 3 equally spaced planets fit.
- 55 = 29 + 2 × 13, so the ring, sun and planets mesh together.

## Gear specs
One row per SolidWorks part. Qty is how many of that part are in the chassis, and "Used as" says where (see [[#Gear positions]]).
- All values were read from each part's equations: 20° pressure angle, no profile shift, and bevel shaft angle 90°.
- A bore of "-" means the part has none: the planets ride on carrier pins, the ring gears bolt to the diff case or range box, and the sleeves slide on their hubs.
- Sprockets are ANSI #25 (6.35 mm pitch), so their pitch Ø is 6.35 / sin(180°/20).

| Part | Used as | Qty | Type | Teeth | Module (mm) | Pitch Ø (mm) | Face width (mm) | Bore (mm) | Pitch cone angle |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| `Gear_m1.25_N29` | Sun (input shaft) | 1 | Spur | 29 | 1.25 | 36.25 | 10 | 8 | - |
| `Gear_m1.25_N13` | Planet | 3 | Spur | 13 | 1.25 | 16.25 | 10 | - | - |
| `Ring_m1.25_N55` | Ring (fixed to range box) | 1 | Internal spur | 55 | 1.25 | 68.75 | 10 | - | - |
| `v1_InDog` | High-range dog (input shaft) | 1 | Dog clutch | 17 | 1.25 | 21.25 | 5 | 8 | - |
| `v1_LoDog` | Low-range dog (carrier) | 1 | Dog clutch | 17 | 1.25 | 21.25 | 5 | 10 | - |
| `v1_RangeHub` | Range hub (mainshaft) | 1 | Splined hub | 17 | 1.25 | 21.25 | 20 | 8 | - |
| `v1_RangeSleeve` | Range sleeve (two-band) | 1 | Shift sleeve (internal) | 17 | 1.25 | 21.25 | 26 | - | - |
| `v1_ModeHub` | Mode hub (mainshaft) | 1 | Splined hub | 20 | 1.25 | 25 | 9 | 14 | - |
| `Dog_m1.25_N20` | Front dog (drive sprocket face) | 1 | Dog clutch | 20 | 1.25 | 25 | 5 | 14 | - |
| `Sleeve_m1.25_N20` | Mode sleeve | 1 | Shift sleeve (internal) | 20 | 1.25 | 25 | 10 | - | - |
| `v1_Sprocket_Drive` | Drive sprocket (mainshaft) | 1 | Roller-chain sprocket | 20 | - (#25, 6.35 pitch) | 40.592 | - | - | - |
| `v1_Sprocket_Front` | Front output sprocket | 1 | Roller-chain sprocket | 20 | - (#25, 6.35 pitch) | 40.592 | - | - | - |
| `v1_CD_Side` | Side gear, rear output | 1 | Straight bevel | 18 | 2.5 | 45 | 9 | 8 | 56.31° |
| `v1_CD_SideF` | Side gear, front output | 1 | Straight bevel | 18 | 2.5 | 45 | 9 | 14 | 56.31° |
| `v1_CD_Spider` | Spider | 2 | Straight bevel | 12 | 2.5 | 30 | 9 | 8 | 33.69° |
| `v1_LockDog` | Lock dog | 1 | Dog clutch | 20 | 1.25 | 25 | 5 | 14 | - |
| `v1_LockCollar` | Lock collar | 1 | Shift sleeve (internal) | 20 | 1.25 | 25 | 10 | - | - |
| `v1_LockHub` | Lock hub | 1 | Splined hub | 20 | 1.25 | 25 | 9 | 8 | - |
| `v1_FD_Pinion` | Front & rear pinion | 2 | Straight bevel | 15 | 2.25 | 33.75 | 12 | 8 | 26.57° |
| `v1_FD_Ring` | Front & rear ring (on diff case) | 2 | Straight bevel | 30 | 2.25 | 67.5 | 12 | - | 63.43° |
| `v1_AX_Side` | Front & rear diff side gears (L + R) | 4 | Straight bevel | 18 | 1.75 | 31.5 | 6 | 8 | 56.31° |
| `v1_AX_Spider` | Front & rear diff spiders | 4 | Straight bevel | 12 | 1.75 | 21 | 6 | 8 | 33.69° |

The same data with the formulas behind it is in `v1_Chassis_Drivetrain_Specs.xlsx` in the v1-chassis repo.
