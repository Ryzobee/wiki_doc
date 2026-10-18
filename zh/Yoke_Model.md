---
title: "Yoke 配件系列"
description: "您可以在这里找到Yoke配件系列的介绍"
tags: "Yoke, Home"
published: true
isPublished: true
---

Yoke 是 RyzoBee / Root 生态中的模块化配件系列，用于为 Root 主机快速扩展显示、灯光、传感、语音、电机、触摸、供电等功能。

通过标准化接口与统一的模块设计，Yoke 配件可以减少复杂接线、降低硬件适配门槛，让 Maker、3D 打印创作者和开发者更快完成项目搭建、功能验证和作品复刻。

## Yoke 是什么

Yoke 是围绕 Root 主机系列设计的扩展模块系统。  
每一个 Yoke 模块都针对一个明确的功能场景设计，例如灯光显示、环境感知、语音交互、电机控制或电池供电。

用户可以根据项目需求选择不同的 Yoke 模块，并通过 Root 主机上的标准接口进行连接，从而快速为 3D 打印作品、桌面装置、互动模型或开发项目增加电子功能。

Yoke 的设计目标是：

- 让电子模块更容易连接

- 让项目功能更容易复刻

- 让 3D 打印作品更容易拥有交互能力

- 让创作者把更多时间放在创意和作品本身，而不是复杂接线和底层驱动上

  

## 接口类型说明

Yoke 模块根据功能和结构需求，使用不同的接口形态与 Root 主机连接。

目前 Yoke 配件主要包含以下接口类型：

