# 隐私政策

最后更新：2026-06-13

本隐私政策适用于 Coastline，一个本地优先的长篇写作管理桌面工具。

## 核心说明

Coastline 是本地优先软件。

在当前版本中，用户数据只会在以下位置处理：

1. 用户自己的本地设备；
2. 用户自行配置的第三方模型 API 服务商。

当前版本支持 OpenAI-compatible provider 配置；用户可以根据自己的服务商填写 Base URL、API key 和模型名称。项目默认示例模型为 `deepseek-v4-pro`，相关 API 请求由用户自行配置的第三方模型 API key 发起。

开发者不运营任何用于 Coastline 核心功能的云端服务器，不论该服务器位于中国大陆境内或境外。

开发者不提供任何 Coastline 云账号系统，不论该账号系统位于中国大陆境内或境外。

开发者无法通过 Coastline 本应用主动获取用户的项目内容、章节文本、API key、导出文件或其他隐私信息。

第三方模型服务商对其自身服务中的数据处理承担责任；Coastline 开发者无法代表第三方服务商作出承诺。

## 本地优先存储

Coastline 将写作项目保存在用户本机。

项目文件、章节、时间线、事实记录、问题记录、导出文件和相关配置默认保存在本地，除非用户自行移动、上传、备份或分享这些文件。

项目文件（JSON 格式）是 source of truth。

## 本地 SQLite 索引与分析缓存

Coastline 2.0.0 使用本地 SQLite 索引和缓存来加速检索和分析。这些是从项目文件派生的可重建索引/缓存，不是项目主存储。项目文件仍是 source of truth。索引和缓存可以随时从项目文件重建，不会向 Coastline developer 或任何 Coastline-operated server 发送。

## 本地 ONNX Reranker

Coastline 2.0.0 包含一个本地 ONNX reranker（bundled_models/reranker-v8/），在用户触发 LLM 分析前对候选上下文进行本地重排。

Reranker 的工作方式：

- 在用户设备本地运行，使用 ONNX Runtime；
- 读取本地 SQLite 索引中的项目文本片段（候选 chunks）；
- 评估候选片段与当前章节的相关性，选出 top-K 最相关片段；
- reranker 不生成正文，不直接写入 timeline / fact bank / state panel / issues，不绕过用户确认；
- reranker 不会把文本发送给 Coastline developer 或 Coastline-operated server。

但被 reranker 选中的上下文，可能作为用户主动触发的 LLM 分析请求的一部分，发送给用户配置的第三方模型 API。这些请求由第三方模型服务商处理，其隐私政策和服务条款由对应服务商制定。

Reranker 上游 base model 为 hfl/rbt3（HFL，Apache-2.0），bundled artifact 为 fine-tuned + ONNX 转换派生模型。

## 没有 Coastline 云账号

Coastline 目前不提供云账号系统。

用户不需要注册 Coastline 账号，也不需要登录开发者提供的服务器。

开发者不运营用于保存用户项目、章节、草稿、导出文件、API key 或使用记录的 Coastline 云端服务器。

## 模型 API 请求

Coastline 的主要模型分析功能依赖用户自行配置的第三方模型 API key。

Coastline 不提供内置模型服务，也不提供由开发者运营的模型代理服务器。

如果用户不配置第三方模型 API key，Coastline 的模型分析相关功能将无法使用或无法完整使用。

只有当用户配置 API key 并使用相关分析功能时，Coastline 才会向用户配置的第三方模型 API 发起请求。

当用户触发 AI 分析或其他依赖模型的功能时，相关项目文本可能会发送到用户配置的第三方模型 API。这可能包括章节内容、项目背景、时间线信息、事实记录、问题记录和相关写作上下文。

这些数据如何被处理，取决于用户选择和配置的第三方模型服务商的隐私政策、服务条款和数据处理规则。

Coastline 开发者无法控制第三方模型服务商的数据处理方式，也无法代替第三方模型服务商作出隐私承诺。

## API key

API key 由用户自行配置，并保存在用户本机。

开发者不会主动收集、上传、查看或保存用户的 API key。

用户需要自行保管 API key，监控 API 使用情况，并承担所选模型服务商产生的 API 费用。

当前版本中，Coastline 开发者不向用户收取软件下载费、订阅费、账号费或模型调用费。用户配置第三方模型 API 后产生的 API 使用费用，由对应第三方模型服务商收取，并由用户自行承担。Coastline 开发者不会通过 Coastline 本应用代收、加价转售或转售第三方模型 API 调用。

## 开发者无法主动获取的信息

在当前版本设计下，开发者无法通过 Coastline 本应用主动获取以下信息：

- 用户的项目文件；
- 用户的章节文本；
- 用户的时间线、事实库和问题记录；
- 用户的导出文件；
- 用户配置的 API key；
- 用户通过 Coastline 本应用产生或保存的本地文件路径；
- 用户的使用记录；
- 用户的个人身份信息。

除非用户主动通过邮件、聊天、Issue、截图、日志、压缩包或其他方式发送给开发者，否则开发者不会接触这些内容。

## 诊断与遥测

Coastline 目前不包含由开发者运营的分析、遥测、用户追踪、崩溃报告或远程日志服务。

如果用户主动提交 bug 反馈、截图、日志或项目文件，用户应自行确认其中是否包含敏感信息。

## 敏感内容

用户不应处理自己无权处理的内容。

除非用户理解并接受所选模型服务商的规则和风险，否则不应将高度敏感、机密、私人、违法或受监管的内容提交给第三方模型 API。

## 用户责任

用户需要自行备份写作项目和导出文件。

