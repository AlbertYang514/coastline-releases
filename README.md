# Coastline

**A Narrative Control System**

> 下载 Coastline 1.3.0 Beta / Download Coastline 1.3.0 Beta:  
> https://github.com/AlbertYang514/coastline-releases/releases/tag/v1.3.0

Coastline 是一个本地优先的长篇写作管理桌面工具，用于帮助作者管理章节、时间线、事实库、连续性问题和导出文件。

它不是 AI 代写工具。Coastline 的目标不是替作者写故事，而是帮助作者保留对叙事结构、人物状态、事实一致性和文本版本的控制权。

> Coastline 目前是个人维护的早期 beta 项目，不是商业服务，也不提供云同步、账号系统或在线存储。

## 产品介绍

Coastline 是一个面向长篇叙事项目的本地优先桌面写作系统，适用于小说、剧本、系列文本、世界观设定和多路线叙事项目。

它不是普通文本编辑器，也不是 AI 代写工具。Coastline 更像一个本地的叙事控制台：用于管理章节、时间线、事实设定、人物状态、连续性问题、路径路线、版本确认、回滚和内容导出。

Coastline 集成 LLM 分析能力，用于辅助提取事实、更新时间线、识别状态变化、检查潜在矛盾，并提示后续写作风险。LLM 的作用是帮助作者维护叙事结构和一致性，而不是替作者生成正文或接管创作判断。

当前版本：**Coastline 1.3.0 Beta**

---

## 核心定位

Coastline 适合用于长篇小说、系列故事、剧本、世界观项目和其他需要长期维护叙事连续性的写作项目。

它主要关注：

- 章节管理；
- 项目背景与设定管理；
- 时间线追踪；
- 事实库与连续性追踪；
- 叙事冲突和问题记录；
- Word / PDF 导出；
- 中文 PDF 导出支持；
- 本地优先存储；
- 用户自行配置模型 API key。

Coastline 是写作管理工具，不是自动写作工具，也不是论文、作业或商业文案代写工具。

## 下载

请从本仓库的 GitHub Releases 页面下载 Coastline。

当前提供：

- macOS：`Coastline-1.3.0-macOS.dmg`
- Windows：`Coastline-1.3.0-win-x64.exe`

## 重要说明

### 本地优先

Coastline 将项目文件默认保存在用户本机。

开发者不运营任何用于 Coastline 的云端服务器，不论该服务器位于中国大陆境内或境外。

开发者不提供任何 Coastline 云账号系统，不论该账号系统位于中国大陆境内或境外。

开发者无法通过 Coastline 本应用主动获取用户的项目内容、章节文本、API key、导出文件或其他隐私信息。

### 第三方模型 API

Coastline 不提供内置模型服务，也不提供由开发者运营的模型代理服务器。

Coastline 的主要模型分析功能依赖用户自行配置的第三方模型 API key。

当前版本支持 OpenAI-compatible provider 配置。用户可以根据自己的服务商填写 Base URL、API key 和模型名称。

如果用户不配置可用的第三方模型 API key，Coastline 的本地项目管理、章节管理和导出等基础功能仍可使用；模型分析、事实核查、时间线提取、人物别名建议等依赖模型的功能将无法使用或无法完整使用。

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

1. 下载 `Coastline-1.3.0-macOS.dmg`。
2. 打开 DMG 文件。
3. 将 `Coastline.app` 拖入“应用程序”文件夹。
4. 从“应用程序”中打开 Coastline。

### macOS 安全提示

Coastline 目前还没有进行 Apple 开发者签名和 notarization 公证。

如果你从 GitHub 下载 macOS 版本，系统可能直接提示：

“应用已损坏，无法打开”。

这通常是 macOS Gatekeeper 对未签名应用的拦截结果，不代表安装包一定真的损坏。

如果你确认安装包来自官方 Release 页面，可以在终端运行：

