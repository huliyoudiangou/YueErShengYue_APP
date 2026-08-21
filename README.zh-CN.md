# 悦耳声阅（YueErShengYue）

<p align="center">
  <a href="README.md">English</a> · <strong>简体中文</strong>
</p>

**悦耳声阅**是一款面向 **Android 与 Windows** 的 [Audiobookshelf](https://www.audiobookshelf.org/) 客户端，提供简洁的有声书体验，包括流媒体播放、书库浏览与进度同步。

**当前稳定版：1.0.4**（Android 与 Windows 同步）— Android `versionCode` 为 **50**。Windows 便携版已同步更新至 **1.0.4**。

---

## 支持平台

| 平台 | 软件包 | 系统要求 | 文件名 |
|------|--------|----------|--------|
| **Android** | 正式签名 APK | Android 8.0+（API **26**），`targetSdk` **35** | `YueErShengYue-1.0.4-release.apk` |
| **Windows** | x86_64 便携包 | 64 位 Windows；内置运行时 | `YueErShengYue-Windows-x86_64-Portable-1.0.4.zip` |

| 标识 | 值 |
|------|----|
| applicationId / 包名 | `com.yueer.shengyue` |
| Android 版本名称 | `1.0.4` |
| Android 版本代码 | `50` |
| Windows 包版本 | `1.0.4` |
| Android minSdk / targetSdk | **26** / **35** |

---

## 下载与安装

1.0.4 正式发布页（Android + Windows）：**[悦耳声阅 1.0.4](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/tag/v1.0.4)**

旧版 Windows 1.0.0 软件包：**[悦耳声阅 1.0.0](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/tag/v1.0.0)**

### 直接下载

| 平台 | 下载 |
|------|------|
| Android | [YueErShengYue-1.0.4-release.apk](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.4/YueErShengYue-1.0.4-release.apk) |
| Windows x86_64 | [YueErShengYue-Windows-x86_64-Portable-1.0.4.zip](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.4/YueErShengYue-Windows-x86_64-Portable-1.0.4.zip) |

### Android

1. 下载 `YueErShengYue-1.0.4-release.apk`。
2. 使用下方 SHA-256 校验文件。
3. 在设备上打开 APK；若 Android 请求授权此来源安装应用，请在系统设置中允许。
4. 启动悦耳声阅，选择语言，填写 Audiobookshelf 服务器地址和账号信息，然后登录。

### Windows 便携版

1. 从 **1.0.4** 发布页下载 `YueErShengYue-Windows-x86_64-Portable-1.0.4.zip`（旧版 1.0.0 便携包仍保留在 1.0.0 发布页；1.0.1 与 1.0.3 未更新 Windows）。
2. 使用下方 SHA-256 校验文件。
3. 将压缩包解压到本地目录，建议使用路径较短且具备常规写入权限的位置。
4. 运行 `YueErShengYue.exe`。请保持 `app/`、`runtime/` 及相关文件原有的相对目录结构。

---

## SHA-256 校验

| 文件 | SHA-256 |
|------|---------|
| `YueErShengYue-1.0.4-release.apk` | `1e4e3b59eff26790403e2fcc6ae57f046d50410965208d555fdd047c73f97970` |
| `YueErShengYue-Windows-x86_64-Portable-1.0.4.zip` | `5575FA43EDE770E3EE49AA5F80A26B94E5F44837D83F02FC8446FD1D2E45B17D` |
| `YueErShengYue-Windows-x86_64-Portable-1.0.0.zip`（旧版） | `090048DDAC795419FD06210C1DADD123CD9358397737122B63CF68E20506C7E1` |

PowerShell 示例：

```powershell
Get-FileHash -Algorithm SHA256 .\YueErShengYue-1.0.4-release.apk
Get-FileHash -Algorithm SHA256 .\YueErShengYue-Windows-x86_64-Portable-1.0.4.zip
```

计算结果与上表对应值一致后，再安装或运行软件包。

---

## 1.0.4 更新内容

### Android

- **Android 性能与体验优化**：冷启动更稳，首页/书库优先读缓存，缓存读取异常自动回退网络加载。
- **修复首次进入卡住问题**：不再因为缓存读取异常导致首页/书库停在加载中。
- **首页后台刷新恢复**：有缓存时先展示缓存，再静默拉取新内容，继续播放/最近添加/推荐/再次收听可自动更新。
- **播放加载优化**：并行获取播放元数据，播放器缓存异步初始化，避免首播抢带宽。
- **底部 Dock 毛玻璃与导航适配**：圆角与搜索框统一，紧凑高度，支持三键导航安全区。
- **缓存实时生效**：调整缓存大小即时作用于播放服务，清流缓存使用服务内安全事务。

### Windows（首次同步至 1.0.4）

- **Windows 便携版与 Android 同步更新至 1.0.4**：1.0.1–1.0.3 期间停留在 1.0.0，本次补齐到当前版本。
- **绿色 x86_64 便携包**：内置运行时，解压到任意目录即可运行，无需安装。
- **mpv 播放引擎**：自动检测本机 mpv.exe（也可在「设置」中手动指定路径），支持 0.5x–3.0x 倍速（音调保持）与声音增强。
- **迷你播放器修复**：快进 10 秒按钮不再变形；播放条底色改为主题着色（不再发白）；音量控件改为喜马拉雅风格横向胶囊，悬浮于喇叭图标正上方，点按/拖动调节、点按空白处收起。
- **退出清理**：退出应用时可靠停止播放并结束 mpv 进程，音频不再残留后台；异常退出遗留的 mpv 会在下次启动时自动清理。
- **最小化到托盘继续播放**，托盘菜单支持显示主窗口 / 退出。

## 1.0.3 更新内容

- **首进自动加载**：进入首页自动加载书单，无需再手动刷新。
- **缓存优先**：二次进入优先读取本地缓存以加快首页流畅度，并在后台静默刷新。
- 修复推荐 / 最近添加残留旧缓存的问题。
- **定时结束自动退出**：定时播放时长结束后自动退出应用。
- **播放器自动重连**：播放器未就绪时自动重连，无需退出应用重新进入。
- 优化「继续播放 / 再次收听」首屏响应速度。
- 修复冷启动首次播放的会话提交闩锁问题。
- **仅发布 Android**（`versionCode` **49**）；Windows 便携版暂时仍停留在 1.0.0。

---

## 1.0.1 更新内容

- **仅发布 Android**：Windows 便携版暂时仍停留在 1.0.0。
- **四个主题**：黑金、薄荷绿、樱花粉、天空蓝。
- 搜索框、迷你播放器与悬浮 Dock 统一毛玻璃处理。
- 底部悬浮圆角 Dock，高度与存在感进一步打磨。
- 倍速预设单行展示，全局/仅本书选中色跟随主题。
- 声音增强默认开启。
- 推荐按自然日刷新，并继续优化加载流畅度与稳定性。
- 桌面显示名称：**YueEr**。
- 正式签名包体继续控制在约 **3 MB**。

---

## 功能亮点

### 播放与进度

- 流媒体有声书播放与章节导航。
- **0.5x 至 3.0x** 播放速度，支持全局默认和单书覆盖。
- 睡眠定时预设，以及按书设置片头片尾跳过时长。
- 播放期间约每 **15 秒**同步一次会话进度，并在暂停和停止时更新。
- Android 媒体通知与锁屏控制。

### 书库与发现

- 首页包含继续播放、最近添加、推荐图书、再次收听和我的收藏。
- 封面网格书库浏览、排序、筛选与全局搜索。
- 书籍详情展示封面、演播者、简介、章节和播放控制。
- 推荐内容按本地自然日刷新，并支持本地缓存和手动刷新。

### 流媒体缓存

- 流媒体缓存可在 **0 至 500 MB** 范围调节，默认 **200 MB**。
- 预缓存当前章节与后续两章。
- 可分别清理封面缓存和流媒体缓存。

### 主题与语言

- **黑金、薄荷绿、樱花粉、天空蓝** 四套主题。
- **English、简体中文、繁體中文**界面。
- 针对窄屏和长屏优化的响应式布局。

### Android 与 Windows 体验

- Android Auto 媒体库浏览与播放集成。
- Windows 便携分发包内置运行时。
- Windows 支持最小化到托盘继续播放，退出时可靠结束 mpv 播放进程。
- Windows 各页面采用统一的鼠标滚轮方向。

---

## 界面预览

| 首页 | 书籍详情 |
|:----:|:--------:|
| ![首页](screenshots/01_home.png) | ![书籍详情](screenshots/02_detail.png) |

| 播放页 | 书库 |
|:------:|:----:|
| ![播放页](screenshots/03_player.png) | ![书库](screenshots/04_library.png) |

| 设置 |
|:----:|
| ![设置](screenshots/05_settings.png) |

截图展示的主题或语言可能因设备配置而异。

---

## 开始使用

1. 安装 Android APK，或解压 Windows 便携包。
2. 打开悦耳声阅并选择界面语言。
3. 选择 `https://` 或 `http://`，然后填写主机、端口、用户名和密码。
4. 浏览首页或书库，打开一本书并开始播放。
5. 在播放页切换章节、调节速度、设置睡眠定时和单书播放选项。
6. 在设置中调整主题、语言、默认速度和缓存大小。

### 服务器地址填写

- 从协议菜单选择协议。
- 在主机栏填写域名或 IP 地址。
- 填写服务器端口；HTTPS 默认端口为 `443`。
- 粘贴完整 URL 时，应用会自动识别并拆分协议与主机信息。

---

## 版本历史

| 版本 | 摘要 |
|------|------|
| **1.0.4** | Android 性能与体验优化：缓存优先、加载兜底、Dock 毛玻璃、导航键适配；Windows 便携版同步至 1.0.4（mpv 引擎、迷你播放器修复、最小化到托盘、退出清理） |
| **1.0.3** | 仅 Android 更新：首页自动加载 + 缓存优先二次进入、推荐/最近添加旧缓存修复、播放器自动重连、继续播放/再次收听响应与冷启动会话闩锁修复 |
| 1.0.1 | 仅 Android 更新：四主题、毛玻璃与悬浮 Dock 打磨、倍速弹窗优化、声音增强默认开启、加载与稳定性提升 |
| 1.0.0 | Android 与 Windows 同步首发；统一 Windows 滚轮体验；稳定性与性能优化 |
| 0.7.x | 双端版本对齐与正式发布加固 |
| 0.5.5 | 全局播放速度行为与每日推荐刷新 |
| 0.1.0-mvp | 初始应用流程与 Audiobookshelf 集成 |

已发布的软件包请查看 [GitHub Releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases)。

---

## 反馈

| | |
|---|---|
| 作者 | **makizhang** |
| 反馈渠道 | Telegram [@makichat_bot](https://t.me/makichat_bot) |

反馈安装、登录或播放问题时，请附上平台、系统版本、服务器版本和现象简述。

---

<p align="center">悦耳声阅 · 用耳朵丈量世界</p>
