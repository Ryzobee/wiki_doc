欢迎来到 Ryzobee Developer Center。  
本页面面向希望基于 Root 主机和 Yoke 模块进行二次开发、固件定制、驱动适配或项目模板开发的用户。

如果你只是希望快速复刻官方项目，建议优先使用 Zoner 平台。
如果你希望修改代码、开发自己的功能、适配新的模块或构建完整项目，可以从本页面开始。

## 开发方式总览

Ryzobee 目前主要支持以下开发方式：

| 开发方式 | 状态 | 适合人群 | 说明 |
|---|---|---|---|
| Ryzobee Arduino 开发 | 可用 | 入门开发者、Maker、教育用户 | 适合快速编写示例、控制灯光、电机、传感器和基础交互 |
| Ryzobee ESP-IDF 开发 | `正在施工中` | 高级开发者、固件工程师 | 适合复杂项目、底层驱动、网络服务、OTA 和性能优化 |
| Zoner 项目模板 | 可用 / 持续完善 | 新手用户、项目复刻用户 | 适合通过模板快速配置和运行项目 |

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
    <h3 class="toc-header" style="margin-top: 0px; color:#FFA600;"><a href="https://github.com/Ryzobee"
            class="toc-anchor"></a>📝<a style="color: #FF6A00; text-decoration: none;">选择您需要的开发环境</a></h3>
    <p style="margin-bottom: 10px;">
        如果您是开发者，希望自己编写固件，可以点击下面的按钮快速抵达开发环境介绍。
    </p>
    <div style="text-align: center;">
        <div
        style="display: inline-block; width: 18%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
        <a href="/zh/dev/Arduino" target="_blank">
            <img src="https://res.8ms.xyz/ryzobee/wiki/Arduino_icon_200.png" alt="RootMaker"
                style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;">
            <br>
            Arduino开发页面
        </a>
    </div>
    <div
        style="display: inline-block; width: 18%; min-width: 140px; margin: 10px; text-align: center; background: rgb(255, 255, 255); border-radius: 5px; padding: 15px; box-shadow: rgba(0, 0, 0, 0.1) 0px 0px 5px;">
        <a href="/zh/dev/ESPIDF" target="_blank">
            <img src="https://res.8ms.xyz/ryzobee/wiki/esp_icon_200.png" alt="RootMaker"
                style="width: 100%; height: auto; border-radius: 5px; margin-bottom: 10px;">
            <br>
            IDF开发页面
        </a>
    </div>
    </div>
</div>

## Ryzobee Arduino 开发

Arduino 开发方式适合希望快速上手 RootMaker 和 Yoke 模块的用户。  
通过 Arduino，你可以更方便地控制 RGBW 灯效、读取传感器数据、驱动电机、处理按键输入，并快速完成自己的互动项目。

适合场景：

- 快速点亮 Yoke-TRGBW RGBW 灯效模块
- 读取 Yoke-SCD4x 二氧化碳传感器数据
- 使用 Yoke-KEYW 或 Yoke-TOUCH4 进行输入控制
- 制作简单的灯光、传感器或桌面互动项目
- 基于官方示例进行二次修改

页面入口：

- [Ryzobee Arduino 开发指南](/zh/dev/Arduino)
- [RootMaker Arduino API](/zh/dev/rootmaker_arduino_api)
- [Arduino 示例工程]()`正在施工中`

## Ryzobee ESP-IDF 开发

ESP-IDF 是面向高级开发者的官方底层开发方式，适合构建更复杂、更稳定、更完整的固件项目。

当前该部分仍在施工中，后续将逐步补充 RootMaker 的 ESP-IDF 工程模板、组件驱动、网络服务、文件系统、OTA、WebServer 和 Yoke 模块适配示例。

适合场景：

- 需要更完整的工程结构
- 需要使用 FreeRTOS 多任务
- 需要开发 WebServer、OTA、MQTT 或云端通信功能
- 需要适配复杂 Yoke 模块
- 需要进行产品级固件开发
- 需要更细致地控制内存、任务和外设资源

