---
title: "Yoke-MOTOR-A"
description: "Yoke-MOTOR-A USB PD 直流马达控制模块"
tags: "Yoke, Motor"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/ZXYoke-MOTOR-A_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-MOTOR-A USB PD 直流马达控制模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-MOTOR-A 是一款通过 USB PD 供电的单路有刷直流马达控制模块。
模块通过 F-BUS 与 Root 主机连接，支持电机正反转、PWM 调速和制动，可为 3D 打印作品添加旋转、传动和联动等动态效果。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-MOTOR-A 可为旋转展示台、动态摆件和机械互动装置提供电机驱动，支持正反转与 PWM 调速。
相比 Yoke-MOTO，本模块采用外部 USB-C PD 供电，可驱动功率更大的直流电机。

| 项目 | 说明 |
|---|---|
| 模块接口 | F-BUS |
| 供电 | USB-C PD 外部供电，默认请求 12V |
| 控制信号 | GPIO / PWM |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 支持直流马达正反转控制
- 支持 PWM 调速、制动和停止
- 适合旋转展示、动态摆件和机械结构驱动
- 使用 F-BUS 与 Root 主机连接
- USB-C PD 外部供电，可同时为 Root 主机供电

## 使用说明

使用 Yoke-MOTOR-A 前，请确认 Root 主机已烧录适配当前模块的固件，并准备支持 12V 输出档位的 USB PD 电源和配套线缆。

### 与 Root 主机连接

请在主机、模块及电机均断电的状态下，将 Yoke-MOTOR-A 的 F-BUS 接口与主机对应接口对齐后插入。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_MOTOR-A_Wiki_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

连接时请注意：

- 请在断电状态下安装或拆卸模块；如主机已连接电池，也需先断开电池。
- 确认双排接口方向正确、针脚完全对齐，避免反插或错位插入。
- 电机连接至模块的 DC-MOTOR 接口，PD 电源连接至 PD POWER IN 接口。
- 【重要】请确认电机额定电压与实际 PD 供电电压匹配，并确认电源能够满足电机启动和运行的电流需求。

### 电机连接与使用

1. 在断电状态下，将两线有刷直流电机连接至 DC-MOTOR 的 XH2.5-2P 接口。
2. 固定电机与传动结构，确认转轴和运动部件没有被卡住。
3. 连接支持 12V 档位的 USB PD 电源，确认主机和模块正常供电。
4. 通过适配固件控制电机方向和 PWM 占空比，首次运行建议从较低占空比开始。
5. 如需调整接线或拆卸模块，请先停止电机并完全断电。

#### 安装建议：

- 避免电机长时间堵转或持续高负载运行，以免导致电机或驱动器过热。
- 为驱动芯片和电机预留散热空间，避免紧贴不耐热结构件。
- 电机轴与齿轮、联轴器等机构安装时，应避免过度侧向受力。
- 电机输出的两个针脚均为驱动输出，请勿将其中任一针脚直接接至电源或 GND。

## 供电需求

Yoke-MOTOR-A 通过 USB-C PD 接口为电机驱动电路供电，默认请求 12V。电源需支持对应档位；普通 5V USB 电源不能提供默认的 12V 工作条件，实际协商电压取决于电源能力和 PD 配置。

使用 Yoke-MOTOR-A 时，建议整机仅通过本模块的 USB-C PD 接口取电，由模块通过 F-BUS 为 Root 主机供电；建议不同时连接主机电池或主机自身的 USB 电源。

实际供电电流随电机负载变化，选择电源时还需考虑电机启动电流和主机用电需求。
实际驱动能力还受适配器输出功率、模块散热、接口和线材承载能力限制。

| 项目 | MAX | Typ. | Min |
|---|---|---|---|
| USB PD 请求电压(V) |  | 12V（默认） |  |
| 电机工作电流(mA) | 4A |  |  |
| 控制逻辑电压(V) |  | 3.3V |  |

## 硬件规格

| 项目 | 参数 |
|---|---|
| 模块型号 | Yoke-MOTOR-A |
| 模块名称 | USB PD 直流马达控制模块 |
| 接口形态 | F-BUS，2 × 12 针，1.27mm 间距 |
| 电机接口 | DC-MOTOR，XH2.5-2P |
| 负载类型 | 单路两线有刷直流电机 |
| 控制方式 | 双输入方向控制 / PWM 调速 |
| 适用场景 | 3D 打印模型动态结构、旋转机构、互动装置 |
| 适配主机 | RootMaker / Root 系列兼容主机，需对应固件支持 |

#### 接口定义  

| 模块 PIN | RootMaker IO |
| ---- | ---- |
| PWM_A / BI（后退输入） | GPIO06 |
| PWM_B / FI（前进输入） | GPIO04 |
| PD_SCL | GPIO40 |
| PD_SDA | GPIO41 |

IIC 连接用于 CH224A 的电源配置与状态读取，电机方向和速度由 PWM_A、PWM_B 控制。

| PWM_A（GPIO06） | PWM_B（GPIO04） | 电机状态 |
|---|---|---|
| 低电平 | 高电平 | 前进 |
| 高电平 | 低电平 | 后退 |
| 高电平 | 高电平 | 制动 |
| 低电平 | 低电平 | 停止，输出高阻 |

电机实际转向取决于两根电机线的连接顺序。
编写控制程序时，驱动电源上电前应将两个控制输入保持为低电平；驱动电源建立后至少等待 3ms 再开始控制。PWM 频率不得超过 30kHz，高、低电平脉宽均不得小于 100ns。

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke-MOTO-A_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-MOTO-A-V11.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.1 · 3.61 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-MOTO-A-V11.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### 连接了马达但是不工作？

请检查以下内容：

1. PD 电源是否接入 PD POWER IN，且支持 12V 输出档位。
2. 模块是否完全插入 F-BUS 接口，主机是否正常供电。
3. 电机是否接入 DC-MOTOR，接线是否牢固。
4. 固件是否适配 Yoke-MOTOR-A，GPIO06 与 GPIO04 是否正确配置。
5. 电机是否堵转，或因电源过载、驱动器过热等原因停止运行。

### 马达的转动方向与预期的不同？

请先断电，再交换马达的两根线；也可以在固件中切换方向控制信号。

### 可以只通过 F-BUS 为电机供电吗？

电机驱动电源来自模块的 USB-C PD 输入。使用时需连接适配的外部 PD 电源。

### 如何选择电机和电源适配器？

电机选型建议以工作电流不超过 4A 为参考，并确认额定电压与实际供电电压匹配。还需考虑电机启动时的电流，避免长时间堵转或持续高负载运行，并为模块和电机预留散热空间。

请选择支持 12V 档位的 PD 适配器，以该档位标注的输出电流和功率为准，并为主机耗电和电机启动预留余量。例如，12V/3A 档位最多提供 36W，电机可用功率还需扣除主机和模块的耗电。

### 可以在通电时插拔 Yoke-MOTOR-A 吗？

禁止热插拔。  
请先停止电机，断开 PD 电源，再连接或拔出模块和电机，以避免接口短路、信号异常或模块损坏。
