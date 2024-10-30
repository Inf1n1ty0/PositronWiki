---
title: Bed Leveling
description: 
published: true
date: 2024-10-30T12:38:51.932Z
tags: general care, bed leveling
editor: markdown
dateCreated: 2024-10-30T12:38:51.932Z
---

# Manual Leveling
1. Home all axis, bed should be about 26mm away from nozzle at the endstop position.
2. Use the controlls to position the nozzle in the back middle of the print volume, if you have the latest configs, this will be done automatically in the next step.
3. Use the touch screen to do "`Z_Endstop_Calibration`" - and tram the bed with a piece of paper between it and the nozzle. Lower the bed until the piece of paper *just* catches, and pinches it between the nozzle and the bed.
4. Save the calibration, printer will restart
5. Home all axis again, bed will be at the endstop again, this is normal when homing.
6. On the touch screen, there is a bed leveling option. It will prompt you to level three "Screws", the first one being the back middle, which you just did with the calibration, so you can move to the front left and the front right screw.
7. Using the same piece of paper, adjust the screws until the nozzle and the bed catch/pinch the paper just like it did on the Z Calibration, you want it to catch with about the same amount of force. Do this for both of the front screws.
8. Your bed is now level, as you print, you can live adjust your Z Offset to get better squish incase you calibrated too close or too far, and micro adjust the screws to adjust the tilt of the bed.