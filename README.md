<p align="center">
  <img src="assets/banner-readme-1200x300.png" alt="RaceEngineer" width="900">
</p>

**RaceEngineer** je desktopová aplikace (Windows a Linux / Steam Deck) pro záznam a analýzu telemetrie ze hry **F1 25** (UDP, formát 2026 Season Pack).

- záznam UDP telemetrie do SQLite
- seznam okruhů s mapou, zatáčkami, rekordem kola a vašimi sessiony
- analýza kol: grafy, mapa trati, porovnání kol, sektory, pozice, nastavení vozu, pneumatiky
- plánovač závodní strategie (okno boxové zastávky, safety car, penalizace)
- MCP server, přes který může AI telemetrii číst i aplikaci ovládat

## Stažení

Balíčky budou na stránce [Releases](../../releases). Zdrojový kód není veřejný.

## Nastavení hry

Ve hře: Nastavení → Telemetrie → UDP telemetrie zapnout, IP `127.0.0.1`, port `20777`, frekvence 20 Hz.

## Zdroje dat

Údaje a obrázky okruhů pocházejí z Wikipedie a Wikimedia Commons (CC BY-SA a další). F1 a F1 25 jsou ochranné známky svých vlastníků; projekt není s nimi nijak spojen.
