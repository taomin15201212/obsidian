# Obsidian 知识库

一个基于 Obsidian 的个人知识管理系统，涵盖 AI 工具、全栈技术、运维实践和自媒体内容。

## 概述

本仓库是一个集中化的知识库，用于收集、整理和同步多个领域的学习笔记和实践经验。通过与 Claude Code 和 Obsidian 的集成，实现智能化的知识管理和 AI 辅助工作流。

## 仓库结构

```
obsidian/
├── AI/                          # AI 工具、提示词和工作流
│   ├── Claude Code 安装.md
│   ├── Claude Code 实战 30 天干货速读.md
│   ├── AI辅助编程计划.md
│   ├── AI知识共享自媒体方案.md
│   ├── MCP.json.md
│   ├── BMad-Method.md
│   └── ...
├── 全栈技术/                     # 编程语言和开发框架
│   ├── Vue.md
│   ├── React、ReactNative.md
│   ├── Angular.md
│   ├── NodeJs.md
│   ├── nestjs.md
│   ├── TypeScript.md
│   ├── ES6.md
│   ├── Html5+css3.md
│   ├── Git 使用.md
│   ├── mysql.md
│   ├── MongoDB 启动.md
│   ├── Redis.md
│   ├── python.md
│   ├── 前端学习进价.md
│   └── ...
├── 工具/                         # 开发工具和生产力
│   ├── IntelliJ IDEA 快捷键指南（Windows & Linux）.md
│   ├── Visual Studio Code 快捷键指南（Windows版）.md
│   ├── Delivery 技巧.md
│   └── Google analytics.md
├── 运维/                         # DevOps 和基础设施
│   ├── Docker.md
│   ├── Linux.md
│   ├── WSL.md
│   ├── Cloudflare.md
│   ├── gitea.md
│   └── iTerm2.md
├── 自媒体/                       # 内容创作和自媒体运营
│   ├── Copilot 能为你做什么.md
│   ├── 短视频变现渠道.md
│   └── Music.md
├── MAC/                          # macOS 工具和配置
├── .claude/                      # Claude Code 配置和自定义技能
│   ├── obsidian-markdown/        # Obsidian Markdown 处理技能
│   ├── obsidian-bases/           # 知识库操作技能
│   ├── json-canvas/              # Canvas 可视化工具技能
│   ├── commands/                 # 自定义命令
│   └── sessions/                 # 会话记录
└── .obsidian/                    # Obsidian 配置文件
```

## 主要特性

- **Obsidian 原生支持**：完整的 Obsidian 仓库配置，支持双链笔记、图谱视图等特性
- **Claude Code 深度集成**：自定义技能实现 AI 辅助的知识管理和内容生成
- **全中文内容**：所有笔记均为中文，便于国内开发者阅读和学习
- **多领域覆盖**：从前端开发到 AI 工具，从运维实践到自媒体运营

## 快速开始

1. **克隆仓库**
   ```bash
   git clone <仓库地址> /Users/keen/git/obsidian
   ```

2. **在 Obsidian 中打开**
   - 打开 Obsidian 应用
   - 选择「打开本地仓库」
   - 选择 `/Users/keen/git/obsidian` 目录

3. **配置 Claude Code**
   - Claude Code 技能位于 `.claude/` 目录
   - 包含 Markdown 处理、知识库操作、Canvas 可视化等技能

## Claude Code 技能

本仓库包含以下自定义 Claude Code 技能：

| 技能 | 描述 |
|------|------|
| `obsidian-markdown` | Obsidian 格式的 Markdown 处理，支持 Wiki 链接、标签等 |
| `obsidian-bases` | 知识库操作，包括笔记查询、整理和关联 |
| `json-canvas` | Canvas 画布的创建和可视化 |

## 内容分类

### AI 与编程助手
- Claude Code 安装与使用技巧
- AI 辅助编程方法论（BMad-Method）
- AI 知识共享与自媒体方案
- MCP（模型上下文协议）配置
- Vibe SaaS 开发模式

### 全栈技术栈
- **前端框架**：Vue、React、React Native、Angular、UniApp
- **后端技术**：Node.js、NestJS
- **编程语言**：TypeScript、ES6、Python
- **基础技术**：HTML5 + CSS3
- **数据库**：MySQL、MongoDB、Redis
- **版本控制**：Git 使用指南
- **构建工具**：Gulp、npm 私服搭建

### 开发工具
- IntelliJ IDEA 快捷键（Windows & Linux）
- Visual Studio Code 快捷键（Windows）
- Delivery 技巧与最佳实践
- Google Analytics 使用

### 运维与基础设施
- Docker 容器化技术
- Linux 系统管理
- WSL（Windows Subsystem for Linux）
- Cloudflare 服务配置
- Gitea 私有代码托管
- iTerm2 终端配置

### 自媒体与内容创作
- GitHub Copilot 功能介绍
- 短视频变现渠道分析
- 音乐创作相关

## 使用建议

1. **日常学习**：使用 Obsidian 的每日笔记功能记录学习心得
2. **知识关联**：利用 Obsidian 的双链功能建立笔记间的关联
3. **AI 辅助**：通过 Claude Code 技能实现智能化内容整理和生成
4. **定期同步**：使用 Git 定期提交和同步知识库更新

## 许可证

个人知识库 - 仅供学习和参考使用。

---

*最后更新：2026-03-01*
