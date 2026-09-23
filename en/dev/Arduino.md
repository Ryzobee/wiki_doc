---
title: "Ryzobee Arduino Library"
description: "Ryzobee Arduino Library Tutorial"
tags: "Arduino, lib"
published: true
isPublished: true
---

Ryzobee Arduino is an Arduino support library designed for Ryzobee development boards. It provides a unified programming interface across board models to make development faster and more efficient.

## Library Overview

The Ryzobee library uses a modular architecture and supports multiple board models. Each board is preconfigured; simply include the header file and specify the board type to get started.

Key features:

- A unified board abstraction layer supporting multiple board models
- Initialize all peripherals with a single line of code
- Enable or disable individual peripherals as needed
- Built-in I2C mutex for safe bus sharing across peripherals
- A wide range of example programs
- Compatible with Yoke expansion modules

## Installation

### 1. Install ESP32 Board Support

Open **Tools > Board > Boards Manager**, search for `esp32`, and install **esp32 by Espressif Systems** (>=v3.3.7).

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_ESP32_pakge.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

### 2. Install the Ryzobee Library

In the Arduino IDE, open **Tools > Manage Libraries**, search for `Ryzobee`, and click Install.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_Ryzobee.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

### 3. Select a Root Series Board

In the Arduino IDE, open **Tools > Board > esp32 > Root Maker**.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Snipaste_2026-06-05_17-10-10.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

### 3. Install Dependencies

In the Arduino IDE, open **Tools > Manage Libraries**, then search for and install the following dependencies:

| Name | Minimum Version | Description |
|:---:|:---:|:---|
| LovyanGFX | >=v1.2.19 | High-performance graphics library for SPI LCDs |
| Adafruit_NeoPixel | >=v1.12.3 | WS2812B RGB LED driver library |
| LIS2DW12 | >=v2.1.1 | LIS2DW12 3D accelerometer driver library |
| AnimatedGIF | >=2.2.0 | GIF animation playback library |

<div style="display:flex;flex-wrap:wrap;gap:16px;margin:20px 0;">
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_LovyanGFX.png" alt="Image 1" style="width:100%;display:block;border-radius:12px;">
  </div>
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_Adafruit_NeoPixel.png" alt="Image 2" style="width:100%;display:block;border-radius:12px;">
  </div>
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_LIS2DW12.png" alt="Image 2" style="width:100%;display:block;border-radius:12px;"></div>
   <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_AnimatedGIF.png" alt="Image 2" style="width:100%;display:block;border-radius:12px;"></div>
</div>


## Basic Usage

```cpp
#include "Ryzobee.h"

// Create a board instance (specify the board model)
Ryzobee board(RYZOBEE_ROOTMAKER);

void setup(void)
{
    Serial.begin(115200);
    board.rootmaker.begin();
}

void loop(void)
{
    // Your code here
}
```

## Supported Boards

| Name | Model Constant | Documentation |
|:---:|:---:|:---:|
| RootMaker | RYZOBEE_ROOTMAKER | [RootMaker API Guide](/en/dev/rootmaker_arduino_api) |

> Support for more board models is being added. Stay tuned for updates.

## License

This project is licensed under the MIT License.
