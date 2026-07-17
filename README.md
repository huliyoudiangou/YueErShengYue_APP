# 悦耳声阅 · YueErShengYue

<p align="center">
  <img src="assets/icon.jpg" alt="悦耳声阅" width="128" />
</p>

<p align="center">
  <b>Audiobookshelf 安卓流媒体听书客户端</b><br/>
  黑金暗色 · 薄荷绿亮色 · 进度同步 · 不整本下载
</p>

<p align="center">
  <a href="https://github.com/huliyoudiangou/YueErShengYue_APP/releases/latest"><img alt="Latest Release" src="https://img.shields.io/github/v/release/huliyoudiangou/YueErShengYue_APP?style=flat-square" /></a>
  <a href="https://github.com/huliyoudiangou/YueErShengYue_APP/releases"><img alt="Downloads" src="https://img.shields.io/github/downloads/huliyoudiangou/YueErShengYue_APP/total?style=flat-square" /></a>
</p>

---

## 下载

| | |
|--|--|
| **当前版本** | `0.4.9` (versionCode 24) |
| **正式包** | [YueErShengYue-0.4.9-release.apk](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v0.4.9/YueErShengYue-0.4.9-release.apk) |
| **全部版本** | [GitHub Releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases) |

> 仅发布 **APK**，不提供源码。请从 **Releases** 下载安装包。

### 安装提示
- Android 8.0+（API 26+）
- 需允许「未知来源」安装
- 与旧版签名一致时可直接覆盖升级
- 首次使用请自备可用的 **Audiobookshelf** 服务器账号

---

## 这是什么？

**悦耳声阅** 是面向 [Audiobookshelf](https://www.audiobookshelf.org/) 的轻量 Android 客户端：流媒体听书、与服务器同步进度、黑金/薄荷绿双主题与多语言。不做整本下载，专注在线收听体验。

登录欢迎语：

> 欢迎加入悦耳声阅  
> 让我们一起用耳朵丈量世界

---

## 主要功能

### 🎧 播放
- **倍速** 可调
- **章节列表**：快速跳转任意章节
- **快进 / 快退 10 秒**
- **睡眠定时**：最长 8 小时，封面角显示剩余倒计时；暂停时倒计时同步暂停
- **每书片头片尾**：详情页按秒数输入设置（每章生效，本地保存）
- **进度展示切换**：全书总进度 / 当前章节进度
- **悬浮迷你播放条** + **系统通知栏媒体控件**
- 点击开始播放后 **直接进入播放页**
- 暂停或关闭应用后再次打开，**悬浮窗可恢复**

### 📚 书库与发现
- **首页分区**：继续播放 · 最近添加 · 推荐图书 · 再次收听 · **我的收藏**
- **收藏**：详情页右上角爱心；收藏列表不限数量（本机保存）
- **书库**：三列封面网格，无限下滑；支持排序（标题 / 演播 / 时间等，同项再点切换升降序）
- **全局搜索**：跨全部媒体库索引结果
- **详情页**：封面、演播、简介（可展开）、片头片尾设置
- 书名过长 **单行跑马灯**；演播展示如「演播：张三」

### 🔗 登录与服务器
- **协议选择**：左侧 `https://` / `http://` 下拉（默认 https）
- **主机地址**：中间占主要宽度；点击不向下撑开；粘贴完整 URL 时自动识别协议并拆分
- **端口**：右侧可改（默认 `443`）
- 未带协议时使用所选协议补齐；已带协议时自动同步到下拉选项

### 🔄 同步与缓存
- 播放中约 **每 15 秒** 向服务器同步进度
- 暂停 / 结束自动回传
- **流式章节缓存**（非整本下载）：打开后向前预缓存，听完章节丢弃，保持缓存水位
- 缓存上限 **200–500 MB**（默认 200）
- 设置内可清除 **封面缓存** / **流媒体缓存**

### 🔄 应用更新
- 登录后自动检查 GitHub Releases（有节流）
- 设置 → 关于 → **检查更新**
- 发现新版本后弹窗，跳转浏览器下载最新 APK

### 🎨 界面与多语言
- **默认黑金暗色主题**
- **薄荷绿亮色主题**（圆润 R 角 + 轻毛玻璃）
- 语言：**English / 简体中文 / 繁體中文**（登录页与设置均可切换，默认英语）
- 窄长屏布局优化

### 🚗 车载
- 支持 **Android Auto** 媒体库浏览与播放
- 需手机具备完整 Android Auto 环境；部分国行机仅有 AA 壳时功能受限

### 🔐 边界说明
- Token 本地加密存储
- **不做**：整本下载、离线整库、服务器管理、电子书阅读
- 仅流媒体播放，专注听书

---

## 界面预览

| 首页 | 书籍详情 |
|:----:|:--------:|
| ![首页](screenshots/01_home.png) | ![详情](screenshots/02_detail.png) |

| 播放页 | 书库 |
|:------:|:----:|
| ![播放](screenshots/03_player.png) | ![书库](screenshots/04_library.png) |

| 设置 |
|:----:|
| ![设置](screenshots/05_settings.png) |

> 截图来自真机预览（主题与语言以本机设置为准）。

---

## 使用说明

1. 安装 APK 并打开应用  
2. 在登录页选择语言  
3. 选择协议（https/http），填写 **主机地址** 与 **端口**（默认 443），再填写用户名 / 密码  
4. 登录后进入 **首页** 浏览：继续播放 / 最近添加 / 推荐 / 再次收听 / 我的收藏  
5. 点进书籍 → 详情页可收藏、可设片头片尾 → **开始播放** 直接进入播放页  
6. 播放页调节倍速、睡眠定时、章节；通知栏可后台控制  
7. 书库页用右上角 **筛选** 切换排序；设置中可切换主题、语言、缓存  

### 进度同步（对用户透明）
- 开始播放会创建服务器会话  
- 播放中定期同步，暂停 / 结束自动回传  
- 与服务器进度冲突时，以更新时间较新的一方为准  

---

## 更新记录（近期）

- **0.4.9** — 收藏（详情爱心 + 首页我的收藏）；首页继续/再次/收藏不限数量；书库三列网格 + 排序筛选  
- **0.4.8** — 应用内检查更新，提示跳转 GitHub Releases 下载  
- **0.4.7** — 登录页协议/主机/端口紧凑布局；粘贴自动识别协议；Android Auto  

完整条目见应用内 **设置 → 关于**（仅显示最近 3 条）。

---

## 反馈与作者

| | |
|--|--|
| 作者 | **makizhang** |
| 反馈与建议 | Telegram [@makichat_bot](https://t.me/makichat_bot) |

欢迎试用与建议。若安装或登录异常，请附上系统版本与现象描述。

---

## 许可证与声明

- 本客户端对接官方 Audiobookshelf REST API，与 ABS 官方项目无隶属关系。  
- 请仅使用你有权访问的服务器与账号，遵守当地法律法规与版权规定。  
- **闭源**：不提供、不上传源代码。  
- 安装包仅发布在 **[GitHub Releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases)**（仅 APK）。  
- 仓库内仅有介绍 README 与界面截图，便于预览与下载说明。  

---

<p align="center">悦耳声阅 · 用耳朵丈量世界</p>
