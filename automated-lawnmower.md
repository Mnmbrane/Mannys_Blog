---
layout: page
title: Automated Lawnmower
permalink: /automated-lawnmower/
---

This is the main project page for the Automated Lawnmower. I will keep this page updated with the overall project direction, architecture, and what is left to build.

## TODO

| Status | Task |
| --- | --- |
| TODO | Confirm motor driver hardware and power budget for drive + steering + rotary blade |
| TODO | Bring up STM32 firmware project and validate PWM output for steering actuator |
| TODO | Add STM32 motor control for drive motor (start/stop/speed ramp) |
| TODO | Add STM32 control path for rotary blade motor with arming and safe stop states |
| TODO | Define and test manual control commands to STM32 (steer, throttle, blade enable) |
| TODO | Implement watchdog and emergency-stop behavior on STM32 for motor/blade safety |
| TODO | Integrate ESP32-S3 Sense camera pipeline and packet format for base-station streaming |
| TODO | Verify end-to-end link: mower camera frames sent from ESP32-S3 Sense to base station |
| TODO | Run bench tests of steering + drive + blade control before field testing |

## Daily Updates

I will add one static page per work day and link it here.

- [March 1, 2026 - Initial Project Setup]({{ '/lawnmower/updates/2026-03-01/' | relative_url }})

## Architecture Overview

Current scope is focused on mower motor and control systems.

1. STM32 (On-Mower Control MCU): primary real-time control of steering, drive motor, and rotary blade motor.
2. Motor/Power Subsystem: motor drivers, power distribution, blade arming path, and hardware safety cutoff.
3. ESP32-S3 Sense (On-Mower Vision MCU): captures/processes camera data and sends it to the base station.
4. Base Station (External, owned by teammate): receives camera data stream and handles higher-level processing/UI.
5. Control Interface: command channel to STM32 for steering, speed, and blade control with fail-safe behavior.

As implementation progresses, this section will be updated with protocol details, command formats, and control diagrams.
