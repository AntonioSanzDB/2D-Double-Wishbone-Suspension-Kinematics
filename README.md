# 2D Kinematics Study Double Wishbone Suspension

## Overview
This project consist in a 2D Kinematic Simulation of a Front Double Wishbone Suspension system, commonly used in Formula SAE (FSAE). 

The project utilizes SolidWorks Sketch Blocks to create a skeleton. This allows for real-time analysis of geometric variables like Linear Displacement, Camber Gain and other parameters

---

## Technical Specifications

### Suspension Hardpoints
The model is defined by specific $X$ and $Y$ coordinates relative to the Car Centerline ($X=0$) and Ground ($Y=0$).

| Pivot Point | X-Coordinate (mm) | Y-Coordinate (mm) |
| :--- | :---: | :---: |
| Chassis Upper (UCA) | $180$ | $320$ |
| Chassis Lower (LCA) | $150$ | $160$ |
| Upright Upper (BJ) | $490$ | $305$ |
| Upright Lower (BJ) | $530$ | $165$ |

### Component Blocks
* Wishbones: Modeled as rigid blocks to maintain constant length.
* Tire and body: A composite block chasis body and tire profile.
* Ground and Center line: Fixed references .
![double wishbone sketch](https://github.com/user-attachments/assets/a5f4454a-50ee-4b3a-9f87-fe25d1bbe6e7)

---

##  Motion Analysis & Simulation
Using the SolidWorks Motion Manager, the system is subjected to a vertical displacement study to observe dynamic behavior.

![kinematics-analysis](https://github.com/user-attachments/assets/82901bfb-beff-45a5-b113-751b27f0b510)

### Simulation Parameters:
* Linear Spring: Applied to simulate the coilover assembly between the LCA and Chassis.
* External Force* A vertical force applied at the tire contact patch center.
* Travel Range: $\pm 25\text{mm}$ from Static Ride Height.

---

## Key Results
The kinematic study focuses on the following outputs:
![displacement-plot](https://github.com/user-attachments/assets/147db844-7488-4620-b4dd-965d4053b29a)
1. Linear displacement: Shows the vertical travel of the wheel and is use for calculating the total wheel travel, chamber gain, roll center migration (low movement in roll center means more stability) and track Scrub.
Based on the data we can deduce that the tire will gain negative camber, because of large displacement cycle the tire will create track scrub increasing temperature and wear.
3. Camber Curve: The relationship between wheel travel and camber angle. (Target: Achieve negative camber gain in bump to compensate for body roll). For every 15mm of bump tire will tilt about 1^\circ of negative camber.
4. Instant Center (IC): Intersection of the UCA and LCA projected lines.
5. Roll Center (RC): The theoretical point about which the sprung mass rotates.
