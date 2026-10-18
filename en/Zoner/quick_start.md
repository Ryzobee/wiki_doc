---
title: "Zoner Quick Start"
description: "Prepare hardware, choose a project, connect a device, deploy firmware, and verify operation"
tags: "Zoner, RootMaker"
published: true
isPublished: true
---

This guide helps you deploy a project that matches your hardware to RootMaker through Zoner. If you are new to the product ecosystem, first read the [Product Quick Start](/en/fast_guide).

## 1. Prepare Hardware and a Browser

- Prepare the RootMaker, Yoke accessories, and power supply required by the project.
- Use a USB-C cable that supports data transfer. A charge-only cable cannot provide a serial connection.
- Open [Zoner](https://zoner.ryzobee.com) in Chrome or Edge on a computer.
- Close serial monitors, development tools, and other browser tabs using the same serial port.

Read the module power instructions first, then install modules with the power off. Leave the enclosure open during initial testing so you can inspect wiring and reach the USB connector.

## 2. Choose a Project and Check Its Resources

Open [All Projects](https://zoner.ryzobee.com/projects) and search by category or name. On the detail page, review:

1. **Project introduction:** Confirm the functions and operating method meet your needs.
2. **Modules and wiring:** Check the controller model, hardware revision, Yoke models, power supply, and wiring.
3. **Project files:** Check that firmware and other resources are available, and read the corresponding version notes.

Confirm the controller model and project version in the deployment area. Choose a version that matches your hardware, rather than simply the highest version number. If a project contains only reference material, prepare files according to the author's instructions; do not substitute another project's firmware.

## 3. Connect the Device

1. Connect the computer following the controller and module power instructions, and keep the USB data connection stable.
2. Open [My Device](https://zoner.ryzobee.com/device).
3. Use the action to connect RootMaker.
4. Select the controller's port in the browser serial-port picker and authorize the connection.
5. Check the connection status and logs to confirm success.

If several serial devices are connected, check the device name and disconnect unrelated devices if necessary. Port numbers vary between computers and USB ports; do not always select a particular COM number.

Device information is supplied by firmware. If status fields are empty or show “—”, first check whether the firmware supports status reporting. This alone does not establish a hardware fault.

## 4. Deploy Project Firmware

1. Return to the verified project detail page and confirm the controller and project version.
2. Back up important scripts and data on the device, and record project settings you need to retain.
3. Use the one-click deployment action and follow the prompts for connection, firmware confirmation, and flashing.
4. Wait for an explicit completion message. Do not unplug USB, change the power supply, or press Reset during flashing.
5. If prompted, restart or reconnect the controller, then check its status.

Flashing overwrites data in the write range. A full image containing the scripts partition may overwrite existing Lua applications and their stored data. Duration depends on firmware size, download speed, and the serial connection. Follow the progress display and completion message.

For a local `.bin` file, see [Local Firmware Flashing](/en/Zoner/device#local-firmware). Do not use an arbitrary firmware file with that tool.

## 5. Verify Project Operation

Test the project while it is easy to inspect, then complete final assembly:

1. Check that the controller starts normally and that displays, lights, and other indicators behave as described.
2. Test the project's buttons, touch input, sensors, voice features, motors, and other functions individually.
3. If networking is required, follow [Device Management](/en/Zoner/device#wifi) or the project's own setup instructions.
4. Record the working project version and hardware combination.
5. Turn off power, secure the enclosure, modules, and cables, then power on and test again.

For the first motor test, confirm that the mechanism is not jammed and follow the module's power and speed-control instructions.

## Troubleshooting <a id="troubleshooting"></a>

### The connection action is missing or serial access is unsupported

Use Chrome or Edge on a computer and open Zoner over HTTPS. Avoid browsers embedded in messaging apps. Check whether serial access is disabled in browser permissions or restricted by an organization policy.

### No device appears in the port picker

Check that the USB cable supports data, the USB port works, the controller is powered, and the operating system recognizes the device. Try another data cable or USB port. If the operating system requests a driver, follow the hardware instructions.

### The port appears, but connection fails or it is busy

Close the Arduino serial monitor, other flashing tools, and browser pages using the port, then reconnect. Verify that the selected port belongs to the intended controller. If firmware is not operating normally, enter download mode according to the controller instructions and retry.

### The project cannot be deployed or firmware download fails

Confirm that deployable firmware is available, its version matches the controller, and the network can access the resource. Record the specific error and project link instead of repeatedly trying unrelated firmware.

### Flashing fails or is interrupted

Open the connection and flashing logs on My Device and record the first error. Check the data cable, power, and port usage. Restore download mode according to the controller instructions, then flash the correct full image again. Do not plug or unplug modules during flashing.

### Flashing finishes, but a module does not respond

Confirm the controller has left download mode and is running the project firmware. Check the module model, wiring, power, and project settings. Turn off power before reseating modules. A module having a Wiki page does not mean the current project firmware supports it.

### The problem remains unresolved

Collect the project link and version, hardware models, steps, and error logs, then follow [Getting Help](/en/Zoner#getting-help).

## Continue Reading

- [Zoner Platform Overview](/en/Zoner)
- [Device Management](/en/Zoner/device)
- [R-Link Beta](/en/Zoner/rlink)
- [Yoke Accessory Series](/en/Yoke_Model)
