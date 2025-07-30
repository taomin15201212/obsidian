Universal AI Agent Framework
https://github.com/bmadcode/BMAD-METHOD


BMad-Method 是一个面向敏捷 AI 驱动开发的通用 AI Agent 框架，支持软件开发、娱乐、创意写作、商业策略、个人健康等多种领域。其核心特色和使用方法总结如下：

1. 两大创新点
    
    - Agentic Planning（代理规划）：专用的 AI 角色（如分析师、产品经理、架构师）与用户协作，生成详细一致的 PRD（产品需求文档）和架构文档，解决传统 AI 辅助开发中规划不一致的问题。
    - Context-Engineered Development（上下文工程开发）：Scrum Master（敏捷教练）Agent 将详细规划转化为开发故事，里面包含实现细节、架构指导等，供开发 Agent 直接使用，避免上下文丢失。
2. 快速上手
    
    - 只需一条命令即可安装或升级：
        
        ```
        npx bmad-method install
        # 或已安装可用 git pull
        npm run install:bmad
        ```
        
        这会自动检测、更新和备份你的自定义文件，并保留项目配置。
    - 前提条件：需要 Node.js v20 及以上。
    - 推荐最快体验方式：下载或克隆官方提供的 full stack 团队文件，上传到 Gemini Gem 或 CustomGPT，配置指令后即可开始对话和规划。
3. 主要流程
    
    - 规划阶段：通过 Web UI 与分析师、PM、架构师等 Agent 生成 PRD 和架构文档。
    - 开发阶段：Scrum Master 将文档拆分为开发故事，Dev 和 QA Agent 按故事推进开发与测试，所有上下文详细传递。
    - 切换到 IDE 后继续开发实现。
4. 代码工具
    
    - 自带代码库扁平化工具，可将整个项目聚合为单一 XML 文件，便于 AI 理解和分析项目结构，支持 .gitignore 过滤、二进制文件自动排除等功能。
5. 扩展与非技术领域
    
    - 支持 Expansion Packs（扩展包），可用于创意写作、商业、健康、教育等领域。用户也可自定义扩展包，添加专属 AI Agent。
6. 文档与社区
    
    - 提供完整用户指南、架构文档、扩展包开发指南等，支持 Discord 社区和 GitHub issue 反馈。

简而言之，BMad-Method 通过多 Agent 协作和上下文工程，极大提升了 AI 辅助开发的规范性和效率，适合希望深度利用 AI 进行敏捷开发和跨领域创新的团队和个人。