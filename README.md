<p align="center">
  <img src="assets/logo/png/banner-readme-1200x300.png" alt="RaceEngineer" width="900">
</p>

**English** · [Čeština](README.cs.md)

**RaceEngineer** is a desktop application (Windows, macOS and Linux / Steam Deck) that records and analyses racing telemetry from several games.

## Supported games

| Game | Source |
|---|---|
| **F1 25** (2026 Season Pack) | UDP telemetry |
| **Forza Horizon 6** | Data Out (Xbox or PC) |
| **Forza Horizon 5** | Data Out (Xbox or PC) |
| **Assetto Corsa EVO** | shared memory (Windows, game on the same PC) |
| **RaceRoom Racing Experience** | shared memory (Windows, game on the same PC) |

## Features

- records UDP telemetry into SQLite, imports `.bin` captures
- home page with the circuits of the game: map, named turns, lap record and your own sessions
- lap analysis: channel charts, track map, lap comparison, sectors, positions, car setup, tyres
- race strategy planner (pit window, safety car, penalties)
- English (default) and Czech interface, automatic updates from GitHub Releases

## Running

Download the package from the public [RaceEngineer releases](https://github.com/AlchKosac/RaceEngineer/releases), unpack the **whole folder** (including `Assets/`) and start `RaceEngineer`. Each game has its own setup steps inside the application (for F1 25: UDP telemetry to `127.0.0.1:20777`, format 2025, 20 Hz).

Development: `dotnet run --project src/RaceEngineer.Desktop`, tests: `dotnet test`. Details are in `docs/NAVRH.md` (design, Czech) and `docs/DISTRIBUCE.md` (distribution, Czech).

## Repositories

- **RaceEngineer-SourceCode** (private): the source code, documentation and tests.
- **[RaceEngineer](https://github.com/AlchKosac/RaceEngineer)** (public): README, logo and the downloadable packages (Releases). The application checks this repository for new versions.

## Releases

1. Raise `<Version>` in `src/RaceEngineer.Desktop/RaceEngineer.Desktop.csproj`.
2. `tools/release.ps1 -Publish` builds `RaceEngineer-win-x64.zip` and `RaceEngineer-linux-x64.zip` with SHA-256 files and creates the GitHub Release `v<Version>` in the public repository.

## Logo

Sources and all sizes are in `assets/logo/` (SVG, PNG 16–1024 px, `app.ico`, banners). `dotnet run --project tools/LogoGen -- <repository root>` regenerates them.

## Licences and data sources

Circuit data and images come from Wikipedia and Wikimedia Commons (CC BY-SA and other licences); authors and licences are listed in `src/RaceEngineer.Circuits/Assets/CREDITS.md`. The EA UDP specification is not redistributed. F1 and F1 25 are trademarks of their owners; this project is not affiliated with them.
