---
title: "Yoke-VOICE"
description: "Yoke-VOICE Voice Module"
tags: "Yoke, Voice"
published: true
isPublished: true
---

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px;">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_VOICE_Wiki_main.png" alt="Yoke-VOICE" style="width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-VOICE Voice Module</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">Yoke-VOICE is an audio module based on the CI1302 voice AI chip. It provides voice capture, playback, and basic voice interaction capabilities for Root-series controllers.</p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">The module integrates a microphone and speaker and communicates with the controller over UART. Developers can implement announcements, voice prompts, offline speech recognition, and voice interaction through controller firmware, or customize it for their projects.</p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">It uses the bottom S-BUS expansion connector for quick integration without additional wiring.</p>
  </div>
</div>

## Overview and Key Features

Yoke-VOICE uses the CI1302 intelligent voice chip for local audio processing and serves as a voice input/output expansion module.

| Item | Description |
|---|---|
| Module interface | S-BUS |
| Main chip | CI1302 |
| Audio input | Onboard microphone |
| Audio output | Built-in speaker |
| Communication | UART |
| Power | Supplied by the controller |
| Compatible controllers | RootMaker / compatible Root-series controllers |

Key features:

- Based on the CI1302 voice AI chip
- Integrated microphone and speaker
- UART communication with the controller
- Suitable for voice prompts and status announcements
- Supports future expansion to offline speech recognition and related functions
- Quick installation and connection through S-BUS

## Usage

Before using Yoke-VOICE, confirm that the controller firmware supports the required voice module features.

### Connecting to a Root Controller

Yoke-VOICE connects to S-BUS on the bottom of the controller.

<div style="text-align: center;">
  <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_VOICE_Wiki_900.png" alt="Yoke-VOICE connection" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

When connecting:

- Install or remove the module with the power off.
- Make sure S-BUS is fully seated.
- Do not strain the connector or install the module backwards.
- If the controller cannot recognize the module, check firmware support.
- If communication is abnormal, check UART settings.

### Audio Usage

The built-in microphone and speaker can be used directly for audio capture and playback.

Recommendations:

- Keep the microphone opening clear.
- Keep speaker openings unobstructed.
- Keep the module away from strong electromagnetic interference.
- Maintain a stable controller power supply during continuous high-volume playback.

## Power Requirements

Power consumption depends on playback volume, processing load, and other factors.

| Item | Max. | Typical | Min. |
|---|---|---|---|
| Supply current | 300mA | | |
| Supply voltage | 5V | | 3.3V |

The maximum supply current is the peak during high-volume speaker playback and full chip load. Normal use is typically well below this value.

## Hardware Specifications

| Item | Specification |
|---|---|
| Model | Yoke-VOICE |
| Module name | Voice Module |
| Main chip | CI1302 |
| Communication | UART |
| Module interface | S-BUS |
| Audio input | Onboard microphone |
| Audio output | Onboard speaker |
| Intended functions | Voice capture, audio playback, voice interaction |
| Compatible controllers | RootMaker / compatible Root-series controllers |

#### Pin Definitions

| VOICE Pin | RootMaker IO |
|---|---|
| TXD1_USER | GPIO36 |
| RXD1_USER | GPIO37 |
| PG_EN | GPIO35 |
| TXD0_DBG | GPIO48 |
| RXD0_DBG | GPIO47 |

## Firmware and Software Support

The specific features of Yoke-VOICE depend on controller and module firmware.

Supported or planned features include:

- Audio playback
- Voice prompts
- Status announcements
- Local voice command recognition
- Extended voice interaction
- Development of AI voice applications

Refer to the relevant firmware version notes for actual feature support.

## 3D Mounting Files

<div style="text-align: center;">
  <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_VOICE_Wiki_mechanical.png" alt="Yoke-VOICE mechanical drawing" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div><strong>3D STEP File: ZXYoke-VOICE-V11.step</strong><br><span style="font-size:12px;color:#777;">STEP · V1.1 · 6.67 MB</span></div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-VOICE-V11.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Frequently Asked Questions

### What if Yoke-VOICE is not recognized?

Check:

1. Is the controller powered normally?
2. Is the module correctly installed in S-BUS?
3. Does S-BUS have good contact?
4. Does the controller firmware support Yoke-VOICE?
5. Are UART settings correct?

### Why is there no sound from the speaker?

Possible causes include:

- Audio playback is not enabled in the firmware
- Volume is too low
- Audio resources did not load correctly
- The speaker is obstructed or damaged

First check firmware and software settings.

### What if the microphone cannot capture sound?

Check:

- Whether the microphone opening is blocked
- Whether recording is enabled
- Whether the controller and module communicate normally
- Whether the current firmware supports audio capture

### Can I plug or unplug Yoke-VOICE while powered on?

Hot-plugging is not recommended. Install or remove the module with the power off to avoid connector damage, communication errors, or module faults.

### Does Yoke-VOICE require the official CI1302 firmware?

Not necessarily. Custom firmware can be used to meet project requirements. Actual functionality is determined jointly by module firmware and controller software.
