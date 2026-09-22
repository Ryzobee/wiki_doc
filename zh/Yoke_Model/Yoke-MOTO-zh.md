<div style="display: flex; align-items: center; gap: 15px; margin: 15px 0; padding: 15px; background: #f7f7f7; border-radius: 16px; ">
  <div style="flex: 0 0 30%;"><img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_MOTO_Wiki_main.png" alt="RootMaker" style=" width: 100%; display: block; border-radius: 12px;"></div>
  <div style="flex: 1;">
    <h1 style="margin: 0 15px 12px 0;">Yoke-MOTO 直流马达控制模块</h1>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    Yoke-MOTO 是一款专为 3D 打印作品设计的直流马达控制模块。
模块通过标准接口与 Root 主机连接，用户可以快速为 3D 打印作品添加电机驱动功能，实现旋转、传动、联动等动态效果，让模型具备更丰富的机械交互能力。
    </p>
    <p style="margin: 0 15px 12px 0; line-height: 1.7;">
    </p>
</div></div></div></div>

## 模块简介&主要特性

Yoke-MOTO 集成直流马达驱动电路，可直接控制小型直流减速电机、风扇、电动机构等负载。
模块支持正反转与 PWM 调速，可满足多数 3D 打印互动装置与机械结构的驱动需求。

| 项目 | 说明 |
|---|---|
| 模块接口 | RS-Port |
| 供电 | 由 Root 主机电源提供 |
| 控制信号 | GPIO / PWM |
| 适配主机 | RootMaker / Root 系列兼容主机 |

主要特性：

- 支持直流马达正反转控制
- 支持 PWM 调速控制
- 适合 3D 打印模型机械结构驱动
- 使用 RS-Port 与 Root 主机快速连接
- 可驱动小型减速电机、风扇等直流负载
- 可配合 Zoner 项目模板快速完成配置

## 使用说明

使用 Yoke-MOTO 前，请确认 Root 主机已正确烧录适配电机控制的固件或项目模板。

### 与 Root 主机连接
Yoke-MOTO 可通过 RS-Port 线缆连接到 Root 主机。

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_MOTO_Wiki_connect2rootmaker.png" alt="RootMaker" style="width: 60%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>



连接时请注意：

- 请在断电状态下连接或拔出模块。
- 确认接口方向正确，避免反插。
- 【重要】请确认所连接电机的工作电压与模块规格兼容。

### 安装方式

<div style="text-align: center;">
     <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke_MOTO_Wiki_connect_900.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

#### 安装建议：

- 建议避免电机长时间堵转或持续高负载运行，以免导致电机或驱动器过热。
- 建议将电机与传动结构可靠固定，避免运行时产生松动或偏移。
- 电机轴与齿轮、联轴器等机构安装时，应避免过度侧向受力。

## 供电需求

Yoke-MOTO 的实际工作电流取决于电机负载，模块内置约 450mA 的过流保护（OCP）。

| 项目 | MAX | Type | Min |
|---|---|---|---|
| 供电电流(mA) | 450mA |  |  |
| 供电电压(V) | 5V |  | 3.3V |

## 硬件规格

| 项目     | 参数                                             |
| -------- | ------------------------------------------------ |
| 模块型号 | Yoke-MOTO                                       |
| 模块名称 | MOTO 直流马达控制模块                               |
| 接口形态 | RS-Port                                          |
| 负载类型 | 小型直流马达 / 直流减速电机 等                 |
| 适用场景 | 3D 打印模型动态结构、旋转机构、互动装置            |
| 适配主机 | RootMaker / Root 系列兼容主机                    |
| 固定方式 | 结构件固定 / 螺丝固定，视项目结构而定 |

## 3D安装结构文件

<div style="text-align: center;">
    <img src="https://res.8ms.xyz/ryzobee/wiki/Yoke/Yoke_MOTO_Wiki_mechanical.png" alt="RootMaker" style="width: 80%; height: auto; border-radius: 5px; margin-bottom: 10px;"> 
</div>

<div style="display:flex;align-items:center;justify-content:space-between;gap:14px;margin:16px 0;padding:14px 16px;background:#fff;border:1px solid #e5e5e5;border-radius:10px;">
  <div style="display:flex;align-items:center;gap:12px;">
    <div style="width:38px;height:38px;border-radius:9px;background:#fff3e8;color:#ff6a00;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;">📄</div>
    <div>
      <div style="font-size:15px;font-weight:700;color:#222;">3D STEP文件 ZXYoke-MOTO.step</div>
      <div style="font-size:12px;color:#777;">STEP · V1.0 · 1.63 MB</div>
    </div>
  </div>
  <a href="https://res.8ms.xyz/ryzobee/wiki/Yoke/step_file/ZXYoke-MOTO.step" download style="padding:7px 13px;background:#ff6a00;color:#fff;text-decoration:none;border-radius:6px;font-size:13px;font-weight:700;white-space:nowrap;">Download</a>
</div>

## 常见问题

### 连接了马达但是不工作？

请检查以下内容：

1. Root 主机是否正常供电。
2. 模块是否连接到正确的 RS-Port 接口。
3. 接口方向是否正确。
4. 固件是否支持当前模块或功能。
5. 马达是否被堵转。
6. 确认马达规格，若电机电流过大，可能触发模块 OCP 保护。

### 马达的转动方向与预期的不同？

可以通过交换马达的两根线转换方向；也可以修改固件，切换转动方向。

### 可以在通电时插拔 Yoke-MOTO 吗？

禁止热插拔。  
请在断电状态下连接或拔出模块，以避免接口短路、信号异常或模块损坏。  
