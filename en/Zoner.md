---
title: "Zoner Platform"
description: "Explore projects, deploy firmware, manage devices, and use the R-Link Lua workspace"
tags: "Zoner, RootMaker"
published: true
isPublished: true
---

Zoner is RyzoBee's browser platform for Root controllers and Yoke accessories. Discover projects, review modules and wiring, access project files, and deploy compatible firmware to your controller. You can also configure the controller through device management and use R-Link to write and manage Lua scripts.

<div style="border-radius: 10px; padding: 20px; background: #fff7ed; border-left: 6px solid #FF6A00; margin: 20px 0;">
  <strong style="color: #4B1F00;">From a project to a working creation</strong>
  <p>Prepare the controller and modules → Choose a project → Check wiring and versions → Connect the device → Deploy firmware → Verify operation</p>
  <a href="https://zoner.ryzobee.com" target="_blank" rel="noopener noreferrer" style="display: inline-block; padding: 8px 20px; background: #FF6A00; color: #fff; border-radius: 20px; text-decoration: none;">Open Zoner →</a>
</div>

## Start Here

- **First time using Zoner:** Follow the [Quick Start](/en/Zoner/quick_start) to choose a project, connect over USB, and deploy firmware.
- **Connecting, setting up Wi-Fi, or flashing a local file:** See [Device Management](/en/Zoner/device) for device status, Wi-Fi, and custom configuration.
- **Writing Lua applications:** See [R-Link Beta](/en/Zoner/rlink) for drafts, device scripts, the UI simulator, and logs.

## How Zoner, Root, and Yoke Work Together

The Root controller runs firmware and controls hardware. Yoke modules provide functions such as lighting, touch, displays, sensing, and motor control. Zoner provides project resources and deployment and configuration tools. After selecting a project, you still need compatible hardware and must connect it according to the project instructions.

Project firmware determines the device's capabilities. Device status, Wi-Fi configuration, custom configuration, and Lua management require corresponding firmware support; a successful connection alone does not mean every feature is available.

## Main Platform Sections

### Discover and All Projects

[Discover](https://zoner.ryzobee.com/) highlights featured creations, while [All Projects](https://zoner.ryzobee.com/projects) lets you browse and find projects. Explore categories such as lighting and ambience, mechanical motion, sensing and interaction, and creative tools, then search by project name.

On a project detail page, focus on three areas:

- **Project introduction:** Learn about the creation's functions, operation, use cases, and limitations.
- **Modules and wiring:** Check the controller, Yoke models, module quantities, and connection instructions.
- **Project files:** Find firmware, models, assembly resources, and other files supplied by the author. Available files vary by project.

When a project provides deployable firmware, select the controller and project version, then use the one-click deployment action. A project marked as reference material does not necessarily include firmware ready to flash; read its files and instructions first.

### My Favorites

Project cards and detail pages include a favorite action. [My Favorites](https://zoner.ryzobee.com/favorites) lets you return to saved projects. Sign in if the page requests it. Saving a favorite does not download project files or deploy firmware.

### My Device

[My Device](https://zoner.ryzobee.com/device) provides USB connection, device status, Wi-Fi configuration, custom configuration, and local firmware flashing. See [Device Management](/en/Zoner/device) for instructions.

### R-Link Beta

[R-Link](https://zoner.ryzobee.com/link) lets you write, manage, and run RootMaker Lua scripts and provides a browser UI simulator. Device features require compatible R-Link firmware. See [R-Link Beta](/en/Zoner/rlink) for details.

## What You Need

1. A Root controller and Yoke modules compatible with the project.
2. A USB-C cable that supports data transfer.
3. A computer with desktop Chrome or Edge and permission to access the selected serial port.
4. A network connection that can access Zoner and project resources.
5. The power supply and assembly materials specified by the project.

Connect Yoke modules with the power off. Externally powered modules such as Yoke-MOTOR-A require the power arrangements described on their module pages; do not assume the usual USB power setup applies.

## Frequently Asked Questions

### Do I need to write code?

To recreate an existing project, you can usually connect the hardware and deploy ready-made firmware by following its instructions. For custom logic, use R-Link Lua or consult [Development Environments](/en/dev) for tools such as Arduino.

### Why is there a module Wiki page but no matching project?

Hardware documentation and project firmware are maintained separately. Check the controllers, modules, and released versions supported by each project; do not substitute incompatible firmware. Start with the [Yoke Accessory Series](/en/Yoke_Model) to confirm module details.

### Will my existing scripts remain after flashing?

Flashing overwrites the contents of the firmware's write range. A full R-Link firmware image may overwrite the scripts partition and its data. Back up important files before updating; a browser draft does not replace a backup of device files.

### What if the interface differs from this guide?

This guide follows the current Zoner interface. Available features can vary with the project, firmware version, or subsequent platform updates. Follow the on-screen prompts and the selected project's instructions.

## Getting Help

For connection and flashing problems, start with [Quick Start troubleshooting](/en/Zoner/quick_start#troubleshooting). For configuration issues, see [Device Management](/en/Zoner/device).

When reporting an issue, include the project link, project version, controller and module models, browser version, reproduction steps, and relevant logs with passwords and keys removed. Contact [support@ryzobee.com](mailto:support@ryzobee.com), or find the relevant project repository on [RyzoBee GitHub](https://github.com/Ryzobee).
