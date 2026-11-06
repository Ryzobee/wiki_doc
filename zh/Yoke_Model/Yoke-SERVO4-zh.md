---
title: "Yoke-SERVO4"
description: "Yoke-SERVO4 四路舵机控制模块"
tags: "Yoke, Servo"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_SERVO4_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-SERVO4 四路舵机控制模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-SERVO4 是一款四路舵机控制模块。  
模块通过 F-BUS 与 Root 主机连接，可接入最多 4 个三线 PWM 舵机，为模型添加摆动、开合和关节运动等机械交互。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-SERVO4 提供 CH1～CH4 四路舵机接口，可将多个舵机集中连接到 Root 主机，适合模型舱门、摆动机构和小型机械关节。各路舵机由主机分别控制，联动顺序和动作范围由所用项目决定。

| 项目 | 说明 |
|---|---|
| 模块接口 | F-BUS |
| 供电 | J1（PH2.0-2P）接电池或外部电源，与主机 VBAT 相连 |
| 通信方式 | GPIO / PWM |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 提供 CH1～CH4 四路接口，可分别连接舵机
- 舵机接口采用 2.54mm 间距三针排针
- 适合模型开合、摆动和机械关节等动作控制
- 使用 F-BUS 与 Root 主机连接，集中整理舵机接线

## 使用说明

使用 Yoke-SERVO4 前，请确认 Root 主机已烧录支持本模块的固件或项目，并选用额定电压与实际供电匹配的三线 PWM 舵机。完成连接后，首次在不带连杆负载的情况下按项目说明触发动作，从小范围运动开始，确认方向和行程后再安装连杆。

### 与 Root 主机连接

在主机、模块及舵机完全断电后，将 Yoke-SERVO4 的 F-BUS 接口与主机对应接口对齐插入，避免反插或错位。舵机连接至 CH1～CH4，接口兼容常见的三线 PWM 舵机，但仍需确认线序。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_SERVO4_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



连接时请注意：

- 插拔模块或舵机前，请断开主机 USB、电池及 J1 外接电源，确认接头牢固、三针接口没有错位后再通电。
- 运行舵机时，请通过 J1 接入匹配的电池或功率足够的外部电源。J1 接电池时，主机 USB 可为电池充电；未接电池或外部电源时，请勿仅依靠主机 USB 驱动舵机。  

#### 安装建议：

- 为舵盘和连杆预留完整活动空间，避免外壳遮挡、机械干涉或运动超出结构允许范围。
- 先确认舵机初始位置和动作方向，再安装舵盘与连杆；不要强行扳动舵盘或让机构长时间卡住。
- 若用于封闭模型内部，应预留接线、维护和散热空间，线缆应避开齿轮、连杆等活动部件。
- 建议通过安装孔或结构件固定模块，并单独固定舵机，使机械负载由模型结构承受，避免拉扯接口。

## 供电需求

| 项目 | MAX | Typ. | Min |
|---|---|---|---|
| 供电电流(mA) | 2000mA |  |  |
| 供电电压(V) | 5V |  | 3.6V |

通过 J1（PH2.0-2P）接入**电池**或**外部电源**为舵机和主机供电。请确认输入的电压满足舵机需求。

使用电池时，主机连接 USB 可为其充电；请勿仅靠主机 USB 运行舵机，以免供电不足导致舵机不动、抖动，或使主机充电电路过热、损坏。

## 硬件规格


| 项目     | 参数                                             |
| -------- | ------------------------------------------------ |
| 模块型号 | Yoke-SERVO4                                      |
| 模块名称 | 四路舵机控制模块                                     |
| 接口形态 | F-BUS（2 × 12 针，1.27mm 间距）；舵机端为 2.54mm 三针排针                                |
| 适用场景 | 3D 打印模型开合、摆动机构、小型机械关节       |
| 适配主机 | RootMaker / Root 系列兼容主机               |
| 固定方式 | 安装孔 / 结构件固定，视项目结构而定 |

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_SERVO4_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-SERVO4-V10.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-SERVO4-V10.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### 舵机连接后没有动作怎么办？

请检查以下内容：

1. J1 供电是否满足供电需求，避免仅靠主机 USB 驱动舵机。
2. F-BUS 接口是否完全插入，方向正确且没有错位。
3. 舵机线缆是否牢固，GND、电源和信号线是否与板上标识对应。
4. 所用项目是否支持 Yoke-SERVO4，并已启用当前舵机通道和对应操作。
5. 外壳是否挡住舵盘，连杆或其他结构是否卡住；先断电解除机械干涉再试。


### 舵机抖动或动作时主机重启怎么办？

可能原因包括：

- 电池、电源及线材无法满足舵机启动时的电流需求；请先检查供电，再只接一个空载舵机测试。
- F-BUS 或舵机接头松动、接线错误；先断电，再检查接头和线缆。
- 机构受阻、负载过重或动作范围过大；先断电解除干涉，再按项目说明缩小动作范围。

### 可以在通电时插拔 Yoke-SERVO4 吗？

禁止热插拔。  
请先停止舵机动作，断开主机 USB、电池及 J1 外接电源，再连接或拔出模块和舵机，以避免接口短路、信号异常或模块损坏。  
