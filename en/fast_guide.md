---
title: "Ryzobee Quick Start Guide"
description: ""
tags: "Ryzobee, Home"
published: true
isPublished: true
---

# Ryzobee Quick Start Guide

Welcome to Ryzobee.  
Ryzobee is a modular electronics ecosystem for 3D printing creators, makers, developers, and educators. It simplifies adding lighting, motion, sensing, displays, voice, and connectivity to 3D-printed creations.

Root controllers, Yoke accessories, and the Zoner platform help you move quickly from an idea through mechanical design and module connections to a working project.

## 1. What You Can Do with Ryzobee

Ryzobee adds electronic functions and interactivity to otherwise static 3D prints.  
Install a Root controller inside your model and connect Yoke modules according to your project needs to add lighting, movement, sensing, displays, voice, or networking.

Common applications include:

| Application | What You Can Build |
| -------- | ------------------------------------------ |
| Lighting | RGBW mood lights, illuminated models, status lights, case lighting |
| Motion | Servo-driven ornaments, rotating mechanisms, desktop robots, vehicles, or gimbals |
| Sensing | Human presence detection, air quality monitoring, temperature distribution sensing |
| Displays | Status panels, expressive screens, sensor dashboards |
| Voice | AI conversational robots, voice-controlled lighting and motors |
| Portable Projects | Battery-powered devices, wirelessly powered ornaments, desktop displays |

Ryzobee helps you build a working creation that you can display and share without having to design circuits from scratch.

<div style="text-align: center;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Ryzobee_desc_800full.gif" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

## 2. No Coding / No Soldering / Plug and Play

Ryzobee is designed for rapid prototyping and recreating projects.  
Most official project templates require no coding or soldering. Simply connect the modules as instructed, then configure the project and flash firmware through Zoner.

The basic workflow is:

1. Choose a project template.
2. Prepare a Root controller and the required Yoke modules.
3. Connect the modules according to the wiring diagram.
4. Use Zoner to flash the firmware or configure the project.
5. Power on and run the project.
6. Install the controller and modules in your 3D-printed structure.

For beginners, we recommend the following projects:

| Starter Project | Recommended Combination |
| -------------- | ----------------------------------- |
| Your first lighting project | RootMaker + Yoke-TRGBW |
| Button-controlled lighting | RootMaker + Yoke-KEYW + Yoke-TRGBW |
| Motion-activated light | RootMaker + Yoke-RAD60 + Yoke-TRGBW |
| Small status panel | RootMaker + Yoke-1D54C |
| Air quality monitor | RootMaker + Yoke-SCD4x + Yoke-1D54C |

Developers can also use Arduino or ESP-IDF to modify project logic and add custom features.

## 3. Designing for 3D Printing

Ryzobee works well with 3D printing.  
When designing a model, reserve space for the Root controller, Yoke modules, cables, and mounting features to make the electronics easier to install, maintain, and display.

Consider the following when designing a 3D-printed structure:

- Root controller mounting position
- Yoke module fastening method
- Light-emitting areas, display windows, or sensor openings
- Cable routing paths
- USB-C access opening for maintenance
- Space for batteries or power modules
- Clearance for heat dissipation and assembly

---

### 3.1 Interface System

<div style="text-align: center;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Ryzobee_interface_desc_800full.gif" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

Ryzobee uses standardized interfaces to connect controllers and expansion modules.  
Different interfaces suit different Yoke modules. Reserve installation space according to the connector locations.

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Interface_desc_RSPORT.png.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">RS-Port</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
      RS-Port connectors provide good mechanical strength and a secure connection that resists loosening. Cables can extend connections over a limited distance, making them suitable for 3D-printed models, desktop devices, and projects with distributed components.  
RS-Port is RootMaker's most commonly used peripheral interface because it is convenient and flexible.
    </p></div></div></div></div>



<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Interface_desc_FBUS.png.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">F-BUS</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
F-BUS modules can usually be secured to the RootMaker controller or other mechanical parts with screws for greater strength and mounting reliability.
RootMaker provides F-BUS connectivity on both the top and bottom. Refer to the relevant Yoke module instructions for connection details.
    </p></div></div></div></div>

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Interface_desc_SBUS.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">S-BUS</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    S-BUS uses an edge connector, which provides weaker mechanical retention than RS-Port or F-BUS. It is better suited to lightweight modules or frequent assembly and removal. For long-term operation, portable use, or vibration, add mechanical support appropriate to the module.
    </p></div></div></div></div>

Design recommendations:

- RS-Port modules can be mounted at different positions in a model using extension cables.
- F-BUS modules are generally best stacked with or mounted close to the controller.
- S-BUS modules suit lightweight expansion or dedicated functions.
- Leave room around USB-C for connecting and disconnecting the cable during flashing and maintenance.

### 3.2 Cable System

The cable system connects Root controllers to Yoke modules.  
Good cable planning makes 3D-printed creations tidier, more reliable, and easier to repair.

Common cables include:

| Cable Type | Purpose |
| ---------------- | --------------------------------------- |
| RS-BUS to RS-BUS | Connect a Root controller to RS-Port Yoke modules |
| RS-BUS to Dupont Jumper Wires | Connect custom peripherals or experimental circuits |
| RS-BUS to Grove | Connect certain Grove sensors or peripherals |
| USB-C Cable | Power, firmware flashing, and serial debugging |

Cable design recommendations:

- Provide routing channels or clips for cables.
- Prevent the enclosure from pinching or sharply bending cables.
- Keep power cables for high-power modules short and secure.
- Leave cable slack near moving parts.
- Provide maintenance openings in enclosed models for reconnecting cables.
- Organize cables for lighting, sensors, and displays into separate groups where possible.

