---
title: "Yoke-THERM5K"
description: "Yoke-THERM5K 热成像传感器模块"
tags: "Yoke, Thermal"
published: true
isPublished: true
---
<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_THERM5K_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-THERM5K 热成像传感器模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-THERM5K 是一款专为 Root 系列主机设计的热成像传感器模块，采用 80 × 62 像素红外热成像传感器，可实时获取目标表面的温度分布信息。

模块安装于 Root 主机 F-BUS 底部扩展接口，通过串口与主机进行通信，并支持外接锂电池供电，方便用户制作便携式热成像仪、温度检测设备、设备巡检工具以及各种创意 3D 打印项目。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-THERM5K 内置 80×62 分辨率热成像传感器，可输出热成像数据并生成温度分布图像。配合 Root 主机及相关项目模板，可快速搭建热成像观察设备。

| 项目     | 说明                      |
| ------ | ----------------------- |
| 模块接口   | F-BUS                   |
| 供电     | F-BUS供电 / 外接电池          |
| 通信方式   | UART                  |
| 热成像分辨率 | 80 × 62                 |
| 有效像素   | 约5K像素                   |
| 电池接口   | 支持                      |
| 适配主机   | RootMaker / Root 系列兼容主机 |

主要特性：

- 80×62 像素红外热成像传感器，约 5000 个温度采样点
- 通过串口与 Root 主机通信
- 集成电池接口，支持便携式应用
- 安装于 F-BUS 底部扩展位
- 适合制作热成像仪、设备巡检工具和创意测温装置
- 可与 3D 打印外壳快速结合构建完整设备
- 支持配合 Zoner 项目模板快速开发

## 使用说明

使用 Yoke-THERM5K 前，请确认 Root 主机已正确烧录支持热成像模块的固件或项目模板。

### 与 Root 主机连接

Yoke-THERM5K 安装于 Root 主机底部 F-BUS 扩展接口。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_THERM5K_Wiki_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

连接时请注意：

- 请在断电状态下安装或拆卸模块。
- 确认 F-BUS 接口安装到位。
- 避免在传感器窗口表面留下指纹或污渍。
- 使用过程中避免遮挡热成像视场区域。
- 若出现通信异常，请检查串口配置及固件版本。

### 安装方式

Yoke-THERM5K 设计用于安装在 Root 主机底部扩展位，可配合 3D 打印外壳构建完整热成像设备。

#### 安装建议：

- 传感器窗口前方应保持无遮挡。
- 避免将热源直接安装在传感器附近。
- 建议预留散热空间。
- 若采用封闭式结构，应确保热成像窗口区域使用红外透过材料或开孔设计。
- 建议为传感器区域设计防护罩，避免灰尘污染。

## 电池与供电

Yoke-THERM5K 集成电池接口，但模块本身不附带电池，用户可根据项目需求自行配置电池。

模块可仅通过外接电池供电开机，也可仅通过 F-BUS 供电开机。当 F-BUS 供电与电池同时连接时，可为电池充电。

下表电压范围仅适用于电池输入接口。

| 项目      | MAX  | Typ. | Min  |
| ------- | ---- | ---- | ---- |
| 电池输入电压(V) | 4.2V | 3.7V | 3.0V |

使用电池供电时请注意：

- 推荐使用单节锂离子或锂聚合物电池。
- 注意模块上标记的电源正负极。
- 长期存放时建议断开电池连接。
- 禁止使用损坏或鼓包电池。

## 硬件规格

| 项目     | 参数                      |
| ------ | ----------------------- |
| 模块型号   | Yoke-THERM5K            |
| 模块名称   | 热成像传感器模块                |
| 接口形态   | F-BUS                   |
| 传感器类型  | 红外热成像传感器                |
| 热成像分辨率 | 80 × 62                 |
| 有效像素   | 约5K像素                   |
| 通信接口   | UART                    |
| 电池接口   | 支持                      |
| 适用场景   | 热成像仪、温度监测、设备巡检、创意3D打印项目 |
| 适配主机   | RootMaker / Root 系列兼容主机 |
| 安装方式   | F-BUS底部安装               |

#### 接口定义  

| THERM5K PIN | RootMaker IO |
| ---- | ---- |
| ENABLE | GPIO08 |
| TXD | GPIO06 |
| RXD | GPIO04 |

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_THERM5K_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-THERM5K-V11.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.1 · 3.50 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-THERM5K-V11.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### Yoke-THERM5K 无法识别怎么办？

请检查以下内容：

1. Root 主机是否正常供电。
2. 模块是否正确安装至 F-BUS 接口。
3. 固件是否支持热成像模块。
4. 串口参数配置是否正确。
5. 模块安装方向是否正确。

### 热成像画面刷新异常怎么办？

可能原因包括：

- 串口通信异常。
- 电源供电不稳定。
- 固件版本不匹配。
- 传感器初始化失败。

建议重新上电并检查固件配置。

### 测温结果不准确怎么办？

请检查：

- 传感器窗口是否被遮挡或污染。
- 是否存在强烈热源干扰。
- 测量目标距离是否过远。
- 环境温度变化是否剧烈。

### 可以在通电时安装或拆卸 Yoke-THERM5K 吗？

禁止热插拔。

请在断电状态下安装或拆卸模块，以避免通信异常或模块损坏。

### 电池接口是否附带电池？

不附带。

用户需根据项目需求自行配置兼容电池，并注意电池极性及安全使用规范。
