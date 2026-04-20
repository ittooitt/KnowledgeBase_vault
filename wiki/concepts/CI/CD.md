---
title: "CI/CD"
type: concept
tags: [自动化, 持续集成, 持续部署]
sources: [raw/01-articles/DeepSeek.md]
last_updated: 2026-04-20
---

## 定义

CI/CD（Continuous Integration / Continuous Deployment）是现代软件开发中的核心实践，指持续集成和持续部署。持续集成是指频繁地将代码集成到主分支并自动运行测试；持续部署是指自动将通过测试的代码部署到生产环境。

## 关键信息

### 核心组成

- **持续集成（CI）**：自动化构建和测试
- **持续部署（CD）**：自动化部署到生产环境

### 在 GitHub 中的应用

- 使用 GitHub Actions 实现 CI/CD 流水线
- 需要的权限：Contents（读写）、Commit statuses（读写）、Deployments（读写）
- 如果涉及 GitHub Pages 部署，还需要 Pages 权限

### 优势

- 快速发现和修复问题
- 提高代码质量
- 加快交付速度
- 降低部署风险

## 关联连接
- [[摘要-github-fine-grained-tokens]] — 来源
- [[GitHub Actions]] — 实现工具
- [[GitHub Pages]] — 部署目标之一
