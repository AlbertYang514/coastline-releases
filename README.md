# Coastline

**A Narrative Control System**

> 下载 Coastline 2.0.0 / Download Coastline 2.0.0:  
> https://github.com/AlbertYang514/coastline-releases/releases/tag/v2.0.0
>
> 官网 / Official websites:  
> 中国大陆用户建议访问：https://usecoastline.cn  
> Users outside mainland China are recommended to visit: https://usecoastline.com

Coastline 是一个本地优先的长篇写作管理桌面工具，用于帮助作者管理章节、时间线、事实库、连续性问题、人物状态、项目版本和导出文件。

它不是 AI 代写工具。Coastline 的目标不是替作者写故事，而是帮助作者保留对叙事结构、人物状态、事实一致性和文本版本的控制权。

> Coastline 目前是个人维护的早期 beta 项目，不是商业服务，也不提供云同步、账号系统或在线存储。

## 产品介绍

Coastline 是一个面向长篇叙事项目的本地优先桌面写作系统，适用于小说、剧本、系列文本、世界观设定和多路线叙事项目。

它不是普通文本编辑器，也不是 AI 代写工具。Coastline 更像一个本地的叙事控制台：用于管理章节、时间线、事实设定、人物状态、连续性问题、路径路线、版本确认、回滚和内容导出。

Coastline 集成 LLM 分析能力，用于辅助提取事实、更新时间线、识别状态变化、检查潜在矛盾，并提示后续写作风险。LLM 的作用是帮助作者维护叙事结构和一致性，而不是替作者生成正文或接管创作判断。

Coastline 2.0.0 还加入了本地 SQLite 索引/缓存和本地 ONNX 模型路径，用于在正式分析前整理和排序相关上下文。这个本地模型不生成正文，也不替作者做创作判断。

当前版本：**Coastline 2.0.0**

---

## Coastline 2.0.0 更新

Coastline 2.0.0 是一次面向长篇项目的基础能力更新，重点是让分析过程更清楚、上下文选择更稳、本地项目管理更完整。

主要变化：

- 新增章节分析和批量分析的真实流式反馈；
- 新增本地 ONNX reranker，用于在正式分析前排序相关上下文；
- 新增本地 SQLite index/cache 层，用于更快访问项目上下文；
- 新增项目归档管理；
- 新增回收站、恢复和永久删除；
- 新增分卷管理；
- 新增引导式更新检查；
- 改进 Windows 启动加载体验；
- 打包随附 `LICENSE.txt`、`EULA.txt`、`PRIVACY.md`、`CHANGELOG.md` 和第三方 notices。

本地 ONNX 模型只负责上下文与时间线线索的筛选和排序。它在用户设备上运行，不需要 CUDA，不需要独立显卡，也不占用 GPU。正式 AI 分析仍然依赖用户自行配置的第三方模型 API。

## 核心定位

Coastline 适合用于长篇小说、系列故事、剧本、世界观项目和其他需要长期维护叙事连续性的写作项目。

它主要关注：

- 章节管理；
- 项目背景与设定管理；
- 时间线追踪；
- 事实库与连续性追踪；
- 人物状态与别名管理；
- 叙事冲突和问题记录；
- 多路径 / 分支路线；
- 版本确认与回滚；
- 项目归档、回收站、恢复与永久删除；
- 分卷管理；
- Word / PDF 导出；
- 中文 PDF 导出支持；
- 本地优先存储；
- 用户自行配置模型 API key。

Coastline 是写作管理工具，不是自动写作工具，也不是论文、作业或商业文案代写工具。

## 下载

请从本仓库的 GitHub Releases 页面下载 Coastline。

当前提供：

- macOS：`Coastline-2.0.0-macOS.dmg`
- Windows：`CoastlineSetup-2.0.0-win-x64.exe`

安装包请从 GitHub Releases 下载。安装包二进制文件不提交到 Git 仓库。

版本索引与文件校验信息见：

- `catalog.json`
- Release 页面中的 checksum / `.sha256` 文件

## 重要说明

### 本地优先

Coastline 将项目文件默认保存在用户本机。

开发者不运营任何用于 Coastline 核心功能的云端服务器，不论该服务器位于中国大陆境内或境外。

