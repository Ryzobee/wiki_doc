---
title: "Zoner Device Management"
description: "Connect RootMaker over USB, view status, configure Wi-Fi and custom settings, and flash local firmware"
tags: "Zoner, RootMaker"
published: true
isPublished: true
---

[My Device](https://zoner.ryzobee.com/device) is Zoner's shared device connection entry point. Once connected, you can read status supported by the firmware, send configuration, and use the local firmware flashing tool.

## Connection and Status

Connect the controller to your computer with a USB data cable. Use the action to connect RootMaker, select the correct serial port, and authorize access. If connection fails, see [Connection Troubleshooting](/en/Zoner/quick_start#troubleshooting).

The device information area can show CPU, RAM, PSRAM, network status, Wi-Fi, and IP address. Use the status refresh action when available. Fields depend on the current firmware's responses; information that is not returned may appear as “—”.

A USB serial connection and a Wi-Fi connection are separate: USB communication does not mean the device has joined a wireless network, and Wi-Fi setup does not replace browser authorization for USB serial access.

## Wi-Fi Configuration <a id="wifi"></a>

1. Confirm that the device is connected and its firmware supports Wi-Fi setup through Zoner.
2. In Wi-Fi configuration, choose a network detected by the device.
3. For a hidden network or an empty scan list, use manual network-name entry and enter the SSID.
4. Enter the Wi-Fi password and save the Wi-Fi configuration.
5. Wait for the device to attempt connection, then check network status and the IP address in device information.

RootMaker uses 2.4GHz Wi-Fi. Confirm the network band is compatible. Saving configuration successfully does not guarantee a successful network connection; check the result separately.

If the project has its own network setup procedure, follow that procedure first. Do not publish Wi-Fi passwords when reporting issues.

## Custom Configuration <a id="custom-config"></a>

The page provides three string settings: `slot1`, `slot2`, and `slot3`. Their meaning is defined by project firmware. Read the project's definition of each setting before changing it.

1. Select the items you want to change.
2. Enter the strings required by the project.
3. Save the custom configuration.
4. Verify that the device uses the new settings according to the project instructions.

Unchecked items retain their existing values. The page states that the current protocol cannot read existing values, so an empty input field does not mean no value is stored on the device. Do not overwrite unrelated settings simply to fill in blank fields.

## Local Firmware Flashing <a id="local-firmware"></a>

Prefer deploying matched firmware from a project's detail page. Use local flashing only when the project author or your development workflow explicitly provides a file suitable for this tool.

The current flashing tool is for **ESP32-S3 merged firmware**. It accepts `.bin` files, with a stated maximum size of **16 MiB** and write address **`0x0`**. Meeting the file-size limit does not establish hardware compatibility.

1. Confirm that the file matches the controller, Flash capacity, and hardware revision.
2. Confirm that it is a merged firmware image starting at `0x0`. Do not treat an application-only `.bin`, separate bootloader, or partition table as a merged image.
3. Back up important device files and settings, and close other tools using the port.
4. Select or drag the file into the firmware flashing area and check the displayed information.
5. Start flashing, follow the prompts, and wait for success.
6. Restart or reconnect the controller if prompted, then verify firmware operation.

Flashing overwrites existing contents in the write range. Do not disconnect USB, change the power supply, or press Reset during flashing. For modules with special power requirements, such as Yoke-MOTOR-A, consult their documentation first to determine the correct wiring for flashing.

## Connection and Flashing Logs

Expand the connection and flashing logs to review the connection or write process. When an error occurs, record the first error and a small amount of surrounding context, together with the controller model, firmware source, and file version. Remove passwords, keys, and other sensitive information before sharing logs.

## Frequently Asked Questions

### The device is connected, but status is not updating

Check that the firmware supports status reporting and that the device is running normally, then refresh status. If it is still in download mode, restore normal operation using the controller or project instructions.

### Wi-Fi or custom configuration actions are unavailable

Confirm that the serial port is connected, compatible firmware is running, and no other operation is in progress. Reloading the page cannot add configuration protocol support to incompatible firmware.

### Can I flash firmware for a regular ESP32 or another board?

This tool is labeled for ESP32-S3, and the actual RootMaker hardware configuration must still match. The same chip name does not guarantee matching Flash, pin assignments, or partition layout. Use explicitly compatible firmware.

## Continue Reading

- [Zoner Platform Overview](/en/Zoner)
- [Project Deployment Quick Start](/en/Zoner/quick_start)
- [R-Link Beta](/en/Zoner/rlink)
