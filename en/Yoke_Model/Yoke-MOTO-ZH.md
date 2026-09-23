---
title: "Yoke-MOTO"
description: "Yoke-MOTO DC Motor Control Module"
tags: "Yoke, Motor"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_MOTO_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-MOTO DC Motor Control Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-MOTO is a DC motor control module designed for 3D-printed creations.
It connects to a Root controller through a standard interface, quickly adding motor control to 3D prints for rotation, transmission, and coordinated motion, enabling richer mechanical interaction.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## Module Overview & Key Features

Yoke-MOTO integrates a DC motor driver circuit that directly controls small geared DC motors, fans, motorized mechanisms, and similar loads.
The module supports forward/reverse rotation and PWM speed control for most interactive 3D-printed devices and mechanisms.

| Item | Description |
|---|---|
| Module Interface | RS-Port |
| Power | Supplied by the Root controller |
| Control Signal | GPIO / PWM |
| Compatible Controllers | RootMaker / compatible Root series controllers |

Key features:

- Forward and reverse DC motor control
- PWM speed control
- Suitable for driving mechanisms in 3D-printed models
- Quickly connects to a Root controller through RS-Port
- Drives small geared motors, fans, and other DC loads
- Quick configuration with Zoner project templates

## Usage Instructions

Before using Yoke-MOTO, make sure the Root controller is flashed with firmware or a project template that supports motor control.

### Connect to a Root Controller
Yoke-MOTO connects to a Root controller with an RS-Port cable.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_MOTO_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



Connection precautions:

- Connect or disconnect the module with the power off.
- Check the connector orientation to avoid reversed connections.
- **Important:** Make sure the motor's operating voltage is compatible with the module specifications.

### Mounting

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_MOTO_Wiki_connect_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### Mounting Recommendations:

- Avoid prolonged motor stalls or continuous heavy loads, which may overheat the motor or driver.
- Secure the motor and drivetrain to prevent loosening or shifting during operation.
- Avoid excessive lateral force on the motor shaft when fitting gears, couplings, or other mechanisms.

## Power Requirements

Yoke-MOTO's operating current depends on the motor load. The module includes overcurrent protection (OCP) at approximately 450mA.

| Item | MAX | Type | Min |
|---|---|---|---|
| Supply Current (mA) | 450mA | | |
| Supply Voltage (V) | 5V | | 3.3V |

## Hardware Specifications

| Item | Specification |
| -------- | ------------------------------------------------ |
| Module Model | Yoke-MOTO |
| Module Name | MOTO DC Motor Control Module |
| Interface Type | RS-Port |
| Load Types | Small DC motors / geared DC motors, etc. |
| Applications | Moving mechanisms in 3D prints, rotating mechanisms, interactive installations |
| Compatible Controllers | RootMaker / compatible Root series controllers |
| Mounting Method | Mechanical retention / screws, depending on the project structure |

## 3D Mounting Files

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_MOTO_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP File ZXYoke-MOTO.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 1.63 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-MOTO.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Frequently Asked Questions

### The motor is connected but does not work?

Check the following:

1. Is the Root controller powered correctly?
2. Is the module connected to the correct RS-Port?
3. Is the connector orientation correct?
4. Does the firmware support this module or function?
5. Is the motor stalled?
6. Check the motor specifications. Excessive motor current may trigger the module's OCP.

### The motor rotates in the wrong direction?

Swap the motor's two wires to reverse its direction, or change the direction in the firmware.

### Can I hot-plug Yoke-MOTO?

Hot-plugging is prohibited.  
Connect or disconnect the module with the power off to prevent connector short circuits, signal errors, or module damage.  