开发者不提供任何 Coastline 云账号系统，不论该账号系统位于中国大陆境内或境外。

开发者无法通过 Coastline 本应用主动获取用户的项目内容、章节文本、API key、导出文件或其他隐私信息。

Coastline 2.0.0 的 SQLite 索引/缓存和本地 ONNX 模型在用户设备上运行。本地模型只负责上下文与时间线线索的筛选和排序，不生成正文，不替作者判断故事。

### 第三方模型 API

Coastline 不提供内置云端模型服务，也不提供由开发者运营的模型代理服务器。

Coastline 的主要模型分析功能依赖用户自行配置的第三方模型 API key。当前版本支持 OpenAI-compatible provider 配置。用户可以根据自己的服务商填写 Base URL、API key 和模型名称。

如果用户不配置可用的第三方模型 API key，Coastline 的本地项目管理、章节管理、索引、归档、回收站和导出等基础功能仍可使用；模型分析、事实核查、时间线提取、人物别名建议等依赖模型的功能将无法使用或无法完整使用。

当用户运行 AI 分析或其他依赖模型的功能时，相关项目文本可能会发送到用户配置的第三方模型 API。API 使用费用、可用性、数据处理方式和服务条款由对应第三方模型服务商决定。

当前版本中，Coastline 开发者不向用户收取软件下载费、订阅费、账号费或模型调用费。用户配置第三方模型 API 后产生的 API 使用费用，由对应第三方模型服务商收取，并由用户自行承担。Coastline 开发者不会通过 Coastline 本应用代收、加价转售或转售第三方模型 API 调用。

使用前请阅读 `PRIVACY.md`。

### 闭源与授权

Coastline 是闭源、专有、仅发布二进制安装包的软件。

源码不公开。公开发布安装包不代表开放源码，也不代表允许复制、修改、逆向、重新打包、二次分发或商业使用。

使用前请阅读：

- `LICENSE.txt`
- `EULA.txt`

### Beta 版本

Coastline 当前是早期 beta 版本，可能存在 bug。

请在使用前备份你的写作项目、导出文件和重要资料。不要把唯一副本只保存在 Coastline 项目目录中。

## macOS 安装说明

1. 下载 `Coastline-2.0.0-macOS.dmg`。
2. 打开 DMG 文件。
3. 将 `Coastline.app` 拖入“应用程序”文件夹。
4. 从“应用程序”中打开 Coastline。

### macOS 安全提示

Coastline 目前还没有进行 Apple 开发者签名和 notarization 公证。

第一次打开 macOS 版时，系统可能提示：

- “Apple 无法检查其是否包含恶意软件”；
- “应用已损坏，无法打开”；
- “无法验证开发者”。

这是当前的已知情况。

推荐打开方式：

请在终端运行：

```bash
xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

<<<<<<< HEAD
如果系统仍提示“应用已损坏”，可以在终端运行：
=======
如果 Coastline 没有安装在“应用程序”文件夹，请把上面的路径替换为实际的 `Coastline.app` 路径。

必要时也可以使用：
>>>>>>> e31b40a (docs: clarify cloud server statement and website links)

```bash
sudo xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

请只从官方 Release 页面下载安装包。若你不信任来源，请不要安装。

## Windows 安装说明

1. 下载 `CoastlineSetup-2.0.0-win-x64.exe`。
2. 运行安装包。
3. 按安装向导完成安装。
4. 从开始菜单或桌面快捷方式打开 Coastline。

### Windows 安全提示

Windows 版目前没有代码签名。

第一次运行安装包时，Windows Defender 或 SmartScreen 可能会显示安全提示。这是当前 beta 版的已知情况。

请只从官方 Release 页面下载安装包。若你不信任来源，请不要安装。

## 使用前建议

- 自行准备模型 API key。
- 先用测试文本试用，不要一开始就导入唯一重要稿件。
- 定期备份项目文件。
- 不要处理自己无权处理的文本。
- 不要将高度敏感、机密、私人、违法或受监管的内容提交给第三方模型 API，除非你理解并接受相关风险。

## Issues 与公开反馈

Issues 是公开的。请不要在 Issues 中发布 API key、私人写作项目、敏感日志、个人信息，或你无权分享的受版权保护文本。

