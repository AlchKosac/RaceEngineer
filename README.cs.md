<p align="center">
  <img src="assets/banner-readme-1200x300.png" alt="RaceEngineer" width="900">
</p>

[English](README.md) · **Čeština**

**RaceEngineer** je desktopová aplikace (Windows a Linux / Steam Deck) pro záznam a analýzu telemetrie ze hry **F1 25** (UDP, formát 2026 Season Pack).

- záznam UDP telemetrie do SQLite
- úvodní stránka s okruhy ze hry: mapa, pojmenované zatáčky, rekord kola a vaše sessiony
- analýza kol: grafy kanálů, mapa trati, porovnání kol, sektory, pozice, nastavení vozu, pneumatiky
- plánovač závodní strategie (okno boxové zastávky, safety car, penalizace)
- MCP server, přes který může AI číst telemetrii a ovládat aplikaci
- rozhraní v angličtině (výchozí) a češtině; aplikace se sama aktualizuje z tady vydaných verzí

## Stažení

Balíčky jsou na stránce [Releases](../../releases): `RaceEngineer-win-x64.zip` (Windows) a `RaceEngineer-linux-x64.zip` (Linux / Steam Deck, po rozbalení jednou spusťte `chmod +x RaceEngineer`). Rozbalte **celou složku** a spusťte `RaceEngineer`. Ke každému balíčku je soubor `.sha256` pro ověření. Zdrojový kód není veřejný.

## Nastavení hry

Ve hře: Nastavení → Telemetrie → UDP telemetrie zapnout, IP `127.0.0.1`, port `20777`, 20 Hz.

## Jazyk a aktualizace

V *Soubor → Nastavení* vyberete angličtinu nebo češtinu (projeví se po restartu) a zapnete či vypnete automatickou kontrolu nových verzí. *Nápověda → Zkontrolovat aktualizace* zkontroluje ručně.

## Zdroje dat

Údaje a obrázky okruhů pocházejí z Wikipedie a Wikimedia Commons (CC BY-SA a další); autoři a licence jsou v souboru `Assets/CREDITS.md` v balíčku. F1 a F1 25 jsou ochranné známky svých vlastníků; projekt není s nimi nijak spojen.
