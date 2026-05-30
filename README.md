# Coastline

**A Narrative Control System**

> 下载 Coastline 1.2.0 Beta / Download Coastline 1.2.0 Beta:  
> https://github.com/AlbertYang514/coastline-releases/releases/tag/v1.2.0

Coastline 是一个本地优先的长篇写作管理桌面工具，用于帮助作者管理章节、时间线、事实库、连续性问题和导出文件。

它不是 AI 代写工具。Coastline 的目标不是替作者写故事，而是帮助作者保留对叙事结构、人物状态、事实一致性和文本版本的控制权。

> Coastline 目前是个人维护的早期 beta 项目，不是商业服务，也不提供云同步、账号系统或在线存储。

当前版本：**Coastline 1.2.0 Beta**

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

- macOS：`Coastline-1.2.0-beta-macOS.dmg`
- Windows：`Coastline-1.2.0-beta-win-x64.exe`

## 重要说明

### 本地优先

Coastline 将项目文件默认保存在用户本机。

开发者不运营任何用于 Coastline 的云端服务器，不论该服务器位于中国大陆境内或境外。

开发者不提供任何 Coastline 云账号系统，不论该账号系统位于中国大陆境内或境外。

开发者无法通过 Coastline 本应用主动获取用户的项目内容、章节文本、API key、导出文件或其他隐私信息。

### 第三方模型 API

Coastline 不提供内置模型服务。

用户需要自行配置模型 API key。当前版本主要支持：

- `deepseek-v4-pro`

当用户运行 AI 分析时，相关项目文本可能会发送到用户配置的第三方模型 API。API 使用费用、可用性、数据处理方式和服务条款由对应第三方模型服务商决定。

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

1. 下载 `Coastline-1.2.dmg`。
2. 打开 DMG 文件。
3. 将 `Coastline.app` 拖入“应用程序”文件夹。
4. 从“应用程序”中打开 Coastline。

### macOS 安全提示

Coastline 目前还没有进行 Apple 开发者签名和 notarization 公证。

第一次打开 macOS 版时，系统可能提示：

- “Apple 无法检查其是否包含恶意软件”；
- “应用已损坏，无法打开”；
- “无法验证开发者”。

这是当前 beta 版的已知情况。

推荐打开方式：

1. 将 `Coastline.app` 拖入“应用程序”文件夹。
2. 打开 **系统设置 → 隐私与安全性**。
3. 找到 Coastline 的拦截提示。
4. 点击 **仍要打开 / Open Anyway**。
5. 再次确认打开。

如果系统仍提示“应用已损坏”，高级用户可以在终端运行：

```bash
xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

请只从官方 Release 页面下载安装包。若你不信任来源，请不要安装。

## Windows 安装说明

1. 下载 `CoastlineSetup-1.2-win-x64.exe`。
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

## 文档

- `PRIVACY.md`：隐私政策；
- `LICENSE.txt`：闭源软件授权；
- `EULA.txt`：最终用户许可协议；
- `CHANGELOG.md`：更新日志。

---

# Coastline

**A Narrative Control System**

> Download Coastline 1.2.0 Beta / Download Coastline 1.2.0 Beta:  
> https://github.com/AlbertYang514/coastline-releases/releases/tag/v1.2.0

Coastline is a local-first desktop writing system for long-form narrative projects.

It helps writers manage chapters, timelines, fact records, continuity issues, and exports. It is not an AI ghostwriter. Coastline is designed to help writers keep control of narrative structure, character states, factual continuity, and text versions.

> Coastline is currently a personally maintained early beta project. It is not a commercial service and does not provide cloud sync, user accounts, or online storage.

Current release: **Coastline 1.2.0 Beta**

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

- macOS: `Coastline-1.2.0-beta-macOS.dmg`
- Windows: `Coastline-1.2.0-beta-win-x64.exe`

## Important notes

### Local-first

Coastline stores project files locally on the user's machine by default.

The developer does not operate any cloud server for Coastline, whether inside or outside mainland China.

The developer does not provide any Coastline cloud account system, whether inside or outside mainland China.

Through the Coastline application itself, the developer cannot actively access the user's project content, chapter text, API key, exported files, or other private information.

### Third-party model API

Coastline does not provide a built-in model service.

Users need to configure their own model API key. The current version mainly supports:

- `deepseek-v4-pro`

When the user runs AI analysis, relevant project text may be sent to the third-party model API configured by the user. API usage, costs, availability, data handling, and terms are governed by the corresponding third-party model provider.

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

1. Download `Coastline-1.2.dmg`.
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

1. Move `Coastline.app` to the `Applications` folder.
2. Open **System Settings → Privacy & Security**.
3. Find the blocked Coastline message.
4. Click **Open Anyway**.
5. Confirm that you want to open the app.

If macOS still reports that the app is damaged, advanced users may remove the quarantine attribute manually:

```bash
xattr -dr com.apple.quarantine "/Applications/Coastline.app"
open "/Applications/Coastline.app"
```

Only install Coastline if you downloaded it from the official release page and trust the developer.

## Windows installation

1. Download `CoastlineSetup-1.2-win-x64.exe`.
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

## Documents

- `PRIVACY.md`: Privacy Policy
- `LICENSE.txt`: Proprietary Software License
- `EULA.txt`: End User License Agreement
- `CHANGELOG.md`: Changelog