<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/RootMaker.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">RootMaker</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    RootMaker 是 RyzoBee / Root 系列中的主力控制器，面向 Maker、3D 打印创作者和互动硬件项目设计。  
它可以作为 3D 打印作品的“电子大脑”，用于连接和控制 Yoke 配件模块，实现灯光、显示、传感、语音、电机、触摸和联网交互等功能。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

### 主要特性：

- 面向 3D 打印作品和 Maker 项目的主控硬件
- 支持连接多种 Yoke 配件模块
- 支持灯光、电机、传感器、显示、语音和触摸等功能扩展
- 支持 Wi-Fi / BLE 无线连接能力
- 支持通过 USB-C 连接电脑进行供电、烧录和调试
- 支持 Zoner 项目模板，降低项目配置和复刻成本
- 支持 Arduino / ESP-IDF 开发方式

## 组件介绍

RootMaker 主机包含多个接口、按键、指示灯和结构固定部件。下图中的编号对应各组件位置，用户可根据编号快速识别主机上的主要功能区域。

<div style="display:flex;flex-wrap:wrap;gap:16px;margin:20px 0;">
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/component_desc_1.png" alt="Image 1" style="width:100%;display:block;border-radius:12px;">
  </div>
  <div style="flex:1 1 calc(50% - 8px);min-width:320px;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/component_desc_2.png" alt="Image 2" style="width:100%;display:block;border-radius:12px;">
  </div>
</div>


| 编号 | 组件名称           | 说明                                                         |
| ---- | ------------------ | ------------------------------------------------------------ |
| 1    | RGB LED 指示灯     | 用于显示设备运行状态、连接状态或项目自定义灯效。             |
| 2    | S-BUS 接口         | 用于连接 S-BUS 类型扩展模块，例如语音、音频等专用功能模块。  |
| 3    | RS-PORT2 接口      | 用于连接 RS-Port 类型 Yoke 模块。                            |
| 4    | RS-PORT4 接口      | 用于连接 RS-Port 类型 Yoke 模块。                            |
| 5    | USB-C 接口         | 用于供电、固件烧录、串口调试和数据通信。                     |
| 6    | BOOT 按键          | 用于进入下载模式或配合固件实现特定功能。                     |
| 7    | F-BUS 接口         | 用于连接 F-BUS 类型扩展模块，例如显示模块、热成像模块或电池模块。 |
| 8    | RESET / POWER 按键 | 多功能按键。短按用于复位；在使用电池供电时，长按可用于开关机。 |
| 9    | RS-PORT1 接口      | 用于连接 RS-Port 类型 Yoke 模块。                            |
| 10   | RS-PORT3 接口      | 用于连接 RS-Port 类型 Yoke 模块。                            |
| 11   | 顶部装饰件         | 用于提升整机外观完整性，也可作为结构识别与装饰部件。         |
| 12   | F-BUS 接口         | 用于连接 F-BUS 类型扩展模块。                                |
| 13   | LEGO 兼容固定孔*   | 用于与积木兼容结构、3D 打印结构件或项目外壳进行固定。        |
| 14   | M1.2 螺丝          | 用于固定顶部装饰件、外壳或相关结构部件。                     |

>LEGO® / 乐高® 为 LEGO Group 的注册商标。本产品非 LEGO Group 官方产品，未获得其授权、赞助或认可。“积木兼容”仅表示机械尺寸兼容，不代表品牌合作关系。



## 接口介绍

RootMaker 提供多种扩展接口，用于连接显示、灯光、传感器、语音、电机、触摸和供电模块。  
不同接口在结构、信号数量、供电能力和适用场景上有所不同。

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📘<a style="color: #FF6A00; text-decoration: none;"> 接口详细规格</a></h3>
  <p style="margin-bottom: 10px;">
  如果您是专业开发者需要接口的向详细IO映射，请看接口详细规格
  </p>
<div style="text-align: center;"><a href="#P_PORT_INFO" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     点击跳转到接口详细规格 →
    </a></div></div>

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/Rootmaker_RSPort.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">RS-Port</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
      RS-Port 是位于 RootMaker 主机两侧的 4 个带锁扣接口，分别为 RS-PORT1、RS-PORT2、RS-PORT3 和 RS-PORT4。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
      RS-Port 接口具备较好的机械强度，连接稳定，不易松脱，并且支持通过连接线进行一定距离的延长，适合安装在 3D 打印模型、桌面装置或需要分离布局的项目中。  
