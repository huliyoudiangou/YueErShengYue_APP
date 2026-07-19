# YueErShengYue

<p align="center">
  <img src="assets/icon.jpg" width="120" alt="YueErShengYue App Icon" />
</p>

<p align="center">
  <b>Audiobookshelf Android audiobook client</b><br/>
  Black &amp; gold dark · Mint green light · Streaming playback · Two-way progress sync
</p>

<p align="center">
  <b>English</b> · <a href="README.zh-CN.md">简体中文</a>
</p>

<p align="center">
  <a href="#download--install">Download</a> ·
  <a href="#features">Features</a> ·
  <a href="#screenshots">Screenshots</a> ·
  <a href="#how-to-use">How to use</a>
</p>

---

## Download &amp; install

| Item | Details |
|------|---------|
| **Current version** | `0.5.5` (versionCode 30) |
| **Package name** | `com.yueer.shengyue` |
| **Requirements** | Android 8.0+ (API 26) |
| **APK** | See [GitHub Releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/latest) |

> On first install, allow installs from unknown sources if the system asks.  
> This repository publishes **docs + official release APK + screenshots only**. Full source code is **not** open-sourced here.

---

## About

**YueErShengYue** is an Android audiobook client for [Audiobookshelf](https://www.audiobookshelf.org/).  
It follows the [official API](https://api.audiobookshelf.org/): login, libraries, playback sessions, and progress upload.  
**Whole-book download is not supported** — only streaming cache for a lightweight, focused listening experience.

Enter your own Audiobookshelf server address (protocol + host + port), then sign in with your account.

---

## Features

### Playback
- **Speed control**: 0.5x – 3.0x
- **Chapter list**: jump to any chapter
- **Seek ±10 seconds**
- **Sleep timer**: theme-colored alarm icon, up to 8 hours, remaining countdown on the cover; countdown pauses when playback pauses
- **Per-book intro/outro skip**: set seconds on the detail page (per chapter, stored locally)
- **Progress mode**: whole-book total progress / current chapter progress
- **Mini floating player** + **system media notification controls**
- Tapping play opens the **full player page** directly
- After pause or app kill, the **mini player can restore** on next open
- **Speed model**: Settings = global default; player can use **Global** (follow Settings) or a **per-book** override

### Library & discovery
- **Home sections**: Continue · Recently added · Recommended · Listen again · Favorites
- **Library browse**: cover + title grid (3 columns), infinite scroll
- **Library sort/filter**: title, narrator, created/modified/added time; tap again to toggle asc/desc
- **Global search** across all media libraries
- **Detail page**: cover, narrator, expandable description, intro/outro skip
- Long titles use a **single-line marquee**; narrator shown as “Narrator: …”
- **Favorites**: heart on the detail page; list under “My favorites” on home
- Long-press **Continue** items to remove and clear progress

### Login & server
- **Protocol**: left dropdown `https://` / `http://` (default https)
- **Host**: domain or IP; pasting a full URL auto-detects protocol
- **Port**: editable (default `443`)
- Protocol is applied when missing; auto-synced when already present in the URL

### Sync & cache
- Progress sync about **every 15 seconds** while playing
- Auto upload on pause / stop
- **Streaming chapter cache** (not whole-book download): prefetch forward, drop finished chapters, keep cache level
- Cache limit **0–500 MB** (default 200; 0 = disable streaming prefetch; prefetch **current + next 2 chapters**)
- Clear **cover cache** / **stream cache** in Settings

### UI & languages
- **Default black & gold dark theme**
- **Mint green light theme** (rounded corners + light frosted glass)
- Languages: **English / Simplified Chinese / Traditional Chinese** (login + Settings; default English)
- Layout tuned for tall narrow phones

### Car
- **Android Auto** library browse & playback
- Requires a complete Android Auto environment; some region-locked devices may be limited

### Boundaries
- Token encrypted at rest
- **Not supported**: whole-book download, offline full library, server admin, ebook reading
- Streaming only — listen-focused

---

## Screenshots

| Home | Book detail |
|:----:|:-----------:|
| ![Home](screenshots/01_home.png) | ![Detail](screenshots/02_detail.png) |

| Player | Library |
|:------:|:-------:|
| ![Player](screenshots/03_player.png) | ![Library](screenshots/04_library.png) |

| Settings |
|:--------:|
| ![Settings](screenshots/05_settings.png) |

> Screenshots from a physical device (theme/language follow local settings).

---

## How to use

1. Install the APK and open the app  
2. Choose language on the login page  
3. Select protocol (https/http), enter **host** and **port** (default 443), then username / password  
4. After login, use **Home**: Continue / Recently added / Recommended / Listen again / Favorites  
5. Open a book → set intro/outro on the detail page if needed → **Play** goes to the player  
6. On the player: speed, sleep timer, chapters; control from the notification while backgrounded  
7. In **Settings**: theme, language, cache size, clear cover / stream cache  

### Progress sync (transparent)
- Starting playback creates a server session  
- Periodic sync while playing; auto upload on pause / end  
- On conflict, the side with the newer update time wins  

### In-app update
- The app checks GitHub Releases for a newer version  
- You can update in-app (download + system install page, SHA-256 verified)  
- Browser download is always available as fallback  
- No forced updates  

---

## Recent changelog

- **0.5.5** — Global default speed always applies to books without override (live Settings change + open race fix); recommended shelf refreshes once per local calendar day (cache-first)  
- **0.5.4** — Settings global default speed + player “Global” / per-book override; recommended once per day  
- **0.5.3** — Sleep timer theme-colored alarm icon; cache 0–500 MB (default 200); stream prefetch current + next 2 chapters  
- **0.5.2** — Fix Continue removal failing (local tombstone + server clear; survives process kill)  
- **0.5.1** — Home local snapshot for faster open; keep intro/outro & favorites across upgrades; long-press remove from Continue  

Full recent entries: in-app **Settings → About** (latest 3 only).  
Download APKs from [Releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases).

---

## Feedback & author

| | |
|--|--|
| Author | **makizhang** |
| Feedback | Telegram [@makichat_bot](https://t.me/makichat_bot) |

Feedback welcome. If install or login fails, please include Android version and a short description.

---

## License & notice

- This client uses the official Audiobookshelf REST API and is **not** affiliated with the ABS project.  
- Only use servers and accounts you are authorized to access; follow local laws and copyright rules.  
- This repository ships: **README docs + official APK + screenshots**.  

---

<p align="center">YueErShengYue · Measure the world with your ears</p>