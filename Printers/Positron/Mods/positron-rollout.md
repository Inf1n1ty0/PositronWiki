---
title: Positron Rollout
description: A macro to prepare the Positron for folding
published: true
date: 2024-11-11T21:19:07.532Z
tags: folding, rollout, travel
editor: markdown
dateCreated: 2024-11-11T21:17:41.019Z
---

# Positron Rollout Macro
This is a macro that can be appended to the end of the `positron_macro.cfg` config file. This macro adds an easy
way to get the Positron ready for travel and has a option menu to unload filament first or simply move all 
axes to their fold up positions.

> Copy and paste the follow text to the end of positron_macro.cfg file
{.is-info}

```
[gcode_macro Positron_Roll_Out]
description:Display options to get Positron ready to pack up
gcode:
  RESPOND TYPE=command MSG="action:prompt_begin Positron abort, not ready yet >>>"
  RESPOND TYPE=command MSG="action:prompt_text POSITRON ROLL OUT"
  RESPOND TYPE=command MSG="action:prompt_footer_button Unload First|_Unload_and_Go"
  RESPOND TYPE=command MSG="action:prompt_footer_button ROLL OUT|_Roll_Out"
  RESPOND TYPE=command MSG="action:prompt_show"
  
[gcode_macro _Roll_Out]
description: moves toolhead and bed to correct positions to be folded up
gcode:
  M300 P100                     ;Button press beep
  RESPOND TYPE=command MSG="action:prompt_end"
  G28 O                         ;Home if not homed
  G90                           ;Set Absolutes
  G1 X135 Y70 Z105 F3600        ;Move to fold up park location
  M84                           ;Disable motors
  M118 Positron, Transform and Roll Out!


[gcode_macro _Unload_and_Go]
description: same as rollout but heats to 230C, unloads filament, cools down, then parks to fold
gcode:
  M300 P100                     ;Button press beep
  RESPOND TYPE=command MSG="action:prompt_end"
  M118 Unloading filament....
  UNLOAD_FILAMENT               ;Activate macro unload filament
  M118 Cooling Hotend Please Wait....
  M106 S255                     ;Max fan for cooling
  M109 S160                     ;Wait until hotend is 160C
  M118 Cooling Hotend to 90C.....
  M109 S90                      ;Wait until hotend is 90C
  _Roll_Out                     ;Move to fold up park location
  TURN_OFF_HEATERS              ;Nozzle heater off
  M106 S0                       ;Part fan off
  ```

---
## Photos of Macro in Use
### From Fluidd web Browser
![rollout_fluidd_image.jpg](/rollout_fluidd_image.jpg)
### Touchscreen Photos
![rollout_photo_macro.jpg](/rollout_photo_macro.jpg)
![rollout_photo_options.jpg](/rollout_photo_options.jpg)
