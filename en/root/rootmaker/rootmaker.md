---
title: "RootMaker Controller"
description: "Start your creative journey with the RootMaker controller"
tags: "Rootmaker, root, main"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/RootMaker.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">RootMaker</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    RootMaker is the main controller in the RyzoBee / Root series, designed for makers, 3D printing creators, and interactive hardware projects.  
It serves as the electronic brain of a 3D-printed creation, connecting and controlling Yoke accessories to provide lighting, displays, sensing, voice, motors, touch, and network interaction.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

### Key Features:

- Controller hardware for 3D-printed creations and maker projects
- Supports a wide range of Yoke accessories
- Expandable lighting, motors, sensors, displays, voice, and touch functions
- Wi-Fi / BLE wireless connectivity
- USB-C connection to a computer for power, flashing, and debugging
- Zoner project templates simplify configuration and project recreation
- Arduino / ESP-IDF development support

## Components

RootMaker includes several interfaces, buttons, indicators, and mounting components. The numbers in the figure below identify the components and their main functions.

<div style="display:flex;flex-wrap:wrap;gap:16px;margin:20px 0;">
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/component_desc_1.png" alt="Image 1" style="width:100%;display:block;border-radius:12px;">
  </div>
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/component_desc_2.png" alt="Image 2" style="width:100%;display:block;border-radius:12px;">
  </div>
</div>


| No. | Component | Description |
| ---- | ------------------ | ------------------------------------------------------------ |
| 1 | RGB LED Indicator | Displays operating status, connection status, or custom project lighting effects. |
| 2 | S-BUS Interface | Connects S-BUS expansion modules, such as dedicated voice or audio modules. |
| 3 | RS-PORT2 Interface | Connects RS-Port Yoke modules. |
| 4 | RS-PORT4 Interface | Connects RS-Port Yoke modules. |
| 5 | USB-C Interface | Provides power, firmware flashing, serial debugging, and data communication. |
| 6 | BOOT Button | Enters download mode or performs firmware-defined functions. |
| 7 | F-BUS Interface | Connects F-BUS expansion modules such as displays, thermal imagers, or batteries. |
| 8 | RESET / POWER Button | Multifunction button: short press to reset; long press to turn on or off when battery-powered. |
| 9 | RS-PORT1 Interface | Connects RS-Port Yoke modules. |
| 10 | RS-PORT3 Interface | Connects RS-Port Yoke modules. |
| 11 | Top Decorative Cover | Completes the device's appearance and serves as a decorative and identifying component. |
| 12 | F-BUS Interface | Connects F-BUS expansion modules. |
| 13 | LEGO-Compatible Mounting Holes* | Secure the device to compatible building-block structures, 3D-printed parts, or project enclosures. |
| 14 | M1.2 Screws | Secure the top decorative cover, enclosure, or related mechanical parts. |

>LEGO® is a registered trademark of the LEGO Group. This product is not an official LEGO Group product and is not authorized, sponsored, or endorsed by the LEGO Group. Building-block compatibility refers only to mechanical dimensions and does not imply a brand partnership.



## Interfaces

RootMaker provides several expansion interfaces for display, lighting, sensor, voice, motor, touch, and power modules.  
The interfaces differ in structure, number of signals, power capacity, and intended use.

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📘<a style="color: #FF6A00; text-decoration: none;"> Detailed Interface Specifications</a></h3>
  <p style="margin-bottom: 10px;">
  Developers who need detailed I/O mappings should consult the detailed interface specifications.
  </p>
<div style="text-align: center;"><a href="#P_PORT_INFO" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     Go to Detailed Interface Specifications →
    </a></div></div>

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/Rootmaker_RSPort.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">RS-Port</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
      RS-Port refers to the four locking connectors on the sides of RootMaker: RS-PORT1, RS-PORT2, RS-PORT3, and RS-PORT4.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
      RS-Port connectors provide good mechanical strength and a secure connection that resists loosening. Cables can extend connections over a limited distance, making them suitable for 3D-printed models, desktop devices, and projects with distributed components.  
RS-Port is RootMaker's most commonly used peripheral interface because it is convenient and flexible.
    </p>
    <a href="#P_YOKE_RS_SUPPLY_LIST" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 0px 20px 0px 0px; box-shadow: none;">
    View the Yoke Compatibility List →
    </a>
    </div></div></div></div>



<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/Rootmaker_FBUS.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">F-BUS</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
      F-BUS is the expansion interface on the top and bottom of RootMaker, primarily for displays, image sensors, thermal imagers, battery modules, and other complex Yoke peripherals.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
