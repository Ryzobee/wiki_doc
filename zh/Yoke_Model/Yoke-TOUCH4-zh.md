<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_Touch4_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-TOUCH4 四通道触摸模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-TOUCH4 是一款专为 3D 打印互动作品设计的四通道触摸输入模块，可用于触摸按键、隐藏式交互面板、桌面互动装置等场景。
模块通过标准接口与 Root 主机连接，用户可以快速为 3D 打印作品增加触摸交互能力，让模型具备更自然、更简洁的人机交互体验。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-TOUCH4 集成四路独立触摸检测通道，采用按压式快拆端子设计，通过双头杜邦针、导线等方式扩展触摸区域。

模块内部支持高灵敏度电容触摸检测，可自动适应一定程度的环境变化，并降低误触发概率，适合嵌入式交互场景使用。

| 项目   | 说明                      |
| ---- | ----------------------- |
| 模块接口 | RS-Port                 |
| 供电   | 由 Root 主机电源提供           |
| 输入类型 | 电容触摸输入                  |
| 通道数量 | 4路独立触摸通道                |
| 接线方式 | 按压式快拆端子                 |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 支持4路独立触摸输入
- 支持导电打印件作为触摸区域
- 可通过双头杜邦针快速连接触摸结构
- 支持导线 + 金属触摸盘扩展使用
- 适合隐藏式触摸按键和无开孔交互结构
- 使用RS-Port与 Root 主机快速连接
- 可配合 Zoner 项目模板快速完成配置

## 使用说明

使用 Yoke-TOUCH4 前，请确认 Root 主机已正确烧录支持触摸输入的固件或项目模板。

### 与 Root 主机连接

Yoke-TOUCH4 可通过 RS-Port 线缆连接到 Root 主机。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_Touch4_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



连接时请注意：

- 请在断电状态下连接或拔出模块。
- 确认接口方向正确，避免反插。
- 若触摸检测异常，请优先检查触摸线是否过长或接触不良。
- 建议避免触摸线与高压、高频或大电流线路并行布线。

### 触摸结构与安装方式

Yoke-TOUCH4 可通过不同结构实现多种触摸交互方式。

例如：

- 导电打印耗材触摸区域
- 金属触摸片
- 铜箔贴片
- 金属螺丝触摸点
- 导线延伸触摸面板
- 隐藏式面板背触摸结构

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_TOUCH4_connect_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### 安装建议：

- 建议触摸区域背后避免大面积金属结构。
- 若使用导电打印件，建议保证导电路径连续且稳定。
- 触摸线越短，抗干扰能力通常越强。
- 若触摸区域位于塑料壳内部，建议减小外壳厚度以提高灵敏度。
- 避免触摸线靠近电机、电源模块或高频设备。
- 对于大型触摸区域，可适当增加触摸阈值避免误触。

## 供电需求

| 项目       | MAX  | Type | Min  |
| -------- | ---- | ---- | ---- |
| 供电电流(mA) | 20mA |      |      |
| 供电电压(V)  |   |   3.3V   |  |

## 硬件规格

| 项目   | 参数                          |
| ---- | --------------------------- |
| 模块型号 | Yoke-TOUCH4                 |
| 模块名称 | 四通道触摸模块                     |
| 接口形态 | RS-Port                     |
| 输入类型 | 电容触摸输入                      |
| 通道数量 | 4路                          |
| 接线方式 | 按压式快拆端子                     |
| 适用场景 | 3D打印互动结构、隐藏按键、触摸面板、创意交互装置   |
| 适配主机 | RootMaker / Root 系列兼容主机     |
| 固定方式 | 结构件固定 / 胶粘固定 / 螺丝固定，视项目结构而定 |

## 3D安装结构文件

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_Touch4_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-TOUCH4-v10.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 1.27 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-TOUCH4-v10.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>


## 常见问题

### Yoke-TOUCH4 无法检测触摸怎么办？

请检查以下内容：

1. Root 主机是否正常供电。
2. 模块是否连接到正确的 RS-Port 接口。
3. 接口方向是否正确。
4. 固件是否支持触摸模块。
5. 触摸区域是否正确连接到对应端子。

### 触摸误触发怎么办？

可能原因包括：

- 触摸线过长。
- 周围存在强干扰源。
- 触摸区域面积过大。
- 触摸区域距离金属结构过近。
- 电源纹波或接地不稳定。

建议：

- 缩短触摸连接线。
- 远离电机和高频模块。
- 减小触摸区域面积。
- 增加绝缘层厚度。
- 更换适配器。

### 导电打印件无法稳定触摸怎么办？

可能原因包括：

- 导电耗材电阻过高。
- 导电路径过长。
- 接触点连接不稳定。
- 外壳厚度过厚。

建议：

- 缩短导电路径，使末端导线距离面板更近。
- 增加导电区域面积。
- 使用更稳定的连接方式。
- 降低触摸区域与手指之间的间隔厚度。

### 可以在通电时插拔 Yoke-TOUCH4 吗？

不建议热插拔。
请在断电状态下连接或拔出模块，以避免接口短路、信号异常或模块损坏。

### Yoke-TOUCH4 可以连接普通导线吗？

可以。
模块支持直接连接导线、金属片、铜箔、导电打印结构等多种触摸介质，用户可以根据项目需求自由设计交互结构。
