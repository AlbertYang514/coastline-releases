# 更新日志

## Coastline 1.3.1 Beta

Coastline 1.3.1 Beta 是 1.3.0 之后的发布修正版本，重点整理桌面应用图标、macOS / Windows 打包命名、发布文件结构、第三方开源组件声明，以及 Windows 后端端口行为。

本版本不引入新的核心写作功能，主要用于让公开 beta 安装包更稳定、更清晰、更适合作为当前推荐下载版本。

### 本版本重点

- 更新 Coastline 应用图标。
- 修复 macOS release 构建过程中图标源文件被旧资源覆盖的问题。
- 修复 macOS DMG release 文件命名，使其与公开发布资产命名保持一致。
- 确认 Windows 后端使用动态本地端口，避免固定占用 `8000`。
- 整理 Windows x64 安装包输出命名。
- 补充并随应用分发第三方开源组件版权声明。
- 整理 release repository 的下载文件、版本索引和公开说明文档。

### 修复 / 改进

- 修复 macOS 打包流程中 `AppIcon.appiconset` 可能被旧图标重新生成覆盖的问题。
- 修复 macOS DMG 默认输出为 `Coastline-1.3.1.dmg`，而不是公开发布所需 `Coastline-1.3.1-macOS.dmg` 的问题。
- 改进 release asset 命名一致性：
  - `Coastline-1.3.1-macOS.dmg`
  - `Coastline-1.3.1-win-x64.exe`
- 确认 Windows 端 `ncs-backend.exe` 启动后监听动态本地端口，而不是固定端口。
- 更新应用图标资源，用于 macOS App、Windows App 与安装包显示。
- 补充 `THIRD-PARTY-NOTICES.txt`，用于声明第三方开源组件版权信息。
- 整理 release repository README 与 catalog 信息，方便用户下载和校验安装包。

### 说明

- Coastline 仍然是本地优先、闭源、仅发布二进制安装包的软件。
- Coastline 不提供内置模型服务。
- 模型分析功能需要用户自行配置第三方模型 API key。
- macOS 与 Windows 构建目前均未签名。
- 用户应定期备份写作项目。
- 本版本主要是发布整理版本，不是功能大版本。

---

# Changelog

## Coastline 1.3.1 Beta

Coastline 1.3.1 Beta is a release-polish update after 1.3.0. It focuses on desktop app icons, macOS / Windows packaging names, release file structure, third-party open-source notices, and Windows backend port behavior.

This release does not introduce major new writing features. Its purpose is to make the public beta installers cleaner, more stable, and more suitable as the current recommended download.

### Highlights

- Updated the Coastline app icon.
- Fixed the macOS release build flow so the new icon source is not overwritten by old generated resources.
- Fixed macOS DMG release naming to match the public release asset name.
- Verified that the Windows backend uses a dynamic local port instead of fixed port `8000`.
- Cleaned up Windows x64 installer output naming.
- Added third-party open-source notices to the distributed application.
- Organized release repository downloads, catalog metadata, and public documentation.

### Fixed / Improved

- Fixed an issue where the macOS packaging flow could regenerate `AppIcon.appiconset` from an outdated icon source.
- Fixed macOS DMG output naming from `Coastline-1.3.1.dmg` to the public release name `Coastline-1.3.1-macOS.dmg`.
- Improved release asset naming consistency:
  - `Coastline-1.3.1-macOS.dmg`
  - `Coastline-1.3.1-win-x64.exe`
- Verified that `ncs-backend.exe` on Windows listens on a dynamic local port instead of a fixed port.
- Updated application icon resources for macOS, Windows, and the installer.
- Added `THIRD-PARTY-NOTICES.txt` for third-party open-source component notices.
- Updated release repository README and catalog metadata for clearer downloads and checksum verification.

### Notes

- Coastline remains local-first, closed-source, and binary-only.
- Coastline does not provide a built-in model service.
- Model-analysis features require a user-configured third-party model API key.
- macOS and Windows builds are currently unsigned.
- Users should back up writing projects regularly.
- This is primarily a release-polish update, not a major feature release.

---

## Coastline 1.3.0 Beta

Coastline 1.3.0 Beta 是首次公开 beta 之后的稳定性与产品化整理版本。

