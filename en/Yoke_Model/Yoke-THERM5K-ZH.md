---
title: "Yoke-THERM5K"
description: "Yoke-THERM5K Thermal Imaging Sensor Module"
tags: "Yoke, Thermal"
published: true
isPublished: true
---

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px;">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_THERM5K_Wiki_main.png" alt="Yoke-THERM5K" style="width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-THERM5K Thermal Imaging Sensor Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">Yoke-THERM5K is a thermal imaging module for Root-series controllers. Its 80 × 62-pixel infrared sensor captures temperature distribution across a target surface in real time.</p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">The module mounts on the controller's bottom F-BUS expansion connector and communicates over a serial interface. It supports an external lithium battery for portable thermal cameras, temperature detection devices, equipment inspection tools, and creative 3D-printed projects.</p>
  </div>
</div>

## Overview and Key Features

Yoke-THERM5K contains an 80 × 62 thermal imaging sensor that outputs thermal data for temperature-distribution images. Combine it with a Root controller and a suitable project template to build a thermal observation device.

| Item | Description |
|---|---|
| Module interface | F-BUS |
| Power | F-BUS / external battery |
| Communication | UART |
| Thermal resolution | 80 × 62 |
| Effective pixels | Approximately 5K |
| Battery connector | Supported |
| Compatible controllers | RootMaker / compatible Root-series controllers |

Key features:

- 80 × 62-pixel infrared thermal sensor, approximately 5,000 temperature sampling points
- Serial communication with the Root controller
- Integrated battery connector for portable applications
- Bottom F-BUS expansion mounting
- Suitable for thermal cameras, equipment inspection, and creative temperature-sensing devices
- Integrates with 3D-printed enclosures to build complete devices
- Supports rapid development with Zoner project templates

## Usage

Before using Yoke-THERM5K, confirm that the Root controller has been flashed with firmware or a project template that supports the thermal imaging module.

### Connecting to a Root Controller

Yoke-THERM5K installs on the bottom F-BUS expansion connector.

<div style="text-align: center;">
  <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_THERM5K_Wiki_900.png" alt="Yoke-THERM5K connection" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

When connecting:

- Install or remove the module with the power off.
- Make sure F-BUS is fully seated.
- Avoid fingerprints or dirt on the sensor window.
- Keep the thermal field of view clear during use.
- If communication is abnormal, check serial settings and the firmware version.

### Mounting

The module is designed for the bottom expansion position of a Root controller and can be integrated with a 3D-printed enclosure to make a complete thermal imaging device.

#### Mounting Recommendations

- Keep the area in front of the sensor window unobstructed.
- Avoid placing heat sources directly beside the sensor.
- Leave space for heat dissipation.
- For a closed enclosure, use an infrared-transmitting material or an opening at the thermal imaging window.
- Consider a protective cover around the sensor area to reduce dust contamination.

## Battery and Power

Yoke-THERM5K includes a battery connector, but a battery is not included. Choose a battery according to your project requirements.

The module can start using only an external battery or only F-BUS power. When both F-BUS power and a battery are connected, the battery can be charged.

The voltage range below applies only to the battery input connector.

| Item | Max. | Typical | Min. |
|---|---|---|---|
| Battery input voltage | 4.2V | 3.7V | 3.0V |

When using battery power:

- A single-cell lithium-ion or lithium-polymer battery is recommended.
- Observe the positive and negative markings on the module.
- Disconnect the battery for long-term storage.
- Do not use damaged or swollen batteries.

## Hardware Specifications

| Item | Specification |
|---|---|
| Model | Yoke-THERM5K |
| Module name | Thermal Imaging Sensor Module |
| Interface | F-BUS |
| Sensor type | Infrared thermal imaging sensor |
| Thermal resolution | 80 × 62 |
| Effective pixels | Approximately 5K |
| Communication | UART |
| Battery connector | Supported |
| Applications | Thermal cameras, temperature monitoring, equipment inspection, creative 3D-printed projects |
| Compatible controllers | RootMaker / compatible Root-series controllers |
| Mounting | Bottom F-BUS mounting |

#### Pin Definitions

| THERM5K Pin | RootMaker IO |
|---|---|
| ENABLE | GPIO08 |
| TXD | GPIO06 |
| RXD | GPIO04 |

## 3D Mounting Files

<div style="text-align: center;">
  <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_THERM5K_Wiki_mechanical.png" alt="Yoke-THERM5K mechanical drawing" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div><strong>3D STEP File: ZXYoke-THERM5K-V11.step</strong><br><span style="font-size:12px;color:#777;">STEP · V1.1 · 3.50 MB</span></div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-THERM5K-V11.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Frequently Asked Questions

### What if Yoke-THERM5K is not recognized?

Check:

1. Is the Root controller powered normally?
2. Is the module correctly installed in F-BUS?
3. Does the firmware support thermal imaging?
4. Are serial parameters configured correctly?
5. Is the module installed in the correct orientation?

### What if thermal images do not refresh correctly?

Possible causes include:

- Serial communication errors
- Unstable power
- A mismatched firmware version
- Sensor initialization failure

Power-cycle the device and check firmware settings.

### What if temperature readings are inaccurate?

Check:

- Whether the sensor window is obstructed or dirty
- Whether strong heat sources cause interference
- Whether the target is too far away
- Whether ambient temperature is changing rapidly

### Can I install or remove Yoke-THERM5K while powered on?

Hot-plugging is prohibited. Install or remove the module with the power off to avoid communication errors or damage.

### Is a battery supplied with the battery connector?

No. Supply a compatible battery for your project, observe polarity, and follow safe battery-use practices.