由于使用方便、扩展灵活，RS-Port 是 RootMaker 上最常用的外设连接接口。
    </p>
    <a href="#P_YOKE_RS_SUPPLY_LIST" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 0px 20px 0px 0px; box-shadow: none;">
    查看Yoke支持列表 →
    </a>
    </div></div></div></div>



<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/Rootmaker_FBUS.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">F-BUS</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
      F-BUS 是位于 RootMaker 顶部与底部的扩展接口，主要用于连接屏幕、图像传感器、热成像模块、电池模块以及其他较复杂的 Yoke 外设。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
F-BUS 模块通常可通过螺丝与 RootMaker 主机或其他机械结构件固定，从而获得更好的整体强度和安装可靠性。
RootMaker 顶部和底部均提供 F-BUS 连接能力。实际连接方式请参考对应 Yoke 模块的使用说明。
    </p>
    <a href="#P_YOKE_FB_SUPPLY_LIST" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 0px 20px 0px 0px; box-shadow: none;">
    查看Yoke支持列表 →
    </a></div></div></div></div>

<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/Rootmaker_SBUS.png" alt="RootMaker" style=" width: 80%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h2 style="margin: 0 15px 12px 0;">S-BUS</h2>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
	S-BUS 接口是位于 RootMaker 下方的金手指连接器，适用于部分专用 Yoke 外设或需要快速插拔的扩展模块。该接口插拔方便，结构紧凑，适合用于语音、音频、调试、临时扩展或特定功能模块。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    由于 S-BUS 采用金手指连接方式，相比 RS-Port 和 F-BUS，其机械固定强度较弱，更适合轻量模块或需要频繁拆装的应用场景。若项目需要长期运行、移动使用或承受震动，建议根据模块结构增加额外固定方式。
    </p>
    <a href="#P_YOKE_SB_SUPPLY_LIST" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 0px 20px 0px 0px; box-shadow: none;">
    查看Yoke支持列表 →
    </a></div></div></div></div>

### 接口连接注意事项

> 请在断电状态下连接或拔出外接模块。  
> 使用高功耗模块时，请确认 RootMaker 的供电能力是否满足项目需求。  
> 不同硬件版本的接口定义可能存在差异，请以当前硬件版本说明为准。

## 使用说明

<div style="border-radius: 10px; padding: 15px; background: linear-gradient(135deg, #FFBA89 0%, #FFD884 100%); margin: 4px 0px; box-shadow: none;"><div style="max-width: 800px; margin: 0px auto; text-align: center; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;"><p style="color: #4B1F00; margin: 0px 0px 1px; font-size: 22px; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;">
      🥇 <strong>如果你是第一次使用Ryzobee产品从这里快速了解产品系统</strong></p> 
<a href="/zh/fast_guide" target="_blank" class="is-internal-link is-valid-page" style="display: inline-block; padding: 4px 50px; background:#ffffff; color: #000000; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; margin-top: 15px; box-shadow: none;">
      📖 查看快速入门指南 →
</a></div></div>


### 使用前准备

在开始使用 RootMaker 前，请先完成以下准备工作，以确保设备可以正常连接、烧录和运行项目。

#### 1. 检查包装内容

请确认包装内的主机、连接线和相关配件完整无损。  
如使用套件版本，请同时确认对应的 Yoke 模块、线缆、螺丝或结构件是否齐全。

建议检查内容：

| 项目 | 说明 |
|---|---|
| RootMaker 主机 | 确认主机外观无明显损坏 |
| USB-C 线缆 | 用于供电、固件烧录和串口调试 |
| Yoke 模块 | 根据项目需求准备对应模块 |
| RS 连接线 | 用于连接 RS-Port 类型模块 |
| 固定螺丝 / 结构件 | 用于安装主机或扩展模块 |
| 快速上手卡 | 用于查看基本连接和入口链接 |

#### 2. 准备供电与连接设备