Coastline 是独立开发的桌面应用（independently developed desktop application），正在积极演进中，可能包含 bug。

用户需要自行决定是否信任本软件、是否配置第三方模型 API，以及是否将特定文本提交给第三方模型服务。

## 联系方式

如有问题、反馈或与本 release 相关的移除请求，请通过官方 GitHub 仓库的 Issues、Releases 页面或其他公开联系方式联系开发者。

---

# Privacy Policy

Last updated: 2026-06-13

This privacy policy applies to Coastline, a local-first desktop writing system.

## Core statement

Coastline is local-first software.

In the current version, user data is processed only in the following places:

1. the user's own local device;
2. the third-party model API provider configured by the user.

The current version supports OpenAI-compatible provider configuration. Users may configure the Base URL, API key, and model name for their chosen provider. The default example model is `deepseek-v4-pro`, and related API requests are made with the third-party model API key configured by the user.

The developer does not operate any cloud server for Coastline's core application features, whether inside or outside mainland China.

The developer does not provide any Coastline cloud account system, whether inside or outside mainland China.

Through the Coastline application itself, the developer cannot actively access the user's project content, chapter text, API key, exported files, or other private information.

Third-party model providers are responsible for their own data handling practices; the Coastline developer cannot make commitments on their behalf.

## Local-first storage

Coastline stores writing projects on the user's local machine.

Project files, chapters, timelines, fact records, issue records, exported files, and related settings are stored locally by default, unless the user manually moves, uploads, backs up, or shares them.

Project files (JSON format) are the source of truth.

## Local SQLite index and analysis cache

Coastline 2.0.0 uses a local SQLite index and cache to accelerate retrieval and analysis. These are rebuildable indexes derived from project files; they are not the primary project store. Project files remain the source of truth. The index and cache can be rebuilt from project files at any time and are never sent to Coastline developers or any Coastline-operated server.

## Local ONNX reranker

Coastline 2.0.0 includes a local ONNX reranker (bundled_models/reranker-v8/) that ranks candidate context locally before user-triggered LLM analysis.

How the reranker works:

- It runs on the user's local device, using ONNX Runtime;
- It reads project text excerpts (candidate chunks) from the local SQLite index;
- It evaluates the relevance of each candidate to the current chapter and selects the top-K most relevant;
- The reranker does not generate text, does not directly write to the timeline / fact bank / state panel / issues, and does not bypass the user confirmation workflow;
- The reranker does not send text to Coastline developers or any Coastline-operated server.

However, context selected by the reranker may be sent to the user's configured third-party model API as part of a user-initiated LLM analysis request. Such requests are processed by the third-party model provider under its own privacy policy and terms of service.

The reranker upstream base model is hfl/rbt3 (HFL, Apache-2.0). The bundled artifact is a fine-tuned and ONNX-converted derived model.

## No Coastline cloud account

Coastline does not currently provide a cloud account system.

Users do not need to register a Coastline account or log in to any server provided by the developer.

The developer does not operate a Coastline cloud server for storing user projects, chapters, drafts, exported files, API keys, or usage records.

## Model API requests

Coastline's primary model-analysis features depend on a third-party model API key configured by the user.

Coastline does not provide a built-in model service and does not operate a model proxy server controlled by the developer.

If the user does not configure a third-party model API key, Coastline's model-analysis features will be unavailable or not fully usable.

Only when the user configures an API key and uses related analysis features does Coastline send requests to the third-party model API configured by the user.

When the user triggers AI analysis or other model-dependent features, relevant project text may be sent to the third-party model API configured by the user. This may include chapter content, project background, timeline information, fact records, issue records, and related writing context.

The handling of such data is governed by the privacy policy, terms of service, and data processing rules of the third-party model provider selected and configured by the user.

The Coastline developer does not control how third-party model providers process data and cannot make privacy commitments on behalf of those providers.

## API keys

API keys are configured by the user and stored on the user's local machine.

The developer does not actively collect, upload, view, or store user API keys.

Users are responsible for keeping their API keys secure, monitoring API usage, and paying any API costs charged by their chosen model provider.

In the current release, the Coastline developer does not charge users any software download fee, subscription fee, account fee, or model usage fee. Any API usage fees incurred through third-party model APIs configured by the user are charged by the corresponding third-party model provider and are the user's responsibility. The Coastline developer does not collect, mark up, resell, or broker third-party model API usage through the Coastline application.

## Information the developer cannot actively access

In the current version design, the developer cannot actively access the following information through the Coastline application itself:

- user project files;
- chapter text;
- timelines, fact records, and issue records;
- exported files;
- configured API keys;
- local file paths generated or stored through the Coastline application itself;
- usage records;
- personal identity information.

Unless the user voluntarily sends such information to the developer through email, chat, Issues, screenshots, logs, archives, or other channels, the developer does not have access to it.

## Diagnostics and telemetry

Coastline does not currently include analytics, telemetry, user tracking, crash reporting, or remote logging services operated by the developer.

If users voluntarily submit bug reports, screenshots, logs, or project files, they should check whether those materials contain sensitive information.

## Sensitive content

Users should not process content that they do not have the right to process.

Users should not submit highly sensitive, confidential, private, illegal, or regulated content to third-party model APIs unless they understand and accept the rules and risks of the selected provider.

## User responsibility

Users are responsible for backing up their writing projects and exported files.

Coastline is an independently developed desktop application that is actively evolving and may contain bugs.

Users are responsible for deciding whether to trust this software, whether to configure a third-party model API, and whether to submit specific text to third-party model services.

## Contact

For questions, feedback, or removal requests related to this release, please contact the developer through Issues, the Releases page, or other public contact methods on the official GitHub repository.