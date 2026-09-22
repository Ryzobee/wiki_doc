---
title: "Ryzobee 快速入门指南"
description: ""
tags: "Ryzobee, Home"
published: true
isPublished: true
---

# Ryzobee 快速入门指南

欢迎使用 Ryzobee。  
Ryzobee 是面向 3D 打印创作者、Maker、开发者和教育用户的模块化电子生态，帮助用户用更简单的方式为 3D 打印作品添加灯光、动作、传感、显示、语音和联网能力。

通过 Root 主机、Yoke 配件和 Zoner 平台，用户可以更快完成从想法、结构设计、模块连接到项目运行的完整流程。

## 1. 使用 Ryzobee 你能做什么

Ryzobee 可以让原本静态的 3D 打印作品拥有电子功能和交互能力。  
你可以将 Root 主机安装在模型内部，再根据项目需求连接不同的 Yoke 模块，让作品具备灯光、运动、感知、显示、语音或联网功能。

常见应用包括：

| 应用方向 | 可以实现的效果                             |
| -------- | ------------------------------------------ |
| 灯光项目 | RGBW 氛围灯、模型发光、状态灯、机箱灯效    |
| 运动项目 | 舵机摆件、旋转结构、桌面机器人、小车或云台 |
| 传感项目 | 人体感应、空气质量检测、温度分布检测       |
| 显示项目 | 状态面板、表情屏幕、传感器数据仪表盘       |
| 语音项目 | AI 对话机器人、语音控制灯光、语音控制电机  |
| 便携项目 | 电池供电装置、无线供电摆件、桌面展示作品   |

Ryzobee 的目标不是让用户从零开始搭电路，而是帮助用户更快完成一个可以运行、可以展示、可以分享的作品。

<div style="text-align: center;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Ryzobee_desc_800full.gif" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

## 2. 0 编程 / 0 焊接 / 即插即用

Ryzobee 面向快速制作和项目复刻场景设计。  
对于大多数官方项目模板，用户不需要编写代码，也不需要焊接电路，只需要按照说明连接模块，并通过 Zoner 平台完成配置和固件烧录。

基本使用流程如下：

1. 选择一个项目模板。
2. 准备 Root 主机和所需 Yoke 模块。
3. 按照接线图连接模块。
4. 使用 Zoner 烧录固件或配置项目。
5. 上电运行项目。
6. 将主机和模块安装到 3D 打印结构中。

对于新手用户，推荐从以下项目开始：

| 入门项目       | 推荐组合                            |
| -------------- | ----------------------------------- |
| 第一个灯效项目 | RootMaker + Yoke-TRGBW              |
| 按键控制灯光   | RootMaker + Yoke-KEYW + Yoke-TRGBW  |
| 人体感应灯     | RootMaker + Yoke-RAD60 + Yoke-TRGBW |
| 小型状态面板   | RootMaker + Yoke-1D54C              |
| 空气质量监测   | RootMaker + Yoke-SCD4x + Yoke-1D54C |

如果你是开发者，也可以使用 Arduino 或 ESP-IDF 自行修改项目逻辑，进一步实现自定义功能。

## 3. 如何配合 3D 打印进行设计

Ryzobee 很适合与 3D 打印结合使用。  
在进行模型设计时，可以提前为 Root 主机、Yoke 模块、线缆和固定结构预留空间，让电子部分更容易安装、维护和展示。

建议在设计 3D 打印结构时重点考虑以下内容：

- Root 主机的安装位置
- Yoke 模块的固定方式
- 发光区域、显示窗口或传感器开孔
- 线缆走线路径
- USB-C 维护口
- 电池或供电模块空间
- 散热和拆装空间

---

### 3.1 接口系统

<div style="text-align: center;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Ryzobee_interface_desc_800full.gif" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

Ryzobee 使用标准化接口连接主机与扩展模块。  
不同接口适合不同类型的 Yoke 模块，设计结构时应根据接口位置预留安装空间。

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Interface_desc_RSPORT.png.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">RS-Port</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
      RS-Port 接口具备较好的机械强度，连接稳定，不易松脱，并且支持通过连接线进行一定距离的延长，适合安装在 3D 打印模型、桌面装置或需要分离布局的项目中。  
