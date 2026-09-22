<div align="center">

# Decan MovieBox-TUI

**A powerful terminal interface for discovering, downloading, and streaming movies, TV shows, anime, and live TV using local media players.**

**Built and maintained by [Lenny Muriuki](https://github.com/lenvartica)**

[ English ](README.md)

[![GitHub](https://img.shields.io/badge/GitHub-lenvartica-181717?style=flat\&logo=github)](https://github.com/lenvartica)
[![Repository](https://img.shields.io/badge/Repository-decan--movie---blue?style=flat\&logo=github)](https://github.com/lenvartica/decan-movie-)
[![Developer](https://img.shields.io/badge/Developer-Lenny%20Muriuki-04AA6D?style=flat)](https://github.com/lenvartica)

</div>

[moviebox-tui-walkthrough.webm](https://github.com/user-attachments/assets/7554a7e5-6ff5-49ec-9d87-f821ea99950e)

---

## About Decan MovieBox-TUI

**Decan MovieBox-TUI** is a terminal-based media application developed and maintained by **Lenny Muriuki / LenvarTica**.

The project provides a fast terminal interface for discovering and watching movies, TV shows, anime, and live television while supporting multiple media players and streaming providers.

The project is part of the **Decan Techs** ecosystem and is developed with a focus on practical software engineering, performance, cross-platform compatibility, and an efficient terminal user experience.

**Developer:** Lenny Muriuki
**GitHub:** [@lenvartica](https://github.com/lenvartica)
**Project:** [Decan MovieBox-TUI](https://github.com/lenvartica/decan-movie-)
**Website:** [Decan Konnect](https://decan-konnect.vercel.app/)
**Country:** Kenya 🇰🇪

---

## Features

* **On Demand Streaming**: Stream movies, series, and anime across multiple providers and community Stremio addons.
* **Live TV and IPTV**: Import custom M3U playlist URLs to search channels, browse categories, and stream live television.
* **Native Video Playback**: Plays directly in your favorite player (`mpv`, `IINA`, `VLC`, or Android video players) with smooth hardware acceleration.
* **Automatic Subtitles**: Automatically searches and loads subtitles in your preferred language into your player.
* **Fast Downloads**: Save single episodes or entire seasons to your computer with pause and resume support.
* **Visual Posters**: Displays cover art and movie posters directly inside your terminal window.
* **Library and History**: Bookmark your favorite titles and pick up watching right where you left off.
* **Custom Themes**: Built-in color themes and settings to match your personal terminal look and feel.
* **Cross Platform**: Works across macOS, Linux, Windows, and Android through Termux.
* **Terminal First**: Designed for users who prefer a fast, keyboard-driven media experience.
* **Local Configuration**: User settings, history, and favorites remain on the local device.
* **Multiple Providers**: Supports multiple content providers and addon-based sources.
* **Download Management**: Supports download management with pause and resume capabilities.

---

## Project Information

| Information              | Details                           |
| :----------------------- | :-------------------------------- |
| **Project Name**         | Decan MovieBox-TUI                |
| **Developer**            | Lenny Muriuki                     |
| **GitHub Username**      | `lenvartica`                      |
| **Repository**           | `lenvartica/decan-movie-`         |
| **Primary Language**     | Rust                              |
| **Interface**            | Terminal UI                       |
| **Platforms**            | Linux, macOS, Windows, Android    |
| **Organization / Brand** | Decan Techs                       |
| **Developer Website**    | https://decan-konnect.vercel.app/ |
| **License**              | MIT / Apache-2.0                  |

---

## Prerequisites

Decan MovieBox-TUI requires at least one compatible media player for streaming.

### mpv

Recommended across:

* Linux
* macOS
* Windows

### IINA

Recommended for:

* macOS

### VLC

Available across multiple platforms:

* Windows
* Linux
* macOS
* Android

### Android Video Players

Android users running the application through Termux can use compatible video players such as:

* VLC
* Just Player
* MX Player

### Terminal Graphics

Poster graphics require a graphics-capable terminal.

Supported terminals may include:

* Ghostty
* Kitty
* WezTerm
* iTerm2

Standard terminals automatically fall back to clean text layouts.

### Optional Download Dependencies

For MovieBox downloads using DASH streams, the following tools may be required:

* `yt-dlp`
* `ffmpeg`

Other providers can use the built-in download engine where supported.

---

## Installation

### macOS and Linux

Clone the repository:

```bash
git clone https://github.com/lenvartica/decan-movie-.git
cd decan-movie-
```

Build the application:

```bash
cargo build --release --locked
```

Run the compiled application:

```bash
./target/release/moviebox-tui
```

### Windows

Open PowerShell:

```powershell
git clone https://github.com/lenvartica/decan-movie-.git
cd decan-movie-
cargo build --release --locked
```

Run:

```powershell
.\target\release\moviebox-tui.exe
```

### Android / Termux

Install the required packages:

```bash
pkg update
pkg install -y git rust cargo curl ffmpeg
```

Clone the repository:

```bash
git clone https://github.com/lenvartica/decan-movie-.git
cd decan-movie-
```

Build:

```bash
cargo build --release --locked
```

Run:

```bash
./target/release/moviebox-tui
```

Configure Android storage if required:

```bash
termux-setup-storage
```

An external Android media player such as VLC may be required for playback.

---

## Cargo Installation

If a published Cargo package is available, it can be installed with:

```bash
cargo install moviebox-tui --locked
```

For development directly from this repository:

```bash
git clone https://github.com/lenvartica/decan-movie-.git
cd decan-movie-
cargo build --release --locked
```

---

## Quick Start

After installation, launch the application:

```bash
moviebox-tui
```

You can then:

* Search for a title.
* Select a movie, series, or anime.
* Choose an available stream.
* Launch playback using your configured media player.
* Add titles to your favorites.
* View your watch history.
* Configure application preferences.
* Browse available live TV sources.

Inside the TUI:

```text
?
```

opens the available keyboard shortcuts.

Settings can be accessed through:

```text
/settings
```

---

## Keyboard Navigation

MovieBox-TUI is designed around keyboard-driven navigation.

Typical controls include:

| Key     | Function          |
| :------ | :---------------- |
| `Enter` | Select / Play     |
| `Esc`   | Close / Go Back   |
| `↑`     | Navigate Up       |
| `↓`     | Navigate Down     |
| `←`     | Navigate Left     |
| `→`     | Navigate Right    |
| `?`     | Show Help         |
| `/`     | Commands / Search |
| `q`     | Quit              |

Available controls may vary depending on the active screen and configuration.

---

## Configuration

Application configuration is stored locally on the user's device.

Configuration can be used to manage settings such as:

* Media players
* Themes
* Providers
* Subtitles
* Downloads
* Network behavior
* Playback preferences
* Favorites
* History
* Addons

Run:

```text
/settings
```

inside the application to access available settings.

---

## Providers and Addons

Decan MovieBox-TUI supports multiple provider implementations and community addon integrations.

The provider architecture is designed to allow different content sources to be integrated without changing the core terminal interface.

Provider-related functionality can be found inside:

```text
src/providers/
```

Addon functionality is located inside:

```text
src/providers/addons/
```

---

## Live TV and IPTV

The application supports custom M3U playlists for live television and IPTV sources.

Users can configure compatible playlists and browse available channels through the terminal interface.

The application does not provide or operate IPTV services itself.

Users are responsible for ensuring that any playlist or media source they configure is legally available to them.

---

## Downloads

Decan MovieBox-TUI supports downloading compatible media sources.

Depending on the provider and stream type, downloads may use the built-in download engine or external tools.

For supported DASH downloads, install:

```bash
yt-dlp
```

and:

```bash
ffmpeg
```

Always ensure that you have the appropriate rights to download content.

---

## Development

Clone the repository:

```bash
git clone https://github.com/lenvartica/decan-movie-.git
```

Enter the project:

```bash
cd decan-movie-
```

Build the project:

```bash
cargo build
```

Build an optimized release:

```bash
cargo build --release --locked
```

Run the application during development:

```bash
cargo run
```

Run tests:

```bash
cargo test
```

Run formatting:

```bash
cargo fmt
```

Run Clippy:

```bash
cargo clippy
```

---

## Project Structure

```text
decan-movie-
├── .cargo/
├── .github/
├── docs/
├── src/
│   ├── providers/
│   ├── tui/
│   ├── updater/
│   ├── cache.rs
│   ├── config.rs
│   ├── download.rs
│   ├── favorites.rs
│   ├── history.rs
│   ├── lib.rs
│   ├── logging.rs
│   ├── main.rs
│   ├── models.rs
│   ├── net.rs
│   ├── player.rs
│   ├── proxy.rs
│   └── service.rs
├── tests/
├── Cargo.toml
├── Cargo.lock
├── LICENSE-APACHE
├── LICENSE-MIT
└── README.md
```

---

## Documentation

Project documentation is available inside the repository:

```text
docs/
```

Important documentation includes:

* Architecture
* Configuration
* Controls
* Downloads
* Installation
* Logging
* Modules
* Players
* Providers
* Testing
* TV mode
* Troubleshooting

Browse the documentation directory:

https://github.com/lenvartica/decan-movie-/tree/main/docs

---

## Contributing

Contributions are welcome.

Before submitting changes:

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test the application.
5. Run formatting and linting.
6. Commit your changes.
7. Open a pull request.

Repository:

https://github.com/lenvartica/decan-movie-

---

## Bug Reports

If you encounter a problem, please provide:

* Operating system
* Architecture
* Rust version
* Application version
* Media player
* Relevant error message
* Steps to reproduce the problem

Open an issue:

https://github.com/lenvartica/decan-movie-/issues

---

## Developer

### Lenny Muriuki

**Full-Stack Developer • AI Builder • Technology Creator**

GitHub:

https://github.com/lenvartica

Portfolio:

https://decan-konnect.vercel.app/

Organization / Brand:

**Decan Techs**

Country:

**Kenya 🇰🇪**

The project is developed as part of the wider **Decan Techs / Decan Konnect** technology ecosystem.

---

## Decan Techs

**Decan Techs** is the development identity behind projects created by Lenny Muriuki.

The broader ecosystem focuses on:

* Software development
* Web applications
* Artificial intelligence
* Automation
* Developer tools
* Mobile applications
* Technology education
* Digital products

Main website:

https://decan-konnect.vercel.app/

GitHub:

https://github.com/lenvartica

---

## Privacy

Decan MovieBox-TUI is designed without built-in telemetry, analytics, or user tracking.

Search history, favorites, and application configuration are stored locally according to the application's configuration and operating environment.

Users should review the source code and their configured providers/addons when evaluating privacy characteristics.

---

## License

This project is licensed under either:

* [MIT License](LICENSE-MIT)
* [Apache License 2.0](LICENSE-APACHE)

You may choose either license according to the terms provided in the corresponding license file.

---

## Disclaimer

Decan MovieBox-TUI does not host or store media content.

The application is a client/interface that can interact with configured media sources, providers, addons, playlists, and external media players.

The availability and legality of individual media sources depend on the source provider and the laws applicable to the user.

Users are responsible for complying with applicable laws, copyright requirements, licensing restrictions, and the terms of services they access.

The developer and Decan Techs do not claim ownership of third-party media or third-party services accessed through the application.

---

## Acknowledgements

This project uses open-source software and libraries maintained by developers and communities around the world.

Special thanks to the Rust ecosystem and the developers of the libraries, terminal frameworks, media players, and tools that make projects like this possible.

---

<div align="center">

**Decan MovieBox-TUI**

Built with Rust 🦀

**Developed by Lenny Muriuki**

**Decan Techs 🇰🇪**

[GitHub](https://github.com/lenvartica) • [Decan Konnect](https://decan-konnect.vercel.app/)

© 2026 Lenny Muriuki / Decan Techs

</div>
