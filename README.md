# YueErShengYue

<p align="center">
  <strong>English</strong> · <a href="README.zh-CN.md">简体中文</a>
</p>

**YueErShengYue** is an [Audiobookshelf](https://www.audiobookshelf.org/) client for **Android and Windows**, focused on audiobook streaming, library browsing, progress synchronization, and cross-platform favorites.

**Current stable release: 1.0.8 — Android + Windows.** Android `versionCode` **55**. This release improves loading and stability on both platforms and adds favorite synchronization. Windows is available as a standard portable package and an **all-in-one bundle with mpv**.

> This repository contains documentation, screenshots, and release packages only; no application source code is published.

---

## Platforms

| Platform | Package | Requirements | File |
|----------|---------|--------------|------|
| **Android** | Signed release APK | Android 8.0+ (API **26**), `targetSdk` **35**, ARM32 / ARM64 | `YueErShengYue-1.0.8-release.apk` |
| **Windows** | x86_64 portable package | 64-bit Windows; bundled runtime; mpv installed or configured separately | `YueErShengYue-Windows-x86_64-Portable-1.0.8.zip` |
| **Windows (recommended)** | All-in-one portable package | 64-bit Windows; runtime and mpv included | `YueErShengYue-Windows-x86_64-Portable-1.0.8-with-mpv.zip` |

| Identifier | Value |
|------------|-------|
| Application ID | `com.yueer.shengyue` |
| Android version name | `1.0.8` |
| Android version code | `55` |
| Windows package version | `1.0.8` |
| Android minSdk / targetSdk | **26** / **35** |

---

## Download and Install

Official release page: **[YueErShengYue 1.0.8](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/tag/v1.0.8)** — bilingual release notes and all three packages.

Older releases: [1.0.7](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/tag/v1.0.7) · [1.0.6](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/tag/v1.0.6) · [1.0.5](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/tag/v1.0.5) · [All releases](https://github.com/huliyoudiangou/YueErShengYue_APP/releases).

### Direct Downloads

| Platform | Download | Size |
|----------|----------|------|
| Android | [YueErShengYue-1.0.8-release.apk](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.8/YueErShengYue-1.0.8-release.apk) | 3.16 MB |
| Windows x86_64 | [YueErShengYue-Windows-x86_64-Portable-1.0.8.zip](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.8/YueErShengYue-Windows-x86_64-Portable-1.0.8.zip) | 61.93 MB |
| Windows x86_64 **with mpv** | [YueErShengYue-Windows-x86_64-Portable-1.0.8-with-mpv.zip](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.8/YueErShengYue-Windows-x86_64-Portable-1.0.8-with-mpv.zip) | 110.68 MB |

### Android

1. Download the APK and verify its SHA-256 below.
2. Open it on the device; grant permission to install from this source if Android asks.
3. Existing users can install over the previous signed version. This build also upgrades the earlier Android-only 1.0.8 build (code 54).
4. New users: choose a language, enter the Audiobookshelf server address and credentials, and sign in.

### Windows Portable

1. Download the **with-mpv bundle** for an all-in-one setup, or the standard package if mpv is already installed/configured.
2. Verify the checksum and exit the old app, including its tray instance.
3. Extract the whole archive to a new local folder. Keep `app/`, `runtime/`, and, for the bundle, `mpv/` next to `YueErShengYue.exe`.
4. Run `YueErShengYue.exe`. Existing settings remain in `%APPDATA%\YueErShengYue`; do not share that data directory.
5. If a custom mpv path was saved previously, switch to automatic detection in Settings to use the bundled player.

The Windows EXE is not Authenticode-signed; verify the checksum before running it.

### Sync Existing Favorites — Important

- Upgrade **both clients** to this 1.0.8 sync release and sign in to the **same Audiobookshelf server and user account**.
- On **each client**, open **Settings → Favorite sync → Import old local favorites**. This merges old favorites into the current account and preserves the original local data; no automatic upload of unscoped legacy favorites occurs.
- New additions/removals sync through the account's private `YueEr Favorites` playlist. Offline changes are saved for retry; foreground checks run about every 30 seconds, or use **Sync now**.
- No extra server is required. Keep the `yueer:favorites:v1` marker in the playlist description. Sync is not guaranteed while apps are closed; conflicting offline edits to one book converge by the last operation successfully applied on the server.

---

## SHA-256 Verification

Download [SHA256SUMS-1.0.8.txt](https://github.com/huliyoudiangou/YueErShengYue_APP/releases/download/v1.0.8/SHA256SUMS-1.0.8.txt), or compare against this table:

| File | SHA-256 |
|------|---------|
| `YueErShengYue-1.0.8-release.apk` | `6d76b9db4b722275e39f4b05b0ae57e43d940fe1ee19a9dcf8bf414efbd8509d` |
| `YueErShengYue-Windows-x86_64-Portable-1.0.8.zip` | `e10b7e6cef709fd5679cc6f9685881bc7bdf3d66f87492aaf7a2b4d6f6cebc68` |
| `YueErShengYue-Windows-x86_64-Portable-1.0.8-with-mpv.zip` | `1ef7213b422f5aa5525722ebbf10c4f4eae8df14288df39ece3bf572307be797` |

```powershell
Get-FileHash -Algorithm SHA256 .\YueErShengYue-1.0.8-release.apk
Get-FileHash -Algorithm SHA256 .\YueErShengYue-Windows-x86_64-Portable-1.0.8.zip
Get-FileHash -Algorithm SHA256 .\YueErShengYue-Windows-x86_64-Portable-1.0.8-with-mpv.zip
```

For older-package checksums, refer to the corresponding release page.

---

## What's New in 1.0.8

### Android

- Off-main-thread settings and player-cache warm-up; independently loaded home shelves and short-lived detail caching.
- Fixed stale search/page results, overlapping refresh/pagination, repeated-page requests, and retry loops; bounded load timeouts.
- Server/account-scoped atomic snapshots, service-owned stream-cache clearing, bounded cover decoding, and safer authentication on redirects.
- Less hidden-page polling and large-book prefetch work; retains 1.0.7's URI-only media artwork and volume-boost behavior.
- Version **1.0.8**, `versionCode: 55`, with the existing release signing identity.

### Windows

- Stable application-graph lifecycle, asynchronous playback warm-up, and one instance per data profile.
- Consistent library pagination, cancellable/bounded search, scoped shelf/detail caches, and fewer duplicate requests.
- Server/account/size-scoped cover caches; bounded download/decoding and memory use; header-only authentication with redirect checks.
- Coalesced volume persistence, reduced hidden-window activity, standard and mpv-bundled portable packages.

### Both Clients

- Private-playlist favorite synchronization, offline pending operations, explicit legacy import, status display, and manual retry.
- **136 unit tests passed**; Android Lint **0 errors** (49 warnings remain). Signing, 16 KB alignment, packaged Windows playback, and two-way favorite tests passed.
- Cross-client validation used an isolated local fixture. Real-server, device-specific, and long-session testing remains recommended; no universal percentage speed-up is claimed.

---

## What's New in 1.0.7

### Android

- **Bluetooth stability fix (drop + auto-reconnect)**: the "Bluetooth/head-unit album art" feature from 1.0.5 is **removed entirely**. It inlined cover bytes into the media session for AVRCP artwork; even the downscaled payload from 1.0.6 still travels through the media session on every track and caused repeated disconnect/reconnect cycles on some Bluetooth stacks (e.g. Redmi K90 with BT speakers/headphones). The media session now carries only the cover URI again (like 1.0.4) — no artwork bytes are ever inlined. In-app notification covers are unaffected.
- **Volume boost stabilization**: the system LoudnessEnhancer is now attached exactly once per audio session instead of being re-created on every audio-session change. Effect attach/detach churn is itself a known A2DP disturbance on some Bluetooth stacks, so this removes another potential trigger of the drop/reconnect loop.
- **Version**: `versionCode` **53**.

---

## What's New in 1.0.6

### Android

- **Fixed unstable Bluetooth connections (drop + auto-reconnect)**: 1.0.5's "Bluetooth/head-unit album art" feature inlined raw cover bytes (up to 2 MB) into the media notification; oversized Bitmaps forwarded through system UI and Bluetooth AVRCP can disrupt the media session, showing up as repeated Bluetooth disconnect/reconnect cycles. The fix downscales the inlined notification cover to ≤256 px JPEG (~15–60 KB), version-bumps the cover cache to v2 (discarding stale raw-image entries), and removes a per-rebuild full-canvas redraw in the notification icon pipeline.
- **Playback framework upgrade**: Media3 1.5.1 → 1.9.4, picking up the intervening media-notification/session fixes (same-bitmap re-compression, stale foreground-service intents, Bluetooth headset key handling, etc.).
- **Version code fix**: `versionCode` 51 → **52** (1.0.5 and the earlier 1.0.6 build shared 51; installs now upgrade correctly).
- Verified on a real device with a Bluetooth headset: 1 hour of continuous playback, zero disconnects. Pausing on Bluetooth disconnect is standard system behavior; this fix targets the abnormal repeated drop/reconnect loop.

---

## What's New in 1.0.5

### Android

- **Faster tap-to-play**: the play path no longer blocks on a full library-item fetch — play-session metadata is used directly, cutting tap-to-sound from ~4.1s to ~1.4s on real devices.
- **Bluetooth / car head-unit album art**: the media notification now carries inlined artwork bytes (cached, bounded fetch), so AVRCP head units that cannot fetch https URIs show covers again.
- **Database integrity for existing installs**: the local database schema is aligned with the shipped 1.0.4 layout (per-account favorites v4), with a safe 3→4 migration for older installs — no more startup crash loops on upgrade.
- **Safer updates**: in-app update downloads are now pinned to official GitHub hosts (every redirect hop verified).

### Windows

- **Fixed "playback stops after one chapter"**: finishing a chapter could emit a duplicate end-of-file event, double-advancing chapters or cancelling the next chapter's load mid-flight. The finished file's state is invalidated immediately on end-of-file, end detection is suppressed while a file is still opening, and duplicate events are deduplicated. Verified with three consecutive automated multi-chapter runs: one end event advances exactly one chapter.
- **Volume control on the player page**: the same Ximalaya-style horizontal pill as the mini player — tap the speaker icon to expand, tap the track to jump, drag for continuous adjustment.
- **New all-in-one bundle with mpv**: the `with-mpv` portable package bundles the mpv player — extract and run, no separate mpv install needed.
- **Session-hardened local stream proxy**: the built-in audio proxy now requires a per-session secret path and only relays the configured Audiobookshelf origin (fixes local confusion-deputy / SSRF exposure).
- **Token hygiene**: playback candidates never attach the session token to non-Audiobookshelf hosts, and perf logs redact token query values.
- **Crash-safe settings storage**: the settings file (holding the session token) is written atomically — a crash can no longer wipe the session.
- **Faster tap-to-play** on Windows as well: play-session metadata is used directly instead of blocking on a full item fetch.

---

## What's New in 1.0.4

### Android

- **Android performance and UX optimizations**: more stable cold start, cache-first home/library loading, and automatic network fallback when cache reads fail.
- **Fixed first-entry hangs**: home/library no longer stay stuck when the local cache cannot be read.
- **Restored home background refresh**: cached shelves appear first, then a silent refresh updates Continue Listening / Recently Added / Recommendations / Listen Again.
- **Playback loading optimizations**: parallel metadata fetching, asynchronous cache player startup, and reduced prefetch contention.
- **Frosted-glass dock and navigation insets**: unified rounded corners, compact height, and proper support for 3-button navigation.
- **Live cache adjustments**: cache size changes apply immediately and stream-cache clearing uses the safe in-service transaction.

### Windows (first synchronized update to 1.0.4)

- **Windows portable synced to 1.0.4** — it stayed on 1.0.0 through 1.0.1–1.0.3 and is now up to date.
- **Green x86_64 package** with a bundled runtime: extract to any folder and run, no installer required.
- **mpv playback engine**: auto-detects a local mpv.exe (or set a custom path in Settings), with pitch-preserving 0.5x–3.0x speed and sound enhancement.
- **Mini player fixes**: repaired forward-10s button, theme-tinted bar chrome (no near-white panel), and a Ximalaya-style horizontal volume pill floating directly above the speaker icon.
- **Clean exit**: playback and the mpv process stop reliably with the app; leftover mpv from an abnormal exit is reaped on the next start.
- **Close-to-tray playback** with a tray menu (show main window / exit).

## What's New in 1.0.3

- **Home page loads automatically on first entry** — no manual refresh needed.
- **Cache-first on re-entry** for a smoother, faster home page, with a silent background refresh.
- Fixed stale cached recommendations / recently added lists.
- **Sleep timer can auto-exit the app** when the timed duration ends.
- **Player auto-reconnect** when the player is not ready — no need to restart the app.
- Faster first-screen response for **Continue Listening / Listen Again**.
- Fixed a cold-start session-commit latch issue for the first play.
- **Android-only release** (`versionCode` **49**); Windows portable stays on **1.0.0**.

---

## What's New in 1.0.1

- **Android-only release**: Windows portable package stays on 1.0.0 for now.
- **Four themes**: Black Gold, Mint Green, Sakura Pink, and Sky Blue.
- Unified glass treatment for search bar, mini player, and floating dock.
- Floating rounded bottom dock with refined height and presence.
- Playback speed presets on one horizontal line, with theme-aware selected chip colors.
- Sound enhancement enabled by default.
- Daily recommendation refresh, smoother loading, and stability polish.
- Launcher display name: **YueEr**.
- Lean signed release package kept near **3 MB**.

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
- Android/Windows favorite sync for the same ABS account, with offline pending changes and explicit legacy import.
- Cover-grid library browsing, sorting, filtering, and global search.
- Book details with cover art, narrator, description, chapters, and playback controls.
- Daily recommendation refresh with local caching and manual refresh.

### Streaming Cache

- Adjustable streaming cache from **0 to 500 MB**, with a default of **200 MB**.
- Chapter prefetch for the current chapter and the next two chapters.
- Separate controls for clearing cover and streaming caches.

### Themes and Languages

- **Black Gold**, **Mint Green**, **Sakura Pink**, and **Sky Blue** themes.
- **English**, **Simplified Chinese**, and **Traditional Chinese** interfaces.
- Responsive layouts for compact and tall displays.

### Android and Windows Experience

- Android Auto media browsing and playback integration.
- Windows portable distribution with a bundled runtime.
- Windows close-to-tray playback, with reliable mpv cleanup on exit.
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
| **1.0.8** | Android + Windows loading/stability optimization and private-playlist favorite sync; standard and mpv-bundled Windows packages; Android `versionCode` 55 |
| **1.0.7** | Android-only update: Bluetooth stability fix (1.0.5's Bluetooth album-art feature fully removed — no inlined artwork bytes; stable single volume-boost attachment), `versionCode` 53 |
| **1.0.6** | Android-only update: fixed unstable Bluetooth connections (drop + auto-reconnect; downscaled notification artwork + Media3 1.9.4), `versionCode` 52 |
| 1.0.5 | Android and Windows synchronized update: faster tap-to-play, Bluetooth/head-unit album art, database alignment on Android; chapter-end stall fix, volume control and mpv bundle on Windows |
| 1.0.4 | Android performance and UX: cache-first loading, first-entry fixes, frosted dock, navigation-bar insets; Windows portable synced to 1.0.4 (mpv engine, mini-player fixes, close-to-tray, clean exit) |
| **1.0.3** | Android-only update: home auto-load + cached first re-entry, recommended/recently-added stale cache fix, player auto-reconnect, Continue Listening / Listen Again response + cold-start session latch fix |
| 1.0.1 | Android-only update: four themes, glass UI polish, floating dock, speed dialog refinements, sound enhancement default-on, loading/stability work |
| 1.0.0 | Android and Windows synchronized launch; Windows wheel consistency; stability and performance refinements |
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