由于使用方便、扩展灵活，RS-Port 是 RootMaker 上最常用的外设连接接口。
    </p></div></div></div></div>



<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Interface_desc_FBUS.png.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">F-BUS</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
F-BUS 模块通常可通过螺丝与 RootMaker 主机或其他机械结构件固定，从而获得更好的整体强度和安装可靠性。
RootMaker 顶部和底部均提供 F-BUS 连接能力。实际连接方式请参考对应 Yoke 模块的使用说明。
    </p></div></div></div></div>

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/public_img/Interface_desc_SBUS.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">S-BUS</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    由于 S-BUS 采用金手指连接方式，相比 RS-Port 和 F-BUS，其机械固定强度较弱，更适合轻量模块或需要频繁拆装的应用场景。若项目需要长期运行、移动使用或承受震动，建议根据模块结构增加额外固定方式。
    </p></div></div></div></div>

设计建议：

- RS-Port 模块适合通过线缆延长安装在模型不同位置。
- F-BUS 模块通常更适合与主机叠装或贴近安装。
- S-BUS 模块适合轻量扩展或专用功能模块。
- USB-C 位置应预留插拔空间，方便后续烧录和维护。

### 3.2 线缆系统

线缆系统用于连接 Root 主机和 Yoke 模块。  
在 3D 打印作品中，合理的线缆规划可以让作品更整洁、更稳定，也更方便后期维修。

常见线缆包括：

| 线缆类型         | 用途                                    |
| ---------------- | --------------------------------------- |
| RS-BUS to RS-BUS | 连接 Root 主机与 RS-Port 类型 Yoke 模块 |
| RS-BUS to 杜邦线 | 连接自定义外设或实验电路                |
| RS-BUS to Grove  | 连接部分 Grove 类型传感器或外设         |
| USB-C 线缆       | 供电、烧录固件和串口调试                |

线缆设计建议：

- 为线缆预留走线槽或固定卡扣。
- 避免线缆被外壳压弯或夹断。
- 高功耗模块的供电线应尽量短且可靠。
- 移动结构附近应预留线缆活动余量。
- 封闭式模型应预留维修口，方便重新插拔线缆。
- 灯光模块、传感器模块和显示模块的线缆应尽量分区整理。

### 3.3 结构安装系统

Root 主机和 Yoke 模块可通过螺丝、结构卡扣、3D 打印支架或兼容积木孔位进行固定。  
良好的结构安装可以提升项目稳定性，也能让作品更容易复刻和分享。

结构设计建议：

| 设计项       | 建议                                           |
| ------------ | ---------------------------------------------- |
| 主机安装     | 为 Root 主机预留平整固定面和螺丝孔             |
| 模块安装     | 根据模块发光面、显示方向或传感方向确定安装角度 |
| USB-C 维护口 | 保留足够插拔空间，便于烧录和供电               |
| 散热空间     | 灯光、电机、电池等高功耗模块周围应保留散热空间 |
| 线缆走线     | 设计隐藏式走线槽或卡扣，避免线缆外露           |
| 维修空间     | 封闭结构应预留拆装口，方便更换模块             |
| 结构强度     | 移动部件和受力部件应避免直接拉扯接口           |

如果项目中使用显示模块、热成像模块或雷达模块，还需要特别注意开孔位置和朝向：

- 显示模块需要预留屏幕窗口。
- 热成像模块应避免被外壳遮挡。
- 雷达模块应朝向检测区域。
- 灯光模块可配合柔光罩或半透明材料使用。
- 语音模块应为麦克风和扬声器预留声孔。

## 4. 强大的无线能力

Root 主机支持 2.4GHz Wi-Fi 和 Bluetooth LE，可用于设备配置、联网控制、网页交互、云端服务和无线调试等功能。

无线能力可以让 Ryzobee 项目不仅是一个本地运行的电子装置，也可以变成一个可以被手机、电脑或云端服务控制的智能设备。

常见无线应用包括：

| 无线功能     | 应用场景                                    |
| ------------ | ------------------------------------------- |
| Wi-Fi 配网   | 将设备连接到本地网络                        |
| Web 控制页面 | 通过浏览器控制灯光、动作或参数              |
| OTA 固件升级 | 无需重新插 USB 即可更新固件                 |
| 云端 API     | 与云服务、AI 服务或数据平台联动             |
| MQTT / HTTP  | 与 Home Assistant、OctoPrint 或其他平台通信 |
| Bluetooth LE | 用于近距离配置、发现或控制设备              |

