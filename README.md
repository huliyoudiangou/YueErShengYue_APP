# YueErShengYue

<p align="center">
  <strong>English</strong> · <a href="README.zh-CN.md">简体中文</a>
</p>

**YueErShengYue** is an [Audiobookshelf](https://www.audiobookshelf.org/) client for **Android and Windows**, focused on a clean audiobook experience with streaming playback, library browsing, and progress synchronization.

**Current stable release: 1.0.0** — Android `versionCode` **33**, with a matching Windows portable build.

---

## Platforms

| Platform | Package | Requirements | File |
|----------|---------|--------------|------|
| **Android** | Signed release APK | Android 8.0+ (API **26**), `targetSdk` **35** | `YueErShengYue-1.0.0-release.apk` |
| **Windows** | x86_64 portable package | 64-bit Windows; bundled runtime | `YueErShengYue-Windows-x86_64-Portable-1.0.0.zip` |

| Identifier | Value |
|------------|-------|
| Application ID | `com.yueer.shengyue` |
| Version name | `1.0.0` |
| Android version code | `33` |
| Android minSdk / targetSdk | **26** / **35** |

---

## Download and Install

Release page: **[YueErShengYue 1.0.0](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/tag/v1.0.0)**

### Direct Downloads

| Platform | Download |
|----------|----------|
| Android | [YueErShengYue-1.0.0-release.apk](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.0/YueErShengYue-1.0.0-release.apk) |
| Windows x86_64 | [YueErShengYue-Windows-x86_64-Portable-1.0.0.zip](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.0/YueErShengYue-Windows-x86_64-Portable-1.0.0.zip) |

### Android

1. Download `YueErShengYue-1.0.0-release.apk`.
2. Verify the SHA-256 checksum below.
3. Open the APK on the device. If Android requests permission to install apps from this source, enable it in system settings.
4. Launch YueErShengYue, select a language, enter the Audiobookshelf server address and account credentials, then sign in.

### Windows Portable

1. Download `YueErShengYue-Windows-x86_64-Portable-1.0.0.zip`.
2. Verify the SHA-256 checksum below.
3. Extract the archive to a local folder, preferably one with a short path and standard write permissions.
4. Run `YueErShengYue.exe`. Keep the bundled `app/`, `runtime/`, and related files in their original relative structure.

---

## SHA-256 Verification

| File | SHA-256 |
|------|---------|
| `YueErShengYue-1.0.0-release.apk` | `AF00CC85D6CBE45AB4C13C913494AEAD10E4DF79ECF2ABC11B2F5D9617083270` |
| `YueErShengYue-Windows-x86_64-Portable-1.0.0.zip` | `090048DDAC795419FD06210C1DADD123CD9358397737122B63CF68E20506C7E1` |

PowerShell example:

```powershell
Get-FileHash -Algorithm SHA256 .\YueErShengYue-1.0.0-release.apk
Get-FileHash -Algorithm SHA256 .\YueErShengYue-Windows-x86_64-Portable-1.0.0.zip
```

Install or run the package after its calculated hash matches the corresponding value above.

---

## What's New in 1.0.0

- **Android and Windows launch together** with matching version numbers.
- **Consistent Windows mouse-wheel behavior on every page**: scroll down to view content below and scroll up to view content above.
- **Stability, responsiveness, and playback-flow improvements** while preserving the existing UI/UX layout.
- Signed Android release APK and self-contained Windows x86_64 portable package.
- Refined playback sessions, progress synchronization, and desktop startup behavior.

---

## Feature Highlights

### Playback and Progress

- Streaming audiobook playback with chapter navigation.
- Playback speed from **0.5x to 3.0x**, with a global default and per-book overrides.
- Sleep timer presets and per-book intro/outro skip settings.
- Playback-session progress synchronization approximately every **15 seconds**, plus updates on pause and stop.
- Android media notifications and lock-screen controls.

### Library and Discovery

- Home sections for Continue Listening, Recently Added, Recommendations, Listen Again, and Favorites.
- Cover-grid library browsing, sorting, filtering, and global search.
- Book details with cover art, narrator, description, chapters, and playback controls.
- Daily recommendation refresh with local caching and manual refresh.

### Streaming Cache

- Adjustable streaming cache from **0 to 500 MB**, with a default of **200 MB**.
- Chapter prefetch for the current chapter and the next two chapters.
- Separate controls for clearing cover and streaming caches.

### Themes and Languages

- Black-and-gold dark theme and mint-green light theme.
- **English**, **Simplified Chinese**, and **Traditional Chinese** interfaces.
- Responsive layouts for compact and tall displays.

### Android and Windows Experience

- Android Auto media browsing and playback integration.
- Windows portable distribution with a bundled runtime.
- Unified mouse-wheel direction across Windows pages.

---

## Screenshots

| Home | Book Details |
|:----:|:------------:|
| ![Home](screenshots/01_home.png) | ![Book details](screenshots/02_detail.png) |

| Player | Library |
|:------:|:-------:|
| ![Player](screenshots/03_player.png) | ![Library](screenshots/04_library.png) |

| Settings |
|:--------:|
| ![Settings](screenshots/05_settings.png) |

Screenshots may reflect a different theme or language depending on the device configuration.

---

## Getting Started

1. Install the Android APK or extract the Windows portable package.
2. Open YueErShengYue and choose the interface language.
3. Select `https://` or `http://`, then enter the host, port, username, and password.
4. Browse the home page or library, open a book, and start playback.
5. Use the player to change chapters, speed, sleep timer, and per-book playback settings.
6. Use Settings to change theme, language, default speed, and cache size.

### Server Address Entry

- Select the protocol from the protocol menu.
- Enter a hostname or IP address in the host field.
- Enter the server port; the default HTTPS port is `443`.
- Pasting a complete URL automatically detects and separates its protocol and host information.

---

## Release History

| Version | Summary |
|---------|---------|
| **1.0.0** | Android and Windows synchronized launch; Windows wheel consistency; stability and performance refinements |
| 0.7.x | Cross-platform version alignment and release hardening |
| 0.5.5 | Global playback-speed behavior and daily recommendation refresh |
| 0.1.0-mvp | Initial application flow and Audiobookshelf integration |

See [GitHub Releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases) for published packages.

---

## Feedback

| | |
|---|---|
| Author | **makizhang** |
| Feedback | Telegram [@makichat_bot](https://t.me/makichat_bot) |

When reporting an installation, login, or playback issue, please include the platform, OS version, server version, and a short description of the observed behavior.

---

<p align="center">YueErShengYue · Measure the world by listening</p>