| 接口类型              | 说明                                                 | 典型模块                              |
| --------------------- | ---------------------------------------------------- | ------------------------------------- |
| [RS-Port](#P_RS_PORT) | 适合小型传感器、灯光、按键、触摸和电机类模块         | Yoke-TRGBW、Yoke-RAD60、Yoke-MOTO     |
| [F-BUS](#P_F_BUS)     | 适合触摸显示、热成像、USB PD 电机驱动等扩展模块 | Yoke-LCD1D54C、Yoke-THERM5K、Yoke-MOTOR-A |
| [S-BUS](#P_S_BUS)     | 适合语音、音频等专用功能扩展模块                     | Yoke-VOICE                            |

<div style="text-align: center;">
    <div style="display: inline-block; width: 20%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
    <a href="#P_RS_PORT" target="_blank" class="is-external-link">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Rootmaker_RSPort.png" alt="RootMaker" style="width: 100%; 	height: auto; border-radius: 5px; margin-bottom: 10px;"> 
    <br> RS-Port 接口配件 </a></div>
    <div style="display: inline-block; width: 20%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
    <a href="#P_F_BUS" target="_blank" class="is-external-link">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Rootmaker_FBUS.png" alt="RootMaker" style="width: 100%; 	height: auto; border-radius: 5px; margin-bottom: 10px;"> 
    <br> F-BUS 接口配件 </a></div>
    <div style="display: inline-block; width: 20%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
    <a href="#P_S_BUS" target="_blank" class="is-external-link">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Rootmaker_SBUS.png" alt="RootMaker" style="width: 100%; 	height: auto; border-radius: 5px; margin-bottom: 10px;"> 
    <br> S-BUS 接口配件 </a></div>
</div>



## RS-Port 接口配件 <a id="P_RS_PORT"></a>

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin: 20px 0;">
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-RGBW-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_RGBW_Wiki_main.png" alt="Yoke-RGBW RGBW 灯效模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-RGBW<br>RGBW 灯效模块
    </a>
  </div>
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-TRGBW-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_main.png" alt="Yoke-TRGBW 3× RGBW 灯效模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-TRGBW<br>3× RGBW 灯效模块
    </a>
  </div>
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-KEYW-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_KEYW_Wiki_main.png" alt="Yoke-KEYW 轻触开关模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-KEYW<br>轻触开关模块
    </a>
  </div>
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-MOTO-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_MOTO_Wiki_main.png" alt="Yoke-MOTO 直流马达控制模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-MOTO<br>直流马达控制模块
    </a>
  </div>
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-RAD60-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_RAD60_Wiki_main.png" alt="Yoke-RAD60 60GHz 毫米波存在传感器模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-RAD60<br>60GHz 毫米波存在传感器模块
    </a>
  </div>
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-TOUCH4-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_Touch4_Wiki_main.png" alt="Yoke-TOUCH4 四通道触摸模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-TOUCH4<br>四通道触摸模块
    </a>
  </div>
</div>

## F-BUS 接口配件 <a id="P_F_BUS"></a>

Yoke-LCD1D54C 提供 240 × 240 像素彩色显示与电容触摸；Yoke-THERM5K 提供 80 × 62 像素热成像；Yoke-MOTOR-A 通过外部 USB-C PD 电源驱动单路有刷直流电机。各模块的安装位置、供电和引脚占用请分别查看详情页。

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin: 20px 0;">
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-LCD1D54C-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_LCD1D54C_Wiki_main.png" alt="Yoke-LCD1D54C 1.54 英寸触摸显示模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-LCD1D54C<br>1.54 英寸触摸显示模块
    </a>
  </div>
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-THERM5K-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_THERM5K_Wiki_main.png" alt="Yoke-THERM5K 热成像传感器模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-THERM5K<br>热成像传感器模块
    </a>
  </div>
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-MOTOR-A-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/ZXYoke-MOTOR-A_Wiki_main.png" alt="Yoke-MOTOR-A USB PD 直流马达控制模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-MOTOR-A<br>USB PD 直流马达控制模块
    </a>
  </div>
</div>

## S-BUS 接口配件 <a id="P_S_BUS"></a>

Yoke-VOICE 集成麦克风与扬声器，通过 UART 与主机通信，可用于语音提示和音频交互。具体功能取决于主机与模块固件支持。

<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 20px; margin: 20px 0;">
  <div style="flex: 0 1 200px; padding: 15px; text-align: center; background: #fff; border-radius: 5px; box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);">
    <a href="/zh/Yoke_Model/Yoke-VOICE-zh">
      <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_VOICE_Wiki_main.png" alt="Yoke-VOICE 语音模块" style="width: 100%; height: 150px; object-fit: contain; border-radius: 5px; margin-bottom: 10px;">
      <br>Yoke-VOICE<br>语音模块
    </a>
  </div>
</div>

## 使用 Yoke 模块的基本流程

1. 根据项目需求选择合适的 Yoke 模块。
2. 确认 Root 主机是否支持该模块的接口类型。
3. 在断电状态下连接模块。
4. 按照 [Zoner 快速开始](/zh/Zoner/quick_start) 选择与主机及模块匹配的项目。
5. 烧录或配置固件。
6. 上电运行并检查模块状态。
7. 根据项目结构安装模块和线缆。
8. 保存配置并完成作品组装。

## 与 Zoner 平台配合使用

[Zoner 平台](/zh/Zoner) 用于查找项目资料、部署固件和管理设备。
用户可以在 Zoner 中查找与 Yoke 模块对应的项目案例、固件资源、配置说明和装配指南。

通过 Zoner，用户可以更快完成以下操作：

- 查找模块支持的项目模板
- 查看模块连接方式
- 下载或烧录固件
- 配置模块参数
- 获取装配说明
- 复刻官方项目案例

项目是否提供可部署固件、支持哪些模块和配置项，请以项目详情页为准。模块已有 Wiki 页面，并不代表所有项目都已支持该模块。

## 使用注意事项

使用 Yoke 模块时，请注意以下事项：

- 请在断电状态下连接或拔出模块。
- 使用前请确认接口方向正确，避免反插。
- 高功耗模块需要确认 Root 主机供电能力是否足够。
- 电机、灯光、无线供电和电池类模块应特别注意电流与散热。
- 不同硬件版本的接口定义可能存在差异，请以实际版本说明为准。
- 如模块工作异常，请优先检查供电、线缆、接口方向和固件配置。
- 不建议在通电状态下频繁插拔 Yoke 模块。

## 页面导航

你可以从以下页面了解每个 Yoke 模块的详细使用方法：

### RS-Port

- [Yoke-RGBW RGBW 灯效模块](/zh/Yoke_Model/Yoke-RGBW-zh)
- [Yoke-TRGBW 3× RGBW 灯效模块](/zh/Yoke_Model/Yoke-TRGBW-zh)
- [Yoke-KEYW 轻触开关模块](/zh/Yoke_Model/Yoke-KEYW-zh)
- [Yoke-MOTO 直流马达控制模块](/zh/Yoke_Model/Yoke-MOTO-zh)
- [Yoke-RAD60 60GHz 毫米波存在传感器模块](/zh/Yoke_Model/Yoke-RAD60-zh)
- [Yoke-TOUCH4 四通道触摸模块](/zh/Yoke_Model/Yoke-TOUCH4-zh)

### F-BUS

- [Yoke-LCD1D54C 1.54 英寸触摸显示模块](/zh/Yoke_Model/Yoke-LCD1D54C-zh)
- [Yoke-THERM5K 热成像传感器模块](/zh/Yoke_Model/Yoke-THERM5K-zh)
- [Yoke-MOTOR-A USB PD 直流马达控制模块](/zh/Yoke_Model/Yoke-MOTOR-A-zh)

### S-BUS

- [Yoke-VOICE 语音模块](/zh/Yoke_Model/Yoke-VOICE-zh)

## 常见问题

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FF6A00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📘<a style="color: #FF6A00; text-decoration: none;"> 查看所有FAQ</a></h3>
  <p style="margin-bottom: 10px;">
  如果这里没有找到您遇到问题，可以查看完整FAQ列表，或通过邮箱联系我们 ✉ support@ryzobee.com
  </p>
<div style="text-align: center;"><a href="/zh/faq" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     点击跳转到FAQ页面 →
    </a></div>
  </div>

### Yoke 模块可以直接热插拔吗？

不建议热插拔。  
请在断电状态下连接或拔出 Yoke 模块，以避免接口短路、通信异常或模块损坏。

### 一个 Root 主机可以连接多个 Yoke 模块吗？

可以，但需要根据 Root 主机的接口数量、引脚占用、安装空间、固件支持情况和整体供电能力进行判断。相同接口类型不代表模块可以任意叠加使用。
如果同时使用多个高功耗模块，例如灯效模块、电机模块和显示模块，应特别注意供电余量。

### Yoke 模块是否需要单独烧录固件？

大多数 Yoke 模块不需要单独烧录固件，由 Root 主机运行项目固件并控制模块。  
部分复杂模块可能需要专用配置或驱动支持，具体请参考对应模块页面。

### Yoke 模块是否只能用于 RootMaker？

Yoke 模块主要面向 Root 主机系列设计。  
如果其他 Root 主机具备相同接口和固件支持，也可以使用对应 Yoke 模块。

### 模块无法识别怎么办？

请检查以下内容：

1. 是否连接到正确接口。
2. 接口方向是否正确。
3. Root 主机是否正常供电。
4. 固件是否支持该模块。
5. Zoner 或项目模板中是否选择了正确模块。
6. 线缆是否损坏或接触不良。

### 灯光、电机或显示异常怎么办？

通常可能与供电不足、接口接触不良或固件配置不匹配有关。  
建议先降低负载、检查线缆连接，并确认当前项目模板是否与实际模块一致。
