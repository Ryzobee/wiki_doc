---
title: "R-Link Beta: Lua Workspace"
description: "Edit, export, and send Lua scripts and preview interfaces in Zoner"
tags: "Zoner, RootMaker"
published: true
isPublished: true
---

Ryzobee Link, labeled **R-Link Beta** in the sidebar, is Zoner's workspace for RootMaker Lua development. It provides script editing, device script management, a UI simulator, and runtime logs.

[Open R-Link](https://zoner.ryzobee.com/link)

## Requirements

Device features require compatible [Ryzobee Link project firmware](https://zoner.ryzobee.com/projects/z000001). Before flashing, check the project controller and version, and back up existing scripts and data. A full firmware image may overwrite the scripts partition.

Connect RootMaker in [My Device](https://zoner.ryzobee.com/device), then open R-Link. The platform uses a shared device connection entry point; there is no separate connection step in R-Link. Without a device connection, you can still edit drafts and use the available UI simulator, but you cannot manage files on the device.

## Create, Open, and Back Up Scripts

1. Create a new script or open a local Lua file.
2. Check the filename and edit the content in the Lua workspace. Use file tabs to switch between open drafts.
3. Check the save status and byte count below the editor. The current page shows a script size limit of 16 KiB.
4. Export important scripts to your computer.

Drafts are saved in the current browser. Do not rely on them to restore work after changing browsers, clearing site data, or losing the local environment. Export anything you need to keep.

## UI Simulator

Run the simulation to preview supported interface content on the browser's 240 × 240 simulated screen. Use simulator logs to review runtime information.

The simulator only simulates the UI and does not control the device. Actual display output, touch, sensors, motors, voice, and networking must still be tested on compatible hardware and firmware. A successful simulation does not complete hardware validation.

## Send and Manage Device Scripts

1. Connect a controller running compatible R-Link firmware in My Device.
2. Return to R-Link and confirm the connection status.
3. Check the current draft's filename and content, then send it to the device. If a same-name file prompt appears, first decide whether the original device file needs to be backed up.
4. Refresh device scripts to view the returned file list and check device storage information.
5. Run the script using the actions available in the device script list or the controller's application interface. Review logs and verify the actual result.

Editing a draft, sending a file, and running a device script are separate operations. A saved browser draft does not mean the script is on the controller. After sending a file, also check whether it is running.

## Logs and Device Console

Filter runtime logs by all output, device output, or simulator output to distinguish browser previews from actual hardware activity. Identify the log source before recording the error location and reproduction steps.

When a supported device is connected, use the device Console according to the project or firmware documentation. Commands are defined by the firmware; do not paste computer terminal commands directly into the device Console.

## Frequently Asked Questions

### Sending to the device is unavailable

Check that My Device shows a successful connection, the controller runs compatible R-Link firmware, and the draft meets the page's filename and size requirements.

### No device scripts are visible

Check the connection, then refresh device scripts. Ordinary project firmware may not support Lua file management. Confirm that the firmware required by the R-Link project is installed.

### The simulation works, but the device does not

Check the firmware's Lua APIs, hardware models, and wiring, and review device logs. The simulator covers UI previews only and cannot replace device testing.

### Scripts disappeared after a firmware update

A full firmware image may overwrite the scripts partition. Restore scripts from previously exported backups and send them to compatible firmware again. Back up device files before future updates.

## Continue Reading

- [Zoner Platform Overview](/en/Zoner)
- [Device Management](/en/Zoner/device)
- [Ryzobee Link Repository](https://github.com/Ryzobee/ryzobee-link)
