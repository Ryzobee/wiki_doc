---
title: "Yoke-EC11"
description: "Yoke-EC11 旋转编码器模块"
tags: "Yoke, Encoder"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_EC11_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-EC11 旋转编码器模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-EC11 是一款专为 3D 打印作品设计的旋转编码器模块。  
模块通过标准接口与 Root 主机连接，用户可以快速为 3D 打印作品添加旋转调节、按压确认和灯光反馈功能，让静态模型具备更强的操作性和互动性。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-EC11 集成带按压功能的旋转编码器和两颗 RGB 彩灯，可增加旋转或按压操作，并用灯光提示当前状态，适合添加直观、方便的旋钮交互功能。

| 项目 | 说明 |
|---|---|
| 模块接口 | RS-Port |
| 供电 | 由 Root 主机电源提供 |
| 通信方式 | I²C（固定地址 `0x70`） |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 支持双向旋转，可用于亮度、音量等参数调节
- 旋钮可按压，可配合项目实现选择确认和模式切换
- 自带两颗 RGB 彩灯，可分别设置颜色，用于状态显示和操作反馈
- 使用 RS-Port 与 Root 主机快速连接
- 适合 3D 打印控制面板、桌面装置和互动模型

## 使用说明

使用 Yoke-EC11 前，请确认 Root 主机已正确烧录适配旋钮控制的固件或项目模板。

### 与 Root 主机连接
Yoke-EC11 可通过 RS-Port 线缆连接到 Root 主机。  

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_EC11_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



连接时请注意：

- 请在断电状态下连接或拔出模块。
- 确认接口方向正确，避免反插。  

左右转动旋钮，可用于调节亮度、音量，或在菜单中选择选项；按下旋钮，可用于确认选择或切换模式。具体操作对应的功能以所用项目为准。

模块还可配合支持的项目区分长短按，例如短按确认、长按切换功能。使用时，请按照项目说明操作。

两颗 RGB 彩灯可以分别显示不同颜色，例如一颗提示当前模式，另一颗提示操作结果。LED1 距离接口较远，LED2 距离接口较近。显示颜色以及是否闪烁、渐变，取决于所用项目。

### 安装方式

Yoke-EC11 可配合 3D 打印面板或外壳安装，将编码器轴从面板开孔处伸出，并安装匹配的旋钮帽，便于旋转调节和按压操作。模块可通过与实际 PCB 匹配的支架或限位结构固定，并通过 RS-Port 线缆连接 Root 主机。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_EC11_connect_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### 安装建议：

- 在旋钮周围预留旋转空间，并为轴向按压预留行程。
- 根据实际轴径、轴型和轴长选择旋钮帽，避免外壳持续压住按键。
- 使用与实际 PCB 匹配的支架或限位结构固定模块，避免操作力由线缆承受。
- 如需观察灯光，可在灯珠位置设计透光窗口或导光结构。
- 模块与导电结构之间应保留绝缘间隔，并预留接口维护空间。

## 供电需求

| 项目 | MAX | Type | Min |
|---|---|---|---|
| 供电电压(V) |  | 3.3V |  |

## 硬件规格


| 项目     | 参数                                             |
| -------- | ------------------------------------------------ |
| 模块型号 | Yoke-EC11                                      |
| 模块名称 | 旋转编码器模块                                     |
| 接口形态 | RS-Port                                |
| 适用场景 | 3D打印模型参数调节、菜单交互、状态指示       |
| 适配主机 | RootMaker / Root 系列兼容主机               |
| 固定方式 | 结构件固定 / 胶粘固定 / 螺丝固定，视项目结构而定 |

#### 接口定义  

| PIN | 1 | 2 | 3 | 4 |
| ---- | ---- | ---- | ---- | ---- |
| 定义 | GND | VCC | SDA | SCL |

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_EC11_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-EC11-V10.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-EC11-V10.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### 旋转或按压没有反应怎么办？

请检查以下内容：

1. Root 主机是否正常供电。
2. 模块是否连接到正确的 RS-Port 接口。
3. 接口方向是否正确，线缆是否插牢。
4. 所用固件或项目是否支持 Yoke-EC11。
5. 旋钮帽或外壳是否妨碍旋转、按压及回弹。

### 旋转方向与预期不同，或调节不顺畅怎么办？

旋转方向和每次调节的幅度取决于所用项目，请先查看项目说明或相关设置。若转动时出现卡顿，或数值变化不稳定，请检查旋钮帽是否与外壳摩擦，并确认线缆连接牢固、主机供电正常。

### RGB 灯不亮怎么办？

可能原因包括：

- 旋钮帽或外壳遮挡了灯光。
- 所用项目未开启灯光，或灯光亮度设置过低。
- 当前模式下灯光不亮，需要切换模式或操作旋钮后查看。
- 线缆未插牢，或主机供电异常。

### 可以在通电时插拔 Yoke-EC11 吗？

不建议热插拔。  
请在断电状态下连接或拔出模块，以避免接口短路、信号异常或模块损坏。  
