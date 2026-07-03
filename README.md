<div align="center">

# 🤖 awesome-agent-skills

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![GitHub Stars](https://img.shields.io/github/stars/yourusername/awesome-agent-skills?style=social)](https://github.com/yourusername/awesome-agent-skills/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/yourusername/awesome-agent-skills?style=social)](https://github.com/yourusername/awesome-agent-skills/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
[![Last Update](https://img.shields.io/badge/Last%20Update-July%202026-blue)]()

**精选 AI Agent 技能合集 · 即插即用的 MCP 服务器大全**

> 一个精心策划的 AI Agent Skills 生态系统合集，帮助你快速构建强大的智能体。

[English](README.en.md) · [中文](README.md) · [提交技能](https://github.com/yourusername/awesome-agent-skills/issues/new?assignees=&labels=&projects=&template=skill-submission.md&title=%5BSkill%5D+)

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
- [🎯 精选 Skill 模板](#-精选-skill-模板)
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
npx @modelcontextprotocol/server-filesystem /path/to/workspace

# 2. 配置 claude_desktop_config.json
# 将服务器配置添加到你的配置文件中
```

### 方式二：在代码中使用

```python
# 使用 LangChain + MCP
from langchain_mcp import MCPToolkit

toolkit = MCPToolkit.from_command(
    command="npx",
    args=["-y", "@modelcontextprotocol/server-github"]
)
tools = toolkit.get_tools()
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
| [PostgreSQL MCP](https://github.com/neondatabase/mcp-server-postgres) | 直接查询 PostgreSQL 数据库，智能 SQL 生成 | Neon | ⭐⭐⭐⭐⭐ |
| [SQLite MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) | 本地 SQLite 数据库查询与管理 | MCP 官方 | ⭐⭐⭐⭐ |
| [Docker MCP](https://github.com/ckreiling/mcp-server-docker) | 管理 Docker 容器、镜像、compose | 社区 | ⭐⭐⭐ |
| [Sentry MCP](https://github.com/getsentry/mcp-server-sentry) | Sentry 错误监控与分析 | Sentry 官方 | ⭐⭐⭐⭐ |

### 生产力

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [Gmail MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/gmail) | 收发邮件、搜索、标签管理 | MCP 官方 | ⭐⭐⭐⭐⭐ |
| [Google Calendar MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/google-calendar) | 日历事件管理、日程安排 | MCP 官方 | ⭐⭐⭐⭐ |
| [Notion MCP](https://github.com/metalbear-co/mcp-server-notion) | Notion 页面读写、数据库查询 | 社区 | ⭐⭐⭐⭐⭐ |
| [Slack MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) | 发送消息、搜索、频道管理 | MCP 官方 | ⭐⭐⭐⭐ |
| [Linear MCP](https://github.com/linear-ai/mcp-linear) | Linear 项目管理、Issue 追踪 | Linear 官方 | ⭐⭐⭐⭐ |
| [Todoist MCP](https://github.com/saisandeep998/mcp-todoist-server) | 任务管理、待办事项同步 | 社区 | ⭐⭐⭐ |

### 数据与搜索

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [Brave Search MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) | Brave 搜索引擎 API 集成 | MCP 官方 | ⭐⭐⭐⭐⭐ |
| [Tavily MCP](https://github.com/tavily-ai/mcp-tavily) | 专为 AI Agent 优化的搜索引擎 | Tavily 官方 | ⭐⭐⭐⭐⭐ |
| [Perplexity MCP](https://github.com/leopiccionia/mcp-perplexity) | Perplexity AI 搜索与问答 | 社区 | ⭐⭐⭐⭐ |
| [Pinecone MCP](https://github.com/pinecone-io/mcp-pinecone) | Pinecone 向量数据库操作 | Pinecone 官方 | ⭐⭐⭐⭐ |
| [Wolfram Alpha MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/wolfram-alpha) | 数学计算、科学数据查询 | MCP 官方 | ⭐⭐⭐⭐ |
| [Weather MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/weather) | 全球天气预报查询 | MCP 官方 | ⭐⭐⭐ |

### 内容创作

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [Figma MCP](https://github.com/figma/mcp-figma) | Figma 设计文件读取与分析 | Figma 官方 | ⭐⭐⭐⭐⭐ |
| [Canva MCP](https://github.com/canva/mcp-canva) | Canva 设计自动化与模板 | Canva 官方 | ⭐⭐⭐⭐ |
| [YouTube MCP](https://github.com/miraclesteven/mcp-youtube) | YouTube 视频搜索、字幕提取 | 社区 | ⭐⭐⭐ |
| [Markdown MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/markdown) | Markdown 文件读写与处理 | MCP 官方 | ⭐⭐⭐⭐ |
| [PDF MCP](https://github.com/rowickib/mcp-pdf-tools) | PDF 读取、解析、文本提取 | 社区 | ⭐⭐⭐ |

### 云服务与 DevOps

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [AWS MCP](https://github.com/awslabs/mcp-server-aws) | AWS 服务操作（EC2、S3、Lambda 等） | AWS 官方 | ⭐⭐⭐⭐⭐ |
| [GCP MCP](https://github.com/googleapis/mcp-google-cloud) | Google Cloud 平台服务集成 | Google 官方 | ⭐⭐⭐⭐ |
| [Vercel MCP](https://github.com/vercel/mcp-vercel) | Vercel 部署、项目管理 | Vercel 官方 | ⭐⭐⭐⭐ |
| [Netlify MCP](https://github.com/netlify/mcp-netlify) | Netlify 部署与站点管理 | Netlify 官方 | ⭐⭐⭐⭐ |
| [Kubernetes MCP](https://github.com/everettraven/mcp-k8s) | K8s 集群管理与资源操作 | 社区 | ⭐⭐⭐⭐ |
| [Terraform MCP](https://github.com/weagle08/mcp-terraform) | Terraform 基础设施即代码 | 社区 | ⭐⭐⭐ |

### 生活助手

| 名称 | 描述 | 平台/框架 | ⭐ |
|------|------|-----------|-----|
| [Spotify MCP](https://github.com/RowanAberdeen/mcp-spotify) | Spotify 音乐播放、播放列表管理 | 社区 | ⭐⭐⭐⭐ |
| [Strava MCP](https://github.com/mmazzarolo/mcp-strava) | Strava 运动数据分析 | 社区 | ⭐⭐⭐ |
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
| [superpowers](https://github.com/evilfactorylabs/superpowers) | ✅ Agent Harness | ⭐⭐⭐⭐ | 轻量级 Agent 框架 |
| [CopilotKit](https://github.com/CopilotKit/CopilotKit) | ✅ MCP 支持 | ⭐⭐⭐⭐ | 前端 AI Copilot |

---

## 📚 学习资源

### 官方文档
- [MCP 官方文档](https://modelcontextprotocol.io/) - Model Context Protocol 官方指南
- [MCP GitHub 仓库](https://github.com/modelcontextprotocol/servers) - 官方服务器集合
- [Anthropic MCP 教程](https://docs.anthropic.com/en/docs/agents-and-tools/model-context-protocol) - Claude MCP 集成指南

### 入门教程
- [MCP 快速上手：5 分钟给 Claude 装工具](https://example.com/mcp-quickstart)
- [从零构建你的第一个 MCP 服务器](https://example.com/build-mcp-server)
- [Agent Skills 设计模式与最佳实践](https://example.com/agent-skills-patterns)

### 深度文章
- [为什么 MCP 是 AI Agent 的 App Store？](https://example.com/mcp-app-store)
- [Agent 工具调用的过去、现在与未来](https://example.com/agent-tools-history)
- [从 Function Calling 到 MCP：Agent 工具生态演进](https://example.com/function-calling-to-mcp)

---

## 🎯 精选 Skill 模板

我们提供了一些即用型 Skill 模板，复制即可使用：

### 📝 代码审查助手
> 自动审查 PR，检查代码风格、潜在 bug、性能问题
>
> **所需 MCP**：GitHub、Git
> **[查看模板 →](skills/code-reviewer.md)**

### 📰 研究助理
> 自动搜索学术论文、总结研究进展、生成文献综述
>
> **所需 MCP**：Tavily/Brave Search、Arxiv
> **[查看模板 →](skills/research-assistant.md)**

### 📧 邮箱管家
> 智能分类邮件、自动回复常见问题、日程提醒
>
> **所需 MCP**：Gmail、Google Calendar
> **[查看模板 →](skills/email-assistant.md)**

### 🌐 全栈开发助手
> 前后端开发 + 数据库设计 + 部署上线一条龙
>
> **所需 MCP**：GitHub、PostgreSQL、Vercel/AWS
> **[查看模板 →](skills/fullstack-dev.md)**

> 📁 更多模板请查看 [skills/](skills/) 目录

---

## 🤝 贡献指南

我们欢迎所有形式的贡献！无论是添加新的 MCP 服务器、改进分类、修复错误还是完善文档。

### 如何贡献

1. **提交新技能**：通过 [Issue 模板](https://github.com/yourusername/awesome-agent-skills/issues/new?assignees=&labels=&projects=&template=skill-submission.md&title=%5BSkill%5D+) 提交
2. **直接 PR**：Fork 本仓库，修改后提交 Pull Request
3. **讨论建议**：在 [Discussions](https://github.com/yourusername/awesome-agent-skills/discussions) 中分享想法

### 收录标准

- ✅ 项目有明确的 README 和使用说明
- ✅ 项目有一定的维护活跃度（近 3 个月有更新）
- ✅ 项目有明确的开源许可证
- ✅ 功能真实可用，不是玩具项目
- ✅ 代码质量有基本保证

### 贡献者

感谢所有为这个项目做出贡献的人！

<a href="https://github.com/yourusername/awesome-agent-skills/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=yourusername/awesome-agent-skills" />
</a>

---

## ⭐ Star 历史

如果你觉得这个项目有帮助，请给一个 ⭐ Star 支持！

```
Star 增长趋势（目标）：

★★★★★★★★★★ 10K  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 目标
★★★★★☆☆☆☆☆  5K  ━━━━━━━━━━━━━━━━━━━━
★★★☆☆☆☆☆☆☆  3K  ━━━━━━━━━━━━━
★★☆☆☆☆☆☆☆☆  2K  ━━━━━━━━━━
★☆☆☆☆☆☆☆☆☆  1K  ━━━━━
☆☆☆☆☆☆☆☆☆☆   0  ━
```

---

<div align="center">

**Made with ❤️ by the AI Agent Community**

[给个 Star ⭐](https://github.com/yourusername/awesome-agent-skills) · [提交 Issue](https://github.com/yourusername/awesome-agent-skills/issues) · [讨论交流](https://github.com/yourusername/awesome-agent-skills/discussions)

</div>
