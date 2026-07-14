# Prompt 变量填充器 Pro Max (V30 浴火重生版)

<p align="center">  <img src="https://img.shields.io/badge/Version-3.0-emerald?style=flat-square" alt="Version">  <img src="https://img.shields.io/badge/TailwindCSS-v3-blue?style=flat-square" alt="Tailwind">  <img src="https://img.shields.io/badge/License-MIT-purple?style=flat-square" alt="License"></p>

**Prompt 变量填充器 Pro Max** 是一款专为 AI 提示词（Prompt）创作者与高频使用者设计的**单文件网页端效率工具**。它无需任何复杂的后端环境，直接运行在浏览器中。

通过直观的交互界面，它可以自动解析提示词模板中的 `{变量}` 并生成网格化输入框，同时支持**本地文件夹深度读取（双向同步与无痕刷新）**以及**利用大语言模型（LLM）一键智能提取、分组及分析变量**。

* * *

## ✨ 核心特性

* **⚡ 即时变量检测与动态网格**
  * 自动抓取模板中所有的 `{变量名}`。
  * 自动生成自适应高度的输入卡片网格，支持一键移除变量恢复原文。
  * 双栏同步滚动，修改变量实时预览最终结果。
* **📂 本地 Prompt 库深度打通 (FileSystem API)**
  * 支持选择本地文件夹，构建高还原度的文件夹目录树。
  * **双重读写机制**：支持直接无痕刷新本地改动，支持右键直接永久删除本地物理文件（兼容不支持 FileSystem API 的旧版浏览器）。
* **🤖 AI 智能变量拆解 (LLM 语义提取)**
  * 集成 LLM 接口，支持自定义 API Base URL、模型与密钥。
  * **三种提取颗粒度**：粗粒度（大概念）、中等粒度（均衡模式）、细颗粒度（高精拆解修饰词/光影参数等）。
  * 提供强大的**智能提取审查弹窗**，以分组卡片形式呈现 AI 建议，支持自主勾选或放弃更改后一键应用。
* **🎨 高级交互与无缝剪贴**
  * **划词设为变量**：在模板中鼠标选中任意词汇，悬浮工具栏一键转为自定义变量。
  * **反向聚焦定位**：在最终结果中点击任何高亮变量，页面将平滑滚动并自动聚焦、全选对应的变量控制台输入框。
  * **智能导出**：支持保留 `{变量}` 格式导出为 `.md`、`.txt` 或 `.json`，文件名自动根据 AI 提取的元数据格式化（分类-摘要-日期）。

* * *

## 🚀 快速开始

### 方式一：直接运行（推荐）

本项目为**纯单文件 HTML/JS 应用**。

1. 下载仓库中的 `index.html`。
2. 双击在任意现代浏览器（推荐 Chrome / Edge）中打开即可使用。

### 方式二：本地部署/静态托管

您可以将其部署到 GitHub Pages、Vercel 或 Netlify 上：

```bash

# 无需构建，直接托管 index.html 即可

🛠️ AI 配置指南
若要启用 AI 提取 功能：

点击右上角的 API 配置。

输入您的 API 凭据：

Base URL：例如 https://api.openai.com/v1 或国内大模型中转地址。

Model：例如 gpt-4o-mini、deepseek-chat 等。

API Key：您的秘钥。

点击保存（API 凭据将长久保存在您的浏览器本地缓存 localStorage 中，数据安全不上传）。

📦 文件夹导入兼容说明
本项目使用现代浏览器的 File System Access API：

在 Chrome / Edge / Opera 等 Blink 内核浏览器中，您可以直接导入本地文件夹，享受物理级的无痕刷新、无痛读取与右键永久删除功能。

在旧版浏览器或不兼容的运行环境中，系统会自动降级为 兼容文件树读取模式（仅提供读取和渲染，无法直接修改/删除本地硬盘文件）。

📄 开源协议
本项目基于 MIT 协议开源。欢迎提交 Issue 或 Pull Request 来共同完善这个工具！


---

### 💡 为什么这样设计？
1. **突出技术栈与特色**：重点指出了 File System Access API 的应用以及降级方案（这在前端单页面应用中是非常高级的 feature）。
2. **极简部署说明**：因为是单文件，强调了“双击即用”和“零服务器依赖”的纯前端优势。
3. **结构化与排版**：使用符合规范的徽章（Badges）和高可读性的列表，保证在 GitHub 仓库主页能给访问者
