---
title: "Yoke-TRGBW"
description: "Yoke-TRGBW RGBW Lighting Module"
tags: "Yoke, LEDs, RGBW"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-TRGBW 3x RGBW Lighting Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-TRGBW is an RGBW lighting module designed for 3D-printed creations, including illuminated models, status indicators, mood lighting, interactive installations, and desktop ornaments.  
It connects to a Root controller through a standard interface, quickly adding controllable lighting effects to 3D prints and enhancing the presentation and interactivity of static models.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## Module Overview & Key Features

Yoke-TRGBW integrates RGBW LEDs with independent white channels in addition to standard RGB, providing more natural white light, softer fill lighting, and richer color mixing.

| Item | Description |
|---|---|
| Module Interface | RS-Port |
| Power | Supplied by the Root controller |
| Control Signal | Single-wire lighting control signal |
| Communication | Digital LED strip control protocol |
| Compatible Controllers | RootMaker / compatible Root series controllers |

Key features:

- Three LEDs with four-channel RGBW lighting
- Suitable for illumination inside 3D-printed models
- Mood lighting, status lights, indicators, and creative lighting effects
- Quickly connects to a Root controller through RS-Port
- Quick configuration with Zoner project templates

## Usage Instructions

Before using Yoke-TRGBW, make sure the Root controller is flashed with firmware or a project template that supports RGBW lighting control.

### Connect to a Root Controller
Yoke-TRGBW connects to a Root controller with an RS-PortA cable.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



Connection precautions:

- Connect or disconnect the module with the power off.
- Check the connector orientation to avoid reversed connections.
- If lights flicker, colors appear incorrect, or the device restarts, check power stability first.
- When using multiple lighting modules or high brightness, make sure the total current does not exceed the controller's power capacity.

### Lighting Orientation and Mounting

Yoke-TRGBW can be installed inside a 3D-printed model, behind a translucent enclosure, beneath a light guide, or inside a lampshade.

The module supports daisy-chaining, as shown below.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_install.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### Mounting Recommendations:

- Point the LED's emitting surface toward the model's translucent area.
- For mood lighting, add a diffuser or translucent diffusion structure.
- For status indication, mount the LED board behind a visible window.
- When mounting inside an enclosed model, provide cooling space and a maintenance opening.
- Avoid prolonged close contact between LEDs and plastic parts, especially at high brightness.

## Power Requirements

Yoke-TRGBW power consumption depends on LED brightness, color, and use of the white channel.

| Item | MAX | Type | Min |
|---|---|---|---|
| Supply Current (mA) | 250mA | | |
| Supply Voltage (V) | 5V | | 3.3V |

“MAX supply current” is the instantaneous maximum under extreme conditions such as full-brightness white on an RGB strip. Normal usage is usually well below this value.

## Hardware Specifications


| Item | Specification |
| -------- | ------------------------------------------------ |
| Module Model | Yoke-TRGBW |
| Module Name | RGBW Lighting Module |
| Interface Type | RS-Port |
| Lighting Type | RGBW |
| Applications | Illuminated 3D-printed models, mood lighting, status indication, interactive installations |
| Compatible Controllers | RootMaker / compatible Root series controllers |
| Mounting Method | Mechanical retention / adhesive / screws, depending on the project structure |

## 3D Mounting Files

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP File ZXYoke-TRGBW.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 527 KB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-TRGBW.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Frequently Asked Questions

### What if Yoke-TRGBW does not light up?

Check the following:

1. Is the Root controller powered correctly?
2. Is the module connected to the correct RS-Port?
3. Is the connector orientation correct?
4. Does the firmware support this lighting module?
5. Is the correct lighting type selected in the project template?


### What if the lighting colors are incorrect?

Possible causes include:

- The RGBW color order is configured incorrectly.
- The wrong LED type is selected in the firmware.
- An RGB template is being used to control an RGBW module.
- A faulty data connection.

Make sure the lighting module type is set to RGBW in Zoner or the firmware configuration.

### What if lights flicker or the Root controller restarts?

This is usually related to insufficient power. Try the following:

- Reduce the lighting brightness.
- Limit prolonged high-brightness use of the white channel.
- Use a more stable 5V supply.
- Check that cables and connectors make good contact.
- Avoid powering multiple high-power modules from the same supply path.

### Can I hot-plug Yoke-TRGBW?

Hot-plugging is not recommended.  
Connect or disconnect the module with the power off to prevent connector short circuits, signal errors, or module damage.

### Can Yoke-TRGBW and Yoke-RGBW be used together?

Yes, but pay attention to the arrow direction.  
