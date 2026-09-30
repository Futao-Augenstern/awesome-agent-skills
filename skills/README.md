# 🎁 现成 Agent Skills 精选

> 别人已经做好、可直接拿来用的 Agent Skills（`SKILL.md`），按领域分类，欢迎按需选用与安装。

> 什么是 Skills？Skills 是一组「文件夹 + `SKILL.md`」的可移植技能，Agent 会在需要时动态加载其中的指令、脚本与资源，从而在特定任务上更可靠地工作（[开箱即读](https://agentskills.io/)）。

---

## 📚 官方与标准

| 资源 | 说明 | 提供方 |
|------|------|--------|
| [Anthropic Skills 仓库](https://github.com/anthropics/skills) | 官方技能库：开发/设计/企业/文档等示例技能 + 规范 + 模板，源码可读、多数 Apache-2.0 | Anthropic 官方 |
| [Agent Skills 开放标准](https://agentskills.io/) | `SKILL.md` 规范主页 | 开放标准（Anthropic 发起） |
| [Skills 规范文档](https://agentskills.io/specification) | 格式、加载流程（发现→激活→执行）与客户端要求的完整规格 | 标准站点 |
| [Skills 客户端清单](https://agentskills.io/clients) | 所有支持 Agent Skills 的 Agent 全家桶一览 | 标准站点 |
| [Claude 技能总览](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview) | 官方技能概念、预置技能与自定义技能说明 | Anthropic 官方 |
| [Claude Skill 发布博客](https://claude.com/blog/skills) | Agent Skills 产品发布与开放标准公告 | Anthropic 官方 |
| [Claude Code Skills 文档](https://code.claude.com/docs/en/skills) | Claude Code 中安装/管理技能 | Anthropic 官方 |
| [支持中心：Skills 是什么](https://support.claude.com/en/articles/12512176-what-are-skills) | 面向使用者的入门问答 | Anthropic 官方 |
| [Skills 设计工程博客](https://anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) | 设计理念、格式与最佳实践 | Anthropic 官方 |

---

## 🧩 技能框架与综合集合

| 名称 | 说明 | 提供方 |
|------|------|--------|
| [obra/superpowers](https://github.com/obra/superpowers) | 完整软件开发方法论，内置可组合技能（规划→TDD→子代理开发→代码审查），支持多数编码 Agent | Jesse Vincent（社区） |
| [awesome-claude-skills](https://github.com/ComposioHQ/awesome-claude-skills) | Claude Skills 精选合集，覆盖各类应用集成 | Composio |
| [ningzimu/awesome-skills](https://github.com/ningzimu/awesome-skills) | 社区技能聚合库：开发、研究、自动化、写作等分类 | 社区 |
| [GitHub awesome-copilot/skills](https://github.com/github/awesome-copilot/tree/main/skills) | GitHub 社区技能目录，按领域索引 | GitHub 社区 |
| [everything-claude-code](https://github.com/affaan-m/everything-claude-code) | Claude Code 生态全景清单（含技能与插件） | affaan-m |

---

## 📄 官方即用技能（分领域 · 开箱即用）

以下技能都可在 `anthropics/skills` 中直接下载/安装使用，也可在 Claude.ai 经授权计划使用。

### 🧾 文档处理
| 技能 | 说明 |
|------|------|
| [docx](https://github.com/anthropics/skills/tree/main/skills/docx) | 创建、编辑、解析 Word 文档，支持样式/批注/兼容性 |
| [pdf](https://github.com/anthropics/skills/tree/main/skills/pdf) | PDF 读取、提取、合并、拆分、水印、表单与 OCR |
| [pptx](https://github.com/anthropics/skills/tree/main/skills/pptx) | 创建、编辑、解析演示文稿并生成缩略图 |
| [xlsx](https://github.com/anthropics/skills/tree/main/skills/xlsx) | Excel 创建、编辑、公式校验与电子表格生成 |

### 🛠️ 开发与测试
| 技能 | 说明 |
|------|------|
| [artifacts-builder](https://github.com/anthropics/skills/tree/main/skills/artifacts-builder) | 构建前端/交互原型产物 |
| [webapp-testing](https://github.com/anthropics/skills/tree/main/skills/webapp-testing) | Web 应用自动化测试技能 |
| [mcp-builder](https://github.com/anthropics/skills/tree/main/skills/mcp-builder) | 构建高质量 MCP 服务器 |
| [frontend-design](https://github.com/anthropics/skills/tree/main/skills/frontend-design) | 前端 UI 设计：配色、排版、布局与可用性 |
| [skill-creator](https://github.com/anthropics/skills/tree/main/skills/skill-creator) | 创建你自己的 Agent Skill |

### 🎨 设计与视觉
| 技能 | 说明 |
|------|------|
| [canvas-design](https://github.com/anthropics/skills/tree/main/skills/canvas-design) | 海报、插画、静态设计输出（.png/.pdf） |
| [brand-guidelines](https://github.com/anthropics/skills/tree/main/skills/brand-guidelines) | 按品牌视觉规范输出内容 |
| [algorithmic-art](https://github.com/anthropics/skills/tree/main/skills/algorithmic-art) | 算法艺术/生成式视觉创意 |

### 🤝 沟通与生态
| 资源 | 说明 |
|------|------|
| [academy-guide](https://github.com/anthropics/skills/tree/main/skills/academy-guide) | 教程/培训场景技能 |
| [Notion for Claude Code](https://claude.com/plugins/notion) | 官方 Notion 技能包：知识捕获、会议纪要、研究整理与规格落地 |

---

## 🛒 怎么安装 / 获取

### 方式一：Claude Code 插件安装（推荐）

```bash
# 1. 注册官方技能仓库为插件市场
/plugin marketplace add anthropics/skills

# 2. 按需安装技能包
/plugin install document-skills@anthropic-agent-skills   # 文档技能（docx/pdf/pptx/xlsx）
/plugin install example-skills@anthropic-agent-skills    # 示例技能
```

### 方式二：网页/平台浏览一批技能

| 渠道 | 说明 |
|------|------|
| [skills.sh/anthropics/skills](https://skills.sh/anthropics/skills) | 网页化浏览官方技能仓库 |
| [Anthropic Skills API](https://docs.claude.com/en/api/skills-guide) | 通过 Claude API 使用预置技能/上传自定义技能 |
| [LobeHub Skills 市场](https://lobehub.com/skills) | 大型社区技能市场（数十万级技能） |
| [ClaudeSkill 市场](https://claudeskil.com/) | 开源 SKILL.md 技能市场，带安装说明 |
| [Claude 插件市场](https://code.claude.com/docs/en/discover-plugins) | 在 Claude Code 中浏览/添加插件市场 |
| [OpenClaw skills](https://docs.openclaw.ai/tools/skills) · [ClawHub](https://docs.openclaw.ai/clawhub) | 全平台 Agent 框架 Skills + 公开注册表 |

---

## ⚙️ 支持 Agent Skills 的运行时

开箱支持 Skills（含执行 `SKILL.md`）的工具/框架，往往只需把技能目录放入对应文件夹：

- [Claude Code](https://code.claude.com/docs/en/skills)、Claude.ai、Claude API
- [OpenClaw](https://docs.openclaw.ai/tools/skills)
- 更多客户端见 [agentskills.io/clients](https://agentskills.io/clients)（Visual Studio Code、GitHub、Gemini CLI、OpenHands、ChatGPT Codex 等）

> 💡 **兼容提示**：绝大多数「Awesome 级」第三方技能都遵循同一 `SKILL.md` 开放格式，可在任意支持该标准的客户端间复用。安装/使用前建议先看对应技能仓库的说明。

---

## 🤝 贡献

想收录更多开箱即用的现成技能？欢迎提交 Issue / PR，把「名称 + 真实可访问链接 + 一句话说明 + 领域分类」发给我们。

---

**[← 返回主 README](../README.md)**