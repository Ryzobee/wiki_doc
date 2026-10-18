---
title: "Zoner 平台"
description: "了解 Zoner 的项目探索、固件部署、设备管理与 R-Link Lua 工作区"
tags: "Zoner, RootMaker"
published: true
isPublished: true
---

Zoner 是 RyzoBee 面向 Root 主机与 Yoke 配件的浏览器平台。你可以在这里发现项目、查看模块与接线、获取项目文件，并将适配的固件部署到主机；也可以通过设备管理页面配置主机，使用 R-Link 编写和管理 Lua 脚本。

<div style="border-radius: 10px; padding: 20px; background: #fff7ed; border-left: 6px solid #FF6A00; margin: 20px 0;">
  <strong style="color: #4B1F00;">从项目到作品</strong>
  <p>准备主机和模块 → 选择项目 → 检查接线与版本 → 连接设备 → 部署固件 → 验证运行</p>
  <a href="https://zoner.ryzobee.com" target="_blank" rel="noopener noreferrer" style="display: inline-block; padding: 8px 20px; background: #FF6A00; color: #fff; border-radius: 20px; text-decoration: none;">打开 Zoner →</a>
</div>

## 从这里开始

- **第一次使用：**[快速开始](/zh/Zoner/quick_start)，完成项目选择、USB 连接与部署。
- **连接、配网或烧录本地固件：**[设备管理](/zh/Zoner/device)，查看设备状态、Wi-Fi 与自定义配置。
- **编写 Lua 应用：**[R-Link Beta](/zh/Zoner/rlink)，了解草稿、设备脚本、UI 模拟器和日志。

## Zoner、Root 与 Yoke 的关系

Root 主机运行固件并控制硬件，Yoke 模块提供灯光、触摸、显示、传感或电机等具体功能，Zoner 提供项目资料与部署、配置工具。选定项目后，仍需要准备匹配的硬件，并按照项目说明完成连接。

项目固件决定设备支持的功能。平台上的设备状态、Wi-Fi 配置、自定义配置与 Lua 管理，需要相应固件配合；不能仅凭主机连接成功，就认定所有功能都可用。

## 平台主要入口

### 发现灵感与所有项目

[发现灵感](https://zoner.ryzobee.com/) 展示精选创作；[所有项目](https://zoner.ryzobee.com/projects) 用于浏览和查找项目。可以按灯光氛围、机械运动、感知交互、创意工具等分类探索，再按名称搜索目标项目。

进入项目详情后，重点阅读三个区域：

- **项目介绍：**了解作品功能、使用方法、适用场景及限制。
- **模块与接线：**核对主机、Yoke 型号、模块数量和连接方法。
- **项目文件：**查看作者提供的固件、模型和装配等资源。具体文件随项目而异。

项目提供可部署固件时，可选择主机和项目版本，再使用“一键部署到设备”。标为“案例资料”的项目不应被视为一定提供可直接烧录的固件，请先阅读项目文件与说明。

### 我的收藏

项目卡片和详情页提供收藏入口。[我的收藏](https://zoner.ryzobee.com/favorites) 用于回到已收藏的项目；如页面要求登录，按页面提示完成登录。收藏项目不等于已经下载文件或部署固件。

### 我的设备

[我的设备](https://zoner.ryzobee.com/device) 提供 USB 连接、设备状态、Wi-Fi 配置、自定义配置和本地固件烧录入口。具体操作见 [设备管理](/zh/Zoner/device)。

### R-Link Beta

[R-Link](https://zoner.ryzobee.com/link) 用于编写、管理与运行 RootMaker Lua 脚本，并提供浏览器 UI 模拟器。设备端功能需要先安装兼容的 R-Link 固件，详细说明见 [R-Link Beta](/zh/Zoner/rlink)。

## 使用前需要准备什么

1. 与项目匹配的 Root 主机及 Yoke 模块。
2. 支持数据传输的 USB-C 线缆。
3. 安装桌面版 Chrome 或 Edge 的电脑，允许浏览器访问所选串口。
4. 可访问 Zoner 及项目资源的网络。
5. 项目要求的电源和装配材料。

Yoke 模块应在断电状态下连接。Yoke-MOTOR-A 等外部供电模块需遵循对应模块页面的供电说明，不能直接套用普通 USB 供电方式。

## 常见问题

### 是否需要编程？

复刻已有项目时，通常可以按说明连接硬件并部署现成固件。需要自定义逻辑时，可以使用 R-Link Lua，或参考 [开发环境](/zh/dev) 使用 Arduino 等工具开发。

### Wiki 中有模块页面，为什么找不到对应项目？

硬件文档与项目固件分别维护。请查看项目支持的主机、模块和发布版本；不要用不匹配的固件替代。可以先阅读 [Yoke 配件系列](/zh/Yoke_Model) 确认模块信息。

### 烧录后原来的脚本还在吗？

烧录会覆盖固件写入范围内的内容。R-Link 完整固件烧录可能覆盖脚本分区及其数据，请在更新前备份重要文件；仅在浏览器里保存草稿不能代替设备文件备份。

### 页面功能和本说明不一致怎么办？

本文按 Zoner 当前中文界面组织。不同项目、固件版本或后续平台更新可能影响可用功能，操作时以页面提示和所选项目说明为准。

## 获取帮助

连接与烧录问题请先查看 [快速开始中的故障排查](/zh/Zoner/quick_start#troubleshooting)，设备配置问题请查看 [设备管理](/zh/Zoner/device)。

如需反馈，请附上项目链接、项目版本、主机和模块型号、浏览器版本、复现步骤，以及去除密码和密钥后的相关日志。可通过 [support@ryzobee.com](mailto:support@ryzobee.com) 联系支持，或从 [RyzoBee GitHub](https://github.com/Ryzobee) 查找对应项目仓库。
