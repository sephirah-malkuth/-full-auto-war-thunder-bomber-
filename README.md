# 📋 Full-Auto War Thunder Bomber v5.0
全量战争雷霆自动化战区轰炸项目

> 🛑 **郑重声明 / DISCLAIMER**
>
> **本项目为免费开源软件 (Free & Open Source Software)。**
>
> 如果你是付费购买的本软件，说明你**被骗了**！请立即申请退款并举报商家。
> 本项目严禁用于任何商业用途，严禁打包倒卖。
>
> **Project URL:** [https://github.com/Sephirah-Malkuth/-Full-Auto-War-Thunder-Bomber-]([https://github.com/Sephirah-Malkuth/-Full-Auto-War-Thunder-Bomber-]

---

## 📖 项目简介 (Introduction)

**Full-Auto War Thunder Bomber** 是一个针对《战争雷霆 (War Thunder)》的**非注入式自动化战区轰炸脚本**。

本项目的初衷是帮助广大没有足够时间肝活动、或没有预算购买高级账户/载具的玩家，跳过枯燥的机械化操作，突破游戏活动的硬性时长限制。

### 核心设计理念
*   **安全性第一**：不读取、不写入游戏内存。完全基于**计算机视觉 (YOLOv8)** 和游戏官方提供的 **本地遥测接口 (localhost:8111)**。
*   **模拟操作**：通过 ViGEmBus 驱动模拟物理 Xbox 手柄信号，配合拟人化算法，极大降低被检测风险。
*   **全流程自动化**：实现从大厅排队、起飞、索敌、投弹到返航的全自动闭环。

## ✨ 核心功能 (Features)

*   **🕹️ 全自动流程**：支持“大厅排队 -> 进图出击 -> 地面/空中起飞 -> 寻找战区 -> 投弹 -> 脱离/返航 -> 循环”的全过程。
*   **🧠 智能感知**：
    *   集成 **YOLOv8** 视觉模型，识别UI按钮、战区图标、跑道、弹窗等。
    *   通过 **8111 API** 实时监控飞行姿态、速度、高度及燃油状态。
*   **💣 多模式投弹**：
    *   **CCRP**: 现代喷气机首选，自动计算投弹点。
    *   **CCIP**: 攻击机俯冲轰炸模式。
    *   **BOMBSIGHT**: 传统轰炸机投弹瞄准镜模式。
*   **🛡️ 安全与防护**：内置超速保护、过载自动改平、跳伞提示自动退出、意外弹窗处理机制。
*   **🎨 现代化 GUI**：基于 Flet (Material Design 3) 构建的配置界面，支持参数热修改与实时状态监控。

## 📂 项目结构 (Structure)

本版本 (v5.0) 采用模块化架构设计，主要目录结构如下：

```text
Full-Auto-WT-Bomber/
├── api/                # 游戏本地遥测接口 (8111 API) 通信模块
├── bombing/            # 投弹核心逻辑 (CCRP/CCIP/Sight 控制器)
├── config/             # 配置文件与用户档案管理
├── controllers/        # 虚拟外设控制 (Gamepad/Keyboard/Mouse)
├── core/               # 主程序核心、状态机与事件分发
├── detectors/          # 视觉检测模块 (YOLOv8 推理与屏幕捕获)
├── flight/             # 飞行控制逻辑 (起飞、巡航、对准、返航)
├── gui/                # 图形用户界面 (Flet)
├── handlers/           # 辅助处理器 (弹窗处理、大厅逻辑)
├── humanize/           # 拟人化行为模拟 (随机抖动、漂移)
├── models/             # YOLO 模型权重文件 (.pt)
├── safety/             # 飞行安全保护模块
└── utils/              # 通用工具类
```

## 🛠️ 使用说明 (Usage)

> 🚧 **文档完善中 / WIP**
>
> 详细的安装教程、环境配置及参数调校指南将在项目代码完全上传后更新。

### 基础环境要求 preview
*   Windows 10/11 (64位)
*   Python 3.8+
*   ViGEmBus 虚拟手柄驱动
*   NVIDIA 显卡 (推荐用于 AI 推理加速)

## 📄 许可证 (License)

本项目采用 **GNU General Public License v3.0 (GPLv3)** 授权。
您可以自由地使用、修改和分发本项目，但**必须保持开源且免费**。

---
*Created with ❤️ for the WT Community.*
```
