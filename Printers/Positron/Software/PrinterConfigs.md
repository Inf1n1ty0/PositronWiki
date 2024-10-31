---
title: Positron Configurations
description: Rhere to find the latest printer configs, and a brief on some settings you might need to update.
published: true
date: 2024-10-31T22:30:22.274Z
tags: configs, klipper, calibrate, configuration, calibration
editor: markdown
dateCreated: 2024-08-01T04:12:16.244Z
---

# Positron Configurations

You want the hottest, freshest, bestest configs? Check out the [Positron Config on Github](https://github.com/Positron3D/PositronConfig) to get 'em straight out the oven!

![GitHub Release](https://img.shields.io/github/v/release/Positron3D/PositronConfig?sort=semver&display_name=release&style=for-the-badge&logo=github&logoColor=white&logoSize=auto&labelColor=black)


## Sensorless Homing Sensitivity
We have a middle of the road average for this, but it will vary between printers, so please check this.

Set a value in your klipper console by running:

`SET_TMC_FIELD STEPPER=stepper_x FIELD=SGTHRS VALUE=60`

Then test the value by homing the X axis:

`G28 X`

This will likely cause your printer to home X too early, the higher the number in `VALUE` the higher the sensitivity of the sensorless homing. Re-run this command with a slightly lower value (we recommend reducing by increments of 5), testing in between, until your X axis is reliably (but still nonviolently) homing.

> You may need to periodicly move the bed down a bit, as some older published configurations move up each time you home any axis
{.is-info}


Once you've found a value you're happy with, save it by setting that value in `printer.cfg`:

```properties
[tmc2209 stepper_x]
diag_pin: ^gpio16
driver_SGTHRS: -> UPDATE THIS VALUE <-
```

Repeat this process for the Y axis using:

`SET_TMC_FIELD STEPPER=stepper_y FIELD=SGTHRS VALUE=60`

and:

`G28 Y`

Then save it to `printer.cfg` in the same way:
```properties
[tmc2209 stepper_y]
diag_pin: ^gpio25
driver_SGTHRS: -> UPDATE THIS VALUE <-
```

## Z Endstop
There have been a few iterations of Z homing hardware various versions of the Positron have used, so it's good to make sure you're set up for the right one.

First, in `printer.cfg`, check your `[stepper_z]` `endstop_pin`:

```properties
[stepper_z]
# endstop_pin: probe:z_virtual_endstop  ; IR probe
endstop_pin: gpio3                      ; microswitch endstop
position_endstop: 22                    ; Comment out if not using endstop
```

By default, the `endstop_pin` is set to `gpio3` for the microswitch endstop. If you have not installed a Z-endstop or otherwise wish to attempt using a probe for homing, instead use the line with the `probe:z_virtual_endstop` like so:

```properties
[stepper_z]
endstop_pin: probe:z_virtual_endstop    ; IR probe
# endstop_pin: gpio3                    ; microswitch endstop
# position_endstop: 22                  ; Comment out if not using endstop
```

This will disable the endstop and use the IR (or other bed probe) for homing

> The IR probe has proven unreliable, especially with glass beds. While it can be used for tramming or mesh compensation with a PCB bed, we still recommend homing with the endstop if possible.
{.is-warning}

## Input Shaper
While all releases of the Positron v3.2 have a toolhead accelerometer, the preinstalled sd card wasn't always set up to use it. If input shaping isn't working or is throwing an error, try installing the required dependencies:

1. SSH into your Positron
2. Run:
```sh
sudo apt update
sudo apt install python3-numpy python3-matplotlib libatlas-base-dev libopenblas-dev
~/klippy-env/bin/pip install -v numpy
```
3. In the Klipper console, run `SHAPER_CALIBRATE`
4. Experiment!