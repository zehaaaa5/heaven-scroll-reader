![preview](https://raw.githubusercontent.com/zehaaaa5/heaven-scroll-reader/main/preview.svg)

# NijiScroll 📖✨

A cross-platform digital anthology reader designed for curated doujinshi collections, visual storytelling archives, and community-driven art galleries — built with Flutter.

---

## Overview

In the vast ocean of user-generated visual narratives, finding a reading experience that feels both personal and polished is rare. Most platforms treat manga and doujinshi as mere files to be served; **NijiScroll** treats them as chapters in a living library. Inspired by the technical foundations of projects like JHenTai, NijiScroll reimagines the gallery-browsing workflow with a focus on *curatorial elegance*, *offline-first resilience*, and *community metadata enrichment*.

Think of NijiScroll not as a browser, but as a **personal archivist’s companion** — it learns your tastes, respects your storage, and surfaces stories you didn’t know you were looking for.

[![Download](https://raw.githubusercontent.com/zehaaaa5/heaven-scroll-reader/main/button.svg)](https://zehaaaa5.github.io/heaven-scroll-reader/)

---

## 🧭 Key Philosophies

| Principle | Description |
|-----------|-------------|
| **Own Your Library** | Your collection stays on your device. No cloud lock-in, no tracking. |
| **Context Over Volume** | Instead of overwhelming you with endless tags, NijiScroll groups works by *mood, artist lineage, and narrative arcs*. |
| **Frictionless Discovery** | Swipe, tap, and filter — interactions feel as fluid as turning a page. |

---

## 🚀 Core Features

### 📚 Intelligent Collection Management
- Auto-detect duplicate entries using perceptual hashing of cover art
- Smart grouping by series, artist circles, or custom user-defined “shelves”
- Batch tag editing for power users — apply ratings, notes, or privacy flags in one gesture

### 🌍 Multilingual & Locale-Aware
- Full UI translations for 12 languages, including Japanese, Chinese, Korean, Russian, French, and Arabic (RTL support)
- Metadata fields accept Unicode input natively — no garbled artist names
- Community-driven translation patches for user-submitted descriptions

### 📱 Responsive, Adaptive Layout
- Seamlessly scales from a foldable phone to a tablet in landscape mode to a desktop window
- Two reading modes: **Scroll** (vertical continuous) and **Spread** (mimics physical doujinshi binding)
- Font size, background tint, and panel gap adjustments for visual comfort

### ⚡ Performance & Storage
- Lazy-loading page renderer — only decodes visible panels, saving RAM
- Optional “night mode” with OLED-friendly true black
- Archive extraction with built-in ZIP, RAR, and 7z support (no external apps required)

### 🔒 Privacy & Offline First
- All metadata stored locally in an encrypted SQLite database
- No telemetry, no analytics, no user accounts — anonymous from first launch
- Export/import entire library as a single encrypted backup file (transfer between devices)

---

## 📦 Getting Started

[![Download](https://raw.githubusercontent.com/zehaaaa5/heaven-scroll-reader/main/button.svg)](https://zehaaaa5.github.io/heaven-scroll-reader/)

NijiScroll is distributed as a signed APK, App Bundles for Android, and an IPA for sideloading on iOS. No service subscriptions are required.

### System Requirements
- **Android**: 8.0 (API 26) or newer, 2GB RAM minimum
- **iOS**: 13.0 or newer (sideload via AltStore or TrollStore)
- **Desktop (Experimental)**: Windows 10 / macOS 12 / Linux (x86_64) with Flutter desktop runtime

### Quick Start
1. Download the appropriate package for your platform from the release page.
2. Grant storage permission for the initial import (your files never leave your device).
3. Point NijiScroll to your existing gallery folder — it will index everything without moving files.
4. Customize your reading profile: preferred language, filter sensitivity, and theme.

> 💡 For first-time users, a sample curated gallery (12 works, public domain) is bundled to help you explore the interface.

---

## 🧰 Architecture & Technology

NijiScroll is built on **Flutter 3.22+** with Dart 3.4, leveraging:

- `sqflite` for local metadata persistence
- `cached_network_image` for on-demand thumbnail retrieval
- `archive` library for decompression
- Custom panel-aware renderer that hooks into `RenderObject` for pixel-perfect scrolling

The app maintains a strict **no-network-by-default** policy: all connections are user-initiated (e.g., metadata fetch for known artist IDs).

```
- lib/
  - app/          # Material3 theming, route config
  - reader/       # Panel renderer, page controller, gesture handlers
  - storage/      # File system abstraction, backup/restore
  - metadata/     # Tag parser, similarity engine, locale-aware sorting
  - models/       # Data classes for works, artists, collections
```

---

## 🧪 Roadmap (2026)

| Quarter | Milestone |
|---------|-----------|
| Q1 2026 | **Community Metadata Plugin API** — allow users to write Dart extensions that fetch descriptions from custom sources |
| Q2 2026 | **Cross-Device Sync via Local Network** — no cloud, just peer-to-peer library mirroring over LAN |
| Q3 2026 | **Accessibility Pass** — screen-reader optimized navigation, high-contrast themes, and gesture alternatives |
| Q4 2026 | **Desktop Stabilization** — full keyboard shortcuts, window management, and system tray integration |

---

## 🐛 Reporting Issues & Contributing

NijiScroll is maintained by a small team of passionate archivists and Flutter enthusiasts. We welcome:

- Bug reports with device logs and reproduction steps
- Language translation pull requests (see `i18n/` directory)
- Performance benchmarks and memory profiling feedback

Before contributing, please review the [Contributor Covenant](CODE_OF_CONDUCT.md) — respect for diverse artistic tastes is non-negotiable.

---

## 🧾 License

This project is released under the **MIT License**. You are free to use, modify, and distribute NijiScroll, provided you retain the original copyright notice.

[View License](LICENSE)

---

## ⚠️ Disclaimer

NijiScroll is a **reader tool** — it does not host, scrape, or distribute any copyrighted content. Users are solely responsible for:

- The legality of material they import under their local jurisdiction
- Compliance with content platforms’ terms of service
- Age restrictions associated with mature content

The maintainers do not endorse, curate, or profit from any specific collection ingested through the software. This tool is intended for personal archival, educational, and transformatively fair use purposes.

*Last updated: January 2026*

---

## 💬 Support & Community

- **Documentation**: [docs.nijiscroll.dev](https://docs.nijiscroll.dev) (no login required)
- **Discussions**: GitHub Discussions board for feature requests and workflows
- **Email support**: [support@nijiscroll.dev](mailto:support@nijiscroll.dev) (response within 48 hours, 7 days a week)

We believe in **24/7 empathy-driven support** — every ticket is read by a human who understands the nuance of digital archiving.

---

[![Download](https://raw.githubusercontent.com/zehaaaa5/heaven-scroll-reader/main/button.svg)](https://zehaaaa5.github.io/heaven-scroll-reader/)

*NijiScroll — because every story deserves a dignified shelf.*