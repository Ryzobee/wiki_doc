---
title: "Yoke-RAD60"
description: "Yoke-RAD60 60GHz Millimeter-Wave Presence Sensor Module"
tags: "Yoke, radar"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_RAD60_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-RAD60 60GHz Millimeter-Wave Presence Sensor Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-RAD60 is a presence sensor based on 60GHz millimeter-wave radar. It connects to a Root controller through a standard interface to quickly add human presence sensing to 3D-printed creations, enabling proximity-triggered lighting, automatic wake-up, interactive triggers, and presence detection. Unlike conventional infrared sensors, Yoke-RAD60 detects both body movement and tiny movements such as breathing when a person is stationary, making it well suited to interactive display models, desktop devices, and smart enclosure projects.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## Module Overview & Key Features

Yoke-RAD60 integrates a 60GHz FMCW millimeter-wave radar sensor for moving-target detection, stationary human presence detection, and target distance output.

| Item | Description |
| ---- | ----------------------- |
| Module Interface | RS-Port |
| Power | Supplied by the Root controller |
| Operating Band | 60GHz millimeter-wave |
| Communication | UART |
| Compatible Controllers | RootMaker / compatible Root series controllers |

Key features:

- Human presence and motion detection, including small movements of stationary people
- Detection range up to approximately 10m
- Outputs target distance, speed, angle, and other information
- Quickly connects to a Root controller through RS-Port
- Suitable for smart sensing, automatic lighting, interactive installations, and human presence detection

## Usage Instructions

Before using Yoke-RAD60, make sure the Root controller is flashed with firmware or a project template that supports the millimeter-wave radar module.

### Connect to a Root Controller

Yoke-RAD60 connects to a Root controller with an RS-Port cable.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_RAD60_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



Connection precautions:

- Connect or disconnect the module with the power off.
- Check the connector orientation to avoid reversed connections.
- If targets are not detected, check the power supply and serial port configuration.
- Avoid large metal obstructions directly in front of the radar.
- When installing multiple radar modules, leave space between them to reduce interference.
- Daisy-chaining is not supported. The connectors on both sides are provided for installation convenience.

### Mounting Orientation and Methods

Yoke-RAD60 supports horizontal, tilted, and overhead mounting.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_RAD60_Wiki_install_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### Mounting Recommendations:

- Keep metal obstructions away from the front of the radar.
- If a cover is needed, use a smooth, even surface with uniform thickness. Metal covers are prohibited.
- Avoid positioning radar modules directly facing each other.

## Detection Performance Reference

| Mounting Method | Motion Detection Distance | Stationary Human Detection Distance |
| ---- | ------ | -------- |
| Horizontal | ≤10m | ≤8m |
| Tilted | ≤9m | ≤7m |
| Overhead | Radius ≤5m | Radius ≤5m |

Actual detection performance depends on the installation environment, target posture, obstructions, enclosure materials, and other factors.

## Power Requirements

| Item | MAX | Type | Min |
| -------- | ----- | ---- | ---- |
| Supply Current (mA) | | 80mA | |
| Supply Voltage (V) | 5.5V | 5V | 3.0V |

## Hardware Specifications

| Item | Specification |
| ------ | --------------------------- |
| Module Model | Yoke-RAD60 |
| Module Name | 60GHz Millimeter-Wave Presence Sensor Module |
| Interface Type | RS-Port |
| Radar Type | FMCW millimeter-wave radar |
| Operating Band | 59~64GHz |
| Horizontal Field of View | ±60° |
| Vertical Field of View | ±60° |
| Maximum Detection Distance | ≤10m |
| Communication Interface | UART |
| Applications | Human presence detection, automatic sensing, interactive installations, smart homes |
| Compatible Controllers | RootMaker / compatible Root series controllers |
| Mounting Method | Mechanical retention / adhesive / screws, depending on the project structure |

## 3D Mounting Files

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_RAD60_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP File ZXYoke-RAD60.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 1.13 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-RAD60.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Frequently Asked Questions

### What if Yoke-RAD60 does not work?

Check the following:

1. Is the Root controller powered correctly?
2. Is the module connected to the correct RS-Port?
3. Is the connector orientation correct? Only one cable may be connected to the module at a time.
4. Does the firmware support this radar module?
5. Are there metal obstructions in front of the radar?

### Why can it detect a person who is not moving?

Yoke-RAD60 supports micro-motion detection.
Even when a person is still, the module can detect small chest movements such as breathing to sense their presence.

### Why do false triggers occur?

Possible causes include:

- Metal reflectors are in front of the radar.
- Multiple radars are interfering with each other.
- The mounting angle is unsuitable.
- Moving objects such as fans or swinging items are present.

Try adjusting the mounting position and sensitivity settings.

### Can I hot-plug Yoke-RAD60?

Hot-plugging is not recommended.
Connect or disconnect modules with the power off to prevent connector short circuits, communication errors, or module damage.

### Can multiple Yoke-RAD60 modules interfere with each other?

Millimeter-wave radar modules may interfere when installed close together and facing each other.

Suggestions:

- Keep radar modules more than 1m apart.
- Avoid pointing radars directly at each other.
- Adjust the mounting angles as needed.

### Can it work through a 3D-printed enclosure?

Usually, yes.
Millimeter-wave radar can penetrate most nonmetallic materials, such as:

- PLA、PETG、ABS
- Acrylic
- Thin wood panels

However, avoid:

- Metal enclosures
- Materials with metallic coatings
- Carbon fiber materials
- Large conductive structures

The cover should have a smooth, even surface and uniform thickness, such as a flat or spherical surface, without bumps or irregularities. Otherwise, detection performance may be affected.
