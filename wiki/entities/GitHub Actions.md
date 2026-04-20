---
title: "GitHub Actions"
type: entity
tags: [CI/CD, 自动化, 工作流]
sources: [raw/01-articles/DeepSeek.md]
last_updated: 2026-04-20
---

## 定义

GitHub Actions 是 GitHub 提供的 CI/CD 自动化平台，允许开发者通过工作流（Workflows）自动化软件构建、测试、部署等流程。

## 关键信息

- 使用 YAML 文件定义工作流
- 支持自定义 runner（运行器）
- 可以管理工作流产物（Artifacts）
- 需要特定权限：Workflows（管理工作流文件）、Actions（管理 Actions 设置）、Commit statuses（标记提交状态）
- 常用于 CI/CD 流水线，需要 Contents（读写）、Commit statuses（读写）、Deployments（读写）等权限

## 关联连接
- [[摘要-github-fine-grained-tokens]] — 来源
- [[GitHub]] — 所属平台
- [[CI/CD]] — 相关概念
- [[Fine-grained Personal Access Token]] — 权限管理
