# Clean Infinite Ask for Windsurf/Cursor

> **开发者Anna QQ群: 1076321843**  
> **GitHub开源**：[https://github.com/crispvibe/windsurf-infinite-ask](https://github.com/crispvibe/windsurf-infinite-ask)

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Version](https://img.shields.io/badge/version-1.0.0-green.svg)

**Clean Infinite Ask** 是一个为 Windsurf 和 Cursor 设计的开源插件，旨在通过 MCP (Model Context Protocol) 机制实现"无限对话"体验。

与市面上的同类收费插件不同，本项目**完全开源、免费、无混淆、无联网验证**，并在本地运行，确保你的数据安全。

---

## 核心特性

- **无限续杯**：通过 MCP 工具介入，让 AI 在结束任务前自动暂停并询问，从而将多次对话合并为单次计费上下文。
- **纯净安全**：
  - **Zero Network**: 移除所有联网鉴权和数据上报代码。
  - **Open Source**: 核心逻辑透明，代码未混淆，可随意审计。
- **开箱即用**：
  - **Native Popup**: 使用系统原生弹窗 (PowerShell / AppleScript)，无需安装额外依赖。
  - **Auto Config**: 安装插件后自动配置 MCP 服务，由插件托管进程。
  - **Auto Rules**: 自动向工作区注入 `.windsurfrules` 规则文件。
- **多平台支持**：完美支持 Windows 和 macOS。

## 安装指南

### 方法 1: 使用 Release 安装包 (推荐)
1. 下载最新发布的 `.vsix` 文件。
2. 打开 Windsurf / VSCode。
3. 进入 **Extensions** 面板 -> 点击右上角 **...** -> 选择 **Install from VSIX...**。
4. 选择下载的文件进行安装。
5. **重启 IDE**。

### 方法 2: 源码编译
```bash
git clone https://github.com/crispvibe/windsurf-clean-infinite-ask.git
cd windsurf-clean-infinite-ask
npm install
npm run compile
npx vsce package
```

## 📖 使用方法

1. **打开项目**：在 IDE 中打开任意一个文件夹（必须打开文件夹，不能是空窗口）。
2. **确认配置**：
   - 检查项目根目录是否生成了 `.windsurfrules` 文件。
   - 检查 MCP 面板中 `infinite_ask` 服务是否为绿色 (Connected)。
3. **快速验证**：
   - 直接发送对话：**"测试 infinite_ask MCP 是否可用"**
   - AI 会立即调用工具，此时你的屏幕中央应该会自动弹出一个原生对话框。
   - 点击 **[继续执行]**，验证链路通畅。
4. **日常使用**：
   - 正常布置任务即可。当任务完成后，系统会自动拦截结束动作并弹窗。
   - 只要不点击"结束对话"，AI 就会一直维持当前上下文，实现"无限续杯"。

## 免责声明与许可协议 (Disclaimer & License)

### 免责声明
1. **仅供学习**：本项目仅供技术研究和学习交流使用，旨在探索 MCP 协议的应用潜力。
2. **风险自负**：使用本项目产生的一切后果（包括但不限于账号风控、服务限制、封禁等）由使用者自行承担，开发者不承担任何法律及连带责任。
3. **安全提示**：虽然本项目移除了原版的联网验证代码，但用户仍需自行评估使用第三方插件的风险。

### 禁止商用
本代码仓库及发行包遵循 MIT License，但**附加以下严格限制**：
1. **严禁商用**：任何个人或组织不得将本项目代码、编译产物（.vsix）或其衍生品用于商业盈利活动。
2. **严禁二次销售**：严禁将本免费开源插件进行二次打包、混淆后进行收费销售或作为引流工具。
3. **原作者权利**：本项目致力于维护用户的数据安全与知情权，如有侵权请联系删除。

## 交流与反馈

欢迎加入我们的交流群，获取更新或反馈问题（请注明来自 GitHub）：

- **QQ群**: 1076321843

---
*Made with ❤️ by Open Source Community*