RootMaker 使用 USB-C 接口供电，推荐使用 **5V / 1A 以上** 的电源适配器或电脑 USB 接口。

如果需要烧录固件或调试设备，请使用支持数据传输的 USB-C 线缆连接电脑。部分仅支持充电的 USB-C 线缆无法用于烧录和串口通信。

<div style="text-align: center;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/Rootmaker_con2cmp.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

> **使用前请注意**
> 推荐使用稳定的 5V 电源,不建议使用劣质或老化的 USB 线缆。
> 若连接灯效、电机、显示屏等高功耗模块，请确认供电能力是否足够。
> 如设备反复重启，通常可能与供电不足或外接模块负载过高有关。

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA00;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📘<a style="color: #FF6A00; text-decoration: none;"> 以下内容使用Zoner平台快速开发</a></h3>
  <p style="margin-bottom: 10px;">
  如果您是专业开发者，想通过Arduino或IDF开发，请访问开发者页面
  </p>
<div style="text-align: center;"><a href="/zh/developer" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     点击跳转到开发者页面 →
    </a></div></div>

#### 3. 准备浏览器

**3.1 使用浏览器访问以下链接打开zoner工具平台。**

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:13px 16px;background:#fff7ed;border:1px solid #ffd4ad;border-radius:10px;">
  <div style="font-size:13px;color:#555;line-height:1.5;">
    <strong style="color:#222;font-size:15px;">访问Zoner平台</strong><br>
    点击右侧按钮访问Zoner平台，或在浏览器地址栏输入zoner.ryzobee.com访问。
  </div>
  <a href="https://www.ryzobee.com" target="_blank" rel="noopener noreferrer" style="padding:7px 12px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Visit Zoner</a>
</div>

**3.2 确保设备与PC连接无误后，点击Connect按钮连接设备。**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step1.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

**3.3 在浏览器弹出的窗口中选择需要连接的串行端口。**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step2.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

**3.4 点击选择需要下载的项目模板，点击“Flash to Device”图标或点击项目标签进入项目详情页。**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step3.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

**3.5 点击“Flash this project to Device”图标更新项目固件至设备。**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step4.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

**3.6 等待设备固件更新完成。更新需要10-60秒，更新时间根据项目不同而不同，更新过程请勿移除与设备连接的USB-C线，或按下设备的Reset按钮。**

<div style="text-align: center;"> <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_zoner_step5.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

<div style="border-radius: 10px; padding: 15px; background: linear-gradient(135deg, #FFBA89 0%, #FFD884 100%); margin: 4px 0px; box-shadow: none;"><div style="max-width: 800px; margin: 0px auto; text-align: center; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;"><p style="color: #4B1F00; margin: 0px 0px 1px; font-size: 22px; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none;">
      🥈 <strong>更多Zoner平台功能请前往Zoner Wiki页面</strong></p> 
<a href="/zh/Zoner" target="_blank" class="is-internal-link is-valid-page" style="display: inline-block; padding: 4px 50px; background:#ffffff; color: #000000; border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; margin-top: 15px; box-shadow: none;">
      📖 查看Zoner Wiki 页面 →
</a></div></div>

#### 4. 准备 Yoke 模块

请根据项目需求选择对应的 Yoke 模块，并确认模块接口类型与 RootMaker 接口一致。

连接模块前，请先关闭 RootMaker 电源，并确认接口方向正确。

#### 5. 确认项目资料

开始搭建项目前，建议先确认当前项目所需资料，包括接线方式、固件版本、结构文件和注意事项。

**建议确认：**

- 项目使用的 Root 主机型号
- 项目需要的 Yoke 模块
- 对应的固件或项目模板
- 接口连接方式
- 供电需求
- 3D 打印结构文件
- 已知问题和使用限制

#### 6. 安全注意事项

在连接、烧录和运行项目之前，请注意以下安全事项：

- 请勿在通电状态下随意插拔模块。
- 请勿让金属物体接触主机接口或电路板。
- 请确认模块接口方向正确，避免反插。
- 请勿超过主机或模块的额定供电能力。
- 使用电机、灯带、电池或无线供电模块时，请特别注意电流、温升和散热。
- 儿童使用时应在成年人指导下操作。

### RootMaker快速指南电子档


