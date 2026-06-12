# Coastline Releases

This repository stores public release artifacts and release metadata for Coastline.

## Current release

### Coastline 1.4.0

Artifacts are stored in:

`releases/1.4.0/`

Current release artifacts:

- `Coastline-1.4.0-macOS.dmg`
- `CoastlineSetup-1.4.0-win-x64.exe`

macOS SHA256:

`8d1b703f938f684e5fcee6c427cbf5f5265bef45b72f4d2cacef4e5d7cac4c23`

Windows SHA256:

`54113161d413eac9d43388995fc78c27037d8d93dbe6ad5a03d87f601073cc43`


# Coastline

**A Narrative Control System**

## Official Website / 官网

https://usecoastline.com

## Download / 下载

**Latest release / 最新版本：Coastline 1.4.0 Beta**

**GitHub Releases / 安装包下载：**  
https://github.com/AlbertYang514/coastline-releases/releases/tag/v1.4.0

当前提供：

- macOS：`Coastline-1.4.0-macOS.dmg`
- Windows：`CoastlineSetup-1.4.0-win-x64.exe`

安装包请从 GitHub Releases 下载。文件校验与版本索引：

- `catalog.json`

---

---

## Coastline 1.4.0 更新内容

Coastline 1.4.0 Beta 是一次 Local Intelligence 功能增强与稳定性更新。它不是单纯换版本号，也不只是打包修正；本版本重点改进长篇项目分析、质量问题识别、识别规则兼容、token 控制和本地结果写入安全。

### 新增 / 增强

- 新增 AI 分析状态提示，让章节分析、批量处理和项目初始化过程更清楚。
- 新增分析预设与 max token 控制，方便在速度、成本和分析深度之间切换。
- 新增章节分析缓存，减少重复分析相同内容时的不必要模型调用。
- 新增 Recognition Rules / 识别规则兼容层，使识别规则可以更稳定地参与当前分析流程。
- 扩展语言与行文质量检查，用于识别非事实类的 prose quality / narrative quality 问题。
- 改进时间线上下文处理，使用 compact timeline digest 和相关事件检索，降低长篇项目 token 压力。
- 新增用户流程模拟脚本与更完整的 release sanity check，覆盖缓存、检索、质量检查和识别规则兼容。

### 修复 / 加固

- 改进分析文本质量处理，减少模型输出格式或文本质量异常带来的后续问题。
- 强化本地分析结果合并逻辑，使事实、时间线、人物状态和 issue 的写入边界更保守。
- 收紧 issue 解决流程，避免自动破坏性关闭或删除问题记录。
- 修复 Windows installer 产物命名检查不一致的问题。
- 统一 1.4.0 macOS / Windows 安装包命名和校验信息。

## 产品介绍

Coastline 是一个本地优先的长篇写作管理桌面工具，用于帮助作者管理章节、时间线、事实库、连续性问题、叙事路径和导出文件。

它不是 AI 代写工具。Coastline 的目标不是替作者写故事，而是帮助作者保留对叙事结构、人物状态、事实一致性和文本版本的控制权。

Coastline 适合用于长篇小说、系列故事、剧本、世界观项目和其他需要长期维护叙事连续性的写作项目。

Coastline 目前是个人维护的早期 beta 项目，不是商业服务，也不提供云同步、账号系统或在线存储。

---

## 核心功能

Coastline 主要关注：

- 章节管理；
- 项目背景与设定管理；
- 时间线追踪；
- 事实库与连续性追踪；
- 人物状态与别名管理；
- 叙事冲突和问题记录；
- 多路径 / 分支路线；
- 版本确认与回滚；
- Word / PDF 导出；
- 中文 PDF 导出支持；
- 本地优先存储；
- 用户自行配置模型 API key。

Coastline 集成 LLM 分析能力，用于辅助提取事实、更新时间线、识别状态变化、检查潜在矛盾，并提示后续写作风险。