计划内容：

- [Ryzobee ESP-IDF 开发指南]() `正在施工中`
- [ESP-IDF 环境安装]() `正在施工中`
- [RootMaker IDF 工程模板]() `正在施工中`
- [Yoke 模块驱动开发]() `正在施工中`
- [OTA 固件升级]() `正在施工中`

> 本章节正在整理中。如果你已经熟悉 ESP-IDF，也可以先参考官方示例工程和 RootMaker 硬件接口说明进行开发。

<div style="border-left: 6px solid #ff6a00;background: #fff7ed;padding: 10px 16px; border-radius: 0px;">
  <h3 class="toc-header" style="margin-top: 0px; color:#FFA600;"><a href="https://github.com/Ryzobee" class="toc-anchor"></a>📝<a style="color: #FF6A00; text-decoration: none;"> 在Github上查看我们的代码仓库</a></h3>
  <p style="margin-bottom: 10px;">
  如果您需要源码支持，并进行二次开发，您可以访问我们的Github仓库，在这里您可以找到我们的SDK与Arduino示例
  </p>
<div style="text-align: center;"><a href="https://github.com/Ryzobee" target="_blank" style="display: inline-block; padding: 4px 25px; background: #FF6A00; color: rgb(255, 255, 255); border-width: medium; border-style: none; border-color: currentcolor; border-image: initial; outline: none; border-radius: 50px; font-weight: bold; text-decoration: none; transition: transform 0.2s; margin: 5px; box-shadow: none;">
     点击跳转到Github仓库 →
</a></div></div>

## 开发前准备

在开始开发前，建议先确认以下内容：

| 准备项       | 说明                                  |
| ------------ | ------------------------------------- |
| Root 主机    | 当前使用的主机型号，例如 RootMaker    |
| 硬件版本     | 不同硬件版本可能存在接口或引脚差异    |
| Yoke 模块    | 确认需要连接的模块型号和接口类型      |
| USB-C 数据线 | 请使用支持数据传输的 USB-C 线缆       |
| 开发方式     | 根据需求选择 Arduino 或 ESP-IDF       |
| 固件版本     | 确认使用的示例或 SDK 是否匹配当前硬件 |
| 串口工具     | 用于查看日志、调试启动信息和排查问题  |

建议第一次开发时先运行官方示例，确认硬件、线缆和环境正常后，再开始修改代码。

## 硬件参考

进行开发时，请优先查看当前硬件版本对应的接口说明和引脚定义。
不同模块使用的接口类型不同，开发前需要确认接口、电源、通信方式和安装方向。

常用参考页面：

- [RootMaker 主机](/zh/root/rootmaker)
- [Yoke 配件生态](/zh/Yoke_Model)

## 贡献与反馈

Ryzobee 欢迎开发者参与生态共建。
你可以提交示例工程、改进文档、反馈问题、适配新的 Yoke 模块，或分享自己的项目模板。

你可以贡献：

- 示例代码
- Bug 反馈
- 文档修正
- 新模块驱动
- 项目模板
- 3D 安装结构
- 教程文章
- 使用案例

提交反馈时，建议提供以下信息：

| 信息     | 示例                      |
| -------- | ------------------------- |
| 主机型号 | RootMaker                 |
| 硬件版本 | ZXROOTEC08 / 其他版本     |
| 开发方式 | Arduino / ESP-IDF         |
| 使用模块 | Yoke-TRGBW、Yoke-RAD60 等 |
| 固件版本 | v1.0.0                    |
| 问题描述 | 现象、复现步骤、预期结果  |
| 日志信息 | 串口日志、编译错误、截图  |

## 开发者支持

如果你在开发过程中遇到问题，可以优先查看 FAQ、示例工程和硬件参考页面。
如果仍无法解决，可以通过社区渠道或技术支持入口提交问题。

支持入口：

- [FAQ 常见问题](/zh/faq)
- [Discord 社区]()`正在施工中`
- [GitHub 仓库](https://github.com/Ryzobee)
- [联系技术支持]()`正在施工中`