使用无线功能时，请注意：

- Root 主机通常使用 2.4GHz Wi-Fi 网络。
- 请确认 Wi-Fi 名称和密码正确。
- 金属外壳或封闭结构可能影响无线信号。
- 天线区域应尽量远离金属件、电池和大面积铜箔。
- 如果无线连接不稳定，请尝试缩短与路由器的距离。
- 某些 AI、云端或网页控制功能需要设备连接互联网。

## 5. 专业术语列表

以下是使用 Ryzobee 时可能遇到的常见术语。

| 术语            | 说明                                                         |
| --------------- | ------------------------------------------------------------ |
| Root 主机       | Ryzobee 生态中的核心控制器，用于运行固件并控制外设模块       |
| RootMaker       | Root 主机系列中的主力型号，适合大多数 Maker 和 3D 打印互动项目 |
| Yoke 模块       | Ryzobee 的配件模块系列，用于扩展灯光、显示、传感、语音、电机、供电等功能 |
| RS-Port         | Root 主机上的常用扩展接口，适合连接小型 Yoke 模块            |
| RS-BUS          | RS-Port 相关的连接系统或线缆系统                             |
| F-BUS           | 用于连接显示、热成像、电池等复杂模块的扩展接口               |
| S-BUS           | 用于连接语音、音频或专用模块的扩展接口                       |
| Zoner           | Ryzobee 的项目模板与配置平台                                 |
| 固件            | 运行在 Root 主机中的程序，用于控制设备功能                   |
| 项目模板        | 官方提供的可复刻项目配置，通常包含固件、接线、模块和说明     |
| OTA             | Over-the-Air，无线固件升级方式                               |
| GPIO            | 通用输入输出引脚，用于连接和控制电子外设                     |
| I²C             | 常见的传感器通信总线                                         |
| PWM             | 脉宽调制，常用于控制舵机、电机或灯光亮度                     |
| RGBW            | 红、绿、蓝、白四色灯光，比普通 RGB 多一个独立白光通道        |
| 3D 安装结构文件 | 用于安装主机或模块的 STL、STEP、3MF 等结构文件               |

## Zoner 平台

Zoner 是 Ryzobee 用于快速配置项目模板的平台。  
用户可以在 Zoner 中查找官方项目、选择 Root 主机和 Yoke 模块、查看接线说明、下载或烧录固件，并根据项目需求完成参数配置。

Zoner 适合以下用户：

| 用户类型      | 使用方式                                           |
| ------------- | -------------------------------------------------- |
| 新手用户      | 选择官方模板，按照说明连接模块并运行项目           |
| 3D 打印创作者 | 查找可复刻的完整项目，包括结构文件、固件和装配说明 |
| Maker 用户    | 快速验证灯光、电机、传感器、语音等功能             |
| 开发者        | 基于官方模板进行二次开发                           |
| 教育用户      | 使用标准化项目模板组织课程或工作坊                 |

Zoner 可帮助用户完成：

- 查找项目模板
- 查看项目所需硬件
- 查看接线方式
- 获取固件资源
- 配置 Wi-Fi 或项目参数
- 查看装配指南
- 下载 3D 安装结构文件
- 复刻官方项目案例

Zoner 的目标是让用户更快完成从“想法”到“可运行作品”的过程，减少重复配置、接线错误和固件查找成本。

<div style="border-radius: 10px; padding: 15px; background: linear-gradient(135deg, #FFBA89 0%, #FFD884 100%); margin: 4px 0px; box-shadow: none;"><div style="max-width: 800px; margin: 0px auto; text-align: center; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;"><p style="color: #4B1F00; margin: 0px 0px 1px; font-size: 22px; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;">
      🥈 <strong>更多Zoner平台功能请前往Zoner Wiki页面</strong></p> 
<a href="/zh/Zoner" target="_blank" class="is-internal-link is-valid-page" style="display: inline-block; padding: 4px 50px; background:#ffffff; color: #000000; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; margin-top: 15px; box-shadow: none;">
      📖 查看Zoner Wiki 页面 →
</a></div></div>