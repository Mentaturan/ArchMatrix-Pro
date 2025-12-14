# 🏗️ ArchMatrix Pro | 建筑空间矩阵生成器

![Version](https://img.shields.io/badge/version-2.0.0-blue.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg) ![Status](https://img.shields.io/badge/status-stable-success.svg)

> **ArchMatrix Pro** 是一款专为计算性设计（Computational Design）和建筑生成算法开发的轻量级前端工具。它允许用户在网格化画布上绘制建筑边界，通过洪水填充算法（Flood Fill）实时计算内部空间，并导出供后续生成式AI模型使用的标准 JSON 矩阵数据。

---

## ✨ 核心特性 (Key Features)

### 🎨 专业的交互体验
* **现代 SaaS 界面设计**：采用 Slate/Inter 建筑师色调，冷静沉稳的视觉风格。
* **无图化渲染**：全矢量 SVG 图标与 CSS 绘图，零外部资源依赖，单文件即可运行。
* **响应式布局**：完美适配桌面端与移动端触控操作。

### ⚡ 强大的核心算法
* **实时闭合检测**：内置高效的洪水填充算法（Flood Fill Algorithm），实时计算建筑边界是否闭合。
* **智能空间识别**：自动区分“外部空白”、“建筑边界”与“内部区域”，并给予实时视觉反馈。
* **非破坏性编辑**：支持完整的 **撤销 (Undo)** 历史记录栈，容错率极高。

### 💾 数据互通
* **标准 JSON I/O**：支持导入/导出标准二维数组矩阵，无缝对接 Grasshopper, Python, 或其他生成式设计后端。
* **动态网格系统**：支持 10x10 (2m精度) 与 20x20 (1m精度) 动态切换。

---

## 🚀 快速开始 (Getting Started)

本项目为**零依赖 (Zero-dependency)** 的纯原生实现。

### 安装与运行
无需 `npm install` 或复杂的构建流程。

1. 下载仓库中的 `matrix_generator.html` 文件。
2. 直接使用 Chrome / Edge / Safari 浏览器打开即可。

### 快捷键 (Shortcuts)

为了提高绘图效率，我们内置了专业软件通用的快捷键：

| 按键 | 功能 | 说明 |
| :--- | :--- | :--- |
| **B** | ✏️ 画笔 (Brush) | 切换至绘制模式 |
| **E** | 🧹 橡皮 (Eraser) | 切换至擦除模式 |
| **Ctrl + Z** | ↩️ 撤销 (Undo) | 回退上一步操作 |
| **右键 (Hold)** | 🔄 临时切换 | 按住右键可临时切换画笔/橡皮 |

---

## 📊 数据结构说明

导出的 `.json` 文件包含一个二维数组（Matrix），直接映射空间的体素化表达。

**数据定义：**
* `1`: **建筑有效区域** (包含围护结构边界及内部闭合区域)
* `0`: **外部无效区域**

**示例 (5x5 简化版):**
```json
[
  [0, 0, 1, 1, 0],
  [0, 1, 1, 1, 0],
  [0, 1, 1, 1, 0],
  [0, 1, 1, 0, 0],
  [0, 0, 0, 0, 0]
]

```

---

##🛠️ 技术栈 (Tech Stack)* **HTML5 / CSS3**: 使用 CSS Variables 管理主题，Flexbox/Grid 布局。
* **Vanilla JavaScript (ES6+)**:
* 面向对象编程 (OOP) 架构。
* 自定义状态管理与历史记录栈 (History Stack)。
* 原生 DOM 操作，无 jQuery/React/Vue 依赖，极致轻量。



---

##📝 待办清单 (Roadmap)* [x] 基础绘图与擦除
* [x] 闭合区域实时检测算法
* [x] 历史记录撤销功能
* [x] JSON 数据导入导出
* [ ] **多楼层支持 (Multi-floor Support)**
* [ ] **功能分区标记** (如：客厅、卧室用不同颜色值标记)
* [ ] **Grasshopper 实时连接插件**

---

##📄 开源协议MIT License.
您可以自由地在个人项目、学术研究或商业项目中使用此代码。

---

*Designed for Architects, by Architects.*

```

### 使用建议：

1.  **添加截图**：建议您运行代码后，截图一张界面，保存为 `screenshot.png`，放在同一目录下。Markdown 代码中我已经预留了位置（虽然目前没有直接引用图片，但您可以添加 `![Screenshot](screenshot.png)` 在标题下方）。
2.  **部署**：由于这是单文件 HTML，您可以直接将其上传到 GitHub Pages，立刻拥有一个在线演示地址。

**需要我教您如何把它部署到 GitHub Pages 上生成一个在线链接吗？**

```
**作者**：Mentat  
**项目地址**：[[GitHub Repository URL](https://github.com/Mentaturan/building-boundary-json-drawer)]  
**联系方式**：uran0831@qq.com
