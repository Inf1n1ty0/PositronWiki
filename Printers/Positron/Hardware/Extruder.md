---
title: Legacy Extruder
description: Extruder Guide for v3.2.0 - v3.2.1
published: true
date: 2024-11-16T06:03:47.522Z
tags: 
editor: markdown
dateCreated: 2024-11-15T17:51:07.879Z
---

# Extruder Assembly Guide
This guide is for extruder hardware kit that was shipped with the Positron v3.2.0 and v3.2.1 (Batch 1 and 2)

---

![extruder_transp.png](/extruderguide/extruder_transp.png)

---
## Required Parts
### Hardware
> Many of these parts will be in a bag labeled Extruder Kit
{.is-info}

- Bearing, MF148ZZ
- Machine Screw, BHCS, M3x25
- M3x3 Set Screw
- Spider Shaft
- Primary Gear
- Bushing, POM, 8x4x11
- Idler Gear, Orbiter 2
- Shaft, 4x16
- Thumbscrew, M3x30
- Spring, 1x5.9x11.3mm
- Bearing, MR148ZZ
- ECAS04 Bowden Coupler
- Shim Washer, 3x6x0.5mm
- Heat set Insert, Brass, M3x6x5
- 3x Heat set Insert, Brass, M2.5x3x4
- 4x Machine Screw, BHCS, M2.5x18
- 2x Self-tapping Screw, M2x10
- Z Endstop Micro Switch and Cable
### Printed Parts
List of printed parts to for the extruder assembly
- Extruder Main Body 
- Extruder Motor Plate
- Extruder Bottom Plate
- Extruder Guidler

