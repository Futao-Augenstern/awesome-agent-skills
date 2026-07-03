<div align="center">

# 🤖 awesome-agent-skills

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![GitHub Stars](https://img.shields.io/github/stars/yourusername/awesome-agent-skills?style=social)](https://github.com/yourusername/awesome-agent-skills/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/yourusername/awesome-agent-skills?style=social)](https://github.com/yourusername/awesome-agent-skills/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
[![Last Update](https://img.shields.io/badge/Last%20Update-July%202026-blue)]()

**Curated Collection of AI Agent Skills · Plug-and-Play MCP Servers**

> A carefully curated collection of AI Agent Skills ecosystem to help you build powerful agents quickly.

[English](README.en.md) · [中文](README.md) · [Submit a Skill](https://github.com/yourusername/awesome-agent-skills/issues/new?assignees=&labels=&projects=&template=skill-submission.md&title=%5BSkill%5D+)

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
- [🎯 Featured Skill Templates](#-featured-skill-templates)
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
| [PostgreSQL MCP](https://github.com/neondatabase/mcp-server-postgres) | Query PostgreSQL directly, smart SQL generation | Neon | ⭐⭐⭐⭐⭐ |
| [SQLite MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/sqlite) | Local SQLite database query & management | MCP Official | ⭐⭐⭐⭐ |
| [Docker MCP](https://github.com/ckreiling/mcp-server-docker) | Manage Docker containers, images, compose | Community | ⭐⭐⭐ |
| [Sentry MCP](https://github.com/getsentry/mcp-server-sentry) | Sentry error monitoring & analysis | Sentry Official | ⭐⭐⭐⭐ |

### Productivity

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [Gmail MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/gmail) | Send/receive emails, search, label management | MCP Official | ⭐⭐⭐⭐⭐ |
| [Google Calendar MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/google-calendar) | Calendar event management, scheduling | MCP Official | ⭐⭐⭐⭐ |
| [Notion MCP](https://github.com/metalbear-co/mcp-server-notion) | Notion page read/write, database queries | Community | ⭐⭐⭐⭐⭐ |
| [Slack MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/slack) | Send messages, search, channel management | MCP Official | ⭐⭐⭐⭐ |
| [Linear MCP](https://github.com/linear-ai/mcp-linear) | Linear project management, issue tracking | Linear Official | ⭐⭐⭐⭐ |
| [Todoist MCP](https://github.com/saisandeep998/mcp-todoist-server) | Task management, todo sync | Community | ⭐⭐⭐ |

### Data & Search

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [Brave Search MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) | Brave Search API integration | MCP Official | ⭐⭐⭐⭐⭐ |
| [Tavily MCP](https://github.com/tavily-ai/mcp-tavily) | Search engine optimized for AI agents | Tavily Official | ⭐⭐⭐⭐⭐ |
| [Perplexity MCP](https://github.com/leopiccionia/mcp-perplexity) | Perplexity AI search & Q&A | Community | ⭐⭐⭐⭐ |
| [Pinecone MCP](https://github.com/pinecone-io/mcp-pinecone) | Pinecone vector database operations | Pinecone Official | ⭐⭐⭐⭐ |
| [Wolfram Alpha MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/wolfram-alpha) | Math computation, scientific data query | MCP Official | ⭐⭐⭐⭐ |
| [Weather MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/weather) | Global weather forecast query | MCP Official | ⭐⭐⭐ |

### Content Creation

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [Figma MCP](https://github.com/figma/mcp-figma) | Figma design file reading & analysis | Figma Official | ⭐⭐⭐⭐⭐ |
| [Canva MCP](https://github.com/canva/mcp-canva) | Canva design automation & templates | Canva Official | ⭐⭐⭐⭐ |
| [YouTube MCP](https://github.com/miraclesteven/mcp-youtube) | YouTube video search, caption extraction | Community | ⭐⭐⭐ |
| [Markdown MCP](https://github.com/modelcontextprotocol/servers/tree/main/src/markdown) | Markdown file read/write & processing | MCP Official | ⭐⭐⭐⭐ |
| [PDF MCP](https://github.com/rowickib/mcp-pdf-tools) | PDF reading, parsing, text extraction | Community | ⭐⭐⭐ |

### Cloud & DevOps

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [AWS MCP](https://github.com/awslabs/mcp-server-aws) | AWS service operations (EC2, S3, Lambda, etc.) | AWS Official | ⭐⭐⭐⭐⭐ |
| [GCP MCP](https://github.com/googleapis/mcp-google-cloud) | Google Cloud platform service integration | Google Official | ⭐⭐⭐⭐ |
| [Vercel MCP](https://github.com/vercel/mcp-vercel) | Vercel deployment, project management | Vercel Official | ⭐⭐⭐⭐ |
| [Netlify MCP](https://github.com/netlify/mcp-netlify) | Netlify deployment & site management | Netlify Official | ⭐⭐⭐⭐ |
| [Kubernetes MCP](https://github.com/everettraven/mcp-k8s) | K8s cluster management & resource ops | Community | ⭐⭐⭐⭐ |
| [Terraform MCP](https://github.com/weagle08/mcp-terraform) | Terraform infrastructure as code | Community | ⭐⭐⭐ |

### Lifestyle

| Name | Description | Platform | ⭐ |
|------|-------------|----------|-----|
| [Spotify MCP](https://github.com/RowanAberdeen/mcp-spotify) | Spotify music playback, playlist management | Community | ⭐⭐⭐⭐ |
| [Strava MCP](https://github.com/mmazzarolo/mcp-strava) | Strava workout data analysis | Community | ⭐⭐⭐ |
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
| [superpowers](https://github.com/evilfactorylabs/superpowers) | ✅ Agent Harness | ⭐⭐⭐⭐ | Lightweight agent framework |
| [CopilotKit](https://github.com/CopilotKit/CopilotKit) | ✅ MCP support | ⭐⭐⭐⭐ | Frontend AI Copilot |

---

## 📚 Learning Resources

### Official Documentation
- [MCP Official Docs](https://modelcontextprotocol.io/) - Model Context Protocol official guide
- [MCP GitHub Repo](https://github.com/modelcontextprotocol/servers) - Official servers collection
- [Anthropic MCP Guide](https://docs.anthropic.com/en/docs/agents-and-tools/model-context-protocol) - Claude MCP integration guide

### Tutorials
- [MCP Quick Start: Add Tools to Claude in 5 Minutes](https://example.com/mcp-quickstart)
- [Build Your First MCP Server from Scratch](https://example.com/build-mcp-server)
- [Agent Skills Design Patterns & Best Practices](https://example.com/agent-skills-patterns)

### Deep Dives
- [Why MCP is the App Store for AI Agents?](https://example.com/mcp-app-store)
- [Past, Present, and Future of Agent Tool Calling](https://example.com/agent-tools-history)
- [From Function Calling to MCP: Agent Tool Ecosystem Evolution](https://example.com/function-calling-to-mcp)

---

## 🎯 Featured Skill Templates

We provide ready-to-use Skill templates — copy and use:

### 📝 Code Reviewer
> Automatically review PRs, check code style, potential bugs, performance issues
>
> **Required MCPs**: GitHub, Git
> **[View Template →](skills/code-reviewer.md)**

### 📰 Research Assistant
> Auto-search academic papers, summarize research progress, generate literature reviews
>
> **Required MCPs**: Tavily/Brave Search, Arxiv
> **[View Template →](skills/research-assistant.md)**

### 📧 Email Assistant
> Smart email classification, auto-reply to FAQs, schedule reminders
>
> **Required MCPs**: Gmail, Google Calendar
> **[View Template →](skills/email-assistant.md)**

### 🌐 Full-Stack Dev Assistant
> End-to-end: frontend + backend + database design + deployment
>
> **Required MCPs**: GitHub, PostgreSQL, Vercel/AWS
> **[View Template →](skills/fullstack-dev.md)**

> 📁 More templates in the [skills/](skills/) directory

---

## 🤝 Contributing

We welcome all forms of contribution! Whether it's adding new MCP servers, improving categorization, fixing bugs, or enhancing documentation.

### How to Contribute

1. **Submit a new skill**: Use our [Issue template](https://github.com/yourusername/awesome-agent-skills/issues/new?assignees=&labels=&projects=&template=skill-submission.md&title=%5BSkill%5D+)
2. **Direct PR**: Fork this repo, make changes, submit a Pull Request
3. **Discuss ideas**: Share thoughts in [Discussions](https://github.com/yourusername/awesome-agent-skills/discussions)

### Inclusion Criteria

- ✅ Project has a clear README and usage instructions
- ✅ Project has maintenance activity (updated within last 3 months)
- ✅ Project has a clear open-source license
- ✅ Functionality is genuinely usable, not a toy project
- ✅ Basic code quality assurance

### Contributors

Thanks to everyone who has contributed to this project!

<a href="https://github.com/yourusername/awesome-agent-skills/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=yourusername/awesome-agent-skills" />
</a>

---

## ⭐ Star History

If you find this project helpful, please give it a ⭐ Star!

```
Star Growth Trend (Target):

★★★★★★★★★★ 10K  ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ TARGET
★★★★★☆☆☆☆☆  5K  ━━━━━━━━━━━━━━━━━━━━
★★★☆☆☆☆☆☆☆  3K  ━━━━━━━━━━━━━
★★☆☆☆☆☆☆☆☆  2K  ━━━━━━━━━━
★☆☆☆☆☆☆☆☆☆  1K  ━━━━━
☆☆☆☆☆☆☆☆☆☆   0  ━
```

---

<div align="center">

**Made with ❤️ by the AI Agent Community**

[⭐ Star](https://github.com/yourusername/awesome-agent-skills) · [📝 Issue](https://github.com/yourusername/awesome-agent-skills/issues) · [💬 Discussion](https://github.com/yourusername/awesome-agent-skills/discussions)

</div>
