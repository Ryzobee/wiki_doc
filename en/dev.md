---
title: "Ryzobee Developer Center"
description: "Browse developer resources here"
tags: "Developer, Home"
published: true
isPublished: true
---

Welcome to the Ryzobee Developer Center.  
This page is for users developing custom applications, firmware, drivers, or project templates for Root controllers and Yoke modules.

If you simply want to recreate official projects quickly, start with the Zoner platform.
Start here if you want to modify code, develop your own features, add support for new modules, or build a complete project.

## Development Options

Ryzobee currently supports the following main development approaches:

| Approach | Status | Intended Users | Description |
|---|---|---|---|
| Ryzobee Arduino Development | Available | Beginners, makers, educators | Quickly write examples and control lighting, motors, sensors, and basic interactions |
| Ryzobee ESP-IDF Development | `Under construction` | Advanced developers, firmware engineers | Complex projects, low-level drivers, network services, OTA, and performance optimization |
| Zoner Project Templates | Available / continuously improving | Beginners and users recreating projects | Quickly configure and run projects using templates |

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
    <h3 class="toc-header" style="margin-top: 0px; color:#FFA600;"><a href="https://github.com/Ryzobee"
            class="toc-anchor"></a>📝<a style="color: #FF6A00; text-decoration: none;">Choose Your Development Environment</a></h3>
    <p style="margin-bottom: 10px;">
        If you want to write your own firmware, use the buttons below to explore the available development environments.
    </p>
    <div style="text-align: center;">
        <div
        style="display: inline-block; width: 18%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
        <a href="/en/dev/Arduino" target="_blank">
            <img src="https://res.8ms.xyz/ryzobee/wiki/Arduino_icon_200.png" alt="RootMaker"
                style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;">
            <br>
            Arduino Development
        </a>
    </div>
    <div
        style="display: inline-block; width: 18%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
        <a href="/en/dev/ESPIDF" target="_blank">
            <img src="https://res.8ms.xyz/ryzobee/wiki/esp_icon_200.png" alt="RootMaker"
                style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;">
            <br>
            IDF Development
        </a>
    </div>
    </div>
</div>

## Ryzobee Arduino Development

Arduino is suitable for users who want to get started quickly with RootMaker and Yoke modules.  
With Arduino, you can easily control RGBW lighting, read sensors, drive motors, handle button input, and build interactive projects quickly.

Suitable for:

- Quickly lighting up a Yoke-TRGBW RGBW lighting module
- Reading data from a Yoke-SCD4x carbon dioxide sensor
- Using Yoke-KEYW or Yoke-TOUCH4 for input control
- Building simple lighting, sensor, or desktop interactive projects
- Modifying official examples for your own applications

Resources:

- [Ryzobee Arduino Development Guide](/en/dev/Arduino)
- [RootMaker Arduino API](/en/dev/rootmaker_arduino_api)
- [Arduino Example Projects]()`Under construction`

## Ryzobee ESP-IDF Development

ESP-IDF is the official low-level development option for advanced developers building more complex, reliable, and complete firmware projects.

This section is under construction. RootMaker ESP-IDF project templates, component drivers, network services, file systems, OTA, WebServer, and Yoke module integration examples will be added gradually.

Suitable for:

- Projects needing a more complete structure
- FreeRTOS multitasking
- WebServer, OTA, MQTT, or cloud communication features
- Support for complex Yoke modules
- Production-grade firmware development
- Finer control over memory, tasks, and peripheral resources

Planned content:

- [Ryzobee ESP-IDF Development Guide]() `Under construction`
- [ESP-IDF Environment Setup]() `Under construction`
- [RootMaker IDF Project Template]() `Under construction`
- [Yoke Module Driver Development]() `Under construction`
- [OTA Firmware Updates]() `Under construction`

> This section is being prepared. If you are already familiar with ESP-IDF, you can start with the official examples and RootMaker hardware interface documentation.

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA600;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📝<a style="color: #FF6A00; text-decoration: none;"> View Our Repositories on GitHub</a></h3>
  <p style="margin-bottom: 10px;">
  For source code and custom development, visit our GitHub repositories to find our SDK and Arduino examples.
  </p>
<div style="text-align: center;"><a href="https://github.com/Ryzobee" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     Go to GitHub →
</a></div></div>

## Before You Start

Before starting development, check the following:

| Preparation | Description |
| ------------ | ------------------------------------- |
| Root Controller | The controller model you are using, such as RootMaker |
| Hardware Revision | Interfaces and pin assignments may differ between revisions |
| Yoke Modules | Confirm the module models and interface types you need |
| USB-C Data Cable | Use a USB-C cable that supports data transfer |
| Development Approach | Choose Arduino or ESP-IDF according to your needs |
| Firmware Version | Confirm that your example or SDK matches the current hardware |
| Serial Tool | View logs, debug startup information, and troubleshoot issues |

For your first project, run an official example to verify the hardware, cable, and environment before modifying the code.

## Hardware Reference

When developing, first consult the interface descriptions and pin definitions for your hardware revision.
Modules use different interfaces. Confirm the interface, power requirements, communication method, and mounting orientation before development.

Common reference pages:

- [RootMaker Controller](/en/root/rootmaker/rootmaker)
- [Yoke Accessory Ecosystem](/en/Yoke_Model)

## Contributions and Feedback

Ryzobee welcomes developers to help build its ecosystem.
You can contribute example projects, improve documentation, report issues, add support for new Yoke modules, or share your own project templates.

You can contribute:

- Example code
- Bug reports
- Documentation corrections
- Drivers for new modules
- Project templates
- 3D mounting structures
- Tutorials
- Use cases

When submitting feedback, include the following information:

| Information | Example |
| -------- | ------------------------- |
| Controller Model | RootMaker |
| Hardware Revision | ZXROOTEC08 / other revision |
| Development Approach | Arduino / ESP-IDF |
| Modules Used | Yoke-TRGBW, Yoke-RAD60, etc. |
| Firmware Version | v1.0.0 |
| Issue Description | Symptoms, steps to reproduce, expected result |
| Logs | Serial logs, compilation errors, screenshots |

## Developer Support

If you encounter a problem during development, first check the FAQ, example projects, and hardware reference pages.
If the issue persists, submit it through the community or technical support channels.

Support resources:

- [Frequently Asked Questions](/en/faq)
- [Discord Community]()`Under construction`
- [GitHub Repositories](https://github.com/Ryzobee)
- [Contact Technical Support]()`Under construction`
