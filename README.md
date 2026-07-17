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
| **当前版本** | `0.5.0` (versionCode 25) |
| **正式包** | [YueErShengYue-0.5.0-release.apk](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v0.5.0/YueErShengYue-0.5.0-release.apk) |
| **全部版本** | [GitHub Releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases) |

> 仅发布 **APK**，不提供源码。请从 **Releases** 下载安装包。

### 安装提示
- Android 8.0+（API 26+）
- 需允许「未知来源」安装
- 与旧版签名一致时可直接覆盖升级
- 首次使用请自备可用的 **Audiobookshelf** 服务器账号
- **应用内更新**：设置 → 关于 → 检查更新；或启动时自动检查（每日最多一次）。可在应用内下载并校验 SHA-256 后安装，也可浏览器打开 GitHub。

### 校验（可选）
```
sha256: ca7d91868a554f751ba86582d13a1797b8a7326022919c60e28cb5013c5c528e
```

---

## 这是什么？

**悦耳声阅** 是面向 [Audiobookshelf](https://www.audiobookshelf.org/) 的轻量 Android 客户端：流媒体听书、与服务器同步进度、黑金/薄荷绿双主题与多语言。不做整本下载，专注在线收听体验。

登录欢迎语：

> 欢迎加入悦耳声阅  
> 让我们一起用耳朵丈量世界

---

## 主要功能

### 播放
- **倍速** 可调
- **章节列表**：快速跳转任意章节
- **快进 / 快退 10 秒**
- **睡眠定时**：最长 8 小时，封面角显示剩余倒计时；暂停时倒计时同步暂停
- **每书片头片尾**：详情页按秒数输入设置（每章生效，本地保存）
- **进度展示切换**：全书总进度 / 当前章节进度
- **悬浮迷你播放条** + **系统通知栏媒体控件**
- 点击开始播放后 **直接进入播放页**
- 暂停或关闭应用后再次打开，**悬浮窗可恢复**

### 书库与发现
- **首页分区**：继续播放 · 最近添加 · 推荐图书 · 再次收听 · **我的收藏**
- **收藏**：详情页右上角爱心；收藏列表不限数量（本机保存）
- **书库**：三列封面网格，无限下拉；支持排序（标题 / 演播 / 时间等，同项再点切换升降序）
- **全局搜索**：从所有媒体库抓取索引结果
- 最近添加 / 推荐最多 10 本；继续播放、再次收听、收藏不限数量

### 同步与缓存
- 播放进度与服务器同步；暂停/结束自动回传
- **流式缓存**（可设约 200–500MB，默认 200MB）：按章向前缓存，章节切换时丢弃上一章，保持缓存上限
- **封面缓存**；均可在设置页清除
- **不允许整本下载**

### 主题与语言
- **黑金暗色**（默认）/ **薄荷绿亮色**（类 Telegram 圆润 + 毛玻璃）
- 简体中文 / 繁体中文 / English（默认英语；登录页与设置内可切换）

### 其他
- **Android Auto** 曲库浏览与播放控制
- **应用内检查更新**：下载 APK + SHA-256 校验 + 系统安装；浏览器兜底
- 播放器对外标识：`YueErShengYue` / Device: `Android`

---

## 截图

<p align="center">
  <img src="screenshots/home.png" width="180" alt="首页" />
  <img src="screenshots/library.png" width="180" alt="书库" />
  <img src="screenshots/player.png" width="180" alt="播放" />
  <img src="screenshots/settings.png" width="180" alt="设置" />
</p>

> 若截图尚未齐全，以实际安装效果为准。

---

## 版本记录

### 0.5.0
- 应用内下载 APK、SHA-256 校验、系统安装页
- 不自动下载；浏览器打开 GitHub 兜底
- 不做强制更新

### 0.4.9
- 收藏（详情页爱心 + 首页我的收藏）
- 书库三列网格 + 排序筛选
- 首页数量策略调整

### 0.4.8
- 应用内检查更新（跳转 GitHub）

### 0.4.7
- 登录页协议/端口选择；Android Auto；正式包流程

---

## 反馈

- 作者：makizhang
- 反馈与建议：Telegram [@makichat_bot](https://t.me/makichat_bot)

---

## 免责声明

本软件为第三方 Audiobookshelf 客户端，与 Audiobookshelf 官方无隶属关系。请遵守当地法律法规及服务器使用条款。源码暂不公开。