F-BUS modules can usually be secured to the RootMaker controller or other mechanical parts with screws for greater strength and mounting reliability.
RootMaker provides F-BUS connectivity on both the top and bottom. Refer to the relevant Yoke module instructions for connection details.
    </p>
    <a href="#P_YOKE_FB_SUPPLY_LIST" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 0px 20px 0px 0px; box-shadow: none;">
    View the Yoke Compatibility List →
    </a></div></div></div></div>

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/Rootmaker_SBUS.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">S-BUS</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
	S-BUS is the edge connector on the underside of RootMaker, suited to certain dedicated Yoke peripherals or expansion modules requiring quick insertion and removal. Its compact, convenient design is suitable for voice, audio, debugging, temporary expansion, and specialized modules.
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    S-BUS uses an edge connector, which provides weaker mechanical retention than RS-Port or F-BUS. It is better suited to lightweight modules or frequent assembly and removal. For long-term operation, portable use, or vibration, add mechanical support appropriate to the module.
    </p>
    <a href="#P_YOKE_SB_SUPPLY_LIST" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 0px 20px 0px 0px; box-shadow: none;">
    View the Yoke Compatibility List →
    </a></div></div></div></div>

### Interface Connection Precautions

> Connect or disconnect external modules only when the power is off.  
> When using high-power modules, make sure RootMaker's power capacity meets the project's requirements.  
> Interface definitions may differ between hardware revisions. Refer to the documentation for your current revision.

## Usage Instructions

<div style="border-radius: 10px; padding: 15px; background: linear-gradient(135deg, #FFBA89 0%, #FFD884 100%); margin: 4px 0px; box-shadow: none;"><div style="max-width: 800px; margin: 0px auto; text-align: center; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;"><p style="color: #4B1F00; margin: 0px 0px 1px; font-size: 22px; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;">
      🥇 <strong>New to Ryzobee? Start here for a quick introduction to the product ecosystem.</strong></p> 
<a href="/en/fast_guide" target="_blank" class="is-internal-link is-valid-page" style="display: inline-block; padding: 4px 50px; background:#ffffff; color: #000000; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; margin-top: 15px; box-shadow: none;">
      📖 View the Quick Start Guide →
</a></div></div>


### Before Use

Complete the following preparations before using RootMaker to ensure the device can connect, flash, and run projects correctly.

#### 1. Check the Package Contents

Make sure the controller, cables, and accessories are complete and undamaged.  
If you have a kit, also check that the Yoke modules, cables, screws, and mechanical parts are all present.

Recommended checks:

| Item | Description |
|---|---|
| RootMaker Controller | Check for visible damage |
| USB-C Cable | For power, firmware flashing, and serial debugging |
| Yoke Modules | Prepare the modules required by your project |
| RS Cables | For connecting RS-Port modules |
| Mounting Screws / Mechanical Parts | For mounting the controller or expansion modules |
| Quick Start Card | Basic connections and resource links |

#### 2. Prepare Power and Connection Equipment

RootMaker is powered through USB-C. Use a **5V / 1A or higher** power adapter or a computer USB port.

For flashing firmware or debugging, connect to a computer with a USB-C data cable. Charge-only USB-C cables cannot be used for flashing or serial communication.

<div style="text-align: center;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/Rootmaker_con2cmp.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

> **Before Use**
> Use a stable 5V power supply and avoid low-quality or worn USB cables.
> When connecting high-power modules such as lights, motors, or displays, make sure sufficient power is available.
> Repeated restarts may indicate insufficient power or an excessive load from external modules.

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📘<a style="color: #FF6A00; text-decoration: none;"> The following instructions use Zoner for rapid development.</a></h3>
  <p style="margin-bottom: 10px;">
  Developers who want to use Arduino or ESP-IDF should visit the Developer Center.
  </p>
<div style="text-align: center;"><a href="/en/dev" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     Go to the Developer Center →
    </a></div></div>

#### 3. Prepare Your Browser

**3.1 Open the Zoner tools platform in your browser using the link below.**

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:13px 16px;background:#fff7ed;border:1px solid #ffd4ad;border-radius:10px;">
  <div style="font-size:13px;color:#555;line-height:1.5;">
    <strong style="color:#222;font-size:15px;">Visit Zoner</strong><br>
    Click the button on the right to visit Zoner, or enter zoner.ryzobee.com in your browser's address bar.
  </div>
  <a href="https://www.ryzobee.com" target="_blank" rel="noopener noreferrer" style="padding:7px 12px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Visit Zoner</a>
</div>

**3.2 Check that the device is connected correctly to your PC, then click Connect.**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step1.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

**3.3 Select the serial port to connect to in the browser dialog.**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step2.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

**3.4 Choose the project template you want to download. Click the “Flash to Device” icon, or click the project card to open its details.**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step3.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

**3.5 Click “Flash this project to Device” to update the device's project firmware.**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step4.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

