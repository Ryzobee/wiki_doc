Ryzobee Arduino 是一款专为 Ryzobee 系列开发板设计的 Arduino 支持库，为不同型号的开发板提供统一的编程接口，使开发过程更加迅速和高效。

## 库简介

Ryzobee 库采用模块化架构设计，支持多种开发板型号。每款开发板已预配置完成，用户只需包含头文件并指定开发板类型即可开始使用。

主要特性：

- 统一的开发板抽象层，支持多型号开发板
- 一行代码完成所有外设初始化
- 支持按需启用/禁用各外设模块
- 内置 I2C 互斥锁，多外设安全共享总线
- 提供丰富的示例代码
- 兼容 Yoke 系列扩展模块

## 安装方式

### 1. 安装 ESP32 支持包

打开 **工具 > 开发板 > 开发板管理器**，搜索 `esp32` 并安装 **esp32 by Espressif Systems**（>=v3.3.7）。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_ESP32_pakge.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

### 2. 安装 Ryzobee 库

在 Arduino IDE 中，打开 **工具 > 管理库**，搜索 `Ryzobee` 并点击安装即可。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_Ryzobee.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

### 3.选择Root系类开发板

在 Arduino IDE 中，打开 **Tool > Board > esp32 > Root Maker**.

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Snipaste_2026-06-05_17-10-10.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

### 3. 安装依赖库

在 Arduino IDE 中，打开 **工具 > 管理库**，搜索并安装以下依赖库：

| 名称 | 最低版本 | 说明 |
|:---:|:---:|:---|
| LovyanGFX | >=v1.2.19 | SPI LCD 高性能图形库 |
| Adafruit_NeoPixel | >=v1.12.3 | WS2812B RGB LED 驱动库 |
| LIS2DW12 | >=v2.1.1 | LIS2DW12 3D 加速度计驱动库 |
| AnimatedGIF | >=2.2.0 | GIF 动画播放库 |

<div style="display:flex;flex-wrap:wrap;gap:16px;margin:20px 0;">
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_LovyanGFX.png" alt="Image 1" style="width:100%;display:block;border-radius:12px;">
  </div>
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_Adafruit_NeoPixel.png" alt="Image 2" style="width:100%;display:block;border-radius:12px;">
  </div>
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_LIS2DW12.png" alt="Image 2" style="width:100%;display:block;border-radius:12px;"></div>
   <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Dev/img/Install_AnimatedGIF.png" alt="Image 2" style="width:100%;display:block;border-radius:12px;"></div>
</div>


## 基本用法

```cpp
#include "Ryzobee.h"

// 创建开发板实例（指定开发板型号）
Ryzobee board(RYZOBEE_ROOTMAKER);

void setup(void)
{
    Serial.begin(115200);
    board.rootmaker.begin();
}

void loop(void)
{
    // 你的代码
}
```

## 支持的开发板

| 名称 | 型号常量 | 文档 |
|:---:|:---:|:---:|
| RootMaker | RYZOBEE_ROOTMAKER | [RootMaker API使用指南](/zh/dev/rootmaker_arduino_api) |

> 更多开发板型号持续增加中，请关注后续更新。

## 许可证

本项目采用 MIT 许可证。
