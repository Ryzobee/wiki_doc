---
title: "FAQ"
description: "Find answers to your questions and troubleshoot issues here"
tags: "FAQ, Home"
published: true
isPublished: true
---

This page covers common issues you may encounter with RyzoBee, RootMaker, Yoke modules, and the Zoner platform.

If you have trouble connecting devices, flashing firmware, configuring Wi-Fi, using modules, or running projects, choose a category below to start troubleshooting.

## Quick Troubleshooting

If you are unsure which category applies, start with these common scenarios.

| Symptom | Suggested Section |
|---|---|
| Computer does not recognize RootMaker | [Device Connection Issues](#device-connection-issues) |
| Firmware flashing fails | [Firmware Flashing Issues](#firmware-flashing-issues) |
| Wi-Fi does not connect | [Wi-Fi and Network Issues](#wi-fi-and-network-issues) |
| Yoke module does not respond | [Yoke Module Issues](#yoke-module-issues) |
| Lights flicker or show incorrect colors | [Lighting Module Issues](#lighting-module-issues) |
| Motor does not rotate or device restarts | [Power and Motor Issues](#power-and-motor-issues) |
| Zoner project does not run | [Zoner Platform Issues](#zoner-platform-issues) |
| Unexpected behavior after mounting in a 3D print | [Mechanical Installation Issues](#mechanical-installation-issues) |

## Device Connection Issues

This category covers connections between RootMaker, computers, USB-C cables, and power adapters.

Common issues include:

- RootMaker does not respond when connected to a computer
- The computer does not recognize the USB device
- The device is missing from the serial port list
- The device repeatedly disconnects and reconnects
- The USB-C cable supplies power but cannot be used for flashing or debugging

Check these items first:

1. Does the USB-C cable support data transfer?
2. Is the computer's USB port working?
3. Is RootMaker powered on correctly?
4. Do you need to enter download mode?
5. Is an external module causing a power issue?

```markdown
- [RootMaker Is Not Recognized by the Computer]()
- [How to Enter Download Mode]()
- [Choosing a USB-C Cable]()
- [Serial Device Not Listed]()
````

## Firmware Flashing Issues

This category covers firmware flashing with Zoner, WebTools, Arduino, and ESP-IDF.

Common issues include:

* WebTools cannot connect to the device
* The browser cannot open the serial port
* Flashing is interrupted
* The device does not respond after flashing
* The wrong firmware version was flashed
* The device keeps restarting after the firmware starts

Check these items first:

1. Are you using a USB-C cable that supports data transfer?
2. Is the correct device port selected?
3. Does the firmware match your RootMaker hardware revision?
4. Is the device in download mode?
5. Does the browser support Web Serial?
6. Is an external module preventing startup?

```markdown
- [Flash Firmware with WebTools]()
- [Troubleshoot Flashing Failures]()
- [How to Reflash the Default Firmware]()
- [How to View Serial Logs]()
- [Choosing a Firmware Version]()
```

## Wi-Fi and Network Issues

This category covers Wi-Fi setup, web control, OTA, cloud services, and network connections.

Common issues include:

* Wi-Fi setup fails
* The device cannot connect to the router
* The browser cannot open the device's web page
* OTA updates fail
* Cloud services are unavailable
* The device cannot be found on the local network

Check these items first:

1. Is the Wi-Fi network using 2.4GHz?
2. Are the SSID and password correct?
3. Does the router restrict new devices?
4. Is RootMaker too far from the router?
5. Is the antenna area obstructed by metal?
6. Does the project firmware support this network feature?

```markdown
- [What to Do When Wi-Fi Setup Fails]()
- [Device Web Page Does Not Open]()
- [How to Find the Device IP Address]()
- [Troubleshoot OTA Update Failures]()
- [Using 2.4GHz Wi-Fi]()
```

## Yoke Module Issues

This category covers Yoke module connection, recognition, and operation issues.

Common issues include:

* The module does not respond after connection
* Module data is abnormal
* The project does not recognize the module
* RootMaker restarts after connecting a module
* The module connector orientation is unclear
* Problems occur when using multiple modules together

Check these items first:

1. Is the module connected to the correct port?
2. Is the connector orientation correct?
3. Is the correct module selected in the project template?
4. Does the firmware support this module?
5. Are the cable connections secure?
6. Can the power supply meet the module's requirements?

```markdown
- [Yoke Module Not Recognized]()
- [Yoke Module Connector Orientation]()
- [Can Yoke Modules Be Hot-Plugged?]()
- [Using Multiple Yoke Modules Together]()
- [Yoke Module Compatibility Table]()
```

## Lighting Module Issues

This category primarily covers Yoke-TRGBW, RGBW LED boards, LED strips, and other lighting modules.

Common issues include:

* LEDs do not light up
* Colors are incorrect
* Lights flicker
* White light is abnormal
* Brightness changes are not smooth
* RootMaker restarts when controlling lights

Check these items first:

1. Is an RGBW lighting template selected?
2. Is the color order configured correctly?
3. Is sufficient current available?
4. Is the brightness set too high?
5. Is the data wire connected correctly?
6. Was the module connected or disconnected while powered on?

```markdown
- [What to Do When Yoke-TRGBW Does Not Light Up]()
- [Incorrect RGBW Colors]()
- [Flickering Lights or Device Restarts]()
- [How to Limit Lighting Brightness]()
- [Lighting Module Power Requirements]()
```

## Display and Touch Issues

This category covers display modules, touch modules, and button modules.

Common issues include:

* The screen does not turn on
* The screen orientation is incorrect
* Images are displayed incorrectly
* Touch input does not respond
* Touch input triggers falsely
* Buttons do not respond
* Button lights do not turn on

Check these items first:

1. Is the module connected to the correct port?
2. Is the screen mounted in the correct orientation?
3. Does the firmware match the display module?
4. Is the enclosure or conductive material affecting the touch area?
5. Is the button module enabled in the project template?

```markdown
- [What to Do When a Display Module Does Not Turn On]()
- [Setting Screen Orientation]()
- [Troubleshoot False Touch Triggers]()
- [Yoke-KEYW Button Does Not Respond]()
```

## Sensor Issues

This category covers radar, carbon dioxide sensors, thermal imaging modules, and other sensor modules.

Common issues include:

* The sensor produces no data
* Data changes unexpectedly
* The radar triggers falsely
* CO₂ readings are abnormal
* Thermal images are abnormal
* The sensor responds slowly

Check these items first:

1. Is the module connected to the correct interface?
2. Is the module mounted in the correct orientation?
3. Is the enclosure obstructing the sensor?
4. Is warm-up or calibration required?
5. Does the current project template support this sensor?
6. Is environmental interference affecting the sensor?

```markdown
- [Yoke-RAD60 False Radar Triggers]()
- [Abnormal Yoke-SCD4x Readings]()
- [Yoke-THERM5K Thermal Imaging Issues]()
- [Sensor Mounting Orientation]()
- [Sensor Calibration]()
```

## Power and Motor Issues

This category covers power supplies, batteries, motors, wireless power, and high-power modules.

Common issues include:

* RootMaker repeatedly restarts
* The motor does not rotate
* The device restarts when the motor runs
* Battery runtime is too short
* Wireless power is unstable
* Problems occur when lights and motors run together

Check these items first:

1. Does the power supply provide 5V / 1A or more?
2. Are high-power modules connected?
3. Is the motor's startup current too high?
4. Is the lighting brightness too high?
5. Is the battery module connected correctly?
6. Are the cables too thin or too long?

```markdown
- [What to Do When RootMaker Keeps Restarting]()
- [Motor Module Power Requirements]()
- [What to Do When Yoke-MOTO Does Not Work]()
- [Using the Battery Module]()
- [Using the Wireless Power Module]()
- [Precautions for High-Power Modules]()
```

## Zoner Platform Issues

This category covers the Zoner platform, project templates, configuration files, and firmware resources.

Common issues include:

* The project template cannot be found
* The project template cannot be downloaded
* The firmware version does not match
* The device does not respond after configuration
* Project settings cannot be saved
* Content is incomplete when opening a project page

Check these items first:

1. Is the correct Root controller model selected?
2. Are the selected Yoke modules the ones actually being used?
3. Does the firmware version match the hardware revision?
4. Is the browser cache preventing the page from updating?
5. Is the network connection working?
6. Is the project template still being updated or tested?

```markdown
- [Using the Zoner Platform]()
- [How to Choose a Project Template]()
- [Project Template Does Not Run]()
- [What to Do When Firmware Versions Do Not Match]()
- [How to Report Zoner Project Issues]()
```

## Development Environment Issues

This category covers Arduino, ESP-IDF, serial debugging, and custom development issues.

Common issues include:

* A board cannot be selected in Arduino
* Compilation fails
* ESP-IDF environment setup fails
* Serial logs contain garbled text
* Example projects do not run
* Custom code behaves incorrectly after flashing

Check these items first:

1. Does the development environment version meet the project requirements?
2. Is the correct board model selected?
3. Is the USB serial connection working?
4. Are all project dependencies installed?
5. Is the example code compatible with the current hardware revision?
6. Are the partition table and Flash settings correct?

```markdown
- [Arduino Development Environment Setup]()
- [ESP-IDF Development Environment Setup]()
- [Troubleshoot Compilation Failures]()
- [Viewing Serial Logs]()
- [Running Example Projects]()
```

## Mechanical Installation Issues

This category covers mounting in 3D prints, mechanical fastening, cable routing, and enclosure assembly.

Common issues include:

* The module is mounted in the wrong orientation
* The enclosure blocks the sensor
* The USB-C plug cannot be inserted
* Cables are pinched or bent
* The display window is incorrectly positioned
* Light diffusion is poor
* There is insufficient space for the battery or motor

Check these items first:

1. Are you using the correct version of the mechanical files?
2. Are the controller and modules oriented correctly?
3. Is there a USB-C access opening for maintenance?
4. Are the cables routed without obstruction?
5. Is the light-emitting surface, display, or sensor detection surface obstructed?
6. Is space provided for heat dissipation around high-power modules?

```markdown
- [RootMaker 3D Mounting Recommendations]()
- [Yoke Module Mounting Recommendations]()
- [Designing a USB-C Maintenance Opening]()
- [Cable Routing Recommendations]()
- [Designing Light Diffusion Structures]()
```

## Safety and Usage Precautions

Follow basic electronics safety requirements when using RootMaker and Yoke modules.

Pay particular attention to the following:

* Connecting or disconnecting modules while powered on is not recommended.
* Keep metal objects away from connectors and PCBs.
* Do not exceed the rated power capacity of the controller or modules.
* Lighting, motor, battery, and wireless power modules may draw high current or become hot.
* Children should use the products under adult supervision.
* If the device becomes unusually hot, smells abnormal, or emits smoke, disconnect power immediately and stop using it.

```markdown
- [Safe Use Guide]()
- [Power Supply Safety]()
- [Battery Module Safety]()
- [High-Power Module Precautions]()
- [Warnings for Use by Children]()
```

## Submit Feedback

If you cannot find an answer in the FAQ, use the following options to report your issue.

When reporting an issue, include the following information:

| Information | Example |
| ----------- | ------------------------------------ |
| Root Controller Used | RootMaker / hardware revision |
| Yoke Modules Used | Yoke-TRGBW, Yoke-RAD60, etc. |
| Project Template Used | Minecraft Ore Lamp, motion-activated light, etc. |
| Firmware Version | For example, v1.0.0 |
| Method Used | Zoner / WebTools / Arduino / ESP-IDF |
| Symptoms | No light, restarts, flashing failure, network connection failure, etc. |
| Serial Logs | Copy relevant logs, if available |
| Photos or Videos | Include wiring, device status, and the unexpected behavior |

```markdown
- [How to Submit Feedback]()
- [GitHub Issue]()
- [Discord Community]()
- [Contact Technical Support]()
```