<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">RootMaker快速指南</div>
      <div style="font-size:12px;color:#777;">PDF · V1.3 · 5.1 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/%E5%BF%AB%E9%80%9F%E5%85%A5%E9%97%A8%E6%8C%87%E5%8D%97V13_H20260603.pdf" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 硬件规格

| 项目          | 参数                                                         |
| ------------- | ------------------------------------------------------------ |
| 产品名称      | RootMaker                                                    |
| 产品型号      | ZXRoot-Maker                                                 |
| 机身尺寸      | 基础组件：40mm × 40mm × 10.1mm<br>屏幕套件：40mm × 40mm × 15.4mm |
| 无线连接      | 2.4GHz Wi-Fi / Bluetooth LE                                  |
| USB 接口      | USB-C                                                        |
| USB 功能      | 供电、固件烧录、串口调试、设备配置                           |
| 输入电压      | 5V DC                                                        |
| 系统工作电压  | 3.3V                                                         |
| 推荐供电      | 5V / 1A 以上                                                 |
| 支持开发方式  | Arduino、ESP-IDF                                             |
| 主要接口      | USB-C、RS-Port / RS-BUS、F-BUS、S-BUS                        |
| 适用人群      | Maker、3D 打印创作者、开发者、教育用户                       |
| 工作环境温度* | 0°C ~ 40°C                                                   |
| 存储环境温度  | -20°C ~ 60°C                                                 |
| 工作环境湿度  | 10% ~ 90% RH，无结露                                         |
| 存储环境湿度  | 5% ~ 95% RH，无结露                                          |

> *工作环境温度为建议使用范围。若设备连接高功耗模块，例如灯效模块、电机模块、显示模块或电池模块，请注意供电能力、散热条件和安装空间。

##  3D安装结构文件

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rootmaker_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXRootMaker_v14_AIO_H20251128</div>
      <div style="font-size:12px;color:#777;">STEP · V1.4 · 44.8 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/ZXRootMaker_v14_AIO_H20251128.STEP" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>
## 详细接口规格<a id="P_PORT_INFO"></a>

### RS-Port
<div style="text-align: center;">
<img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/rs_port_interface.png" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>


| 项目         | 参数      | 备注                                                         |
| ------------ | --------- | -------------------------------- |
| 物理连接器   | GH1.25-4P |                                                              |
| GPIO电平     | 3.3V TTL  | 当使用超过3.3V TTL电频的器件时应添加电平转换芯片，否则会损坏GPIO端口 |
| GPIO数量     | 2         | 每RS-Port提供2个GPIO                                         |
| 3.3V供电能力 | 0.8A MAX  | 每RS-Port提供0.8A，整机3.3V输出不大于1.5A                    |

### F-BUS

<div style="text-align: center;">
<img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/f_bus_interface.png" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>


