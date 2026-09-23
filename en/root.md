---
title: "Root Controller Series"
description: "Explore the Root controller series here"
tags: "Root, Home"
published: true
isPublished: true
---
<div style="border-radius: 10px; padding: 15px; background: linear-gradient(135deg, #FFBA89 0%, #FFD884 100%); margin: 4px 0px; box-shadow: none;"><div style="max-width: 800px; margin: 0px auto; text-align: center; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;"><p style="color: #4B1F00; margin: 0px 0px 1px; font-size: 22px; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;">
      🥇 <strong>New to Ryzobee? Start here for a quick introduction to the product ecosystem.</strong></p> 
<a href="/en/fast_guide" target="_blank" class="is-internal-link is-valid-page" style="display: inline-block; padding: 4px 50px; background:#ffffff; color: #000000; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; margin-top: 15px; box-shadow: none;">
      📖 View the Quick Start Guide →
</a></div></div>


## Root Controller Series


The Root series is Ryzobee's range of modular smart controllers for makers, 3D printing enthusiasts, creative developers, and education.

Root controllers serve as the core control unit for 3D prints, creative installations, desktop robots, lighting projects, sensor projects, and interactive devices. Standardized module interfaces, visual tools, example projects, and an accessory ecosystem help users turn ideas into display-ready creations faster.

Root controllers quickly connect displays, lighting, sensors, audio, motors, batteries, and other modules. Zoner, example firmware, and project templates support the development process.

## Root Controller Lineup

| Name | Positioning | Status | Suitable Applications |
| ------------------------------- | --------------- | ------ | --------------------------------------------- |
| [RootMaker](/en/root/rootmaker/rootmaker) | Standard maker controller | Released | 3D prints, desktop robots, lighting control, sensor projects |
| RootEvo | Expandable controller | Planned | More complex creative projects and multiple expansion modules |
| RootMerlin | High-performance controller | Planned | Graphical interfaces, visual interaction, multimedia projects |
| RootCell | Communications controller | Planned | Mobile connectivity, remote monitoring, outdoor or standalone devices |

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;">📍 <a style="color: #FF6A00; text-decoration: none;"> Choosing a Controller</a></h3>
  <p style="margin-bottom: 10px;">
       Interfaces, performance, and supported modules may differ between Root models. Check the wiki page for the relevant model before use.<br>All controllers are listed below. Click a model to open its wiki page.
  </p></div>

<div style="text-align: center;">
    <div style="display: inline-block; width: 20%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
    <a href="/en/root/rootmaker/rootmaker" target="_blank" class="is-external-link">
    <img src="https://res.8ms.xyz/ryzobee/wiki/RootMaker.png" alt="RootMaker" style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
    <br> RootMaker </a> </div>
	<div style="display: inline-block; width: 20%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_coming_soon.png" alt="RootMaker" style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
    <br> RootMerlin (Coming Soon) </div>
    <div style="display: inline-block; width: 20%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_coming_soon.png" alt="RootMaker" style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
    <br> RootEvo (Coming Soon) </div>
    <div style="display: inline-block; width: 20%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_coming_soon.png" alt="RootMaker" style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
    <br> RootCell (Coming Soon) </div>
</div>

## Interfaces and Accessory Ecosystem

Root controllers connect to Yoke accessories through standardized interfaces to form the Ryzobee modular ecosystem.

Common interfaces include:

| Interface | Description |
| ------- | -------------------------------------------- |
| RS-Port | Commonly used for side-mounted modules, cable-connected modules, and external expansion |
| S-BUS | Commonly used for bottom expansion modules such as sensors and batteries |
| F-BUS | Commonly used for top or rear expansion modules such as displays, sensors, and batteries |
| USB-C | Power, firmware flashing, debugging, or data communication |

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;">📍 <a style="color: #FF6A00; text-decoration: none;"> Interface Configuration</a></h3>
  <p style="margin-bottom: 10px;">
   Refer to the page for your Root controller model for specific interface definitions.
  </p></div>

## Power Supply

Root controllers are typically powered through USB-C. Battery or external power modules may also be connected depending on the model and project.

When using the device, note the following:

> **Warning**  
> Make sure the total power consumption of external modules does not exceed the rated output of the controller or power module.
{.is-warning}

> **Warning**  
> Separate power supplies or dedicated expansion modules are recommended for high-power peripherals such as LED strips, motors, and speakers.
{.is-warning}

> **Note**  
> If your project includes multiple high-power modules, consult the power recommendations on the relevant controller page first.
{.is-info}

## Frequently Asked Questions

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📘<a style="color: #FF6A00; text-decoration: none;"> View All FAQs</a></h3>
  <p style="margin-bottom: 10px;">
  If your issue is not covered here, view the full FAQ or email us at ✉ ryzobee@support.com.
  </p>
<div style="text-align: center;"><a href="/en/faq" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     Go to the FAQ →
    </a></div></div>


### Do Root controllers require soldering?

Usually not. Root controllers and Yoke modules primarily connect through standard interfaces, ribbon cables, or connecting cables.

### Do I need to write code?

Many basic projects require no coding when using official example firmware and Zoner.  
For custom features, you can develop with Arduino, ESP-IDF, or MicroPython.

### Can Root controllers directly control a 3D printer?

Root controllers primarily control 3D-printed creations and creative peripherals; they are not 3D printer mainboards.  
Some projects can integrate with the 3D printing ecosystem through networking, serial communication, or plugins.

### Can different Yoke modules be used together?

Check interface, voltage, dimensions, and software support for each module. Consult the relevant module pages first.

### Are third-party modules supported?

Some interfaces can connect to third-party modules, but users must verify electrical compatibility, driver support, and mounting methods.

## Page Navigation

- [RootMaker](/en/root/rootmaker/rootmaker)
- RootEvo
- RootMerlin
- RootCell
- [Yoke Accessory Ecosystem](/en/Yoke_Model)
- Quick Start Guide
- Ryzobee Zoner Platform
- Frequently Asked Questions

## Technical Support

If you encounter problems with a Root controller or Yoke module, first check:

1. The wiki page for the relevant model
2. The Quick Start Guide
3. The FAQ page
4. Ryzobee community and technical support channels

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>💡<a style="color: #FF6A00; text-decoration: none;"> More Information</a></h3>
  <p style="margin-bottom: 10px;">
  Visit our official website for the latest product information or to contact us.
  </p>
<div style="text-align: center;"><a href="https://www.ryzobee.com" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     Go to the Official Website →
    </a></div></div>
