# 更新日志

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