STL models can be found on the [Positron Printed Parts Github](https://github.com/Positron3D/Positron/tree/main/Printed%20Parts%20%26%20CAD%20Models/Current%20Release%20Printed%20Parts/Extruder) 
> Models have not been scaled to account for material shrinkage
{.is-info}

![extruder_parts_transp.png](/extruderguide/extruder_parts_transp.png)

# Assemble
## Prepare the Printed Parts
> Install heat set inserts into the printed parts
{.is-info}

Parts Needed:
- 1x Heat set Insert, Brass, M3x6x5
- 3x Heat set Insert, Brass, M2.5x3x4
- Extruder Guidler
- Extruder Main Body

---

### Guilder
![guilder.gif](/extruderguide/guilder.gif)

- Install the M3x6x5 heat set insert into the printed guidler.

### Extruder Main Body
> Batch 1 Extruder Main Body did not use heat set insert but had screws that threaded directly into the printed part.
{.is-info}

![main_body_hs.gif](/extruderguide/main_body_hs.gif)

- Install all three M2.5x3x4 heat set inserts into the printed extruder main body.

---

## Motor Plate and Planetary Gear Shaft
> For all the M2.5 screws, please use the included LDO screwdriver.
{.is-warning}

Parts Needed:
- 1x Bearing, MF148ZZ
- 1x M3x3 Set Screw
- 1x Spider Shaft
- 1x Primary Gear
- 1x Bearing, MR148ZZ
- Extruder Motor Plate
![motor_plate_1_0.png](/extruderguide/motor_plate_1_0.png)

---

### Install CNC Shaft
![motor_plate_1_0.gif](/extruderguide/motor_plate_1_0.gif)
- Place the MF148ZZ bearing into the hole of the printed motor plate and be sure it sits
flush or below the surface of the part.

---

![motor_plate_2.gif](/extruderguide/motor_plate_2.gif)
- Insert the shaft through the hole of the bearing.

### Install Primary Gear
---
![motor_plate_3.gif](/extruderguide/motor_plate_3.gif)
- Slide the Primary Gear onto the CNC Shaft.
- Line up the hole in the Gear with the flat spot on the CNC Shaft.
- Screw in the Set Screw through the gear and stop right before it touches the flat spot. 
- Now slide the gear all the way down the CNC shaft until the Set Screw hits the end of the flat spot.
- Tightened down the Set Screw until the gear doesn't move, the height of the gear will be adjusted later.
- Place the MR148ZZ bearing on the end of the shaft and get ready for the next step.

---

## Install Lower Half

Parts Needed:
- 3x Machine Screw, BHCS, M2.5x18
- Extruder Main Body
- Extruder Bottom Plate

![lower_complete.png](/extruderguide/lower_complete.png)

---
### Main Extruder Body
![lower_1_2.gif](/extruderguide/lower_1_2.gif)
- Combine the Extruder Motor Plate and Extruder Main Body.
- Flip over for next step.

---

### Install Extruder Bottom Plate
![lower_2.gif](/extruderguide/lower_2.gif)
- Cover the Extruder Main Body with the Extruder Bottom Plate and press it flat. If it does not
sit flat press the MR148ZZ bearing into the Extruder Bottom Plate first.
- Secure Extruder Bottom Plate with three M2.5x18 BHCS Screws
> Batch 1 uses three M2.5x10 BHCS Screws and only taps into printed part.
{.is-info}

---

## Prepare the Extruder Guidler

Parts Needed:
- 1x Bushing, POM, 8x4x11
- 1x Idler Gear, Orbiter 2
- 1x Shaft, 4x16
- Extruder Guidler

![guidler_1_1.gif](/extruderguide/guidler_1_1.gif)
- Place the bushing into Idler Gear.
- Rotate Extruder Guidler so larger opening is facing up.
- Position the Idler Gear into the opening of the Extruder Guidler and secure with the 4x16 Shaft (Smooth end first)
---
## Check Filament Path

Parts Needed:
- Piece of filament
- Assembled Extruder Body

![filament_path.png](/filament_path.png)
- First loosen the M3x3 Set Screw so the Primary Gear can slide up and down.
- Insert a piece of filament as shown in above photo.
- Align the Primary Gear so the filament is centered and tighten down the M3x3 Set Screw.

---

## Install the Extruder Guidler

Part Needed:
- 1x Machine Screw, BHCS, M3x25
- 1x Machine Screw, BHCS, M2.5x18
- Assembled Extruder Main Body
- Extruder Guidler
![guilder_install_4_1.png](/guilder_install_4_1.png)

---

### Secure Guilder
![guilder_install_1.gif](/guilder_install_1.gif)
- Position the Extruder Guidler into the Extruder Main Body. 
- Secure with a M3x25 BHCS Screw. The screw taps into the Extruder Bottom plate.

---

### Anchor Motor Plate
![guilder_install_2_2.gif](/guilder_install_2_2.gif)
- Secure Extruder Motor Plate with a M2.5x18 BHCS Screw. Screw taps directly into the printed parts.

---

## Install the Bowden Coupler

Parts Needed:
- 1x ECAS04 Bowden Coupler
- Assembled Extruder Body

![bowden_coupler_1_1.gif](/bowden_coupler_1_1.gif)

- Remove any rubber from the Bowden Coupler
- Install the Bowden Coupler into the extruder. The Bowden Coupler flange should be flush with the Extruder Body.

---

## Install the Thumbscrew

Parts Needed:
- 1x Thumbscrew, M3x30
- 1x Spring, 1x5.9x11.3mm
- 1x Shim Washer, 3x6x0.5mm
- Assembled Extruder Body

![thumbscrew.gif](/thumbscrew.gif)

- While holding the Thumbscrew, drop the Spring onto the bolt end followed by the Shim Washer. 
- Insert Thumbscrew from opposite side of the Guidler and thread into the Heat Set insert until Thumbscrew head is flush with the printed part above it. 

---

## Install the Endstop

Parts Needed:
- 2x Self-tapping Screw, M2x10
- 1x Z Endstop Micro Switch and Cable
- Assembled Extruder Body





