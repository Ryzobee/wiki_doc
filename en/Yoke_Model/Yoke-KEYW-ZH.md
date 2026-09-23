---
title: "Yoke-KEYW"
description: "Yoke-KEYW Tactile Switch Module"
tags: "Yoke, keys, key"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_KEYW_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-KEYW Tactile Switch Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-KEYW is a tactile switch module designed for 3D-printed creations.  
It connects to a Root controller through a standard interface, allowing users to quickly add button interaction to 3D prints and make static models more interactive and controllable.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## Module Overview & Key Features

Yoke-KEYW includes an illuminated tactile switch. Compared with an ordinary button module, it combines button input and status feedback, simplifying interaction design, reducing wiring, and making installation easier in 3D-printed creations.

| Item | Description |
|---|---|
| Module Interface | RS-Port |
| Power | Supplied by the Root controller |
| Communication | GPIO |
| Compatible Controllers | RootMaker / compatible Root series controllers |

Key features:

- One backlit tactile switch, with support for a keycap
- Suitable for interactive control in 3D-printed models
- Lighting can serve as backlighting or status indication
- Quickly connects to a Root controller through RS-Port
- Quick configuration with Zoner project templates

## Usage Instructions

Before using Yoke-KEYW, make sure the Root controller is flashed with firmware or a project template that supports button control.

### Connect to a Root Controller
Yoke-KEYW connects to a Root controller with an RS-Port cable.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_KEYW_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



Connection precautions:

- Connect or disconnect the module with the power off.
- Check the connector orientation to avoid reversed connections.  

#### Mounting Recommendations:

- Leave sufficient clearance around the button so the enclosure or mechanical parts do not press on it continuously.
- For status indication, use a keycap with a light guide.
- Provide a maintenance opening when mounting inside an enclosed model.
- Use screw posts, clips, or retaining features to keep the module secure during use.

## Power Requirements

| Item | MAX | Type | Min |
|---|---|---|---|
| Supply Current (mA) | 10mA | | |
| Supply Voltage (V) | | 3.3V | |

## Hardware Specifications


| Item | Specification |
| -------- | ------------------------------------------------ |
| Module Model | Yoke-KEYW |
| Module Name | Tactile Switch Module |
| Interface Type | RS-Port |
| Applications | Function control in 3D-printed models, status indication, interactive installations |
| Compatible Controllers | RootMaker / compatible Root series controllers |
| Mounting Method | Mechanical retention / adhesive / screws, depending on the project structure |

## 3D Mounting Files

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_KEYW_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP File ZXYoke-KEYW-V10.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 961 KB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-KEYW-V10.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Frequently Asked Questions

### What if pressing the tactile switch has no effect?

Check the following:

1. Does the button make a clear click when pressed?
2. Is the Root controller powered correctly?
3. Is the module connected to the correct RS-Port?
4. Is the connector orientation correct?
5. Does the firmware support it?


### What if the switch backlight does not turn on?

Possible causes include:

- Physical obstruction.
- The firmware lacks the required logic, or the GPIO for the button light is not configured.
- A faulty data connection.

### Can I hot-plug Yoke-KEYW?

Hot-plugging is not recommended.  
Connect or disconnect the module with the power off to prevent connector short circuits, signal errors, or module damage.  
