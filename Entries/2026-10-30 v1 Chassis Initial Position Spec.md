---
date: 2026-10-30
authors:
  - Mo Zhou
sprint: 2
commits:
  - https://github.com/MIE243/v1-chassis/commit/05346374efa3cc5cd24e5675a533f0eb41dff52a
tags:
  - "#v1-CAD"
---
![[Pasted image 20261030213413.png]]

The above sketch is added to master geometry with each sketch point representing the center of a mechanism (with annotation for what it is) on the v1 chassis

## v1 Gear Centre Positions
Origin (0,0) is the center of the input shaft, same as what is on the v1 master geometry CAD file.

| Gear                              | Spec                                         | X (mm)  | Z (mm)   |
| --------------------------------- | -------------------------------------------- | ------- | -------- |
| **Origin**: middle of input shaft | Ø8 × 65 shaft, Z -32.5 to 32.5               | 0       | 0        |
| Sun gear, on the input shaft      | Sun 29T m1.25, pitch Ø36.25                  | 0       | 10.5     |
| Planetary ring                    | Ring 55T internal m1.25, pitch Ø68.75        | 0       | 10.5     |
| Planet 1                          | Planet 13T m1.25, pitch Ø16.25               | 26.25   | 10.5     |
| Planet 2                          | Planet 13T m1.25, pitch Ø16.25               | -13.125 | 10.5     |
| Planet 3                          | Planet 13T m1.25, pitch Ø16.25               | -13.125 | 10.5     |
| Centre diff front side gear       | Side gear 18T m2.5, pitch Ø45                | 0       | -138.996 |
| Centre diff rear side gear        | Side gear 18T m2.5, pitch Ø45                | 0       | -164.004 |
| Centre diff spider 1              | Spider 12T m2.5, pitch Ø30                   | 0       | -151.5   |
| Centre diff spider 2              | Spider 12T m2.5, pitch Ø30                   | 0       | -151.5   |
| Drive sprocket                    | #25 sprocket 20T, pitch Ø40.6                | 0       | -92.5    |
| Front output                      | #25 sprocket 20T, pitch Ø40.6                | -63.5   | -92.5    |
| Front pinion                      | Pinion 15T m2.25, pitch Ø33.75               | -63.5   | 104.867  |
| Front diff case                   | Ring 30T m2.25, pitch Ø67.5 on the diff case | -49.308 | 133.25   |
| Front left side gear              | Side gear 18T m2.5, pitch Ø45                | -50.719 | 133.25   |
| Front right side gear             | Side gear 18T m2.5, pitch Ø45                | -76.281 | 133.25   |
| Front spider 1                    | Spider 12T m2.5, pitch Ø30                   | -63.5   | 133.25   |
| Front spider 2                    | Spider 12T m2.5, pitch Ø30                   | -63.5   | 152.422  |
| Front spider 3                    | Spider 12T m2.5, pitch Ø30                   | -63.5   | 133.25   |
| Front spider 4                    | Spider 12T m2.5, pitch Ø30                   | -63.5   | 114.078  |
| Rear pinion                       | Pinion 15T m2.25, pitch Ø33.75               | 0       | -224.367 |
| Rear diff case                    | Ring 30T m2.25, pitch Ø67.5 on the diff case | -14.192 | -252.75  |
| Rear left side gear               | Side gear 18T m2.5, pitch Ø45                | 12.781  | -252.75  |
| Rear right side gear              | Side gear 18T m2.5, pitch Ø45                | -12.781 | -252.75  |
| Rear spider 1                     | Spider 12T m2.5, pitch Ø30                   | 0       | -252.75  |
| Rear spider 2                     | Spider 12T m2.5, pitch Ø30                   | 0       | -233.578 |
| Rear spider 3                     | Spider 12T m2.5, pitch Ø30                   | 0       | -252.75  |
| Rear spider 4                     | Spider 12T m2.5, pitch Ø30                   | 0       | -271.922 |
