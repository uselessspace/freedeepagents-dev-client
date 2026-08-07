# FreeDeepAgents Dev Client

FreeDeepAgents（FDA）智能活动开发者客户端 —— 一个桌面应用，用于本地开发活动、同步到服务端并实时预览。支持 **macOS** 与 **Windows**。

> 本仓库仅用于分发安装包。源码暂不开源，最新版本请见 [Releases](../../releases/latest)。

## 下载

前往 **[Releases](../../releases/latest)** 下载最新安装包：

| 系统 | 安装包 | 说明 |
|---|---|---|
| **macOS**（Apple Silicon / arm64） | `FreeDeepAgents-Dev-Client-macOS-arm64.dmg` | 拖入「应用程序」即可 |
| **Windows**（x64，Win10 2004+ / Win11） | `FreeDeepAgents-Dev-Client-windows-x64.zip` | 便携版，解压双击运行，无需安装 |

安装包已预置 HTTPS 服务端地址，安装后用开发者账号登录、选择活动文件夹即可使用。
macOS 客户端还会自动安装同版本 Coding Agent CLI 到
`~/.local/bin/fda-dev`，无需单独下载或配置。

## 安装

### macOS

1. 双击下载的 `.dmg`，把 **FreeDeepAgents Dev Client** 拖进「应用程序」。
2. 首次打开如提示「无法打开，因为它来自身份不明的开发者 / 已损坏」，这是因为安装包未做 Apple 公证（正常现象）。任选一种方式放行：
   - **右键打开**：在「应用程序」里右键点图标 → 「打开」→ 在弹窗里再次「打开」。
   - 或在「终端」执行（把路径换成实际安装路径）：
     ```bash
     xattr -dr com.apple.quarantine /Applications/dev-client.app
     ```
3. 打开后用你的开发者账号登录，选择本地活动文件夹即可开始开发。
4. 首次启动会自动安装/更新 `fda-dev`。新开终端后可直接验证：
   ```bash
   fda-dev --version
   fda-dev --folder /path/to/activity doctor
   ```

`fda-dev` 与桌面客户端共享登录会话，只允许 HTTPS；自签证书选项仅放宽证书
校验，不会启用明文 HTTP。

### Windows

1. 解压下载的 `.zip`，双击 `FreeDeepAgents-Dev-Client.exe`（便携版，无需安装）。
2. 首次运行 Windows SmartScreen 可能提示「未知发布者」（安装包未签名，正常现象）：点「更多信息」→「仍要运行」。
3. 登录并选择活动文件夹即可。
4. 需要微软 **WebView2 运行时**（Win10 2004+ 与 Win11 已预装）。若窗口空白，从微软官网安装「Evergreen WebView2 Runtime」。

## 反馈

使用中有问题请提 [Issue](../../issues)。