本版本重点改进真实写作流程中的可靠性，包括稿件导出、时间线审阅、事实核查、高风险批量暂停、人物别名处理、模型配置、启动恢复、前端资源刷新，以及 macOS / Windows 桌面发布打包。

### 本版本重点

- 大幅整理前端工作台，并拆分 workspace UI 组件。
- 改进事实库页面布局与视觉层级。
- 新增 Timeline v2 叙事分组与更清晰的故事时间提取。
- 新增人物别名建议与合并审阅流程。
- 新增高级 OpenAI-compatible 模型服务配置。
- 改进 DOCX 与 PDF 稿件导出格式。
- 修复 disabled facts 和 pass fact checks 错误影响风险检测的问题。
- 修复高风险批量暂停后草稿章节被错误只读的问题。
- 修复启动时恢复最后活动项目的问题。
- 修复 release app 显示旧前端资源的问题。
- 修复 macOS 窗口缩放时红绿灯位置重置的问题。
- 改进 macOS DMG 布局与 Windows release 打包脚本。

### 新增 / 改进

- 新增 Timeline v2，支持按叙事 / 来源章节分组。
- 新增 timeline 条目的显式故事时间属性。
- 新增人物别名建议、接受 / 拒绝生命周期，以及前端别名面板。
- 新增高级 OpenAI-compatible provider 配置。
- 改进事实库页面布局与 macOS 顶栏布局。
- 改进稿件导出的层级、段落间距、首行缩进和仅导出当前 active path 的行为。
- 在重做后的工作台中，让重要章节操作控件和审阅切换更容易访问。
- 改进 Windows release 打包与 Python 解析逻辑。

### 修复

- 修复高风险批量暂停后，草稿章节被错误设置为只读的问题。
- 修复事实库命中被误判为高风险冲突的问题。
- 修复已通过的 fact checks 被写入持久问题或高风险阻塞的问题。
- 修复 disabled facts 仍继续影响动态风险检测的问题。
- 修复章节分析后 narrative pacing 不更新的问题。
- 修复应用有时打开第一个项目，而不是最后活动项目的问题。
- 修复 DOCX 与 PDF 稿件导出格式问题。
- 修复 release build 显示旧前端资源的问题。
- 修复 malformed / legacy timeline 数据导致时间线页面不稳定的问题。
- 修复 onboarding notice 持久化问题。
- 修复 macOS 窗口缩放时红绿灯位置重置的问题。
- 修复 Windows release PowerShell 脚本参数块错误。

### 说明

- Coastline 仍然是本地优先、闭源、仅发布二进制安装包的软件。
- Coastline 不提供内置模型服务。
- 模型分析功能需要用户自行配置第三方模型 API key。
- macOS 与 Windows 构建目前均未签名。
- 用户应定期备份写作项目。

---

## Coastline 1.2.0 Beta

第一个公开二进制 beta 版本。

Coastline 1.2.0 Beta 是 Coastline 的首次公开二进制发布版本，包含 macOS 与 Windows 桌面安装包，以及长篇叙事项目管理、LLM 分析、连续性追踪和导出相关功能。

### 本版本重点

- 新增 Windows x64 桌面版与安装包。
- 新增 WPF / WebView2 Windows 壳。
- 新增 Windows backend.exe 打包与启动流程。
- 修复 Windows WebView2 用户数据目录写入安装目录的问题。
- 改进中文 PDF 导出支持，通过可用 CJK 字体生成中文 PDF。
- 建立公开二进制 release 仓库与发布文档。

### 首次公开 beta 包含

- macOS 桌面版。
- Windows 桌面版与安装包。
- 本地优先项目存储。
- 用户自行配置模型 API key。
- 项目与章节管理。
- 多章节写作项目管理。
- LLM 辅助章节分析流程。
- 时间线与事实追踪。
- 人物状态与设定变化追踪。
- 连续性问题追踪。
- 路径 / 分支管理。
- 章节确认与回滚。
- Word 导出。
- PDF 导出。
- 中文 PDF 导出支持。

### 说明

- Coastline 当前为闭源、仅发布二进制安装包的软件。
- Coastline 不提供内置模型服务，主要模型分析功能依赖用户自行配置的第三方模型 API key。
- 当前版本主要支持 `deepseek-v4-pro`。
- 第三方模型 API 费用由对应模型服务商收取，并由用户自行承担。
- macOS 版目前尚未进行代码签名和公证。
- Windows 版目前尚未进行代码签名。
- 用户应定期备份写作项目。

