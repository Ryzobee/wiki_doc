---
title: "Yoke-MOTOR-A"
description: "Yoke-MOTOR-A USB PD DC Motor Control Module"
tags: "Yoke, Motor"
published: true
isPublished: true
---

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px;">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/ZXYoke-MOTOR-A_Wiki_main.png" alt="Yoke-MOTOR-A" style="width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-MOTOR-A USB PD DC Motor Control Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">Yoke-MOTOR-A is a single-channel brushed DC motor control module powered by USB PD. It connects to a Root controller through F-BUS and supports forward/reverse rotation, PWM speed control, and braking, adding rotation, transmission, and linked motion to 3D-printed creations.</p>
  </div>
</div>

## Overview and Key Features

Yoke-MOTOR-A drives motors for rotating display stands, moving ornaments, and interactive mechanisms, with forward/reverse control and PWM speed control. Compared with Yoke-MOTO, it uses an external USB-C PD supply to drive higher-power DC motors.

| Item | Description |
|---|---|
| Module interface | F-BUS |
| Power | External USB-C PD; requests 12V by default |
| Control signals | GPIO / PWM |
| Compatible controllers | RootMaker / compatible Root-series controllers |

Key features:

- Forward and reverse DC motor control
- PWM speed control, braking, and stopping
- Suitable for rotating displays, moving ornaments, and mechanical drives
- F-BUS connection to the Root controller
- External USB-C PD power, which can also supply the Root controller

## Usage

Before use, confirm that the Root controller runs firmware compatible with this module. Prepare a USB PD supply that supports a 12V output profile and suitable cables.

### Connecting to a Root Controller

With the controller, module, and motor all unpowered, align Yoke-MOTOR-A's F-BUS connector with the corresponding controller connector and insert it.

<div style="text-align: center;">
  <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_MOTOR-A_Wiki_900.png" alt="Yoke-MOTOR-A connection" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

When connecting:

- Install or remove the module only with the power off. Disconnect any controller battery first.
- Check the orientation of the double-row connector and align every pin to avoid reversed or offset insertion.
- Connect the motor to DC-MOTOR and the PD supply to PD POWER IN.
- **Important:** Match the motor's rated voltage to the actual PD supply voltage, and ensure the supply meets both starting and running current requirements.

### Connecting and Operating the Motor

1. With power off, connect a two-wire brushed DC motor to the DC-MOTOR XH2.5-2P connector.
2. Secure the motor and transmission, and check that the shaft and moving parts are not jammed.
3. Connect a USB PD supply supporting 12V and confirm that the controller and module are powered normally.
4. Use compatible firmware to control direction and PWM duty cycle. Start with a low duty cycle for the first run.
5. Stop the motor and disconnect all power before changing wiring or removing the module.

#### Mounting Recommendations

- Avoid prolonged stalls or continuous heavy loads, which can overheat the motor or driver.
- Leave cooling space around the driver and motor, and keep them clear of heat-sensitive structural parts.
- Avoid excessive lateral force on the motor shaft when fitting gears or couplings.
- Both motor connector pins are driven outputs. Do not connect either pin directly to a power rail or GND.

## Power Requirements

The motor driver is powered through USB-C PD and requests 12V by default. The supply must support the corresponding profile. A standard 5V USB supply cannot provide the default 12V operating conditions; the negotiated voltage depends on supply capabilities and PD configuration.

For Yoke-MOTOR-A, it is recommended to power the entire system only through the module's USB-C PD input, with the module supplying the Root controller through F-BUS. Avoid simultaneously connecting a controller battery or the controller's own USB power supply.

Current varies with motor load. Account for motor starting current and controller power consumption when choosing a supply. Actual drive capability is also limited by adapter output power, module cooling, connectors, and cable current capacity.

| Item | Max. | Typical | Min. |
|---|---|---|---|
| Requested USB PD voltage | | 12V (default) | |
| Motor operating current | 4A | | |
| Control logic voltage | | 3.3V | |

## Hardware Specifications

| Item | Specification |
|---|---|
| Model | Yoke-MOTOR-A |
| Module name | USB PD DC Motor Control Module |
| Interface | F-BUS, 2 × 12 pins, 1.27mm pitch |
| Motor connector | DC-MOTOR, XH2.5-2P |
| Load | One two-wire brushed DC motor |
| Control | Dual-input direction control / PWM speed control |
| Applications | Moving 3D-printed structures, rotating mechanisms, interactive installations |
| Compatible controllers | RootMaker / compatible Root-series controllers, with matching firmware support |

#### Pin Definitions

| Module Pin | RootMaker IO |
|---|---|
| PWM_A / BI (reverse input) | GPIO06 |
| PWM_B / FI (forward input) | GPIO04 |
| PD_SCL | GPIO40 |
| PD_SDA | GPIO41 |

I²C (IIC) is used for CH224A power configuration and status reading. PWM_A and PWM_B control motor direction and speed.

| PWM_A (GPIO06) | PWM_B (GPIO04) | Motor State |
|---|---|---|
| Low | High | Forward |
| High | Low | Reverse |
| High | High | Brake |
| Low | Low | Stop, high-impedance outputs |

Actual rotation direction depends on the order of the two motor wires.

When writing control software, keep both control inputs low before applying driver power. Wait at least 3ms after driver power is established before starting control. PWM frequency must not exceed 30kHz, and both high and low pulse widths must be at least 100ns.

## 3D Mounting Files

<div style="text-align: center;">
  <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke-MOTO-A_Wiki_mechanical.png" alt="Yoke-MOTOR-A mechanical drawing" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div><strong>3D STEP File: ZXYoke-MOTO-A-V11.step</strong><br><span style="font-size:12px;color:#777;">STEP · V1.1 · 3.61 MB</span></div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-MOTO-A-V11.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Frequently Asked Questions

### The motor is connected but does not run. What should I check?

1. Is the PD supply connected to PD POWER IN, and does it support a 12V profile?
2. Is the module fully seated in F-BUS, and is the controller powered normally?
3. Is the motor connected securely to DC-MOTOR?
4. Does the firmware support Yoke-MOTOR-A, with GPIO06 and GPIO04 configured correctly?
5. Is the motor stalled, or has it stopped because of supply overload, driver overheating, or a similar issue?

### The motor turns in the wrong direction. What should I do?

Turn off power, then swap the two motor wires. Alternatively, change the direction control signals in firmware.

### Can F-BUS alone power the motor?

Motor drive power comes from the module's USB-C PD input. A compatible external PD supply is required.

### How should I choose a motor and power adapter?

Use an operating current of no more than 4A as a motor selection reference, and match rated voltage to the actual supply voltage. Account for starting current, avoid prolonged stalls and continuous heavy loads, and provide cooling space for the module and motor.

Choose a PD adapter with a 12V profile. Use that profile's rated output current and power, leaving headroom for controller consumption and motor startup. For example, a 12V/3A profile provides at most 36W; the controller and module consumption must be deducted to determine the power available to the motor.

### Can I plug or unplug Yoke-MOTOR-A while powered on?

Hot-plugging is prohibited. Stop the motor and disconnect PD power before connecting or removing the module or motor, to avoid connector short circuits, signal errors, or damage.