LLM 的作用是帮助作者维护叙事结构和一致性，而不是替作者生成正文或接管创作判断。

Coastline 是写作管理工具，不是自动写作工具，也不是论文、作业或商业文案代写工具。

---

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

---

## macOS 安装说明

1. 下载 `Coastline-1.4.0-macOS.dmg`。
2. 打开 DMG 文件。
3. 将 `Coastline.app` 拖入“应用程序”文件夹。
4. 从"应用程序"中打开 Coastline。

### macOS 安全提示

Coastline 目前还没有进行 Apple 开发者签名和 notarization 公证。

如果你从 GitHub 下载 macOS 版本，系统可能直接提示：

"应用已损坏，无法打开"。

这通常是 macOS Gatekeeper 对未签名应用的拦截结果，不代表安装包一定真的损坏。

如果你确认安装包来自官方 Release 页面，可以在终端运行：

xattr -dr com.apple.quarantine "/Applications/Coastline.app"

然后打开应用：

open "/Applications/Coastline.app"

如果终端提示权限不足，可以改用：

sudo xattr -dr com.apple.quarantine "/Applications/Coastline.app"

请只从官方 Release 页面下载安装包。若你不信任来源，请不要安装。

---

## Windows 安装说明

1. 下载 `CoastlineSetup-1.4.0-win-x64.exe`。
2. 运行安装包。
3. 按安装向导完成安装。
4. 从开始菜单或桌面快捷方式打开 Coastline。

### Windows 安全提示

Windows 版目前没有代码签名。

第一次运行安装包时，Windows Defender 或 SmartScreen 可能会显示安全提示。这是当前 beta 版的已知情况。

请只从官方 Release 页面下载安装包。若你不信任来源，请不要安装。

---

## 使用前建议

- 自行准备模型 API key。
- 先用测试文本试用，不要一开始就导入唯一重要稿件。
- 定期备份项目文件。
- 不要处理自己无权处理的文本。
- 不要将高度敏感、机密、私人、违法或受监管的内容提交给第三方模型 API，除非你理解并接受相关风险。

---

## Issues 与公开反馈

Issues 是公开的。请不要在 Issues 中发布 API key、私人写作项目、敏感日志、个人信息，或你无权分享的受版权保护文本。

包含密钥、敏感信息、攻击性内容、垃圾信息或无关内容的 issue 可能会被编辑、关闭或删除。

---

## 文档

- `PRIVACY.md`：隐私政策；
- `LICENSE.txt`：闭源软件授权；
- `EULA.txt`：最终用户许可协议；
- `CHANGELOG.md`：更新日志；
- `THIRD-PARTY-NOTICES.txt`：第三方开源组件版权声明；
- `catalog.json`：版本索引与安装包校验信息。

---

## English Summary

Coastline is a local-first desktop writing system for long-form narrative projects.

It helps writers manage chapters, timelines, fact records, continuity issues, narrative paths, version confirmation, rollback, and exports.

Coastline is not an AI ghostwriter. It is designed to help writers keep control of narrative structure, character states, factual continuity, and text versions.

Current release:

- **Coastline 1.3.2 Beta**
- Official website: https://usecoastline.com
- Download: https://github.com/AlbertYang514/coastline-releases/releases/tag/v1.4.0

Available builds:

- macOS: `Coastline-1.4.0-macOS.dmg`
- Windows: `CoastlineSetup-1.4.0-win-x64.exe`

Coastline stores project files locally by default. It does not provide cloud sync, user accounts, or online storage.

Coastline does not provide a built-in model service. Model-analysis features require a user-configured third-party model API key.

Coastline is currently unsigned on both macOS and Windows. macOS Gatekeeper and Windows SmartScreen may show security warnings.

Coastline is proprietary, closed-source, and binary-only. Please read `LICENSE.txt`, `EULA.txt`, and `PRIVACY.md` before using it.