```bash
xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

如果终端提示权限不足，可以改用：

```bash
sudo xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

请只从官方 Release 页面下载安装包。若你不信任来源，请不要安装。

## Windows 安装说明

1. 下载 `Coastline-1.3.0-win-x64.exe`。
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
- `CHANGELOG.md`：更新日志。

---

# Coastline

**A Narrative Control System**

> Download Coastline 1.3.0 Beta:  
> https://github.com/AlbertYang514/coastline-releases/releases/tag/v1.3.0

Coastline is a local-first desktop writing system for long-form narrative projects.

It helps writers manage chapters, timelines, fact records, continuity issues, and exports. It is not an AI ghostwriter. Coastline is designed to help writers keep control of narrative structure, character states, factual continuity, and text versions.

> Coastline is currently a personally maintained early beta project. It is not a commercial service and does not provide cloud sync, user accounts, or online storage.

## Product overview

Coastline is a local-first desktop writing system for long-form narrative projects, including novels, screenplays, serial fiction, worldbuilding projects, and branching narrative work.

It is not a generic text editor and it is not an AI ghostwriter. Coastline is closer to a local narrative control console: it helps manage chapters, timelines, factual settings, character states, continuity issues, narrative paths, version confirmation, rollback, and exports.

Coastline integrates LLM-based analysis to help extract facts, update timelines, identify state changes, detect potential contradictions, and surface future writing risks. The role of the LLM is to support narrative continuity and structural review, not to replace the author's writing or creative judgment.

Current release: **Coastline 1.3.0 Beta**

---

## What Coastline is for

Coastline is designed for long-form novels, serial fiction, screenplays, worldbuilding projects, and other writing projects that require long-term narrative continuity management.

It focuses on:

- chapter management;
- project background and setting management;
- timeline tracking;
- fact and continuity tracking;
- narrative issue tracking;
- Word / PDF export;
- Chinese PDF export support;
- local-first storage;
- user-configured model API keys.

Coastline is a writing management tool. It is not an automatic writing tool, a homework generator, or a commercial copywriting ghostwriter.

## Downloads

Please download Coastline from the GitHub Releases page of this repository.

Available builds:

- macOS: `Coastline-1.3.0-macOS.dmg`
- Windows: `Coastline-1.3.0-win-x64.exe`

## Important notes

### Local-first

Coastline stores project files locally on the user's machine by default.

The developer does not operate any cloud server for Coastline, whether inside or outside mainland China.

The developer does not provide any Coastline cloud account system, whether inside or outside mainland China.

Through the Coastline application itself, the developer cannot actively access the user's project content, chapter text, API key, exported files, or other private information.

### Third-party model API

Coastline does not provide a built-in model service and does not operate a model proxy server controlled by the developer.

Coastline's primary model-analysis features depend on a third-party model API key configured by the user.

The current version supports OpenAI-compatible provider configuration. Users can provide their own Base URL, API key, and model name.

Without a valid third-party model API key, Coastline's local project management, chapter management, and export features remain available. Model-analysis features such as manuscript analysis, fact checking, timeline extraction, and character alias suggestions will be unavailable or not fully usable.

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

1. Download `Coastline-1.3.0-macOS.dmg`.
2. Open the DMG file.
3. Move `Coastline.app` to the `Applications` folder.
4. Open Coastline from `Applications`.

### macOS Gatekeeper notice

Coastline is currently not code-signed or notarized.

When downloaded from GitHub, macOS may report:

"Coastline" is damaged and can't be opened.

This is usually caused by macOS Gatekeeper blocking an unsigned app. It does not necessarily mean the installer is actually damaged.

If you downloaded Coastline from the official release page and trust this release, you can remove the quarantine attribute manually:

```bash
xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

If Terminal reports a permission error, try:

```bash
sudo xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

Only install Coastline if you downloaded it from the official release page and trust the developer.

## Windows installation

1. Download `Coastline-1.3.0-win-x64.exe`.
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