**3.6 Wait for the firmware update to finish. It takes 10-60 seconds depending on the project. Do not disconnect the USB-C cable or press Reset during the update.**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step5.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

<div style="border-radius: 10px; padding: 15px; background: linear-gradient(135deg, #FFBA89 0%, #FFD884 100%); margin: 4px 0px; box-shadow: none;"><div style="max-width: 800px; margin: 0px auto; text-align: center; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;"><p style="color: #4B1F00; margin: 0px 0px 1px; font-size: 22px; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;">
      🥈 <strong>Visit the Zoner Wiki page for more platform features.</strong></p> 
<a href="/en/Zoner" target="_blank" class="is-internal-link is-valid-page" style="display: inline-block; padding: 4px 50px; background:#ffffff; color: #000000; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; margin-top: 15px; box-shadow: none;">
      📖 View the Zoner Wiki →
</a></div></div>

#### 4. Prepare Yoke Modules

Select the Yoke modules required for your project and confirm that their interface types match RootMaker's ports.

Turn off RootMaker before connecting modules, and check the connector orientation.

#### 5. Check Project Resources

Before building, check the project's wiring instructions, firmware version, mechanical files, and precautions.

**Check the following:**

- Root controller model used in the project
- Required Yoke modules
- Matching firmware or project template
- Interface connections
- Power requirements
- 3D-printing mechanical files
- Known issues and limitations

#### 6. Safety Precautions

Before connecting, flashing, or running the project, observe the following:

- Do not connect or disconnect modules while powered on.
- Keep metal objects away from the controller's connectors and circuit board.
- Check connector orientation to avoid reversed connections.
- Do not exceed the rated power capacity of the controller or modules.
- Pay particular attention to current, temperature rise, and heat dissipation when using motors, LED strips, batteries, or wireless power modules.
- Children should operate the device under adult supervision.

### RootMaker Quick Guide: Digital Copy


<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">RootMaker Quick Guide</div>
      <div style="font-size:12px;color:#777;">PDF · V1.3 · 5.1 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8%E6%8C%87%E5%8D%97V13_H20260603.pdf" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## Hardware Specifications

| Item | Specification |
| ------------- | ------------------------------------------------------------ |
| Product Name | RootMaker |
| Product Model | ZXRoot-Maker |
| Dimensions | Base unit: 40mm × 40mm × 10.1mm<br>Display kit: 40mm × 40mm × 15.4mm |
| Wireless Connectivity | 2.4GHz Wi-Fi / Bluetooth LE |
| USB Interface | USB-C |
| USB Functions | Power, firmware flashing, serial debugging, device configuration |
| Input Voltage | 5V DC |
| System Operating Voltage | 3.3V |
| Recommended Power Supply | 5V / 1A or higher |
| Supported Development Environments | Arduino, ESP-IDF |
| Main Interfaces | USB-C, RS-Port / RS-BUS, F-BUS, S-BUS |
| Intended Users | Makers, 3D printing creators, developers, educators |
| Operating Temperature* | 0°C ~ 40°C |
| Storage Temperature | -20°C ~ 60°C |
| Operating Humidity | 10% ~ 90% RH, non-condensing |
| Storage Humidity | 5% ~ 95% RH, non-condensing |

> *The operating temperature is the recommended range. When connecting high-power modules such as lighting, motors, displays, or batteries, consider power capacity, cooling, and installation space.

##  3D Mounting Files

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP File ZXRootMaker_v14_AIO_H20251128</div>
      <div style="font-size:12px;color:#777;">STEP · V1.4 · 44.8 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/ZXRootMaker_v14_AIO_H20251128.STEP" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>
## Detailed Interface Specifications<a id="P_PORT_INFO"></a>

### RS-Port
<div style="text-align: center;">
<img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rs_port_interface.png" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>


| Item | Specification | Notes |
| ------------ | --------- | -------------------------------- |
| Physical Connector | GH1.25-4P | |
| GPIO Logic Level | 3.3V TTL | Use a level shifter with devices above 3.3V TTL; otherwise the GPIO port may be damaged |
| GPIO Count | 2 | Each RS-Port provides 2 GPIOs |
| 3.3V Power Capacity | 0.8A MAX | Each RS-Port provides 0.8A; total 3.3V output must not exceed 1.5A |

### F-BUS

<div style="text-align: center;">
<img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/f_bus_interface.png" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>


