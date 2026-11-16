---
date: 2026-11-16
authors:
  - Mo Zhou
sprint: 2
commits:
  - https://github.com/MIE243/v1-chassis/commit/fd4187921e635e04f3c8b2109aee30e688d462d7
tags:
  - "#v1-CAD"
  - "#BOM"
---
A first, rough bill of materials for the v1 chassis, checked against the **Total Cost ≤ 300 CAD** and **Manufacturability** targets in Engineering Specification v1. The detailed CAD isn't finished, so this is an estimate only.
- Parts already modelled in [v1-chassis@fd41879](https://github.com/MIE243/v1-chassis/commit/fd4187921e635e04f3c8b2109aee30e688d462d7) are marked **Yes** under *In CAD*. Their gear specs and positions are in [[2026-11-16 v1 Chassis Gear Specs and Positions]].
- Housings, supports, shafts, bearings, fasteners and guards don't exist in CAD yet (**No**). Their sizes and costs are ballpark guesses.

## How costs were estimated
- **3D-printed parts in CAD:** part volume read from SolidWorks × about $0.025 per cm³. That rate assumes FDM PETG/PLA at about $25/kg, roughly 0.75 g printed per cm³ of solid (walls plus 20–30 % infill), and about 25 % extra for failed prints and supports.
- **3D-printed parts not in CAD yet:** a guessed volume at the same rate.
- **Purchased parts:** rough Canadian online retail prices (Amazon.ca, Pololu, McMaster-equivalent) for the pack size you'd actually buy. These are not quotes.
- **Laser cutting:** material cost only, assuming makerspace access.
- All costs are line totals in CAD.

## Cost summary

| Section                                         | Est. cost (CAD) |
| ----------------------------------------------- | --------------- |
| Input and power                                 | $87.50          |
| Transfer case                                   | $14.60          |
| Chain drive                                     | $12.50          |
| Centre diff                                     | $5.40           |
| Front and rear axles (same parts, qty for both) | $7.40           |
| Steering and wheels                             | $28.30          |
| Shafts, bearings and couplers                   | $72.00          |
| Chassis, supports and guards                    | $40.00          |
| Fasteners and small hardware                    | $41.00          |
| **Total**                                       | **$308.70**     |

This comes out **about $9 over the $300 target**. Most of the money is in the motor and power parts (about $88) and in shafts, bearings and couplers (about $72). All the printed parts together cost under $50. Easy places to cut:
- Run the motor from a lab bench supply instead of IN-05 and IN-06 (saves about $24).
- Swap some 608 bearings for printed or bronze bushings on slow shafts (saves about $5–10).
- Use the hand crank only, with no motor (saves about $70, but the input is then manual).

## Bill of materials

### Input and power

| ID    | Item                   | Qty | Specification                                                                          | Source / fabrication method               | Est. cost (CAD) | In CAD      |
| ----- | ---------------------- | --- | -------------------------------------------------------------------------------------- | ----------------------------------------- | --------------- | ----------- |
| IN-01 | DC gearmotor           | 1   | 25D metal gearmotor, 12 V, ~100 rpm (≈99:1), 4 mm D-shaft                              | Purchased (Pololu or equivalent)          | $55.00          | Placeholder |
| IN-02 | Motor mount            | 1   | Face mount for 25D motor, M3                                                           | 3D printed (FDM PETG)                     | $0.50           | No          |
| IN-03 | Slip clutch            | 1   | ~0.5 N·m friction torque limiter: 2 printed plates, cork/felt pad, spring, M3 adjuster | Custom: 3D printed + purchased spring/pad | $4.00           | No          |
| IN-04 | Motor coupler          | 1   | Flexible beam coupler, 4 mm to 8 mm                                                    | Purchased                                 | $4.00           | No          |
| IN-05 | Power supply           | 1   | 12 V 2 A wall adapter, 5.5 × 2.1 mm barrel                                             | Purchased                                 | $12.00          | No          |
| IN-06 | Speed control + switch | 1   | PWM DC motor speed controller, rocker switch, barrel jack, hook-up wire                | Purchased                                 | $12.00          | No          |
|       | **Subtotal**           |     |                                                                                        |                                           | **$87.50**      |             |

### Transfer case

| ID | Item | Qty | Specification | Source / fabrication method | Est. cost (CAD) | In CAD |
| --- | --- | --- | --- | --- | --- | --- |
| TC-01 | Sun gear | 1 | Spur 29T m1.25, 10 face, Ø8 bore | 3D printed (FDM PETG, 0.12 mm layers; resin if the m1.25 mesh is rough) | $0.20 | Yes |
| TC-02 | Planet gears | 3 | Spur 13T m1.25, 10 face | 3D printed (FDM PETG, 0.12 mm layers; resin if the m1.25 mesh is rough) | $0.20 | Yes |
| TC-03 | Ring gear | 1 | Internal 55T m1.25, 10 face | 3D printed (FDM PETG, 0.12 mm layers; resin if the m1.25 mesh is rough) | $0.30 | Yes |
| TC-04 | Planet carrier | 1 | Carrier plate, 3 pins on Ø52.5 circle | 3D printed (FDM PETG) | $0.40 | Layout only |
| TC-05 | Planet pins | 3 | Ø3 × 16 mm steel dowel pin | Purchased | $3.00 | No |
| TC-06 | High-range dog | 1 | Dog 17T m1.25 (CAD includes input-shaft stub) | 3D printed (FDM PETG) | $0.20 | Yes |
| TC-07 | Low-range dog | 1 | Dog 17T m1.25 on carrier, Ø65 | 3D printed (FDM PETG) | $0.90 | Yes |
| TC-08 | Range hub | 1 | Hub 17T m1.25 × 20 (CAD includes mainshaft section) | 3D printed (FDM PETG) | $0.30 | Yes |
| TC-09 | Range sleeve | 1 | Internal 17T m1.25, two-band, 26 long | 3D printed (FDM PETG) | $0.20 | Yes |
| TC-10 | Mode hub | 1 | Hub 20T m1.25 × 9, Ø14 bore | 3D printed (FDM PETG) | $0.20 | Yes |
| TC-11 | Front dog | 1 | Dog 20T m1.25 × 5, Ø14 bore | 3D printed (FDM PETG) | $0.20 | Yes |
| TC-12 | Mode sleeve | 1 | Internal 20T m1.25 × 10 | 3D printed (FDM PETG) | $0.20 | Yes |
| TC-13 | Shift forks + rails | 2 | Range and mode forks, Ø4 steel rail, ball detent (3 mm ball, spring, M3 set screw) | Custom: 3D printed forks + purchased rod/detent | $5.30 | No |
| TC-14 | Transfer case housing | 1 | 2-piece, bearing pockets, viewing window | 3D printed (FDM PETG) | $3.00 | No |
| | **Subtotal** | | | | **$14.60** | |

### Chain drive

| ID | Item | Qty | Specification | Source / fabrication method | Est. cost (CAD) | In CAD |
| --- | --- | --- | --- | --- | --- | --- |
| CH-01 | Drive sprocket | 1 | ANSI #25, 20T | 3D printed (FDM PETG) | $0.20 | Yes |
| CH-02 | Front output sprocket | 1 | ANSI #25, 20T (CAD includes front shaft) | 3D printed (FDM PETG) | $0.30 | Yes |
| CH-03 | Roller chain | 1 | ANSI #25, 40 links (254 mm) + master link | Purchased | $12.00 | Yes |
| | **Subtotal** | | | | **$12.50** | |

### Centre diff

| ID | Item | Qty | Specification | Source / fabrication method | Est. cost (CAD) | In CAD |
| --- | --- | --- | --- | --- | --- | --- |
| CD-01 | Side gear, rear | 1 | Bevel 18T m2.5, Ø8 bore | 3D printed (FDM PETG) | $0.20 | Yes |
| CD-02 | Side gear, front | 1 | Bevel 18T m2.5, Ø14 bore | 3D printed (FDM PETG) | $0.20 | Yes |
| CD-03 | Spider gears | 2 | Bevel 12T m2.5, Ø8 bore | 3D printed (FDM PETG) | $0.20 | Yes |
| CD-04 | Diff case | 1 | 2-piece case carrying cross pin | 3D printed (FDM PETG) | $0.80 | Layout only |
| CD-05 | Diff lock (dog, collar, hub) | 1 | 20T m1.25 set: dog × 5, collar × 10, hub × 9 | 3D printed (FDM PETG) | $0.30 | Yes |
| CD-06 | Lock shift fork + rail | 1 | Fork, Ø4 rail, detent | 3D printed (FDM PETG) + purchased rod | $2.20 | No |
| CD-07 | Centre diff housing | 1 | Bearing supports + guard mounts | 3D printed (FDM PETG) | $1.50 | No |
| | **Subtotal** | | | | **$5.40** | |

### Front and rear axles (same parts, qty for both)

| ID | Item | Qty | Specification | Source / fabrication method | Est. cost (CAD) | In CAD |
| --- | --- | --- | --- | --- | --- | --- |
| AX-01 | Pinion | 2 | Bevel 15T m2.25, Ø8 bore | 3D printed (FDM PETG) | $0.40 | Yes |
| AX-02 | Ring gear | 2 | Bevel 30T m2.25, bolts to diff case | 3D printed (FDM PETG) | $1.30 | Yes |
| AX-03 | Side gears | 4 | Bevel 18T m1.75, Ø8 bore | 3D printed (FDM PETG) | $0.30 | Yes |
| AX-04 | Spider gears | 4 | Bevel 12T m1.75, Ø8 bore | 3D printed (FDM PETG) | $0.20 | Yes |
| AX-05 | Diff cases | 2 | Case + cross pin bore, ring bolt pattern | 3D printed (FDM PETG) | $1.20 | No |
| AX-06 | Axle housings | 2 | Pinion + case bearing supports | 3D printed (FDM PETG) | $4.00 | No |
| | **Subtotal** | | | | **$7.40** | |

### Steering and wheels

| ID | Item | Qty | Specification | Source / fabrication method | Est. cost (CAD) | In CAD |
| --- | --- | --- | --- | --- | --- | --- |
| ST-01 | Front wheels | 2 | Ø100 × 40, 15 % infill | 3D printed (FDM PETG) | $6.60 | Yes |
| ST-02 | Rear wheels | 2 | Ø100 (CAD includes half-shaft) | 3D printed (FDM PETG) | $10.00 | Yes |
| ST-03 | Tyres | 4 | TPU printed tyre or Ø100 rubber O-ring | 3D printed (TPU) or purchased | $5.00 | No |
| ST-04 | Steering arms | 2 | Left + right | 3D printed (FDM PETG) | $0.70 | Yes |
| ST-05 | Arm holders | 2 | Left + right | 3D printed (FDM PETG) | $0.60 | Yes |
| ST-06 | Tie arm | 1 | 171.8 long | 3D printed (FDM PETG) | $0.20 | Yes |
| ST-07 | Front axles + U-joints | 2 | Left + right, printed U-joint yokes | 3D printed (FDM PETG) | $0.20 | Yes |
| ST-08 | Steering + U-joint pins | 6 | 2 steering pins (printed in CAD) → Ø3 steel; 4 × Ø1.5 U-joint cross pins | Purchased (dowel pins / steel wire) | $3.00 | Partly |
| ST-09 | Wheel markers | 4 | High-contrast stickers for speed comparison (D2) | Purchased / printed on paper | $2.00 | No |
| | **Subtotal** | | | | **$28.30** | |

### Shafts, bearings and couplers

| ID | Item | Qty | Specification | Source / fabrication method | Est. cost (CAD) | In CAD |
| --- | --- | --- | --- | --- | --- | --- |
| SB-01 | Steel shaft stock | 2 | Ø8 h6 rod × 500 mm (input, mainshaft, driveshafts, half-shafts, cross pins ≈ 1.1 m) | Purchased; cut by hacksaw, flats filed for set screws | $16.00 | Partly (some shafts are printed into parts) |
| SB-02 | Hollow front output tube | 1 | Ø14 × 1 mm aluminium tube × 300 mm | Purchased; cut to length | $8.00 | No |
| SB-03 | Ball bearings | 20 | 608-2RS, 8 × 22 × 7 | Purchased (10-packs) | $18.00 | No |
| SB-04 | Thin-section bearings | 4 | 6802-2RS, 15 × 24 × 5 (diff cases, hollow output) | Purchased | $10.00 | No |
| SB-05 | Module couplers | 4 | 8 mm to 8 mm jaw coupler (front + rear driveshafts, quick module swap) | Purchased | $12.00 | No |
| SB-06 | Shaft collars | 10 | 8 mm, M3 set screw | Purchased | $8.00 | No |
| | **Subtotal** | | | | **$72.00** | |

### Chassis, supports and guards

| ID | Item | Qty | Specification | Source / fabrication method | Est. cost (CAD) | In CAD |
| --- | --- | --- | --- | --- | --- | --- |
| CS-01 | Base plate | 1 | 500 × 250, 6 mm plywood or 5 mm acrylic | Laser cut (makerspace) | $15.00 | No |
| CS-02 | Module supports / brackets | 8 | Pillow-block style mounts, slotted for M3 to base | 3D printed (FDM PETG) | $2.00 | No |
| CS-03 | Clear safety guards | 1 | 2 mm clear acrylic covers over every gear mesh and the chain | Laser cut + printed standoffs | $20.00 | No |
| CS-04 | Rubber feet | 4 | Self-adhesive bumpers | Purchased | $3.00 | No |
| | **Subtotal** | | | | **$40.00** | |

### Fasteners and small hardware

| ID | Item | Qty | Specification | Source / fabrication method | Est. cost (CAD) | In CAD |
| --- | --- | --- | --- | --- | --- | --- |
| FH-01 | M3 screw kit | 1 | M3 SHCS 6–30 mm, nuts, washers (~300 pcs) | Purchased | $15.00 | No |
| FH-02 | Heat-set inserts | 50 | M3 brass inserts for printed parts | Purchased (100-pack) | $10.00 | No |
| FH-03 | Set screws | 30 | M3 × 4 cup point, gear hubs to shafts | Purchased | $5.00 | No |
| FH-04 | Retaining rings | 1 | 8 mm E-clip / circlip assortment | Purchased | $6.00 | No |
| FH-05 | Shim washers | 20 | 8 × 14 × 0.5 mm, bearing spacing | Purchased | $5.00 | No |
| | **Subtotal** | | | | **$41.00** | |

## Notes for the detailed CAD
- Several parts have a shaft modelled into the printed part: `v1_InDog`, `v1_RangeHub`, `v1_LockHub`, `v1_Sprocket_Front` and the rear wheels. The BOM assumes these become Ø8 steel shafts (SB-01) with printed hubs fixed by M3 set screws and heat-set inserts. Printed shafts would be the weak point under the 2.5 N·m durability load.
- The planet carrier, centre diff carrier and axle diff cases are only layout parts so far. All housings, module supports and guards still need to be modelled.
- SB-05 couplers sit between modules so one module can be removed with a single tool (Modular Assembly target).
- CS-03 guards cover every gear mesh and the chain but stay clear, to meet the Moving-Part Safety target.
