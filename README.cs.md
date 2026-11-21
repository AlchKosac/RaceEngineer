<p align="center">
  <img src="assets/logo/png/banner-readme-1200x300-cs.png" alt="RaceEngineer" width="900">
</p>

[English](README.md) · **Čeština**

**RaceEngineer** je desktopová aplikace (Windows, macOS a Linux / Steam Deck) pro záznam a analýzu závodní telemetrie z více her.

## Podporované hry

| Hra | Zdroj dat |
|---|---|
| **F1 25** (2026 Season Pack) | UDP telemetrie |
| **Forza Horizon 6** | Data Out (Xbox nebo PC) |
| **Forza Horizon 5** | Data Out (Xbox nebo PC) |
| **Assetto Corsa EVO** | sdílená paměť (Windows, hra na stejném PC) |
| **RaceRoom Racing Experience** | sdílená paměť (Windows, hra na stejném PC) |

## Funkce

- záznam UDP telemetrie do SQLite, import nahrávek `.bin`
- úvodní stránka s okruhy ze hry: mapa, pojmenované zatáčky, rekord kola a vaše sessiony
- analýza kol: grafy kanálů, mapa trati, porovnání kol, sektory, pozice, nastavení vozu, pneumatiky
- plánovač závodní strategie (okno boxové zastávky, safety car, penalizace)
- rozhraní v angličtině (výchozí) a češtině, automatické aktualizace z GitHub Releases

## Spuštění

Stáhněte balíček z veřejného repozitáře [RaceEngineer](https://github.com/AlchKosac/RaceEngineer/releases), rozbalte **celou složku** (včetně `Assets/`) a spusťte `RaceEngineer`. Postup nastavení každé hry je přímo v aplikaci (u F1 25: UDP telemetrie na `127.0.0.1:20777`, formát 2025, 20 Hz).

Vývoj: `dotnet run --project src/RaceEngineer.Desktop`, testy: `dotnet test`. Podrobnosti jsou v `docs/NAVRH.md` a `docs/DISTRIBUCE.md`.

## Repozitáře

- **RaceEngineer-SourceCode** (soukromý): zdrojový kód, dokumentace a testy.
- **[RaceEngineer](https://github.com/AlchKosac/RaceEngineer)** (veřejný): README, logo a stahovatelné balíčky (Releases). Aplikace v něm hledá nové verze.

## Vydání nové verze

1. Zvyšte `<Version>` v `src/RaceEngineer.Desktop/RaceEngineer.Desktop.csproj`.
2. `tools/release.ps1 -Publish` sestaví `RaceEngineer-win-x64.zip` a `RaceEngineer-linux-x64.zip` se soubory SHA-256 a vytvoří GitHub Release `v<Version>` ve veřejném repozitáři.

## Logo

Zdroje a všechny velikosti jsou v `assets/logo/` (SVG, PNG 16–1024 px, `app.ico`, bannery). Znovu je vygeneruje `dotnet run --project tools/LogoGen -- <kořen repozitáře>`.

## Licence a zdroje dat

Údaje a obrázky okruhů pocházejí z Wikipedie a Wikimedia Commons (CC BY-SA a další); autoři a licence jsou v `src/RaceEngineer.Circuits/Assets/CREDITS.md`. Specifikace UDP od EA se nedistribuuje. F1 a F1 25 jsou ochranné známky svých vlastníků; projekt není s nimi nijak spojen.
