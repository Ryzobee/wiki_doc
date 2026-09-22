---
title: "Yoke-RAD60"
description: "Yoke-RAD60 60GHz毫米波存在传感器模块"
tags: "Yoke, radar"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_RAD60_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-RAD60 60GHz毫米波存在传感器模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-RAD60 是一款基于 60GHz 毫米波雷达技术的存在传感器模块，模块通过标准接口与 Root 主机连接，可快速为 3D 打印作品增加“人体感知”能力，实现靠近亮灯、自动唤醒、互动触发和存在检测等功能。相比传统红外传感器，Yoke-RAD60 不仅能够检测人体运动，还能够在人体静止时通过呼吸等微小动作持续感知人体存在，更适合用于互动展示模型、桌面装置以及智能外壳项目。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-RAD60 集成 60GHz FMCW 毫米波雷达传感器，可实现运动目标检测、静态人体存在检测以及目标距离信息输出。

| 项目   | 说明                      |
| ---- | ----------------------- |
| 模块接口 | RS-Port                 |
| 供电   | 由 Root 主机电源提供           |
| 工作频段 | 60GHz 毫米波               |
| 通信方式 | UART             |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 支持人体存在检测与运动检测，支持静止人体微动感知
- 最远支持约 10m 探测范围
- 支持目标距离、速度、角度等信息输出
- 使用 RS-Port 与 Root 主机快速连接
- 可用于智能感应、自动亮灯、互动装置和人体感知应用

## 使用说明

使用 Yoke-RAD60 前，请确认 Root 主机已正确烧录支持毫米波雷达模块的固件或项目模板。

### 与 Root 主机连接

Yoke-RAD60 可通过 RS-Port 线缆连接到 Root 主机。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_RAD60_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



连接时请注意：

- 请在断电状态下连接或拔出模块。
- 确认接口方向正确，避免反插。
- 若无法检测到目标，请检查供电与串口配置是否正常。
- 避免雷达正前方存在大面积金属遮挡物。
- 多个雷达模块同时安装时，建议保持一定间距，避免互相干扰。
- 不支持串接，左右两侧的接口是为了安装方便预留。

### 安装方向与方式

Yoke-RAD60 支持水平安装、倾斜安装以及顶部安装。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_RAD60_Wiki_install_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### 安装建议：

- 雷达前方应避免金属遮挡。
- 如果需要覆盖，覆盖面需光滑平整，厚度均匀一致，禁止金属遮挡。
- 避免多个雷达模块正面互相照射。

## 探测能力参考

| 安装方式 | 运动检测距离 | 静态人体检测距离 |
| ---- | ------ | -------- |
| 水平安装 | ≤10m   | ≤8m      |
| 倾斜安装 | ≤9m    | ≤7m      |
| 顶部安装 | 半径≤5m  | 半径≤5m    |

实际探测效果会受到安装环境、目标姿态、遮挡物以及外壳材料等因素影响。

## 供电需求

| 项目       | MAX   | Type | Min  |
| -------- | ----- | ---- | ---- |
| 供电电流(mA) |  | 80mA |      |
| 供电电压(V)  | 5.5V  | 5V   | 3.0V |

## 硬件规格

| 项目     | 参数                          |
| ------ | --------------------------- |
| 模块型号   | Yoke-RAD60                  |
| 模块名称   | 60GHz毫米波存在传感器模块             |
| 接口形态   | RS-Port                     |
| 雷达类型   | FMCW 毫米波雷达                  |
| 工作频段   | 59~64GHz                    |
| 水平视角   | ±60°                        |
| 俯仰视角   | ±60°                        |
| 最大探测距离 | ≤10m                        |
| 通信接口   | UART                 |
| 适用场景   | 人体存在检测、自动感应、互动装置、智能家居       |
| 适配主机   | RootMaker / Root 系列兼容主机     |
| 固定方式   | 结构件固定 / 胶粘固定 / 螺丝固定，视项目结构而定 |

## 3D安装结构文件

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_RAD60_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-RAD60.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 1.13 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-RAD60.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### Yoke-RAD60 无法使用怎么办？

请检查以下内容：

1. Root 主机是否正常供电。
2. 模块是否连接到正确的 RS-Port 接口。
3. 接口方向是否正确，模块同时只能连一根线。
4. 固件是否支持当前雷达模块。
5. 雷达前方是否存在金属遮挡物。

### 为什么人在静止时依然能检测到？

Yoke-RAD60 支持微动检测。
即使人体保持静止，模块依然可以通过检测呼吸等胸腔微动实现存在感知。

### 为什么会出现误触发？

可能原因包括：

- 雷达前方存在金属反射物。
- 多个雷达互相干扰。
- 安装角度不合理。
- 环境中存在风扇、摆动物体等运动目标。

建议调整安装位置与灵敏度参数。

### 可以在通电时插拔 Yoke-RAD60 吗？

不建议热插拔。
请在断电状态下连接或拔出模块，以避免接口短路、通信异常或模块损坏。

### Yoke-RAD60 会受到多个模块互相干扰吗？

在多个毫米波雷达近距离正面安装时，可能存在互相干扰情况。

建议：

- 雷达模块之间，间距离保持 1m 以上。
- 避免雷达正面互相照射。
- 适当调整安装角度。

### 可以隔着 3D 打印外壳使用吗？

通常可以。
毫米波雷达可穿透大部分非金属材料，例如：

- PLA、PETG、ABS
- 亚克力
- 薄木板

但应避免：

- 金属外壳
- 含金属涂层材料
- 碳纤维材料
- 大面积导电结构

并且覆盖面光滑平整，厚度均匀一致。如平面或者球面，不能凹凸不平。否则可能影响探测效果。
