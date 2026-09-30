<div align="center">

# 🤖 awesome-agent-skills

[![Awesome](https://cdn.jsdelivr.net/gh/sindresorhus/awesome@main/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![GitHub Stars](https://img.shields.io/github/stars/Futao-Augenstern/awesome-agent-skills?style=social)](https://github.com/Futao-Augenstern/awesome-agent-skills/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Futao-Augenstern/awesome-agent-skills?style=social)](https://github.com/Futao-Augenstern/awesome-agent-skills/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![Last Commit](https://img.shields.io/github/last-commit/Futao-Augenstern/awesome-agent-skills)](https://github.com/Futao-Augenstern/awesome-agent-skills/commits)

**精选 AI Agent 技能合集 · 即插即用的 MCP 服务器大全**

> 一个精心策划的 AI Agent Skills 生态系统合集，帮助你快速构建强大的智能体。

[English](README.en.md) · [中文](README.md) · [提交技能](https://github.com/Futao-Augenstern/awesome-agent-skills/issues/new?assignees=&labels=&projects=&template=skill-submission.md&title=%5BSkill%5D+)

</div>

---

## 📋 目录

- [🔥 什么是 Agent Skills？](#-什么是-agent-skills)
- [⚡ 快速开始](#-快速开始)
- [🏆 精选 MCP 服务器](#-精选-mcp-服务器)
  - [开发工具](#开发工具)
  - [生产力](#生产力)
  - [数据与搜索](#数据与搜索)
  - [内容创作](#内容创作)
  - [云服务与 DevOps](#云服务与-devops)
  - [生活助手](#生活助手)
- [🛠️ Agent 框架集成](#️-agent-框架集成)
- [📚 学习资源](#-学习资源)
- [🎁 现成 Agent Skills 精选](#-现成-agent-skills-精选)
- [🤝 贡献指南](#-贡献指南)
- [⭐ Star 历史](#-star-历史)

---

## 🔥 什么是 Agent Skills？

**Agent Skills** 是 AI 智能体（Agent）的"能力插件"——就像给你的 AI 助理装上各种专业工具。通过 [MCP（Model Context Protocol）](https://modelcontextprotocol.io/) 标准，Agent 可以调用外部工具、访问数据、执行操作，从"能聊天"变成"能干活"。

```
┌─────────────────────────────────────────────────┐
│                   AI Agent                       │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐         │
│  │ 搜索技能 │  │ 编码技能 │  │ 邮件技能 │  ...   │
│  └────┬────┘  └────┬────┘  └────┬────┘         │
│       │            │            │               │
│  ┌────┴────────────┴────────────┴────┐          │
│  │     MCP (Model Context Protocol)   │         │
│  └─────────────────┬──────────────────┘         │
└────────────────────┼────────────────────────────┘
                     │
         ┌───────────┴───────────┐
         │   外部工具 / 数据源    │
         └───────────────────────┘
```

**为什么需要这个仓库？**
- ✅ **节省时间**：不用自己找工具，精选优质 MCP 服务器一键接入
- ✅ **分类清晰**：按场景分类，快速找到所需技能
- ✅ **质量保证**：每个收录项目都经过基本质量审核
- ✅ **持续更新**：紧跟 Agent 生态发展，每周更新

---

## ⚡ 快速开始

### 方式一：使用 Claude Desktop（推荐）

```bash
# 1. 安装 MCP 服务器（以 filesystem 为例）
npx -y @modelcontextprotocol/server-filesystem /path/to/workspace

# 2. 配置 claude_desktop_config.json
# 将服务器配置添加到你的配置文件中
```

### 方式二：在代码中使用

```python
# 使用 LangChain + MCP（以 filesystem 为例）
from langchain_mcp import MCPToolkit

toolkit = MCPToolkit.from_command(
    command="npx",
    args=["-y", "@modelcontextprotocol/server-filesystem", "/path/to/workspace"]
)
tools = toolkit.get_tools()
# GitHub 官方 MCP 现为远程服务器：https://api.githubcopilot.com/mcp/
```

### 方式三：浏览本仓库

直接浏览下方分类，找到你需要的技能，点击链接查看详情和安装方法。

---

## 🏆 精选 MCP 服务器

### 开发工具

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [GitHub MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/github) | 管理 GitHub 仓库、Issue、PR、代码搜索 | MCP 官方 | ⭐⭐⭐⭐⭐ |
| [GitLab MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/gitlab) | GitLab 仓库管理、CI/CD 操作 | MCP 官方 | ⭐⭐⭐⭐ |
| [Neon MCP (PostgreSQL)](https://github.com/neondatabase/mcp-server-neon) | 直接查询 PostgreSQL 数据库，智能 SQL 生成 | Neon 官方 | ⭐⭐⭐⭐⭐ |
| [SQLite MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) | 本地 SQLite 数据库查询与管理 | MCP 官方 | ⭐⭐⭐⭐ |
| [Docker MCP](https://github.com/ckreiling/mcp-server-docker) | 管理 Docker 容器、镜像、compose | 社区 | ⭐⭐⭐ |
| [Sentry MCP](https://github.com/getsentry/sentry-mcp) | Sentry 错误监控与分析 | Sentry 官方 | ⭐⭐⭐⭐ |

### 生产力

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [Gmail MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/gmail) | 收发邮件、搜索、标签管理 | MCP 官方 | ⭐⭐⭐⭐⭐ |
| [Google Calendar MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/google-calendar) | 日历事件管理、日程安排 | MCP 官方 | ⭐⭐⭐⭐ |
| [Notion MCP](https://developers.notion.com/docs/mcp) | Notion 页面读写、数据库查询（官方远程 MCP） | Notion 官方 | ⭐⭐⭐⭐⭐ |
| [Slack MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) | 发送消息、搜索、频道管理 | MCP 官方 | ⭐⭐⭐⭐ |
| [Linear MCP](https://linear.app/docs/mcp) | Linear 项目管理、Issue 追踪（官方远程 MCP） | Linear 官方 | ⭐⭐⭐⭐ |
| [Todoist MCP](https://github.com/Doist/todoist-mcp) | 任务管理、待办事项同步 | Doist 官方 | ⭐⭐⭐⭐ |

### 数据与搜索

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [Brave Search MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) | Brave 搜索引擎 API 集成 | MCP 官方 | ⭐⭐⭐⭐⭐ |
| [Tavily MCP](https://github.com/tavily-ai/tavily-mcp) | 专为 AI Agent 优化的搜索引擎 | Tavily 官方 | ⭐⭐⭐⭐⭐ |
| [Perplexity MCP](https://github.com/perplexityai/modelcontextprotocol) | Perplexity AI 搜索与问答 | Perplexity 官方 | ⭐⭐⭐⭐ |
| [Pinecone MCP](https://github.com/pinecone-io/pinecone-mcp) | Pinecone 向量数据库操作 | Pinecone 官方 | ⭐⭐⭐⭐ |
| [Wolfram Alpha MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/wolfram-alpha) | 数学计算、科学数据查询 | MCP 官方 | ⭐⭐⭐⭐ |
| [Weather MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/weather) | 全球天气预报查询 | MCP 官方 | ⭐⭐⭐ |

### 内容创作

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [Figma MCP](https://github.com/figma/mcp-server-guide) | Figma 设计文件读取与分析 | Figma 官方 | ⭐⭐⭐⭐⭐ |
| [Canva MCP](https://www.canva.dev/docs/apps/mcp/) | Canva 设计自动化与模板（远程 MCP） | Canva 官方 | ⭐⭐⭐⭐ |
| [YouTube MCP](https://github.com/kevinwatt/yt-dlp-mcp) | YouTube 视频搜索、字幕提取 | 社区 | ⭐⭐⭐⭐ |
| [Markdown MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/markdown) | Markdown 文件读写与处理 | MCP 官方 | ⭐⭐⭐⭐ |
| [MarkItDown MCP](https://github.com/microsoft/markitdown) | PDF、Office、图片等文件转 Markdown（支持 MCP） | Microsoft 官方 | ⭐⭐⭐⭐⭐ |

### 云服务与 DevOps

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [AWS MCP](https://github.com/awslabs/mcp) | AWS 服务操作（EC2、S3、Lambda 等） | AWS 官方 | ⭐⭐⭐⭐⭐ |
| [GCP MCP](https://github.com/google/mcp) | Google Cloud 平台服务集成 | Google 官方 | ⭐⭐⭐⭐ |
| [Vercel MCP](https://vercel.com/docs/mcp) | Vercel 部署、项目管理（远程 MCP） | Vercel 官方 | ⭐⭐⭐⭐ |
| [Netlify MCP](https://github.com/netlify/netlify-mcp) | Netlify 部署与站点管理 | Netlify 官方 | ⭐⭐⭐⭐ |
| [Kubernetes MCP](https://github.com/flux159/mcp-server-kubernetes) | K8s 集群管理与资源操作 | 社区 | ⭐⭐⭐⭐ |
| [Terraform MCP](https://github.com/hashicorp/terraform-mcp-server) | Terraform 基础设施即代码 | HashiCorp 官方 | ⭐⭐⭐⭐ |

### 生活助手

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [Spotify MCP](https://github.com/varunneal/spotify-mcp) | Spotify 音乐播放、播放列表管理 | 社区 | ⭐⭐⭐⭐ |
| [Strava MCP](https://github.com/r-huijts/strava-mcp) | Strava 运动数据分析 | 社区 | ⭐⭐⭐⭐ |
| [Shopping List MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/shopping-list) | 购物清单管理 | MCP 官方 | ⭐⭐ |
| [Reminder MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/reminders) | 提醒事项管理 | MCP 官方 | ⭐⭐⭐ |

> 💡 **更多 MCP 服务器**请查看 [mcp-servers/](mcp-servers/) 目录下的详细分类。

---

## 🛠️ Agent 框架集成

| 框架 | MCP 支持 | 流行度 | 适用场景 |
|------|---------|--------|---------|
| [Claude Code](https://www.anthropic.com/claude-code) | ✅ 原生支持 | ⭐⭐⭐⭐⭐ | 代码开发、终端操作 |
| [LangChain / LangGraph](https://www.langchain.com/) | ✅ `langchain-mcp` | ⭐⭐⭐⭐⭐ | 复杂 Agent 工作流、生产部署 |
| [CrewAI](https://www.crewai.com/) | ✅ MCP 工具集成 | ⭐⭐⭐⭐ | 多智能体协作 |
| [AutoGPT](https://agpt.co/) | ✅ 插件系统 | ⭐⭐⭐⭐ | 自主 Agent |
| [Dify](https://dify.ai/) | ✅ 工具节点 | ⭐⭐⭐⭐⭐ | 可视化编排、企业级应用 |
| [OpenClaw](https://github.com/openclaw/openclaw) | ✅ 原生支持 | ⭐⭐⭐⭐⭐ | 全平台 Agent 框架 |
| [superpowers](https://github.com/obra/superpowers) | ✅ Agent Harness | ⭐⭐⭐⭐⭐ | 轻量级 Agent 框架 |
| [CopilotKit](https://github.com/CopilotKit/CopilotKit) | ✅ MCP 支持 | ⭐⭐⭐⭐ | 前端 AI Copilot |

---

## 📚 学习资源

### 官方文档
- [MCP 官方文档](https://modelcontextprotocol.io/) - Model Context Protocol 官方指南
- [MCP GitHub 仓库](https://github.com/modelcontextprotocol/servers) - 官方服务器集合
- [Anthropic MCP 教程](https://docs.anthropic.com/en/docs/agents-and-tools/model-context-protocol) - Claude MCP 集成指南

### 入门教程
- [MCP 官方快速入门](https://modelcontextprotocol.io/quickstart) - 5 分钟构建并连接你的第一个 MCP 服务器
- [从零构建 MCP 服务器](https://modelcontextprotocol.io/docs/develop/build-server) - MCP 官方服务器构建指南
- [Agent Skills 设计模式与最佳实践](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) - Anthropic 官方工程博客

### 深度文章
- [Introducing the Model Context Protocol](https://www.anthropic.com/news/model-context-protocol) - Anthropic 官方发布公告
- [Agent 工具调用与协议演进时间线](https://hidekazu-konishi.com/entry/tool_use_and_agent_protocol_history_and_timeline.html) - 从早期工具调用到 MCP 的完整历史
- [MCP 与 Function Calling 对比](https://qveris.ai/zh-cn/guides/mcp-vs-function-calling) - Agent 工具生态演进深度分析

---

## 🎁 现成 Agent Skills 精选

你想找**别人已经做好、可直接拿来用**的 Agent Skills？不必自己从零写。下面是最值得关注的官方与社区来源：

### 📚 官方与标准
| 资源 | 说明 |
|------|------|
| [Anthropic Skills 官方仓库](https://github.com/anthropics/skills) | 官方技能库（docx/pdf/pptx/xlsx、webapp-testing、canvas-design、brand-guidelines 等） |
| [Agent Skills 开放标准](https://agentskills.io/) | `SKILL.md` 规范、规格与客户端清单 |
| [Claude Skills 文档](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) | 官方技能总览与预置技能说明 |

### 🧩 技能框架与综合集合
| 名称 | 说明 |
|------|------|
| [obra/superpowers](https://github.com/obra/superpowers) | 完整软件开发方法论 + 可组合技能（规划→TDD→子代理→代码审查） |
| [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | Claude 现成技能精选合集 |
| [ningzimu/awesome-skills](https://github.com/ningzimu/awesome-skills) | 社区技能聚合库，按领域分类 |

### ⚙️ 快速安装（Claude Code）
```bash
/plugin marketplace add anthropics/skills
/plugin install document-skills@anthropic-agent-skills   # docx/pdf/pptx/xlsx
```

> 📁 完整分类目录（官方技能、框架集合、技能市场、支持 Skills 的运行时）见 [skills/](skills/) 目录。

---

## 🤝 贡献指南

我们欢迎所有形式的贡献！无论是添加新的 MCP 服务器、改进分类、修复错误还是完善文档。

### 如何贡献

1. **提交新技能**：通过 [Issue 模板](https://github.com/Futao-Augenstern/awesome-agent-skills/issues/new?assignees=&labels=&projects=&template=skill-submission.md&title=%5BSkill%5D+) 提交
2. **直接 PR**：Fork 本仓库，修改后提交 Pull Request
3. **讨论建议**：在 [Issues](https://github.com/Futao-Augenstern/awesome-agent-skills/issues) 中分享想法

### 收录标准

- ✅ 项目有明确的 README 和使用说明
- ✅ 项目有一定的维护活跃度（近 3 个月有更新）
- ✅ 项目有明确的开源许可证
- ✅ 功能真实可用，不是玩具项目
- ✅ 代码质量有基本保证

### 贡献者

感谢所有为这个项目做出贡献的人！

<a href="https://github.com/Futao-Augenstern/awesome-agent-skills/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Futao-Augenstern/awesome-agent-skills" />
</a>

---

## ⭐ Star 历史

如果你觉得这个项目有帮助，请给一个 ⭐ Star 支持！

[![Star History Chart](https://api.star-history.com/svg?repos=Futao-Augenstern/awesome-agent-skills&type=Date)](https://star-history.com/#Futao-Augenstern/awesome-agent-skills&Date)

---

<div align="center">

**Made with ❤️ by the AI Agent Community**

[给个 Star ⭐](https://github.com/Futao-Augenstern/awesome-agent-skills) · [提交 Issue](https://github.com/Futao-Augenstern/awesome-agent-skills/issues)

</div>