包含密钥、敏感信息、攻击性内容、垃圾信息或无关内容的 issue 可能会被编辑、关闭或删除。

## 文档

- `PRIVACY.md`：隐私政策；
- `LICENSE.txt`：闭源软件授权；
- `EULA.txt`：最终用户许可协议；
- `CHANGELOG.md`：更新日志；
- `THIRD-PARTY-NOTICES.txt`：第三方开源组件版权声明；
- `THIRD-PARTY-LICENSES.json`：第三方依赖许可数据；
- `catalog.json`：版本索引与安装包校验信息。

---

# Coastline

**A Narrative Control System**

> Download Coastline 2.0.0:  
> https://github.com/AlbertYang514/coastline-releases/releases/tag/v2.0.0
>
> Official websites:  
> Mainland China: https://usecoastline.cn  
> Outside mainland China: https://usecoastline.com

Coastline is a local-first desktop writing system for long-form narrative projects.

It helps writers manage chapters, timelines, fact records, continuity issues, character state, project versions, and exports. It is not an AI ghostwriter. Coastline is designed to help writers keep control of narrative structure, character states, factual continuity, and text versions.

> Coastline is currently a personally maintained early beta project. It is not a commercial service and does not provide cloud sync, user accounts, or online storage.

## Product overview

Coastline is a local-first desktop writing system for long-form narrative projects, including novels, screenplays, serial fiction, worldbuilding projects, and branching narrative work.

It is not a generic text editor and it is not an AI ghostwriter. Coastline is closer to a local narrative control console: it helps manage chapters, timelines, factual settings, character states, continuity issues, narrative paths, version confirmation, rollback, and exports.

Coastline integrates LLM-based analysis to help extract facts, update timelines, identify state changes, detect potential contradictions, and surface future writing risks. The role of the LLM is to support narrative continuity and structural review, not to replace the author's writing or creative judgment.

Coastline 2.0.0 also includes a local SQLite index/cache layer and a local ONNX model path. These features help organize and rank relevant context before formal analysis. The local model does not generate prose and does not make creative decisions for the author.

Current release: **Coastline 2.0.0**

---

## Coastline 2.0.0 changes

Coastline 2.0.0 is a foundation update for long-form projects. It focuses on clearer analysis progress, steadier context selection, and fuller local project management.

Main changes:

- real streamed feedback for chapter analysis and batch analysis;
- bundled local ONNX reranker for ranking relevant context before formal analysis;
- local SQLite index/cache layer for faster project context access;
- project archive management;
- trash, restore, and permanent delete workflows;
- volume grouping for long projects;
- guided update check;
- improved Windows startup loading experience;
- packaged `LICENSE.txt`, `EULA.txt`, `PRIVACY.md`, `CHANGELOG.md`, and third-party notices.

The local ONNX model only ranks context and timeline clues. It runs on the user's device, does not require CUDA, does not require a dedicated GPU, and does not use GPU resources. Formal AI analysis still depends on a third-party model API configured by the user.

## What Coastline is for

Coastline is designed for long-form novels, serial fiction, screenplays, worldbuilding projects, and other writing projects that require long-term narrative continuity management.

It focuses on:

- chapter management;
- project background and setting management;
- timeline tracking;
- fact and continuity tracking;
- character state and alias management;
- narrative issue tracking;
- multiple paths / branches;
- version confirmation and rollback;
- project archive, trash, restore, and permanent delete;
- volume grouping;
- Word / PDF export;
- Chinese PDF export support;
- local-first storage;
- user-configured model API keys.

Coastline is a writing management tool. It is not an automatic writing tool, a homework generator, or a commercial copywriting ghostwriter.

## Downloads

Please download Coastline from the GitHub Releases page of this repository.

Available builds:

- macOS: `Coastline-2.0.0-macOS.dmg`
- Windows: `CoastlineSetup-2.0.0-win-x64.exe`

Installers should be downloaded from GitHub Releases. Installer binaries are not committed to the Git repository.

Release metadata and verification information:

- `catalog.json`
- checksum / `.sha256` files on the Release page

## Important notes

### Local-first

Coastline stores project files locally on the user's machine by default.

The developer does not operate any cloud server for Coastline's core application features, whether inside or outside mainland China.

