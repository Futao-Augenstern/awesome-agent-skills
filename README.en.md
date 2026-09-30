<div align="center">

# 🤖 awesome-agent-skills

[![Awesome](https://cdn.jsdelivr.net/gh/sindresorhus/awesome@main/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![GitHub Stars](https://img.shields.io/github/stars/Futao-Augenstern/awesome-agent-skills?style=social)](https://github.com/Futao-Augenstern/awesome-agent-skills/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/Futao-Augenstern/awesome-agent-skills?style=social)](https://github.com/Futao-Augenstern/awesome-agent-skills/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
[![Last Commit](https://img.shields.io/github/last-commit/Futao-Augenstern/awesome-agent-skills)](https://github.com/Futao-Augenstern/awesome-agent-skills/commits)

**Curated Collection of AI Agent Skills · Plug-and-Play MCP Servers**

> A carefully curated collection of AI Agent Skills ecosystem to help you build powerful agents quickly.

[English](README.en.md) · [中文](README.md) · [Submit a Skill](https://github.com/Futao-Augenstern/awesome-agent-skills/issues/new?assignees=&labels=&projects=&template=skill-submission.md&title=%5BSkill%5D+)

</div>

---

## 📋 Table of Contents

- [🔥 What are Agent Skills?](#-what-are-agent-skills)
- [⚡ Quick Start](#-quick-start)
- [🏆 Featured MCP Servers](#-featured-mcp-servers)
  - [Developer Tools](#developer-tools)
  - [Productivity](#productivity)
  - [Data & Search](#data--search)
  - [Content Creation](#content-creation)
  - [Cloud & DevOps](#cloud--devops)
  - [Lifestyle](#lifestyle)
- [🛠️ Agent Framework Integration](#️-agent-framework-integration)
- [📚 Learning Resources](#-learning-resources)
- [🎁 Ready-Made Agent Skills](#-ready-made-agent-skills)
- [🤝 Contributing](#-contributing)
- [⭐ Star History](#-star-history)

---

## 🔥 What are Agent Skills?

**Agent Skills** are "capability plugins" for AI Agents — like equipping your AI assistant with various professional tools. Through the [MCP (Model Context Protocol)](https://modelcontextprotocol.io/) standard, agents can call external tools, access data, and execute operations, evolving from "chat-capable" to "action-capable."

```
┌─────────────────────────────────────────────────┐
│                   AI Agent                       │
│  ┌─────────┐  ┌─────────┐  ┌─────────┐         │
│  │  Search │  │  Coding │  │  Email  │  ...   │
│  └────┬────┘  └────┬────┘  └────┬────┘         │
│       │            │            │               │
│  ┌────┴────────────┴────────────┴────┐          │
│  │     MCP (Model Context Protocol)   │         │
│  └─────────────────┬──────────────────┘         │
└────────────────────┼────────────────────────────┘
                     │
         ┌───────────┴───────────┐
         │  External Tools / Data │
         └───────────────────────┘
```

**Why this repository?**
- ✅ **Save time**: No need to hunt for tools yourself — curated high-quality MCP servers ready to use
- ✅ **Well-organized**: Categorized by use case, quickly find the skills you need
- ✅ **Quality assured**: Every listed project passes basic quality review
- ✅ **Always up-to-date**: Following the Agent ecosystem evolution, updated weekly

---

## ⚡ Quick Start

### Option 1: Use with Claude Desktop (Recommended)

```bash
# 1. Install an MCP server (e.g., filesystem)
npx @modelcontextprotocol/server-filesystem /path/to/workspace

# 2. Configure claude_desktop_config.json
# Add the server configuration to your config file
```

### Option 2: Use in Code

```python
# Using LangChain + MCP
from langchain_mcp import MCPToolkit

toolkit = MCPToolkit.from_command(
    command="npx",
    args=["-y", "@modelcontextprotocol/server-github"]
)
tools = toolkit.get_tools()
```

### Option 3: Browse This Repository

Simply browse the categories below to find the skills you need, click links for details and installation instructions.

---

## 🏆 Featured MCP Servers

### Developer Tools

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [GitHub MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/github) | Manage GitHub repos, issues, PRs, code search | MCP Official | ⭐⭐⭐⭐⭐ |
| [GitLab MCP Server](https://github.com/modelcontextprotocol/servers/tree/main/src/gitlab) | GitLab repo management, CI/CD operations | MCP Official | ⭐⭐⭐⭐ |
| [Neon MCP (PostgreSQL)](https://github.com/neondatabase/mcp-server-neon) | Query PostgreSQL directly, smart SQL generation | Neon Official | ⭐⭐⭐⭐⭐ |
| [SQLite MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) | Local SQLite database query & management | MCP Official | ⭐⭐⭐⭐ |
| [Docker MCP](https://github.com/ckreiling/mcp-server-docker) | Manage Docker containers, images, compose | Community | ⭐⭐⭐ |
| [Sentry MCP](https://github.com/getsentry/sentry-mcp) | Sentry error monitoring & analysis | Sentry Official | ⭐⭐⭐⭐ |

### Productivity

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [Gmail MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/gmail) | Send/receive emails, search, label management | MCP Official | ⭐⭐⭐⭐⭐ |
| [Google Calendar MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/google-calendar) | Calendar event management, scheduling | MCP Official | ⭐⭐⭐⭐ |
| [Notion MCP](https://developers.notion.com/docs/mcp) | Notion page read/write, database queries (official remote MCP) | Notion Official | ⭐⭐⭐⭐⭐ |
| [Slack MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) | Send messages, search, channel management | MCP Official | ⭐⭐⭐⭐ |
| [Linear MCP](https://linear.app/docs/mcp) | Linear project management, issue tracking (official remote MCP) | Linear Official | ⭐⭐⭐⭐ |
| [Todoist MCP](https://github.com/Doist/todoist-mcp) | Task management, todo sync | Doist Official | ⭐⭐⭐⭐ |

### Data & Search

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [Brave Search MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) | Brave Search API integration | MCP Official | ⭐⭐⭐⭐⭐ |
| [Tavily MCP](https://github.com/tavily-ai/tavily-mcp) | Search engine optimized for AI agents | Tavily Official | ⭐⭐⭐⭐⭐ |
| [Perplexity MCP](https://github.com/perplexityai/modelcontextprotocol) | Perplexity AI search & Q&A | Perplexity Official | ⭐⭐⭐⭐ |
| [Pinecone MCP](https://github.com/pinecone-io/pinecone-mcp) | Pinecone vector database operations | Pinecone Official | ⭐⭐⭐⭐ |
| [Wolfram Alpha MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/wolfram-alpha) | Math computation, scientific data query | MCP Official | ⭐⭐⭐⭐ |
| [Weather MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/weather) | Global weather forecast query | MCP Official | ⭐⭐⭐ |

### Content Creation

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [Figma MCP](https://github.com/figma/mcp-server-guide) | Figma design file reading & analysis | Figma Official | ⭐⭐⭐⭐⭐ |
| [Canva MCP](https://www.canva.dev/docs/apps/mcp/) | Canva design automation & templates (remote MCP) | Canva Official | ⭐⭐⭐⭐ |
| [YouTube MCP](https://github.com/kevinwatt/yt-dlp-mcp) | YouTube video search, caption extraction | Community | ⭐⭐⭐⭐ |
| [Markdown MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/markdown) | Markdown file read/write & processing | MCP Official | ⭐⭐⭐⭐ |
| [MarkItDown MCP](https://github.com/microsoft/markitdown) | Convert PDF, Office, images to Markdown (MCP support) | Microsoft Official | ⭐⭐⭐⭐⭐ |

### Cloud & DevOps

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [AWS MCP](https://github.com/awslabs/mcp) | AWS service operations (EC2, S3, Lambda, etc.) | AWS Official | ⭐⭐⭐⭐⭐ |
| [GCP MCP](https://github.com/google/mcp) | Google Cloud platform service integration | Google Official | ⭐⭐⭐⭐ |
| [Vercel MCP](https://vercel.com/docs/mcp) | Vercel deployment, project management (remote MCP) | Vercel Official | ⭐⭐⭐⭐ |
| [Netlify MCP](https://github.com/netlify/netlify-mcp) | Netlify deployment & site management | Netlify Official | ⭐⭐⭐⭐ |
| [Kubernetes MCP](https://github.com/flux159/mcp-server-kubernetes) | K8s cluster management & resource ops | Community | ⭐⭐⭐⭐ |
| [Terraform MCP](https://github.com/hashicorp/terraform-mcp-server) | Terraform infrastructure as code | HashiCorp Official | ⭐⭐⭐⭐ |

### Lifestyle

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [Spotify MCP](https://github.com/varunneal/spotify-mcp) | Spotify music playback, playlist management | Community | ⭐⭐⭐⭐ |
| [Strava MCP](https://github.com/r-huijts/strava-mcp) | Strava workout data analysis | Community | ⭐⭐⭐⭐ |
| [Shopping List MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/shopping-list) | Shopping list management | MCP Official | ⭐⭐ |
| [Reminder MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/reminders) | Reminder & task management | MCP Official | ⭐⭐⭐ |

> 💡 **More MCP servers** in the [mcp-servers/](mcp-servers/) directory with detailed categories.

---

## 🛠️ Agent Framework Integration

| Framework | MCP Support | Popularity | Use Case |
|-----------|-------------|------------|----------|
| [Claude Code](https://www.anthropic.com/claude-code) | ✅ Native | ⭐⭐⭐⭐⭐ | Code development, terminal ops |
| [LangChain / LangGraph](https://www.langchain.com/) | ✅ `langchain-mcp` | ⭐⭐⭐⭐⭐ | Complex agent workflows, production |
| [CrewAI](https://www.crewai.com/) | ✅ MCP tools | ⭐⭐⭐⭐ | Multi-agent collaboration |
| [AutoGPT](https://agpt.co/) | ✅ Plugin system | ⭐⭐⭐⭐ | Autonomous agents |
| [Dify](https://dify.ai/) | ✅ Tool nodes | ⭐⭐⭐⭐⭐ | Visual orchestration, enterprise |
| [OpenClaw](https://github.com/openclaw/openclaw) | ✅ Native | ⭐⭐⭐⭐⭐ | Full-stack agent framework |
| [superpowers](https://github.com/obra/superpowers) | ✅ Agent Harness | ⭐⭐⭐⭐⭐ | Lightweight agent framework |
| [CopilotKit](https://github.com/CopilotKit/CopilotKit) | ✅ MCP support | ⭐⭐⭐⭐ | Frontend AI Copilot |

---

## 📚 Learning Resources

### Official Documentation
- [MCP Official Docs](https://modelcontextprotocol.io/) - Model Context Protocol official guide
- [MCP GitHub Repo](https://github.com/modelcontextprotocol/servers) - Official servers collection
- [Anthropic MCP Guide](https://docs.anthropic.com/en/docs/agents-and-tools/model-context-protocol) - Claude MCP integration guide

### Tutorials
- [MCP Official Quickstart](https://modelcontextprotocol.io/quickstart) - Build and connect your first MCP server in 5 minutes
- [Build an MCP Server from Scratch](https://modelcontextprotocol.io/docs/develop/build-server) - Official MCP server build guide
- [Equipping Agents for the Real World with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) - Anthropic engineering blog

### Deep Dives
- [Introducing the Model Context Protocol](https://www.anthropic.com/news/model-context-protocol) - Official Anthropic announcement
- [Tool Use & Agent Protocol History & Timeline](https://hidekazu-konishi.com/entry/tool_use_and_agent_protocol_history_and_timeline.html) - From early tool calling to MCP
- [MCP vs Function Calling](https://qveris.ai/zh-cn/guides/mcp-vs-function-calling) - Agent tool ecosystem evolution analysis

---

## 🎁 Ready-Made Agent Skills

Looking for **Agent Skills that others have already built and are ready to use**? No need to write them from scratch. Here are the top official and community sources:

### 📚 Official & Standards
| Resource | Description |
|------|------|
| [Anthropic Skills repo](https://github.com/anthropics/skills) | Official skill library (docx/pdf/pptx/xlsx, webapp-testing, canvas-design, brand-guidelines, etc.) |
| [Agent Skills open standard](https://agentskills.io/) | `SKILL.md` spec, specification & client showcase |
| [Claude Skills docs](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) | Official skills overview & pre-built skills |

### 🧩 Skill Frameworks & Collections
| Name | Description |
|------|------|
| [obra/superpowers](https://github.com/obra/superpowers) | Complete dev methodology + composable skills (planning→TDD→subagents→code review) |
| [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | Curated list of ready-made Claude skills |
| [ningzimu/awesome-skills](https://github.com/ningzimu/awesome-skills) | Community skill library, organized by domain |

### ⚙️ Quick Install (Claude Code)
```bash
/plugin marketplace add anthropics/skills
/plugin install document-skills@anthropic-agent-skills   # docx/pdf/pptx/xlsx
```

> 📁 Full categorized directory (official skills, frameworks, marketplaces, compatible runtimes) in the [skills/](skills/) directory.

---

## 🤝 Contributing

We welcome all forms of contribution! Whether it's adding new MCP servers, improving categorization, fixing bugs, or enhancing documentation.

### How to Contribute

1. **Submit a new skill**: Use our [Issue template](https://github.com/Futao-Augenstern/awesome-agent-skills/issues/new?assignees=&labels=&projects=&template=skill-submission.md&title=%5BSkill%5D+)
2. **Direct PR**: Fork this repo, make changes, submit a Pull Request
3. **Discuss ideas**: Share thoughts in [Issues](https://github.com/Futao-Augenstern/awesome-agent-skills/issues)

### Inclusion Criteria

- ✅ Project has a clear README and usage instructions
- ✅ Project has maintenance activity (updated within last 3 months)
- ✅ Project has a clear open-source license
- ✅ Functionality is genuinely usable, not a toy project
- ✅ Basic code quality assurance

### Contributors

Thanks to everyone who has contributed to this project!

<a href="https://github.com/Futao-Augenstern/awesome-agent-skills/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=Futao-Augenstern/awesome-agent-skills" />
</a>

---

## ⭐ Star History

If you find this project helpful, please give it a ⭐ Star!

[![Star History Chart](https://api.star-history.com/svg?repos=Futao-Augenstern/awesome-agent-skills&type=Date)](https://star-history.com/#Futao-Augenstern/awesome-agent-skills&Date)

---

<div align="center">

**Made with ❤️ by the AI Agent Community**

[⭐ Star](https://github.com/Futao-Augenstern/awesome-agent-skills) · [📝 Issue](https://github.com/Futao-Augenstern/awesome-agent-skills/issues)

</div>