---

# Changelog

## Coastline 1.3.0 Beta

Coastline 1.3.0 Beta is a stability and product-polish release after the first public beta.

This release improves real writing workflow reliability, including manuscript export, timeline review, fact checking, high-risk batch pauses, character alias handling, provider configuration, startup restoration, frontend asset freshness, and desktop release packaging.

### Highlights

- Major frontend overhaul and workspace component split.
- Improved facts page layout and visual hierarchy.
- Added Timeline v2 narrative grouping with clearer story-time extraction.
- Added character alias suggestions and merge review workflow.
- Added advanced OpenAI-compatible provider configuration.
- Improved DOCX and PDF manuscript export formatting.
- Fixed disabled facts and pass fact checks incorrectly affecting risk detection.
- Fixed high-risk batch pause read-only behavior for draft chapters.
- Fixed last active project restoration on startup.
- Fixed release app stale frontend cache issues.
- Fixed macOS traffic light behavior during live window resize.
- Improved macOS DMG layout and Windows release packaging scripts.

### Added / Improved

- Added Timeline v2 with narrative/source-chapter grouping.
- Added explicit story-time attributes for timeline entries.
- Added character alias suggestions, accept/reject lifecycle, and frontend alias panel.
- Added advanced OpenAI-compatible provider configuration.
- Improved facts page layout and macOS topbar layout.
- Improved manuscript export hierarchy, paragraph spacing, first-line indentation, and active-path-only export behavior.
- Kept important chapter action controls and review toggles easier to access in the redesigned workspace.
- Improved Windows release packaging and Python resolver behavior.

### Fixed

- Fixed draft chapters becoming incorrectly read-only after high-risk batch pauses.
- Fixed fact-library hits being confused with high-risk conflicts.
- Fixed passed fact checks becoming persistent issues or high-risk blockers.
- Fixed disabled facts continuing to affect dynamic risk detection.
- Fixed narrative pacing not updating after chapter analysis.
- Fixed the app sometimes opening the first project instead of the last active project.
- Fixed DOCX and PDF manuscript export formatting problems.
- Fixed release builds showing stale frontend assets.
- Fixed timeline page instability caused by malformed or legacy timeline data.
- Fixed onboarding notice persistence.
- Fixed macOS traffic lights resetting during window resize.
- Fixed Windows release script parameter block errors.

### Notes

- Coastline remains local-first, closed-source, and binary-only.
- Coastline does not provide a built-in model service.
- Model-analysis features require a user-configured third-party model API key.
- macOS and Windows builds are currently unsigned.
- Users should back up writing projects regularly.

---

## Coastline 1.2.0 Beta

First public binary beta release.

Coastline 1.2.0 Beta is the first public binary release of Coastline, including macOS and Windows desktop installers, long-form narrative project management, LLM-assisted analysis, continuity tracking, and export features.

### Highlights

- Added Windows x64 desktop build and installer.
- Added WPF / WebView2 Windows shell.
- Added Windows backend.exe packaging and startup flow.
- Fixed WebView2 user data directory handling on Windows.
- Improved Chinese PDF export support by using available CJK fonts.
- Established the public binary release repository and release documentation.

### Included in this first public beta

- macOS desktop build.
- Windows desktop build and installer.
- Local-first project storage.
- User-configured model API key.
- Project and chapter management.
- Multi-chapter writing project management.
- LLM-assisted chapter analysis workflow.
- Timeline and fact tracking.
- Character state and setting change tracking.
- Continuity issue tracking.
- Path / branch management.
- Chapter confirmation and rollback.
- Word export.
- PDF export.
- Chinese PDF export support.

### Notes

- Coastline is currently closed-source and binary-only.
- Coastline does not provide a built-in model service. Its main model-analysis features depend on a third-party model API key configured by the user.
- The current version mainly supports `deepseek-v4-pro`.
- Third-party model API fees are charged by the corresponding model provider and are the user's responsibility.
- The macOS build is currently not code-signed or notarized.
- The Windows build is currently unsigned.
- Users should back up writing projects regularly.