The developer does not provide any Coastline cloud account system, whether inside or outside mainland China.

Through the Coastline application itself, the developer cannot actively access the user's project content, chapter text, API key, exported files, or other private information.

In Coastline 2.0.0, the SQLite index/cache and local ONNX model run on the user's device. The local model only ranks context and timeline clues; it does not generate prose or make creative decisions for the author.

### Third-party model API

Coastline does not provide a built-in cloud model service and does not operate a model proxy server controlled by the developer.

Coastline's primary model-analysis features depend on a third-party model API key configured by the user. The current version supports OpenAI-compatible provider configuration. Users can provide the Base URL, API key, and model name for their provider.

If the user does not configure a usable third-party model API key, Coastline's local project management, chapter management, index, archive, trash, and export features remain available. Model analysis, fact checking, timeline extraction, character alias suggestions, and other model-dependent features will be unavailable or not fully usable.

When the user runs AI analysis or other model-dependent features, relevant project text may be sent to the third-party model API configured by the user. API usage, costs, availability, data handling, and terms are governed by the corresponding third-party model provider.

In the current release, the Coastline developer does not charge users any software download fee, subscription fee, account fee, or model usage fee. Any API usage fees incurred through third-party model APIs configured by the user are charged by the corresponding third-party model provider and are the user's responsibility. The Coastline developer does not collect, mark up, resell, or broker third-party model API usage through the Coastline application.

Please read `PRIVACY.md` before using the software.

### Closed source and license

Coastline is proprietary, closed-source, binary-only software.

The source code is not publicly available. Public access to the installer does not grant permission to copy, modify, reverse engineer, repackage, redistribute, or commercially use the software.

Please read:

- `LICENSE.txt`
- `EULA.txt`

### Beta release

Coastline is currently an early beta release and may contain bugs.

Please back up your writing projects, exported files, and important materials before using it. Do not keep the only copy of important work inside a Coastline project folder.

## macOS installation

1. Download `Coastline-2.0.0-macOS.dmg`.
2. Open the DMG file.
3. Move `Coastline.app` to the `Applications` folder.
4. Open Coastline from `Applications`.

### macOS Gatekeeper notice

Coastline is currently not code-signed or notarized.

When opening the macOS app for the first time, macOS may show warnings such as:

- "Coastline" cannot be opened because Apple cannot check it for malicious software.
- "Coastline" is damaged and can't be opened.
- The developer cannot be verified.

This is expected for the current beta release.

Recommended opening method:

Please run this command in terminal:

```bash
xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

If macOS still reports that the app is damaged, advanced users may remove the quarantine attribute manually:

```bash
sudo xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

If Coastline is installed somewhere other than the `Applications` folder, replace the path above with the actual `Coastline.app` path.

If needed, you may also run:

```bash
sudo xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

Only install Coastline if you downloaded it from the official release page and trust the developer.

## Windows installation

1. Download `CoastlineSetup-2.0.0-win-x64.exe`.
2. Run the installer.
3. Follow the installation wizard.
4. Open Coastline from the Start menu or desktop shortcut.

### Windows security notice

The Windows build is currently unsigned.

Windows Defender or SmartScreen may show a warning when opening the installer for the first time. This is expected for the current beta release.

Only install Coastline if you downloaded it from the official release page and trust the developer.

## Before using

- Prepare your own model API key.
- Try the app with test text first.
- Back up project files regularly.
- Do not process text that you do not have the right to process.
- Do not submit highly sensitive, confidential, private, illegal, or regulated content to third-party model APIs unless you understand and accept the related risks.

## Issues and public feedback

Issues are public. Please do not post API keys, private writing projects, sensitive logs, personal data, or copyrighted text that you do not have the right to share.

Issues containing secrets, sensitive data, abusive content, spam, or off-topic material may be edited, closed, or removed.

## Documents

- `PRIVACY.md`: Privacy Policy
- `LICENSE.txt`: Proprietary Software License
- `EULA.txt`: End User License Agreement
- `CHANGELOG.md`: Changelog
- `THIRD-PARTY-NOTICES.txt`: Third-party notices
- `THIRD-PARTY-LICENSES.json`: Third-party dependency license data
- `catalog.json`: Release metadata and installer verification information
