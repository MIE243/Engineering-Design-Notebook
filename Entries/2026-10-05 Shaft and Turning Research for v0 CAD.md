---
date: 2026-10-05
authors:
  - Mo Zhou
sprint: 1
commits: []
tags:
  - v0-CAD
---
# Shaft
## Issue
Because we want steering and also the ability to demonstrate 4 wheel drive, we need a special joint between the front axle and the wheels to allow it to still be driven while it is not perfectly perpendicular to the front axle. 

## Possible Solutions

| Joint    | Pros                                    | Cons                                  | Image                                |
| -------- | --------------------------------------- | ------------------------------------- | ------------------------------------ |
| U-Joint  | Cheap, simple                           | At larger angles output speed wobbles | ![[Pasted image 20261005210343.png]] |
| Dogbone  | Very simple, allows some length changes | Can pop out and has slop              | ![[Pasted image 20261005211252.png]] |
| CV Joint | Smooth constant speed                   | Complex                               | ![[Pasted image 20261005211307.png]] |
## Decision
We will use a U joint for these reasons mainly because its simple, while very easy to understand (teaching).

# Steering

## Ackermann Steering
![[Pasted image 20261005212927.png]]
We will use a very simple four bar to steer the car's front wheels. There will be a simple method to adjust the steering angle and no suspension as this is not a part that we are focusing on for our design. 