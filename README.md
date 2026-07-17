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
| **当前版本** | `0.5.2` (versionCode 27) |
| **正式包** | [YueErShengYue-0.5.2-release.apk](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v0.5.2/YueErShengYue-0.5.2-release.apk) |
| **全部版本** | [GitHub Releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases) |

> 仅发布 **APK**，不提供源码。请从 **Releases** 下载安装包。

### 安装提示
- Android 8.0+（API 26+）
- 需允许「未知来源」安装
- 与旧版签名一致时可直接覆盖升级
- 首次使用请自备可用的 **Audiobookshelf** 服务器账号
- **应用内更新**：设置 → 关于 → 检查更新；或启动时自动检查（每日最多一次）

### 校验（可选）
```
sha256: 7aaffdeec27026b2214c035d62c4554c197cbf9aebd9d4f2c3dae4325db225ad
```

---

## 这是什么？

**悦耳声阅** 是面向 [Audiobookshelf](https://www.audiobookshelf.org/) 的轻量 Android 客户端：流媒体听书、与服务器同步进度、黑金/薄荷绿双主题与多语言。不做整本下载，专注在线收听体验。

---

## 主要功能

### 播放
- 倍速、章节列表、快进/快退 10 秒
- 睡眠定时（最长 8 小时）
- 每书片头片尾（本机保存，**升级保留**）
- 全书/章节进度切换、悬浮条、通知栏控件

### 书库与发现
- 首页：继续播放 / 最近添加 / 推荐 / 再次收听 / 我的收藏
- **继续播放长按移除**（清服务器进度；旧书/非正在播放同样生效）
- **首页本地快照**冷启动先出书单再后台刷新
- 书库三列网格与排序筛选、全局搜索

### 同步与缓存
- 进度同步；流式缓存 200–500MB；封面缓存；不整本下载

### 其他
- 黑金/薄荷绿主题；简中/繁中/English
- Android Auto；应用内更新（SHA-256 + 系统安装）

---

## 版本记录

### 0.5.2
- 修复「继续播放」移除失败：很早听过、当前未播放的书也可移出
- 本地持久墓碑 + 服务器 hide/DELETE 清除，杀进程/重开不再回弹
- 再次播放同一本后会重新出现在继续播放

### 0.5.1
- 首页本地快照秒开，后台刷新
- 升级保留片头片尾与收藏（修复 Room 破坏性迁移）
- 继续播放长按移除（清进度）

### 0.5.0
- 应用内下载 APK、SHA-256 校验、系统安装页

### 0.4.9
- 收藏、书库网格与排序筛选

---

## 反馈

- 作者：makizhang
- 反馈与建议：Telegram [@makichat_bot](https://t.me/makichat_bot)

---

## 免责声明

本软件为第三方 Audiobookshelf 客户端，与 Audiobookshelf 官方无隶属关系。源码暂不公开。
