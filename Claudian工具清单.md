---
title: "Claudian 工具清单"
type: synthesis
tags: [工具文档, 系统能力]
last_updated: 2026-04-20
---

# Claudian 工具清单

## 核心工具

**Read**: 读取文件（支持文本、图片、PDF、Jupyter Notebook）
**Write**: 创建新文件或完全重写文件（⚠️ 限制 100 行以内）
**Edit**: 精确字符串替换编辑文件
**Glob**: 文件模式匹配搜索（如 `**/*.md`）
**Grep**: 基于 ripgrep 的内容搜索工具
**Bash**: 执行 bash 命令

## 任务管理

**TodoWrite**: 创建和管理结构化任务列表
**TaskOutput**: 获取后台任务输出
**TaskStop**: 停止后台任务

## 协作与规划

**Agent**: 启动专用子代理处理复杂任务
**AskUserQuestion**: 向用户提问获取决策
**EnterPlanMode**: 进入规划模式设计方案
**ExitPlanMode**: 退出规划模式提交计划

## Web 工具

**WebSearch**: 搜索网络获取最新信息
**WebFetch**: 获取并分析网页内容

## 专用工具

**NotebookEdit**: 编辑 Jupyter Notebook 文件
**Skill**: 调用外部技能系统
**CronCreate**: 创建定时任务
**CronList**: 列出所有定时任务
**CronDelete**: 删除定时任务
**EnterWorktree**: 创建隔离的 git worktree 环境
**ExitWorktree**: 退出 worktree 环境

## Agent 类型

**general-purpose**: 通用代理，处理复杂多步骤任务
**Explore**: 快速探索代码库的专用代理
**Plan**: 软件架构规划代理
**superpowers:code-reviewer**: 代码审查代理

## 可用 Skills

### Obsidian 专用
**ingest**: 将 raw/ 目录资料编译到 wiki/
**query**: 在本地知识库中回答问题
**lint**: 知识库健康检查（死链、孤儿页面）
**obsidian-markdown**: 创建 Obsidian 格式文档
**obsidian-canvas-creator**: 创建 Obsidian Canvas 文件
**obsidian-bases**: 创建和编辑 Obsidian Bases 文件
**obsidian-cli**: 使用 Obsidian CLI 管理笔记

### 可视化
**mermaid-visualizer**: 生成 Mermaid 图表
**excalidraw-diagram**: 生成 Excalidraw 图表

### 学习系统
**tutor**: 交互式测验辅导
**tutor-setup**: 将知识源转换为学习库

### 开发工具
**claude-api**: 构建 Claude API 应用
**simplify**: 代码质量和效率审查
**loop**: 定时循环执行命令
**defuddle**: 提取网页干净内容

### Superpowers 系列
**superpowers:brainstorming**: 创意工作前的头脑风暴
**superpowers:writing-plans**: 编写实施计划
**superpowers:executing-plans**: 执行实施计划
**superpowers:systematic-debugging**: 系统化调试流程
**superpowers:test-driven-development**: TDD 开发流程
**superpowers:verification-before-completion**: 完成前验证
**superpowers:requesting-code-review**: 请求代码审查
**superpowers:receiving-code-review**: 接收代码审查反馈
**superpowers:dispatching-parallel-agents**: 并行代理调度
**superpowers:subagent-driven-development**: 子代理驱动开发
**superpowers:using-git-worktrees**: 使用 git worktree
**superpowers:finishing-a-development-branch**: 完成开发分支
**superpowers:writing-skills**: 创建和编辑技能
**superpowers:using-superpowers**: 技能系统使用指南

