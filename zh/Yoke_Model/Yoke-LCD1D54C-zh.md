---
title: "Yoke-LCD1D54C"
description: "Yoke-LCD1D54C 1.54寸触摸显示模块"
tags: "Yoke, LCD, Touch"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_LCD1D54C_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-LCD1D54C 1.54寸触摸显示模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-LCD1D54C 是一款安装于 Root 主机上的 1.54 英寸彩色触摸显示模块，分辨率为 240 × 240 像素。

通过该模块，用户可以为 3D 打印作品增加图形界面、状态显示和触摸交互功能，适用于设备面板、桌面终端、互动装置、智能摆件以及各类创意项目。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-LCD1D54C 通过 F-BUS 与主机连接，集成彩色 LCD 显示屏和触摸功能，其中显示通过 SPI 通信，触摸通过 IIC 通信，可用于显示设备状态、菜单界面、传感器数据以及用户自定义内容。

| 项目    | 说明            |
| ----- | ------------- |
| 模块接口  | F-BUS         |
| 显示尺寸  | 1.54 英寸       |
| 分辨率   | 240 × 240 |
| 显示类型  | 彩色 LCD        |
| 触摸功能  | 电容触摸  |
| 通信接口  | 显示：SPI；触摸：IIC |
| 安装方式  | 主机扩展  |

主要特性：

- 1.54 英寸彩色 LCD 显示屏
- 240×240 分辨率显示
- 支持触摸交互功能
- F-BUS 即插即用扩展
- 可显示文字、图标、菜单和实时数据
- 适用于状态显示、控制面板和交互界面
- 适合嵌入各类 3D 打印外壳和设备结构

## 使用说明

### 模块安装

Yoke-LCD1D54C 安装于 RootMaker 主机顶部，需要先拆除主机底部四角固定螺丝。

安装步骤：

1. 完全断电并断开电池。
2. 使用螺丝刀拆除主机底部四角固定螺丝。
3. 将显示模块与主机上的 F-BUS 接口对准。
4. 确认双排排针与排母完全对应后垂直压入。
5. 使用螺丝重新固定主机与模块。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_LCD1D54C_Wiki_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;">
</div>

#### 安装注意事项

> **请务必确认排针与接口完全对齐后再进行安装。**
>
> **若发生错位插入，可能导致模块、主机或接口损坏。**

安装时请注意：

- 需断电状态下安装或拆卸模块。
- 请勿倾斜插入，或使用过大力量强行安装。
- 如发现插接阻力明显异常，请立即停止并检查接口位置。
- 安装完成后应确认模块与主机贴合平整。

### 安装建议

Yoke-LCD1D54C 适合作为设备前面板、控制终端或状态显示窗口使用。

设计 3D 打印结构时建议：

- 为屏幕预留完整显示窗口。
- 避免结构件遮挡触摸区域。
- 预留足够的手指操作空间。
- 预留维护和拆装空间。
- 屏幕边缘避免受到持续挤压。

## 供电需求

Yoke-LCD1D54C 的功耗，会根据显示内容和背光亮度动态变化。

| 项目       | MAX | Typ. | Min  |
| -------- | --- | ---- | ---- |
| 供电电流(mA) | 100mA |      |      |
| 供电电压(V)  |  |   3.3V   |  |


## 硬件规格

| 项目    | 参数                      |
| ----- | ----------------------- |
| 模块型号  | Yoke-LCD1D54C           |
| 模块名称  | 1.54寸触摸显示模块             |
| 接口形态  | F-BUS                   |
| 显示尺寸  | 1.54 英寸                 |
| 分辨率 | 240 × 240            |
| 显示颜色  | 彩色                      |
| 触摸功能  | 电容触摸                     |
| 通信接口  | 显示：SPI；触摸：IIC |
| 显示驱动  | ST7789                  |
| 适配主机  | RootMaker / Root 系列兼容主机 |
| 安装方式  | 主机堆叠安装                  |

#### 接口定义  

| LCD PIN | RootMaker IO |
| ---- | ---- |
| LCD_CS | GPIO05 |
| LCD_RS | GPIO03 |
| LCD_SCK | GPIO12 |
| LCD_SDA | GPIO09 |
| LCD_RST | GPIO10 |
| LCD_BL | GPIO07 |
| TP_SCL | GPIO40 |
| TP_SDA | GPIO41 |
| TP_RST | GPIO02 |
| TP_INT | GPIO01 |

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_LCD1D54C_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-LCD1D54C-V10.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 8.21 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-LCD1D54C-V10.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### 模块安装后无显示怎么办？

请检查以下内容：

1. 模块是否完全插入 F-BUS 接口。
2. 排针是否存在错位安装情况。
3. 主机是否正常供电。
4. 固件是否支持显示模块。
5. 模块安装过程中是否造成排针弯曲。

### 屏幕显示异常或花屏怎么办？

可能原因包括：

- 固件配置错误。
- 显示驱动未正确初始化。
- 模块未完全安装到位。
- 接口接触不良。

建议重新安装模块并检查软件配置。

### 触摸功能无法使用怎么办？

请检查：

- 固件是否启用了触摸功能。
- 触摸驱动是否已正确配置。
- 模块是否安装到位。
- 屏幕表面是否存在影响触摸的覆盖物。

### 可以在通电时安装或拆卸模块吗？

禁止热拔插。

涉及到拆装螺丝，请在完全断电且断开电池的状态下安装或拆卸模块，以避免接口短路、通信异常或模块损坏。

### 安装时排针插歪了或怀疑插歪了怎么办？

请立即断电并拆下模块。

检查排针是否弯曲、变形或发生短路后再重新安装。

若发现针脚已经损坏，请停止继续使用并更换相关部件，以免造成进一步损坏。

