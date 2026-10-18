---
title: "Yoke-LCD1D54C"
description: "Yoke-LCD1D54C 1.54-inch Touch Display Module"
tags: "Yoke, LCD, Touch"
published: true
isPublished: true
---

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px;">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_LCD1D54C_Wiki_main.png" alt="Yoke-LCD1D54C" style="width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-LCD1D54C 1.54-inch Touch Display Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">Yoke-LCD1D54C is a 1.54-inch color touch display module for Root controllers, with a resolution of 240 × 240 pixels.</p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">It adds graphical interfaces, status displays, and touch interaction to 3D-printed creations. Applications include device panels, desktop terminals, interactive installations, smart ornaments, and other creative projects.</p>
  </div>
</div>

## Overview and Key Features

Yoke-LCD1D54C connects through F-BUS and integrates a color LCD and touch input. The display uses SPI, while touch uses I²C (IIC). It can show device status, menus, sensor data, and custom content.

| Item | Description |
|---|---|
| Module interface | F-BUS |
| Display size | 1.54 inches |
| Resolution | 240 × 240 |
| Display type | Color LCD |
| Touch input | Capacitive touch |
| Communication | Display: SPI; touch: I²C |
| Mounting | Controller expansion |

Key features:

- 1.54-inch color LCD
- 240 × 240 resolution
- Touch interaction
- Plug-in F-BUS expansion
- Displays text, icons, menus, and real-time data
- Suitable for status displays, control panels, and interactive interfaces
- Fits a variety of 3D-printed enclosures and device structures

## Usage

### Installing the Module

Yoke-LCD1D54C mounts on top of RootMaker. First remove the four corner screws on the bottom of the controller.

Installation steps:

1. Turn off all power and disconnect the battery.
2. Use a screwdriver to remove the four bottom corner screws.
3. Align the display module with the controller's F-BUS connector.
4. Check that both rows of pins align fully with the socket, then press straight down.
5. Reinstall the screws to secure the controller and module.

<div style="text-align: center;">
  <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_LCD1D54C_Wiki_900.png" alt="Yoke-LCD1D54C installation" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

#### Installation Precautions

> **Ensure that the pins and connector are fully aligned before installation.**
>
> **Misaligned insertion can damage the module, controller, or connector.**

During installation:

- Install or remove the module only with the power off.
- Do not insert it at an angle or force it into place.
- Stop immediately and check alignment if insertion resistance is unusually high.
- Confirm that the module sits flat against the controller after installation.

### Mounting Recommendations

Yoke-LCD1D54C can serve as a front panel, control terminal, or status display window.

When designing a 3D-printed structure:

- Leave the full display area visible.
- Keep structural parts clear of the touch area.
- Allow enough space for finger operation.
- Provide access for maintenance and disassembly.
- Avoid sustained pressure on the screen edges.

## Power Requirements

Power consumption varies with display content and backlight brightness.

| Item | Max. | Typical | Min. |
|---|---|---|---|
| Supply current | 100mA | | |
| Supply voltage | | 3.3V | |

## Hardware Specifications

| Item | Specification |
|---|---|
| Model | Yoke-LCD1D54C |
| Module name | 1.54-inch Touch Display Module |
| Interface | F-BUS |
| Display size | 1.54 inches |
| Resolution | 240 × 240 |
| Display colors | Color |
| Touch input | Capacitive touch |
| Communication | Display: SPI; touch: I²C |
| Display driver | ST7789 |
| Compatible controllers | RootMaker / compatible Root-series controllers |
| Mounting | Stacked on the controller |

#### Pin Definitions

| LCD Pin | RootMaker IO |
|---|---|
| LCD_CS | GPIO05 |
| LCD_RS | GPIO03 |
| LCD_SCK | GPIO12 |
| LCD_SDA | GPIO09 |
| LCD_RST | GPIO10 |
| LCD_BL | GPIO07 |
| TP_SCL | GPIO40 |
| TP_SDA | GPIO41 |
| TP_RST | GPIO02 |
| TP_INT | GPIO01 |

## 3D Mounting Files

<div style="text-align: center;">
  <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_LCD1D54C_Wiki_mechanical.png" alt="Yoke-LCD1D54C mechanical drawing" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div><strong>3D STEP File: ZXYoke-LCD1D54C-V10.step</strong><br><span style="font-size:12px;color:#777;">STEP · V1.0 · 8.21 MB</span></div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-LCD1D54C-V10.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Frequently Asked Questions

### There is no display after installation. What should I check?

1. Is the module fully inserted into F-BUS?
2. Are the pins misaligned?
3. Is the controller powered normally?
4. Does the firmware support the display module?
5. Were any pins bent during installation?

### What if the display is abnormal or corrupted?

Possible causes include:

- Incorrect firmware configuration
- Display driver initialization failure
- Incomplete module insertion
- Poor connector contact

Reinstall the module and check the software configuration, following the power-off installation procedure above.

### What if touch input does not work?

Check:

- Whether touch is enabled in the firmware
- Whether the touch driver is configured correctly
- Whether the module is fully installed
- Whether a covering on the screen interferes with touch

### Can I install or remove the module while powered on?

Hot-plugging is prohibited.

Installation involves removing screws. Turn off all power and disconnect the battery before installing or removing the module to prevent connector short circuits, communication errors, or damage.

### What if the pins were inserted incorrectly, or I suspect misalignment?

Immediately disconnect power and remove the module. Check for bent or deformed pins and short circuits before reinstalling it.

If pins are damaged, stop using the affected parts and replace them to prevent further damage.
