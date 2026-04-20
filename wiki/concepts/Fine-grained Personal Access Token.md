---
title: "Fine-grained Personal Access Token"
type: concept
tags: [安全, 权限管理, 认证]
sources: [raw/01-articles/DeepSeek.md]
last_updated: 2026-04-20
---

## 定义

Fine-grained Personal Access Token（细粒度个人访问令牌）是 GitHub 提供的一种高级权限管理机制，允许用户对每个权限项进行单独控制，可以设置为"无访问"（No access）、"只读"（Read-only）或"读写"（Read and write）。

## 关键信息

### 权限分类

**仓库核心内容与数据**：
- Contents（仓库内容）：控制源代码、文件、提交和 Releases 的读写
- Metadata（仓库元数据）：自动授予，不可取消
- Commit statuses（提交状态）：标记 commit 的检查状态
- Deployments（部署）：记录部署过程和状态
- Pages（GitHub Pages）：配置和构建站点

**安全与漏洞警报**：
- Code scanning alerts（代码扫描警报）：管理 CodeQL 等工具发现的代码漏洞
- Dependabot alerts（依赖项警报）：管理依赖项安全漏洞警报
- Dependabot secrets（Dependabot 密钥）：管理访问私有依赖库的敏感信息
- Secret scanning alerts（密钥扫描警报）：管理代码中明文存储的敏感信息警报
- Secret scanning alert dismissal requests（密钥扫描警报关闭请求）
- Secret scanning push protection bypass requests（密钥扫描推送保护绕过请求）

**协作与流程管理**：
- Issues（议题）：问题追踪、任务管理
- Pull requests（拉取请求）：代码审查、合并管理
- Discussions（讨论）：社区互动、问答和公告
- Workflows（工作流）：管理 GitHub Actions 工作流文件
- Webhooks（Web 钩子）：在特定事件发生时向外部服务发送 HTTP 请求
- Environments（环境）：管理 CI/CD 环境配置和保护规则
- Merge queues（合并队列）：自动排队合并多个 PR

**高级配置与管理**：
- Administration（仓库管理）：仓库设置、协作管理、分支保护规则
- Actions（GitHub Actions）：管理 Actions 设置、runner 和缓存
- Codespaces（代码空间）：管理云端开发环境
- Codespaces lifecycle admin（生命周期管理）：启动、停止、删除 Codespaces
- Codespaces metadata（元数据）：读取 Codespaces 相关信息
- Codespaces secrets（密钥）：管理 Codespaces 环境变量
- Custom properties（自定义属性）：仓库分类和标记
- Repository security advisories（安全公告）：私下讨论和修复安全漏洞
- Attestations（证明）：验证工件的来源和完整性
- Artifact metadata（工件元数据）：管理工作流产物的元数据

### 最佳实践

遵循**最小权限原则**，根据实际需求精确配置权限。例如：
- 仅读取 Issue：Metadata（只读）+ Issues（读写）
- CI/CD 流水线：Contents（读写）+ Commit statuses（读写）+ Deployments（读写）

### 优势

相比经典令牌，细粒度令牌的精确控制能显著降低令牌泄露带来的安全风险。

## 关联连接
- [[摘要-github-fine-grained-tokens]] — 来源
- [[GitHub]] — 所属平台
- [[最小权限原则]] — 安全原则
- [[GitHub Actions]] — 常用场景