### 3.3 Mechanical Mounting System

Root controllers and Yoke modules can be secured with screws, clips, 3D-printed brackets, or compatible building-block mounting holes.  
Good mechanical mounting improves project reliability and makes creations easier to reproduce and share.

Mechanical design recommendations:

| Design Item | Recommendation |
| ------------ | ---------------------------------------------- |
| Controller Mounting | Provide a flat mounting surface and screw holes for the Root controller |
| Module Mounting | Choose the mounting angle according to the light-emitting surface, display orientation, or sensing direction |
| USB-C Maintenance Opening | Leave sufficient cable access for flashing and power |
| Heat Dissipation | Leave space around high-power modules such as lights, motors, and batteries |
| Cable Routing | Use concealed channels or clips to avoid exposed cables |
| Maintenance Access | Provide openings in enclosed structures for module replacement |
| Mechanical Strength | Prevent moving or load-bearing parts from pulling directly on connectors |

If your project uses display, thermal imaging, or radar modules, pay special attention to opening locations and orientation:

- Display modules need a screen window.
- Thermal imaging modules must not be blocked by the enclosure.
- Radar modules should face the detection area.
- Lighting modules can be used with diffusers or translucent materials.
- Voice modules need acoustic openings for the microphone and speaker.

## 4. Powerful Wireless Capabilities

Root controllers support 2.4GHz Wi-Fi and Bluetooth LE for device configuration, network control, web interaction, cloud services, wireless debugging, and more.

Wireless connectivity lets a Ryzobee project become a smart device controlled by a phone, computer, or cloud service in addition to running locally.

Common wireless applications include:

| Wireless Feature | Application |
| ------------ | ------------------------------------------- |
| Wi-Fi Setup | Connect the device to a local network |
| Web Control Page | Control lighting, motion, or settings through a browser |
| OTA Firmware Updates | Update firmware without reconnecting USB |
| Cloud APIs | Integrate with cloud services, AI services, or data platforms |
| MQTT / HTTP | Communicate with Home Assistant, OctoPrint, or other platforms |
| Bluetooth LE | Configure, discover, or control nearby devices |

When using wireless features, note the following:

- Root controllers typically use 2.4GHz Wi-Fi networks.
- Check that the Wi-Fi name and password are correct.
- Metal enclosures or enclosed structures may affect wireless signals.
- Keep the antenna area away from metal parts, batteries, and large copper foil areas.
- If the wireless connection is unstable, move closer to the router.
- Some AI, cloud, or web control features require an internet connection.

## 5. Glossary

The following terms are commonly used with Ryzobee.

| Term | Description |
| --------------- | ------------------------------------------------------------ |
| Root Controller | The core controller in the Ryzobee ecosystem; runs firmware and controls peripheral modules |
| RootMaker | The main model in the Root controller series, suited to most maker and interactive 3D printing projects |
| Yoke Module | Ryzobee accessories that add lighting, displays, sensing, voice, motors, power, and other functions |
| RS-Port | A common expansion interface on Root controllers for small Yoke modules |
| RS-BUS | The connection or cable system associated with RS-Port |
| F-BUS | An expansion interface for complex modules such as displays, thermal imagers, and batteries |
| S-BUS | An expansion interface for voice, audio, or dedicated modules |
| Zoner | Ryzobee's project template and configuration platform |
| Firmware | Software running on a Root controller to control device functions |
| Project Template | An official reproducible project configuration, usually including firmware, wiring, modules, and instructions |
| OTA | Over-the-Air firmware updates |
| GPIO | General-purpose input/output pins for connecting and controlling electronic peripherals |
| I²C | A common communication bus for sensors |
| PWM | Pulse-width modulation, commonly used to control servos, motors, or lighting brightness |
| RGBW | Red, green, blue, and white lighting; adds an independent white channel to standard RGB |
| 3D Mounting Files | STL, STEP, 3MF, and other mechanical files for mounting controllers or modules |

## Zoner Platform

Zoner is Ryzobee's platform for quickly configuring project templates.  
In Zoner, users can find official projects, select Root controllers and Yoke modules, view wiring instructions, download or flash firmware, and configure project parameters.

Zoner is suitable for:

| User Type | Usage |
| ------------- | -------------------------------------------------- |
| Beginners | Choose an official template, connect modules as instructed, and run the project |
| 3D Printing Creators | Find complete projects to recreate, including mechanical files, firmware, and assembly instructions |
| Makers | Quickly test lighting, motors, sensors, voice, and other functions |
| Developers | Customize official templates |
| Educators | Organize courses or workshops using standardized project templates |

Zoner helps users:

- Find project templates
- View required hardware
- View wiring instructions
- Obtain firmware resources
- Configure Wi-Fi or project parameters
- View assembly guides
- Download 3D mounting files
- Recreate official projects

Zoner helps users move from an idea to a working creation faster, reducing repetitive configuration, wiring errors, and time spent finding firmware.

<div style="border-radius: 10px; padding: 15px; background: linear-gradient(135deg, #FFBA89 0%, #FFD884 100%); margin: 4px 0px; box-shadow: none;"><div style="max-width: 800px; margin: 0px auto; text-align: center; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;"><p style="color: #4B1F00; margin: 0px 0px 1px; font-size: 22px; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;">
      🥈 <strong>Visit the Zoner Wiki page for more platform features.</strong></p> 
<a href="/en/Zoner" target="_blank" class="is-internal-link is-valid-page" style="display: inline-block; padding: 4px 50px; background:#ffffff; color: #000000; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; margin-top: 15px; box-shadow: none;">
      📖 View the Zoner Wiki →
</a></div></div>