### 示例 Skills
**example-skills:frontend-design**: 前端界面设计
**example-skills:mcp-builder**: 创建 MCP 服务器
**example-skills:web-artifacts-builder**: 构建 Web artifacts
**example-skills:webapp-testing**: Web 应用测试
**example-skills:skill-creator**: 创建新技能
**example-skills:pdf**: PDF 文件操作
**example-skills:docx**: Word 文档操作
**example-skills:pptx**: PowerPoint 操作
**example-skills:xlsx**: Excel 表格操作
**example-skills:canvas-design**: 创建视觉艺术
**example-skills:algorithmic-art**: 算法艺术（p5.js）
**example-skills:theme-factory**: 主题样式工具
**example-skills:brand-guidelines**: Anthropic 品牌规范
**example-skills:doc-coauthoring**: 文档协作编写
**example-skills:internal-comms**: 内部沟通文档
**example-skills:slack-gif-creator**: Slack GIF 创建

### Superpowers Lab
**superpowers-lab:slack-messaging**: Slack 消息交互
**superpowers-lab:finding-duplicate-functions**: 查找重复函数
**superpowers-lab:mcp-cli**: 按需使用 MCP 服务器
**superpowers-lab:using-tmux-for-interactive-commands**: 使用 tmux 运行交互式命令
**superpowers-lab:windows-vm**: 管理 Windows 虚拟机

## MCP 插件

### Figma
**mcp__Figma__get_design_context**: 获取 Figma 设计上下文
**mcp__Figma__use_figma**: 通过 Plugin API 操作 Figma
**mcp__Figma__get_screenshot**: 生成 Figma 节点截图
**mcp__Figma__get_metadata**: 获取节点元数据（XML 格式）
**mcp__Figma__get_figjam**: 生成 FigJam UI 代码
**mcp__Figma__search_design_system**: 搜索设计系统资源
**mcp__Figma__get_libraries**: 获取设计库列表
**mcp__Figma__get_variable_defs**: 获取变量定义
**mcp__Figma__get_code_connect_map**: 获取 Code Connect 映射
**mcp__Figma__get_code_connect_suggestions**: 获取 Code Connect 建议
**mcp__Figma__get_context_for_code_connect**: 获取组件元数据
**mcp__Figma__add_code_connect_map**: 添加 Code Connect 映射
**mcp__Figma__send_code_connect_mappings**: 批量保存映射
**mcp__Figma__create_design_system_rules**: 创建设计系统规则
**mcp__Figma__create_new_file**: 创建新 Figma 文件
**mcp__Figma__generate_diagram**: 创建流程图/甘特图（Mermaid）
**mcp__Figma__generate_figma_design**: 将网页转换为 Figma 设计
**mcp__Figma__whoami**: 获取认证用户信息

### Playwright
**mcp__playwright__browser_navigate**: 导航到 URL
**mcp__playwright__browser_snapshot**: 捕获页面可访问性快照
**mcp__playwright__browser_take_screenshot**: 截图
**mcp__playwright__browser_click**: 点击元素
**mcp__playwright__browser_type**: 输入文本
**mcp__playwright__browser_fill_form**: 填写表单
**mcp__playwright__browser_select_option**: 选择下拉选项
**mcp__playwright__browser_hover**: 悬停元素
**mcp__playwright__browser_drag**: 拖放元素
**mcp__playwright__browser_press_key**: 按键
**mcp__playwright__browser_evaluate**: 执行 JavaScript
**mcp__playwright__browser_run_code**: 运行 Playwright 代码
**mcp__playwright__browser_wait_for**: 等待文本出现/消失
**mcp__playwright__browser_console_messages**: 获取控制台消息
**mcp__playwright__browser_network_requests**: 获取网络请求
**mcp__playwright__browser_handle_dialog**: 处理对话框
**mcp__playwright__browser_file_upload**: 上传文件
**mcp__playwright__browser_tabs**: 管理浏览器标签页
**mcp__playwright__browser_navigate_back**: 返回上一页
**mcp__playwright__browser_resize**: 调整浏览器窗口大小
**mcp__playwright__browser_close**: 关闭页面

## 工具使用优先级

**文件操作**: Read > Edit > Write > Bash
**搜索**: Grep/Glob > Bash find/grep
**任务管理**: 简单任务直接执行 > TodoWrite (3+ 步) > Agent (复杂)
**信息获取**: 本地文件 > 本地搜索 > WebSearch > WebFetch

---

## 关联链接
- [[CLAUDE.md]]
