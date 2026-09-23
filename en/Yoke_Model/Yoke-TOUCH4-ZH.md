---
title: "Yoke-TOUCH4"
description: "Yoke-TOUCH4 Four-Channel Touch Module"
tags: "Yoke, LEDs, RGBW"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_Touch4_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-TOUCH4 Four-Channel Touch Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-TOUCH4 is a four-channel touch input module designed for interactive 3D prints, including touch buttons, concealed interactive panels, and desktop interactive devices.
It connects to a Root controller through a standard interface, quickly adding touch interaction to 3D prints for a more natural and streamlined user experience.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## Module Overview & Key Features

Yoke-TOUCH4 integrates four independent touch detection channels and push-release terminals. The touch area can be extended using double-ended Dupont pins, wires, and similar connections.

The module supports high-sensitivity capacitive touch detection, automatically adapting to some environmental changes and reducing false triggers for embedded interactive applications.

| Item | Description |
| ---- | ----------------------- |
| Module Interface | RS-Port |
| Power | Supplied by the Root controller |
| Input Type | Capacitive touch input |
| Channel Count | 4 independent touch channels |
| Wiring Method | Push-release terminals |
| Compatible Controllers | RootMaker / compatible Root series controllers |

Key features:

- Four independent touch inputs
- Supports conductive 3D prints as touch areas
- Quickly connects to touch structures using double-ended Dupont pins
- Supports expansion with wires and metal touch pads
- Suitable for concealed touch buttons and interactive structures without openings
- Quickly connects to a Root controller through RS-Port
- Quick configuration with Zoner project templates

## Usage Instructions

Before using Yoke-TOUCH4, make sure the Root controller is flashed with firmware or a project template that supports touch input.

### Connect to a Root Controller

Yoke-TOUCH4 connects to a Root controller with an RS-Port cable.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_Touch4_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



Connection precautions:

- Connect or disconnect the module with the power off.
- Check the connector orientation to avoid reversed connections.
- If touch detection is abnormal, first check for excessively long touch wires or poor contact.
- Avoid routing touch wires parallel to high-voltage, high-frequency, or high-current wiring.

### Touch Structures and Mounting

Yoke-TOUCH4 supports various forms of touch interaction through different structures.

For example:

- Touch areas made from conductive printing filament
- Metal touch plates
- Copper foil pads
- Metal screw touch points
- Touch panels extended through wires
- Concealed touch structures behind panels

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_TOUCH4_connect_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### Mounting Recommendations:

- Avoid large metal structures behind the touch area.
- With conductive prints, ensure a continuous and stable conductive path.
- Shorter touch wires generally provide better interference resistance.
- If the touch area is inside a plastic enclosure, reduce the wall thickness to improve sensitivity.
- Keep touch wires away from motors, power modules, and high-frequency devices.
- For large touch areas, increase the touch threshold as needed to prevent false triggers.

## Power Requirements

| Item | MAX | Type | Min |
| -------- | ---- | ---- | ---- |
| Supply Current (mA) | 20mA | | |
| Supply Voltage (V) | | 3.3V | |

## Hardware Specifications

| Item | Specification |
| ---- | --------------------------- |
| Module Model | Yoke-TOUCH4 |
| Module Name | Four-Channel Touch Module |
| Interface Type | RS-Port |
| Input Type | Capacitive touch input |
| Channel Count | 4 |
| Wiring Method | Push-release terminals |
| Applications | Interactive 3D-printed structures, hidden buttons, touch panels, creative interactive installations |
| Compatible Controllers | RootMaker / compatible Root series controllers |
| Mounting Method | Mechanical retention / adhesive / screws, depending on the project structure |

## 3D Mounting Files

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_Touch4_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP File ZXYoke-TOUCH4-v10.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 1.27 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-TOUCH4-v10.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>


## Frequently Asked Questions

### What if Yoke-TOUCH4 cannot detect touch?

Check the following:

1. Is the Root controller powered correctly?
2. Is the module connected to the correct RS-Port?
3. Is the connector orientation correct?
4. Does the firmware support the touch module?
5. Is the touch area correctly connected to the corresponding terminal?

### What if touch input triggers falsely?

Possible causes include:

- Touch wires are too long.
- Strong interference sources are nearby.
- The touch area is too large.
- The touch area is too close to metal structures.
- Power supply ripple or unstable grounding.

Suggestions:

- Shorten the touch wires.
- Move away from motors and high-frequency modules.
- Reduce the touch area.
- Increase the insulation thickness.
- Replace the power adapter.

### What if touch detection through conductive prints is unreliable?

Possible causes include:

- The conductive filament has excessive resistance.
- The conductive path is too long.
- The contact connection is unstable.
- The enclosure wall is too thick.

Suggestions:

- Shorten the conductive path and bring the wire end closer to the panel.
- Increase the conductive area.
- Use a more reliable connection method.
- Reduce the thickness separating the touch area from the finger.

### Can I hot-plug Yoke-TOUCH4?

Hot-plugging is not recommended.
Connect or disconnect the module with the power off to prevent connector short circuits, signal errors, or module damage.

### Can Yoke-TOUCH4 connect to ordinary wires?

Yes.
The module directly supports wires, metal plates, copper foil, conductive printed structures, and other touch media, allowing you to design interactions to suit your project.
