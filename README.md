# FreeDeepAgents Dev Client

FreeDeepAgents（FDA）智能活动开发者客户端 —— 一个 macOS 桌面应用，用于本地开发活动、同步到服务端并实时预览。

> 本仓库仅用于分发安装包。源码暂不开源，最新版本请见 [Releases](../../releases/latest)。

## 下载

前往 **[Releases](../../releases/latest)** 下载最新的 `.dmg`。

- 系统要求：**macOS（Apple Silicon / M 系列芯片，arm64）**
- 安装包已预置服务端地址，安装后登录、选择活动文件夹即可使用。

## 安装

1. 双击下载的 `.dmg`，把 **FreeDeepAgents Dev Client** 拖进「应用程序」。
2. 首次打开如提示「无法打开，因为它来自身份不明的开发者 / 已损坏」，这是因为安装包未做 Apple 公证（正常现象）。任选一种方式放行：
   - **右键打开**：在「应用程序」里右键点图标 → 「打开」→ 在弹窗里再次「打开」。
   - 或在「终端」执行（把路径换成实际安装路径）：
     ```bash
     xattr -cr "/Applications/FreeDeepAgents Dev Client.app"
     ```
3. 打开后用你的开发者账号登录，选择本地活动文件夹即可开始开发。

## 反馈

使用中有问题请提 [Issue](../../issues)。