| 项目                             | 参数          | 备注                                                         |
| ------------ | --------- | -------------------------------- |
| 物理连接器                       | 排母1.27-2*12 | 顶部底部均为排母1.27-2*12                                    |
| GPIO电平                         | 3.3V TTL      | 当使用超过3.3V TTL电频的器件时应添加电平转换芯片，否则会损坏GPIO端口 |
| GPIO数量                         | 16            | 每RS-Port提供2个GPIO                                         |
| 3.3V供电能力                     | 1.0A MAX      | 每3V3 Pin提供0.5A供电能力，整机3.3V输出不大于1.5A            |
| [*VBAT供电能力* *](#P_VBAT_NOTE) | 1.0A MAX      | 每VBAT Pin提供0.5A供电能力                                   |

### S-BUS

<div style="text-align: center;">
<img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/s_bus_interface.png" alt="RootMaker" style="width: 50%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>


| 项目                             | 参数                      | 备注                                                         |
| ------------ | --------- | -------------------------------- |
| 物理连接器                       | SFP金手指连接器           |                                                              |
| GPIO电平                         | 3.3V TTL                  | 当使用超过3.3V TTL电频的器件时应添加电平转换芯片，否则会损坏GPIO端口 |
| GPIO数量                         | 14                        | 每RS-Port提供2个GPIO                                         |
| 3.3V供电能力                     | 1.0A MAX                  | 每3V3 Pin提供0.5A供电能力，整机3.3V输出不大于1.5A            |
| [*VBAT供电能力* *](#P_VBAT_NOTE) | 1.0A MAX                  | 每VBAT Pin提供0.5A供电能力                                   |
| VBUS供电能力                     | V<sub>BAT</sub>~5V @ 0.5A | VBUS为USB输入与VBAT输入合路后的电源，当电池供电时，电压为V<sub>BAT</sub>，当USB供电时，为5V |

<a id="P_VBAT_NOTE"></a>
> **VBAT引脚说明**
>
> 接通USB电源时可通过VBTA为电池充电，充电电流约为500mA，建议使用1000mAh以上的电池（0.5C），输出电流的最大值根据电池供电能力不同而不同，通常不大于2A。当需要开关机功能且电源长带电时，电池接口也可用于不大于5V的外部电源输入。
>
> VBUS会受到开关机影响，关机后VBUS不带电

## Yoke支持列表

### RS-PORT<a id="P_YOKE_RS_SUPPLY_LIST"></a>

- [Yoke-KEYW 轻触开关模块](/zh/Yoke_Model/Yoke-KEYW-ZH)
- [Yoke-MOTO 直流马达控制模块](/zh/Yoke_Model/Yoke-MOTO-ZH)
- [Yoke-RAD60 60GHz毫米波存在传感器模块](/zh/Yoke_Model/Yoke-RAD60-ZH)
- [Yoke-RGBW RGBW灯效模块](/zh/Yoke_Model/Yoke-TRGBW-ZH)
- [Yoke-TRGBW 3x RGBW灯效模块](/zh/Yoke_Model/Yoke-TRGBW-ZH)
- [Yoke-TOUCH4 四通道触摸模块](/zh/Yoke_Model/Yoke-TOUCH4-ZH)

### F-BUS<a id="P_YOKE_FB_SUPPLY_LIST"></a>



### S-BUS<a id="P_YOKE_SB_SUPPLY_LIST"></a>

## 产品爆炸图

<div style="text-align: center;"><img src="https://res.8ms.xyz/ryzobee/wiki/Root/rootmaker/img/RootMaker_main_img.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> </div>

## 常见问题

### RootMaker 无法被电脑识别怎么办？

请检查 USB-C 数据线是否支持数据传输，确认电脑 USB 接口正常，并尝试重新进入下载模式。

---

### 固件烧录失败怎么办？

请确认 RootMaker 已进入下载模式，浏览器或开发工具是否具有串口访问权限，并检查所选固件是否适用于当前硬件版本。

---

### RootMaker 上电后没有反应怎么办？

请检查供电是否正常，USB-C 线缆是否可靠，是否存在外接模块短路或高功耗模块导致电源保护。

---

### 连接 Yoke 模块后设备重启怎么办？

通常可能与供电不足、模块反接、线缆接触不良或负载过高有关。  
请先断电，移除外接模块，确认 RootMaker 可单独启动后，再逐个连接模块测试。

---

### 可以在通电状态下插拔 Yoke 模块吗？

不建议热插拔。  
请在断电状态下连接或拔出模块，以避免接口短路、通信异常或模块损坏。

---

### RootMaker 是否必须使用 Zoner 平台？

不是。  
Zoner 平台适合快速配置和复刻项目。开发者也可以使用 Arduino、ESP-IDF  进行自定义开发。

---

### RootMaker 可以连接多个 Yoke 模块吗？

可以，但需要根据接口数量、固件支持和整体供电能力判断。  
如果同时连接灯光、电机、显示或语音模块，请特别注意电源余量。

---

### Wi-Fi 连接失败怎么办？

请确认 Wi-Fi 为 2.4GHz 网络，SSID 和密码正确，并避免特殊字符或弱信号环境。  
如果项目支持重新配网，请按照对应项目说明进入配网模式。

---

### 如何恢复默认固件？

可以通过 Zoner 重新选择官方默认模板并烧录固件。  
如果无法进入正常模式，请尝试进入下载模式后重新烧录。

---

### RootMaker 适合哪些项目？

RootMaker 适合 3D 打印互动作品、桌面机器人、灯光装置、传感器面板、AI 语音设备、教学项目和快速硬件原型。
