---
title: "Yoke-VOICE"
description: "Yoke-VOICE 语音模块"
tags: "Yoke, Voice"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_VOICE_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-VOICE 语音模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-VOICE 是一款基于 CI1302 语音 AI 芯片设计的音频功能模块，可为 Root 系列主机提供语音采集、语音播放以及基础语音交互能力。

模块集成麦克风与扬声器，并通过 UART 与主机进行通信。开发者可以基于主机固件实现语音播报、语音提示、离线语音识别、语音交互等功能，也可以根据项目需求进行二次开发。

模块采用 S-BUS 底部扩展接口连接，无需额外接线即可快速接入系统。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-VOICE 采用 CI1302 智能语音芯片作为核心处理器，具备本地音频处理能力，可作为主机的语音输入输出扩展模块使用。

| 项目   | 说明                      |
| ---- | ----------------------- |
| 模块接口 | S-BUS                   |
| 核心芯片 | CI1302                  |
| 音频输入 | 板载麦克风                   |
| 音频输出 | 内置扬声器                   |
| 通信方式 | UART                    |
| 供电   | 由主机提供                   |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 基于 CI1302 语音 AI 芯片
- 集成麦克风与扬声器
- 通过 UART 与主机进行数据通信
- 可用于语音提示、状态播报等应用
- 支持后续扩展离线语音识别等功能
- 通过 S-BUS 接口快速安装与连接

## 使用说明

使用 Yoke-VOICE 前，请确认主机固件已支持对应的语音模块功能。

### 与 Root 主机连接

Yoke-VOICE 通过主机底部的 S-BUS 接口连接。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_VOICE_Wiki_900.png" alt="Yoke-VOICE" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

连接时请注意：

- 请在断电状态下安装或拆卸模块。
- 确认 S-BUS 接口已完全插入。
- 避免接口受力或反向安装。
- 若主机无法识别模块，请检查固件版本是否支持该模块。
- 若出现通信异常，请检查 UART 配置是否正确。

### 音频使用说明

Yoke-VOICE 内置麦克风与扬声器，可直接用于音频采集和播放。

建议：

- 麦克风开孔不要被遮挡。
- 扬声器出音孔应保持畅通。
- 避免模块靠近强电磁干扰源。
- 在高音量连续播放时应保证主机供电稳定。

## 供电需求

Yoke-VOICE 的功耗与音频播放音量、处理负载等因素有关。

| 项目       | MAX   | Typ. | Min  |
| -------- | ----- | ---- | ---- |
| 供电电流(mA) | 300mA |      |      |
| 供电电压(V)  | 5V    |      | 3.3V |

“MAX供电电流”为扬声器高音量播放以及芯片满负载运行时的峰值电流，正常使用时通常远低于该数值。

## 硬件规格

| 项目   | 参数                      |
| ---- | ----------------------- |
| 模块型号 | Yoke-VOICE              |
| 模块名称 | 语音模块                    |
| 核心芯片 | CI1302                  |
| 通信接口 | UART                    |
| 模块接口 | S-BUS                   |
| 音频输入 | 板载麦克风                   |
| 音频输出 | 板载扬声器                   |
| 功能方向 | 语音采集、音频播放、语音交互          |
| 适配主机 | RootMaker / Root 系列兼容主机 |

#### 接口定义  

| VOICE PIN | RootMaker IO |
| ---- | ---- |
| TXD1_USER | GPIO36 |
| RXD1_USER | GPIO37 |
| PG_EN | GPIO35 |
| TXD0_DBG | GPIO48 |
| RXD0_DBG | GPIO47 |

## 固件与软件支持

Yoke-VOICE 的具体功能取决于主机与模块固件实现。

目前可支持或计划支持的功能包括：

- 音频播放
- 语音提示
- 状态播报
- 本地语音命令识别
- 语音交互扩展
- AI语音相关应用开发

具体支持功能请参考对应固件版本说明。

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_VOICE_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-VOICE-V11.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.1 · 6.67 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-VOICE-V11.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### Yoke-VOICE 无法被识别怎么办？

请检查以下内容：

1. 主机是否正常供电。
2. 模块是否正确安装至 S-BUS 接口。
3. S-BUS 接口是否接触良好。
4. 主机固件是否支持 Yoke-VOICE。
5. UART 配置是否正确。

### 扬声器没有声音怎么办？

可能原因包括：

- 固件未启用音频播放功能。
- 音量设置过低。
- 音频资源未正确加载。
- 扬声器被遮挡或损坏。

建议首先确认固件和软件配置是否正常。

### 麦克风无法采集声音怎么办？

请检查：

- 麦克风开孔是否被遮挡。
- 是否启用了录音功能。
- 主机与模块通信是否正常。
- 当前固件是否支持音频采集。

### 可以在通电时插拔 Yoke-VOICE 吗？

不建议热插拔。

请在断电状态下安装或拆卸模块，以避免接口损坏、通信异常或模块故障。

### Yoke-VOICE 是否必须使用 CI1302 官方固件？

不一定。

Yoke-VOICE 可根据项目需求使用定制固件，其具体功能由模块固件与主机软件共同决定。
