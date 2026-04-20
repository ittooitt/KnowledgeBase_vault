---
title: "DeepSeek"
source: "https://chat.deepseek.com/a/chat/s/d86e9f4f-0e56-4b3c-82cb-61df1d963ab4"
author:
published:
created: 2026-04-20
description: "Chat with DeepSeek AI – your intelligent assistant for coding, content creation, file reading, and more. Upload documents, engage in long-context conversations, and get expert help in AI, natural language processing, and beyond. | 深度求索（DeepSeek）助力编程代码开发、创意写作、文件处理等任务，支持文件上传及长文本对话，随时为您提供高效的AI支持。"
tags:
  - "clippings"
---
GitHub 的 Fine-grained personal access tokens（细粒度个人访问令牌）允许你对每个权限进行单独控制，你可以为每一项设置 `No access`（无访问）、`Read-only`（只读）或 `Read and write`（读写）[\-4](https://wenku.csdn.net/answer/8486m7kdnr)。

你列出的这些权限覆盖了仓库操作的方方面面，下面是它们的详细解释：

### 📋 仓库核心内容与数据

- **Contents**：**仓库内容**。控制对仓库源代码、文件、提交和 Releases（发布）的读写权限。这是最核心的权限，通常需要设为 `Read and write` 才能进行代码的拉取和推送 [\-2](https://docs.amazonaws.cn/en_us/codebuild/latest/userguide/access-tokens-github.html)[\-3](https://gitea.cn/actions/checkout/commit/2292b247791f879c36ad9107ae81c8b66fc06048.patch)。
- **Metadata**：**仓库元数据**。这是几乎所有其他权限的依赖项，**通常会自动授予且不可取消**。它允许访问仓库的基础信息，如可见性、所有者、主题等。
- **Commit statuses**：**提交状态**。允许读取和写入每次提交的状态。CI/CD 系统（如 GitHub Actions）常用它来标记一个 commit 的检查是通过还是失败 [\-1](https://arinco.com.au/blog/changes-to-the-default-github_token-permissions/#content)[\-2](https://docs.amazonaws.cn/en_us/codebuild/latest/userguide/access-tokens-github.html)。
- **Deployments**：**部署**。控制对部署（Deployments）的访问，用于记录代码部署到特定环境（如生产、预发布）的过程和状态。
- **Pages**：**GitHub Pages**。控制对仓库的 GitHub Pages 站点的配置和构建权限。

### 🛡️ 安全与漏洞警报

> **注意**：要访问这些安全功能，通常还需要对仓库有较高的访问权限（如 `Write` 或 `Admin` 角色）。

- **Code scanning alerts**：**代码扫描警报**。管理由 GitHub 原生代码扫描工具（如 CodeQL）发现的代码漏洞和错误警报 。
- **Dependabot alerts**：**依赖项警报**。管理 Dependabot 自动检测到的有安全漏洞的依赖项警报 [\-5](https://kb.phoenix.security/?ht_kb=dependabot-integration)。
- **Dependabot secrets**：**Dependabot 密钥**。管理 Dependabot 用于执行操作的敏感信息（如访问私有依赖库的 token）。
- **Secret scanning alerts**：**密钥扫描警报**。管理 GitHub 扫描到仓库中明文存储的敏感信息（如密码、API 密钥、私钥）的警报 。
- **Secret scanning alert dismissal requests**：**密钥扫描警报关闭请求**。允许处理用户提出的关闭某个“密钥扫描警报”的请求。
- **Secret scanning push protection bypass requests**：**密钥扫描推送保护绕过请求**。当有人试图提交包含密钥的代码时，此权限控制是否处理其提出的绕过拦截的请求。

### 🔧 协作与流程管理

- **Issues**：**议题**。控制对 Issues（问题追踪、任务管理）的读写权限，包括创建、编辑、关闭和分配 issue [\-1](https://arinco.com.au/blog/changes-to-the-default-github_token-permissions/#content)。
- **Pull requests**：**拉取请求**。控制对 Pull requests（PR）的管理权限，包括创建、审查、合并和修改 PR [\-1](https://arinco.com.au/blog/changes-to-the-default-github_token-permissions/#content)[\-2](https://docs.amazonaws.cn/en_us/codebuild/latest/userguide/access-tokens-github.html)。
- **Discussions**：**讨论**。控制对仓库 Discussions（论坛式讨论区）的访问，用于社区互动、问答和公告。
- **Environments**：**环境**。管理 CI/CD 流程中定义的环境（如 `production`），包括配置其保护规则和必要的审查者。
- **Merge queues**：**合并队列**。管理“合并队列”功能，该功能通过自动将多个 PR 排队合并来确保 `main` 分支始终是可通过的。
- **Webhooks**：**Web 钩子**。管理仓库的 Webhooks，允许你在特定事件（如 push 或 PR）发生时，自动向外部服务发送 HTTP 请求 [\-2](https://docs.amazonaws.cn/en_us/codebuild/latest/userguide/access-tokens-github.html)。
- **Workflows**：**GitHub Actions 工作流**。管理 GitHub Actions 的工作流文件。允许创建、修改、触发和取消工作流运行 [\-1](https://arinco.com.au/blog/changes-to-the-default-github_token-permissions/#content)。

### ⚙️ 高级配置与管理

- **Administration**：**仓库管理**。最高级别的权限，控制仓库的设置、协作管理、分支保护规则和删除仓库等操作 [\-2](https://docs.amazonaws.cn/en_us/codebuild/latest/userguide/access-tokens-github.html)[\-4](https://wenku.csdn.net/answer/8486m7kdnr)。
- **Actions**：**GitHub Actions**。控制对 Actions 本身的设置管理，如管理仓库的 Action 权限、runner（运行器）和缓存 [\-1](https://arinco.com.au/blog/changes-to-the-default-github_token-permissions/#content)。
- **Codespaces**：**代码空间**。管理 GitHub Codespaces（云端开发环境）的整体访问权限。
- **Codespaces lifecycle admin**：**Codespaces 生命周期管理**。对 Codespaces 执行更高级的生命周期操作，如停止、启动或删除其他人的 codespace。
- **Codespaces metadata**：**Codespaces 元数据**。允许读取与 Codespaces 相关的元数据信息。
- **Codespaces secrets**：**Codespaces 密钥**。管理用于 Codespaces 的加密敏感信息（如环境变量）。
- **Custom properties**：**自定义属性**。管理仓库的自定义元数据，可用于对组织内的仓库进行分类和标记。
- **Repository security advisories**：**仓库安全公告**。允许创建和管理仓库的安全公告，用于私下讨论和修复安全漏洞。
- **Attestations**：**证明**。管理与软件供应链安全相关的“证明”信息，用于验证工件的来源和完整性。
- **Artifact metadata**：**工件元数据**。管理 GitHub Actions 生成的工作流产物（Artifacts）的元数据信息。
- **Agent tasks**：**Agent 任务**。管理某些 GitHub 高级功能或集成的代理任务（此功能较为特殊，通用性较低）。

### 👥 组织与集成相关

- **Organization administration**：**组织管理**。控制对 GitHub 组织账户的设置和策略的管理权限（通常在组织级别的 token 中出现）。
- **Organization announcements**：**组织公告**。允许管理在组织内广播的公告信息。
- **Organization custom org role**：**组织自定义角色**。管理组织内自定义角色的创建和配置。
- **Organization projects**：**组织项目**。控制对组织级别的 Projects（项目看板）的管理权限。
- **Organization secrets**：**组织密钥**。管理在组织级别设置的、可供多个仓库使用的加密密钥。
- **Organization variables**：**组织变量**。管理在组织级别设置的、可供多个仓库使用的通用配置变量。

### 📦 包与计费

- **Packages**：**GitHub Packages**。控制对 GitHub Packages（包管理服务）的访问，包括上传、下载和删除包 [\-1](https://arinco.com.au/blog/changes-to-the-default-github_token-permissions/#content)。
- **Billing**：**计费**。允许查看和修改账户的计费信息、使用情况和订阅。

---

### 💡 一个实用的策略建议

作为最佳实践，在分配权限时，建议遵循**最小权限原则**。

例如，如果你只需要创建一个 Token 来自动化读取 Issue 并回复，你可以这样配置：

- `Metadata`：Read-only (自动授予)
- `Issues`：Read and write
- 其他所有权限：No access

这种**精确控制**是细粒度令牌相比经典令牌的最大优势，能显著降低令牌泄露带来的安全风险[\-4](https://wenku.csdn.net/answer/8486m7kdnr)。

如果你的 Token 是用于 CI/CD 流水线（如 GitHub Actions）自动构建部署，通常需要开启 `Contents`（读写）、`Commit statuses`（读写）和 `Deployments`（读写）。如果涉及需要更新 GitHub Pages，则还需开启 `Pages` 权限。