| Item | Specification | Notes |
| ------------ | --------- | -------------------------------- |
| Physical Connector | 1.27mm 2×12 female header | Both top and bottom use 1.27mm 2×12 female headers |
| GPIO Logic Level | 3.3V TTL | Use a level shifter with devices above 3.3V TTL; otherwise the GPIO port may be damaged |
| GPIO Count | 16 | Each RS-Port provides 2 GPIOs |
| 3.3V Power Capacity | 1.0A MAX | Each 3V3 pin supplies 0.5A; total 3.3V output must not exceed 1.5A |
| [*VBAT Power Capacity* *](#P_VBAT_NOTE) | 1.0A MAX | Each VBAT pin supplies 0.5A |

### S-BUS

<div style="text-align: center;">
<img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/s_bus_interface.png" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>


| Item | Specification | Notes |
| ------------ | --------- | -------------------------------- |
| Physical Connector | SFP edge connector | |
| GPIO Logic Level | 3.3V TTL | Use a level shifter with devices above 3.3V TTL; otherwise the GPIO port may be damaged |
| GPIO Count | 14 | Each RS-Port provides 2 GPIOs |
| 3.3V Power Capacity | 1.0A MAX | Each 3V3 pin supplies 0.5A; total 3.3V output must not exceed 1.5A |
| [*VBAT Power Capacity* *](#P_VBAT_NOTE) | 1.0A MAX | Each VBAT pin supplies 0.5A |
| VBUS Power Capacity | V<sub>BAT</sub>~5V @ 0.5A | VBUS combines the USB and VBAT inputs. On battery power, the voltage is V<sub>BAT</sub>; on USB power, it is 5V |

<a id="P_VBAT_NOTE"></a>
> **VBAT Pin Notes**
>
> With USB connected, the battery can be charged through VBTA at approximately 500mA. A battery of at least 1000mAh is recommended (0.5C). Maximum output current depends on the battery's capability and is typically no greater than 2A. When on/off control is required with a continuously powered source, the battery connector can also accept an external supply of no more than 5V.
>
> VBUS follows the power on/off state and is unpowered when the device is off.

## Supported Yoke Modules

### RS-PORT<a id="P_YOKE_RS_SUPPLY_LIST"></a>

- [Yoke-KEYW Tactile Switch Module](/en/Yoke_Model/Yoke-KEYW-ZH)
- [Yoke-MOTO DC Motor Control Module](/en/Yoke_Model/Yoke-MOTO-ZH)
- [Yoke-RAD60 60GHz Millimeter-Wave Presence Sensor Module](/en/Yoke_Model/Yoke-RAD60-ZH)
- [Yoke-RGBW RGBW Lighting Module](/en/Yoke_Model/Yoke-RGBW-ZH)
- [Yoke-TRGBW 3x RGBW Lighting Module](/en/Yoke_Model/Yoke-TRGBW-ZH)
- [Yoke-TOUCH4 Four-Channel Touch Module](/en/Yoke_Model/Yoke-TOUCH4-ZH)

### F-BUS<a id="P_YOKE_FB_SUPPLY_LIST"></a>



### S-BUS<a id="P_YOKE_SB_SUPPLY_LIST"></a>

## Exploded View

<div style="text-align: center;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/RootMaker_main_img.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

## Frequently Asked Questions

### What if the computer does not recognize RootMaker?

Check that the USB-C cable supports data transfer and the computer's USB port works, then try entering download mode again.

---

### What if firmware flashing fails?

Make sure RootMaker is in download mode, the browser or development tool has permission to access the serial port, and the selected firmware matches your hardware revision.

---

### What if RootMaker does not respond after power-on?

Check the power supply and USB-C cable. Check whether an external module is shorted or a high-power module has triggered power protection.

---

### What if the device restarts after connecting a Yoke module?

Possible causes include insufficient power, reversed module connections, poor cable contact, or excessive load.  
First turn off power and disconnect external modules. Confirm that RootMaker starts by itself, then connect and test the modules one at a time.

---

### Can I connect or disconnect Yoke modules while powered on?

Hot-plugging is not recommended.  
Connect or disconnect modules with the power off to prevent connector short circuits, communication errors, or module damage.

---

### Is Zoner required to use RootMaker?

No.  
Zoner is useful for quick configuration and recreating projects. Developers can also use Arduino or ESP-IDF for custom development.

---

### Can RootMaker connect to multiple Yoke modules?

Yes, depending on the number of interfaces, firmware support, and total power capacity.  
Pay particular attention to the available power margin when using lighting, motor, display, or voice modules together.

---

### What if Wi-Fi connection fails?

Make sure the network uses 2.4GHz Wi-Fi and the SSID and password are correct. Avoid special characters and weak signal conditions.  
If the project supports Wi-Fi reconfiguration, follow its instructions to enter setup mode.

---

### How do I restore the default firmware?

Select the official default template in Zoner and flash the firmware again.  
If the device cannot enter normal mode, try entering download mode and reflashing.

---

### What projects is RootMaker suitable for?

RootMaker is suitable for interactive 3D prints, desktop robots, lighting installations, sensor panels, AI voice devices, educational projects, and rapid hardware prototyping.
