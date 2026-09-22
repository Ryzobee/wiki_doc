---
title: "Yoke-KEYW"
description: "Yoke-KEYW 轻触开关模块"
tags: "Yoke, keys, key"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_KEYW_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-KEYW 轻触开关模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-KEYW 是一款专为 3D 打印作品设计的轻触开关模块。  
模块通过标准接口与 Root 主机连接，用户可以快速为 3D 打印作品添加可控按键交互功能，让静态模型具备更强的操作性和互动性。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-KEYW 包含带灯的轻触开关，相比普通按键模块，可同时实现按键输入与状态反馈，让 3D 打印作品的交互设计更简洁、走线更少、安装更方便。

| 项目 | 说明 |
|---|---|
| 模块接口 | RS-Port |
| 供电 | 由 Root 主机电源提供 |
| 通信方式 | GPIO |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 单个带底灯的轻触开关，可安装键帽
- 适合 3D 打印模型交互控制
- 灯光既可作为背光，也可用于状态显示
- 使用RS-Port与 Root 主机快速连接
- 可配合 Zoner 项目模板快速完成配置

## 使用说明

使用 Yoke-KEYW 前，请确认 Root 主机已正确烧录适配按键控制的固件或项目模板。

### 与 Root 主机连接
Yoke-KEYW 可通过 RS-Port 线缆连接到 Root 主机。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_KEYW_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



连接时请注意：

- 请在断电状态下连接或拔出模块。
- 确认接口方向正确，避免反插。  

#### 安装建议：

- 建议在按键周围预留适当活动空间，避免外壳或结构件持续压迫按键。
- 若需要状态指示，需要使用带导光结构的键帽。
- 若用于封闭模型内部，应预留维护开口。
- 建议使用螺丝柱、卡扣或限位结构固定模块，避免模块在使用过程中松动。

## 供电需求

| 项目 | MAX | Type | Min |
|---|---|---|---|
| 供电电流(mA) | 10mA |  |  |
| 供电电压(V) |  | 3.3V |  |

## 硬件规格


| 项目     | 参数                                             |
| -------- | ------------------------------------------------ |
| 模块型号 | Yoke-KEYW                                      |
| 模块名称 | 轻触开关模块                                     |
| 接口形态 | RS-Port                                |
| 适用场景 | 3D打印模型功能控制、状态指示、互动装置       |
| 适配主机 | RootMaker / Root 系列兼容主机               |
| 固定方式 | 结构件固定 / 胶粘固定 / 螺丝固定，视项目结构而定 |

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_KEYW_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-KEYW-V10.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 961 KB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-KEYW-V10.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### 轻触开关按下没反应怎么办？

请检查以下内容：

1. 按键按下是否有清脆的“click”声音
2. Root 主机是否正常供电。
3. 模块是否连接到正确的 RS-Port 接口。
4. 接口方向是否正确。
5. 固件是否支持。


### 轻触开关的背光灯不亮怎么办？

可能原因包括：

- 物理遮挡。
- 固件中没有相应的逻辑，或没有配置控制按键灯的GPIO。
- 数据线连接异常。

### 可以在通电时插拔 Yoke-KEYW 吗？

不建议热插拔。  
请在断电状态下连接或拔出模块，以避免接口短路、信号异常或模块损坏。  
