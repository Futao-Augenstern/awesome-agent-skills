# Agent Skill 模板合集

> 精选的 AI Agent Skill 模板，复制即用，快速构建你的专属智能体。

## 📋 目录

- [代码审查助手](#代码审查助手-code-reviewer)
- [研究助理](#研究助理-research-assistant)
- [邮箱管家](#邮箱管家-email-assistant)
- [全栈开发助手](#全栈开发助手-full-stack-dev-assistant)
- [如何使用](#如何使用)
- [贡献模板](#贡献模板)

---

## 📝 代码审查助手 (Code Reviewer)

**评分**: ⭐⭐⭐⭐⭐ 实用性 | ⭐⭐⭐⭐ 易用性

自动审查 Pull Request，检查代码风格、潜在 bug、性能问题和安全隐患。

**所需 MCP**: GitHub MCP, Filesystem MCP

**[查看详情 →](code-reviewer.md)**

---

## 📰 研究助理 (Research Assistant)

**评分**: ⭐⭐⭐⭐⭐ 实用性 | ⭐⭐⭐⭐⭐ 易用性

自动搜索学术论文、总结研究进展、生成文献综述，是学术研究的得力助手。

**所需 MCP**: Tavily MCP, Brave Search MCP

**[查看详情 →](research-assistant.md)**

---

## 📧 邮箱管家 (Email Assistant)

**评分**: ⭐⭐⭐⭐⭐ 实用性 | ⭐⭐⭐⭐⭐ 易用性

智能分类邮件、自动回复常见问题、日程提醒，让你的邮箱井井有条。

**所需 MCP**: Gmail MCP, Google Calendar MCP

**[查看详情 →](email-assistant.md)**

---

## 🌐 全栈开发助手 (Full-Stack Dev Assistant)

**评分**: ⭐⭐⭐⭐⭐ 实用性 | ⭐⭐⭐⭐ 易用性

前后端开发 + 数据库设计 + 部署上线一条龙服务，你的专属全栈开发搭档。

**所需 MCP**: GitHub MCP, Filesystem MCP, PostgreSQL MCP, Vercel MCP

**[查看详情 →](fullstack-dev.md)**

---

## 🚀 如何使用

### 方法一：复制系统提示词

1. 选择你需要的 Skill 模板
2. 复制文件中的「系统提示词」部分
3. 粘贴到你的 Agent 框架中（Claude Code、LangChain、CrewAI 等）
4. 配置所需的 MCP 服务器
5. 开始使用！

### 方法二：在 Claude Desktop 中使用

1. 打开 Claude Desktop 配置文件
2. 添加所需的 MCP 服务器配置
3. 在对话中引用 Skill 模板的指令
4. Claude 就会按照模板的角色工作

### 方法三：在代码中集成

```python
from langchain_mcp import MCPToolkit
from langchain.agents import AgentExecutor, create_openai_tools_agent

# 加载 MCP 工具
toolkit = MCPToolkit.from_command(
    command="npx",
    args=["-y", "@modelcontextprotocol/server-github"]
)
tools = toolkit.get_tools()

# 使用 Skill 模板的系统提示词
system_prompt = open("skills/code-reviewer.md").read()

# 创建 Agent
agent = create_openai_tools_agent(llm, tools, system_prompt)
agent_executor = AgentExecutor(agent=agent, tools=tools)
```

---

## 🤝 贡献模板

有好用的 Skill 模板想分享？欢迎贡献！

### 模板格式要求

每个 Skill 模板应包含：
1. **技能评分** - 实用性、易用性等维度的评分
2. **技能描述** - 一句话说明这个 Skill 是做什么的
3. **所需 MCP 服务器** - 需要哪些 MCP 服务器
4. **功能清单** - 详细的功能点列表
5. **使用方法** - 系统提示词、常用指令等
6. **输出模板** - 典型的输出格式示例
7. **配置选项** - 可定制的参数
8. **最佳实践** - 使用技巧和建议

### 如何提交

1. Fork 本仓库
2. 在 `skills/` 目录下创建新的 `.md` 文件
3. 按照模板格式填写内容
4. 在本 `README.md` 中添加你的 Skill 介绍
5. 提交 Pull Request

---

## 💡 提示

- **按需组合**: 多个 Skill 模板可以组合使用，打造全能 Agent
- **持续优化**: 根据实际使用效果调整系统提示词
- **安全第一**: 涉及敏感操作的 Skill 务必设置确认步骤
- **分享反馈**: 使用中发现问题或有改进建议，欢迎提 Issue

---

**[← 返回主 README](../README.md)**
