# Obsidian Skills 指南

## 简介

Obsidian Skills 是一套遵循 [Agent Skills 规范](https://agentskills.io/specification) 的代理技能集合，可以被任何兼容 Skills 的代理使用，包括 Claude Code 和 Codex CLI。

## 安装方式

### 方式一：Marketplace（市场）

```bash
/plugin marketplace add kepano/obsidian-skills
/plugin install obsidian@obsidian-skills
```

### 方式二：npx skills

```bash
npx skills add git@github.com:kepano/obsidian-skills.git
```

### 方式三：手动安装

#### Claude Code

将此仓库的内容添加到 Obsidian vault 根目录（或你与 Claude Code 一起使用的任何文件夹）的 `/.claude` 文件夹中。详见 [Claude Skills 官方文档](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)。

#### Codex CLI

将 `skills/` 目录复制到你的 Codex skills 路径（通常是 `~/.codex/skills`）。详见 [Agent Skills 规范](https://agentskills.io/specification)。

#### OpenCode

将整个仓库克隆到 OpenCode skills 目录（`~/.opencode/skills/`）：

```bash
git clone https://github.com/kepano/obsidian-skills.git ~/.opencode/skills/obsidian-skills
```

**注意**：不要只复制内部的 `skills/` 文件夹，要克隆完整的仓库，使目录结构为 `~/.opencode/skills/obsidian-skills/skills/<skill-name>/SKILL.md`。

OpenCode 会自动发现 `~/.opencode/skills/` 下所有的 `SKILL.md` 文件。无需修改 `opencode.json` 或任何配置文件。重启 OpenCode 后技能即可使用。

## 包含的技能

| 技能名称 | 功能描述 |
|---------|---------|
| **obsidian-markdown** | 创建和编辑 [Obsidian 风格 Markdown](https://help.obsidian.md/obsidian-flavored-markdown)（`.md`）文件，支持 wiki 链接、嵌入、标注框、属性和其他 Obsidian 特定语法 |
| **obsidian-bases** | 创建和编辑 [Obsidian Bases](https://help.obsidian.md/bases/syntax)（`.base`）文件，支持视图、过滤器、公式和摘要 |
| **json-canvas** | 创建和编辑 [JSON Canvas](https://jsoncanvas.org/) 文件（`.canvas`），支持节点、边、分组和连接 |
| **obsidian-cli** | 通过 [Obsidian CLI](https://help.obsidian.md/cli) 与 Obsidian vault 交互，包括插件和主题开发 |
| **defuddle** | 使用 [Defuddle](https://github.com/kepano/defuddle-cli) 从网页提取干净的 markdown 内容，移除杂乱信息以节省 token |

## 技能详解

### 1. obsidian-markdown
用于创建和编辑 Obsidian 风格的 Markdown 文件。支持所有 Obsidian 特定的语法特性，如双向链接、嵌入、标注框等。

### 2. obsidian-bases
用于创建和编辑 Obsidian Bases 文件。Bases 是 Obsidian 中的数据库功能，支持多种视图和数据操作。

### 3. json-canvas
用于创建和编辑 JSON Canvas 文件。Canvas 是一种可视化的知识图谱格式，支持节点、连接和分组。

### 4. obsidian-cli
提供命令行接口与 Obsidian vault 交互，支持插件和主题的开发工作。

### 5. defuddle
一个网页内容提取工具，能够从网页中提取干净的 markdown 内容，自动移除导航、广告等杂乱元素，有效节省 token 使用。

## 使用场景

- **知识管理**：使用 obsidian-markdown 和 obsidian-bases 组织和管理知识库
- **可视化思维**：使用 json-canvas 创建思维导图和知识图谱
- **自动化工作流**：使用 obsidian-cli 自动化 Obsidian 相关任务
- **内容采集**：使用 defuddle 从网络采集和清理内容

## 相关资源

- [Agent Skills 规范](https://agentskills.io/specification)
- [Claude Skills 文档](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)
- [Obsidian 官方文档](https://help.obsidian.md/)
- [Defuddle CLI](https://github.com/kepano/defuddle-cli)

---

**来源**：[kepano/obsidian-skills](https://github.com/kepano/obsidian-skills)  
**最后更新**：2026-04-19
