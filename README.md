# 悦耳声阅 (YueErShengYue)

个人向 **[Audiobookshelf](https://www.audiobookshelf.org/)** 客户端：**Android + Windows** 同步首发，黑金主题、流媒体播放、进度双向同步。

**当前正式版：1.0.0**（Android `versionCode` **33**；Windows 便携包同号）

对接 [官方 REST API](https://api.audiobookshelf.org/)：登录、书库、播放会话、进度回传；**不提供整本下载**，只做流式缓存，轻量、干净、专注听。

---

## 支持平台

| 平台 | 形态 | 要求 | 产物文件名 |
|------|------|------|------------|
| **Android** | 正式签名 APK | Android 8.0+（API **26**），`targetSdk` **35** | `YueErShengYue-1.0.0-release.apk` |
| **Windows** | x86_64 便携包（免安装） | 64 位 Windows；解压即用，自带 runtime | `YueErShengYue-Windows-x86_64-Portable-1.0.0.zip` |

| 标识 | 值 |
|------|-----|
| applicationId / 包名 | `com.yueer.shengyue` |
| versionName | `1.0.0` |
| Android versionCode | `33` |
| minSdk / targetSdk | **26** / **35** |

> iOS 不在本轮公开发布范围内。

---

## 下载与安装

正式发布页：**[v1.0.0 Release](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/tag/v1.0.0)**  
仓库 Releases 列表：https://github.com/huliyoudiangou/YueErShengYue_APP/releases

请下载 **1.0.0** 对应产物，并以下文 SHA256 校验后再安装。

### 直接下载（1.0.0）

| 产物 | 直接下载 |
|------|----------|
| Android 正式 APK | [YueErShengYue-1.0.0-release.apk](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.0/YueErShengYue-1.0.0-release.apk) |
| Windows x86_64 便携包 | [YueErShengYue-Windows-x86_64-Portable-1.0.0.zip](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.0/YueErShengYue-Windows-x86_64-Portable-1.0.0.zip) |
| Windows SHA256 | [YueErShengYue-Windows-x86_64-Portable-1.0.0.sha256.txt](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.0/YueErShengYue-Windows-x86_64-Portable-1.0.0.sha256.txt) |
| Windows 清单 | [YueErShengYue-Windows-x86_64-Portable-1.0.0.manifest.txt](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.0/YueErShengYue-Windows-x86_64-Portable-1.0.0.manifest.txt) |

### Android

1. 下载 [`YueErShengYue-1.0.0-release.apk`](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.0/YueErShengYue-1.0.0-release.apk)
2. 用下方哈希校验文件完整性
3. 在手机上打开 APK 安装；若提示「未知来源」，在系统设置中允许安装此应用
4. 打开应用 → 选择语言 → 填写服务器地址（协议 / 主机 / 端口）与账号密码后登录

### Windows（便携版）

1. 下载 [`YueErShengYue-Windows-x86_64-Portable-1.0.0.zip`](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.0/YueErShengYue-Windows-x86_64-Portable-1.0.0.zip)
2. 用下方哈希校验
3. 解压到任意本地目录（建议路径尽量短、避免权限受限目录）
4. 运行解压目录中的 `YueErShengYue.exe`（目录内含 `app/`、`runtime/` 等，**请保持相对结构完整**，不要只拷贝单个 exe）

---

## 完整性校验（SHA256）

发布前请核对下载文件的 SHA256，与下表完全一致再安装：

| 文件 | SHA256 |
|------|--------|
| `YueErShengYue-1.0.0-release.apk` | `695ADF9D1D3B4560E6697FFE20DC1EE8BC29FB1D73983FF35D38DE3E2FF272C2` |
| `YueErShengYue-Windows-x86_64-Portable-1.0.0.zip` | `090048DDAC795419FD06210C1DADD123CD9358397737122B63CF68E20506C7E1` |

**Windows PowerShell 示例：**

```powershell
Get-FileHash -Algorithm SHA256 .\YueErShengYue-1.0.0-release.apk
Get-FileHash -Algorithm SHA256 .\YueErShengYue-Windows-x86_64-Portable-1.0.0.zip
```

**校验通过标准：** 输出的 `Hash`（忽略大小写）与上表一致。

---

## 1.0.0 更新内容（双端同步首发）

- **正式版 1.0.0**：Android 与 Windows 版本号统一；Android `versionCode` **33**
- **双端产物**：正式 release APK + Windows x86_64 便携 zip（自带 runtime，可冷启动）
- **听书闭环**：登录 / 书库 / 详情 / 播放 / 设置；进度会话同步（play → 周期 sync → close，冲突以 **lastUpdate 较新** 为准）
- **倍速**：0.5x–3.0x；设置页「全局默认」+ 播放页「全局」或本书覆盖
- **推荐图书**：按本地自然日每日最多拉网一次（当天缓存）；可手动强制刷新
- **流式缓存**：可调 **0–500MB**，默认 **200MB**（0=关闭）；预缓存当前章 + 后两章（**非整本下载**）
- **片头片尾**：每书本地秒数，**不同步服务器**
- **睡眠定时**：固定档位（含更长时长能力，以端上 UI 为准）
- **主题与语言**：黑金暗色 / 薄荷绿亮色；English / 简体中文 / 繁體中文
- **边界不变**：永不整本下载；不做服务器管理、播客、电子书阅读

---

## 已定决策（请勿随意改）

| 项 | 决定 |
|----|------|
| 技术栈（Android） | Kotlin + Jetpack Compose + Media3 |
| 技术栈（Windows） | Kotlin + Compose Multiplatform Desktop + shared 核心；播放侧 JavaFX Media |
| 共享核心 | `shared/`：API、模型、仓库（无 UI） |
| 包名 | `com.yueer.shengyue` |
| minSdk | 26 |
| 下载 | **永不支持整本下载** |
| 缓存 | 可调 **0–500MB**，默认 **200MB**（0=关闭；流式预缓存当前+后两章） |
| 进度 | Session `sync` + Media Progress；冲突以 **lastUpdate 较新** 为准 |
| 片头片尾 | 每书本地秒数，**不同步服务器** |
| 定时 | 固定分钟档 + 取消（本章结束等能力在服务层预留，以 UI 为准） |
| 倍速 | 0.5x–3.0x；设置=全局默认；播放页可选「全局」或仅本书倍速 |
| 推荐图书 | 按本地自然日 **每日更新一次**（当天内用缓存）；可手动强制刷新 |
| 证书 | 可选信任自签名（须用户显式开启） |
| MVP / 1.0 范围 | 仅有声书：登录 / 书库 / 详情 / 播放 / 设置 |

官方 API：https://api.audiobookshelf.org/

---

## 环境要求（从源码构建）

- **JDK 17**
- **Android**：Android Studio Ladybug+（或兼容 AGP 8.7）、Android SDK 35
- **Windows 桌面**：同一 JDK 17；Compose Desktop 依赖由 Gradle 拉取
- 本机若尚未安装 Android Studio，请先安装后再用 IDE 打开本目录

---

## 打开与构建

### 模块结构（概要）

```
app/       Android 客户端（Compose + Media3 + Hilt）
desktop/   Windows Compose Desktop 客户端
shared/    跨端核心（API / 模型 / 仓库）
```

### Android

1. Android Studio → Open → 选择本仓库根目录  
2. 等待 Gradle Sync  
3. 连接真机或模拟器 → Run `app`

命令行（需已配置 `JAVA_HOME` 与 SDK）：

```powershell
.\gradlew.bat :app:assembleDebug
.\gradlew.bat :app:assembleRelease
```

正式 release 产物命名：`YueErShengYue-1.0.0-release.apk`（以发布脚本 / copy 任务输出为准）。  
Release 签名依赖本机 `app/signing.properties`（**勿提交密钥与密码**）。

### Windows Desktop

```powershell
.\gradlew.bat :desktop:run
.\gradlew.bat :desktop:packageReleaseDistributionForCurrentOS
```

便携分发包经项目打包流程输出为：

`YueErShengYue-Windows-x86_64-Portable-1.0.0.zip`

（工作区常见落点：`dist/` 或 `desktop/build/compose/binaries/...`，以实际构建日志为准。）

> 首次若缺少 Gradle Wrapper jar，请用 Android Studio 打开工程自动生成，或执行  
> `gradle wrapper --gradle-version 8.9`

可选桌面冒烟（环境变量开启后跑 desktop）：

```powershell
$env:YUEER_SMOKE = "1"
.\gradlew.bat :desktop:run
```

期望日志出现 `[smoke] PASS`（能登录、开播并短暂 playing；需可用的测试服配置）。

---

## 进度同步流程

1. `POST /api/items/{id}/play` 打开 PlaybackSession  
2. 播放中约每 **15 秒** `POST /api/session/{id}/sync`  
3. 暂停 / 停止 / 销毁服务时 sync + `close`  
4. 关闭时额外 `PATCH /api/me/progress/{id}` 兜底  

冲突策略：以 **lastUpdate 较新** 的一方为准。

---

## 明确不做

- 整本下载 / 离线整库  
- 服务器管理（扫盘、用户、元数据编辑）  
- 播客（可二期）  
- 电子书阅读  
- 本轮公开发布 **不包含 iOS**

---

## 使用说明（摘要）

1. 安装 Android APK 或解压运行 Windows 便携包  
2. 登录页选择语言；选择协议（https/http），填写主机与端口，再填用户名 / 密码  
3. 登录后浏览首页：继续播放 / 最近添加 / 推荐 / 再次收听 等  
4. 进入书籍详情 → 可设片头片尾 → 开始播放  
5. 播放页调节倍速、睡眠定时、章节；Android 支持通知栏媒体控件  
6. 设置中可切换主题、语言、缓存上限，并清除封面 / 流媒体缓存  

---

## 版本历史（摘要）

| 版本 | 说明 |
|------|------|
| **1.0.0** | Android + Windows **同步首发**；versionCode 33；正式 APK + x86_64 便携包 |
| 0.7.x | 双端版本对齐与播放稳定性硬化（发布前迭代） |
| 0.5.5 | 全局默认倍速始终生效；推荐图书按本地自然日每日刷新 |
| 0.1.0-mvp | 骨架 + 核心链路可联调 |

---

## 免责声明

- 本客户端为个人向第三方客户端，对接官方 Audiobookshelf REST API，**与 Audiobookshelf 官方项目无隶属或担保关系**。  
- 请仅连接你有权访问的服务器与账号，并遵守当地法律法规与版权规定；音频内容版权归权利人所有。  
- 软件按「现状」提供，作者不对数据丢失、服务不可用、账号封禁等间接损失承担责任。  
- 可选「信任自签名证书」仅在用户**显式开启**时生效，存在中间人风险，请仅在可信局域网环境使用。  
- **永不提供整本下载**；流式缓存不可当作完整离线书库管理。  
- 发布物请以 GitHub Releases 中的安装包与本文 SHA256 为准；请勿从不明来源获取篡改包。  
- 密钥、`local.properties`、签名密码等敏感信息不得提交或随安装包分发。

---

<p align="center">悦耳声阅 · 用耳朵丈量世界</p>