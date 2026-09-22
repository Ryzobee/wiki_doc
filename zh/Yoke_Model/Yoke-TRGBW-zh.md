---
title: "Yoke-TRGBW"
description: "Yoke-TRGBW RGBW灯效模块"
tags: "Yoke, LEDs, RGBW"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-TRGBW 3x RGBW灯效模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-TRGBW 是一款专为 3D 打印作品设计的 RGBW 灯效模块，可用于模型发光、状态指示、氛围灯效、互动装置和桌面摆件等场景。  
模块通过标准接口与 Root 主机连接，用户可以快速为 3D 打印作品添加可控灯光效果，让静态模型具备更强的展示性和交互性。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-TRGBW 集成 RGBW 灯珠，相比普通 RGB 灯效模块，额外增加独立白光通道，可实现更自然的白色显示、更柔和的补光效果，以及更丰富的混色表现。

| 项目 | 说明 |
|---|---|
| 模块接口 | RS-Port |
| 供电 | 由 Root 主机电源提供 |
| 控制信号 | 单线灯效控制信号 |
| 通信方式 | 数字灯带控制协议 |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 拥有3颗灯，支持 RGBW 四通道灯效显示
- 适合 3D 打印模型内置发光
- 可用于氛围灯、状态灯、指示灯和创意灯效
- 使用RS-Port与 Root 主机快速连接
- 可配合 Zoner 项目模板快速完成配置

## 使用说明

使用 Yoke-TRGBW 前，请确认 Root 主机已正确烧录支持 RGBW 灯效控制的固件或项目模板。

### 与 Root 主机连接
Yoke-TRGBW 可通过 RS-PortA 线缆连接到 Root 主机。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



连接时请注意：

- 请在断电状态下连接或拔出模块。
- 确认接口方向正确，避免反插。
- 如果灯光出现闪烁、颜色异常或设备重启，请优先检查供电是否稳定。
- 若项目中使用多个灯效模块或高亮度灯效，建议确认总电流是否超过主机供电能力。

### 显示方向与安装方式

Yoke-TRGBW 可安装在 3D 打印模型内部、半透明外壳后方、导光结构下方或灯罩内部。

模块支持级联，级联方式如下图。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_install.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### 安装建议：

- 灯珠发光面应朝向模型透光区域。
- 若用于氛围灯，建议增加柔光罩或半透明扩散结构。
- 若用于状态指示，建议将灯板固定在可视窗口后方。
- 若用于封闭模型内部，应预留散热空间和维护开口。
- 避免灯珠与塑料结构长时间紧密接触，尤其是在高亮度运行时。

## 供电需求

Yoke-TRGBW 的功耗与灯珠亮度、颜色和白光通道使用情况有关。

| 项目 | MAX | Type | Min |
|---|---|---|---|
| 供电电流(mA) | 250mA |  |  |
| 供电电压(V) | 5V |  | 3.3V |

“MAX供电电流”为 RGB 灯条全白满亮等极限工况下的瞬时最大电流，正常使用时通常远低于该数值。

## 硬件规格


| 项目     | 参数                                             |
| -------- | ------------------------------------------------ |
| 模块型号 | Yoke-TRGBW                                       |
| 模块名称 | RGBW灯效模块                                     |
| 接口形态 | RS-Port                                          |
| 灯光类型 | RGBW                                             |
| 适用场景 | 3D打印模型发光、氛围灯、状态指示、互动装置       |
| 适配主机 | RootMaker / Root 系列兼容主机                    |
| 固定方式 | 结构件固定 / 胶粘固定 / 螺丝固定，视项目结构而定 |

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_TRGBW_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-TRGBW.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 527 KB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-TRGBW.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### Yoke-TRGBW 不亮怎么办？

请检查以下内容：

1. Root 主机是否正常供电。
2. 模块是否连接到正确的 RS-Port 接口。
3. 接口方向是否正确。
4. 固件是否支持当前灯效模块。
5. 项目模板中是否选择了正确的灯效类型。


### 灯光颜色显示不正确怎么办？

可能原因包括：

- RGBW 颜色顺序配置不正确。
- 固件中灯珠类型选择错误。
- 使用了 RGB 模板控制 RGBW 模块。
- 数据线连接异常。

建议在 Zoner 或固件配置中确认灯效模块类型为 RGBW。

### 灯光闪烁或 Root 主机重启怎么办？

通常与供电不足有关。请尝试：

- 降低灯光亮度。
- 减少白光通道长时间高亮。
- 使用更稳定的 5V 电源。
- 检查线缆和接口是否接触良好。
- 避免多个高功耗模块同时由同一路电源供电。

### 可以在通电时插拔 Yoke-TRGBW 吗？

不建议热插拔。  
请在断电状态下连接或拔出模块，以避免接口短路、信号异常或模块损坏。

### Yoke-TRGBW 可以与 Yoke-RGBW 混用吗？

可以混用，但是要注意箭头方向。  
