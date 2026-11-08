# Medemus – hemsida

Enkel grund i ren HTML, CSS och JavaScript. Inget bygg-steg behövs.

## Sidor

| Sida | Fil |
|---|---|
| Startsida | `index.html` |
| Behandling | `pages/behandling.html` |
| Utredning | `pages/utredning.html` |
| Om oss | `pages/om-oss.html` |
| Boka tid | `pages/boka-tid.html` |
| Kontakt | `pages/kontakt.html` |

Designen finns i Figma-filen Medemus (https://www.figma.com/design/wZK5ZJWkrVwrYaTe2xn60w/Medemus). Sidorna i koden följer ramarna där.

## Mappstruktur

```
Medemus/
├── index.html           Startsida
├── pages/               Undersidor
├── css/
│   ├── reset.css        Nollställer webbläsarens standardstil
│   ├── variables.css    Färger, typsnitt, avstånd – källan till sanning
│   ├── base.css         Grundstil för rubriker, brödtext och länkar
│   ├── components.css   Knappar (.btn) m.m.
│   └── site.css         Allt sidspecifikt: header, hero, kort, dragspel, formulär, footer
├── js/main.js           Meny, "Boka tid" som glider in, kopiera e-post, dragspel på mobil, bokningsformulär
├── assets/images/       Bilder som visas på sidan (logotyp och fyra foton)
└── referens/            Material som INTE visas på sidan (referensbilder, designsystem)
```

## Designsystemet

Alla färger och typsnitt (Poppins för rubriker, Inter för brödtext) ligger i `css/variables.css`. Ändrar du en färg där slår det igenom på hela sajten. `referens/dokument/designsystem.html` visar färger, typografi och kontrastvärden (WCAG 2.1 AA).

## Det här bör du känna till

- **Bilder:** Fotona är sparade lokalt i `assets/images/` (från medemus.se): `hero-mottagning.webp` (startsidan), `vi-behandlar-room.webp` (Behandling), `manuela-scheidenberger.webp` (Om oss) och `entre-teatergatan-19.webp` (Kontakt), plus logotypen. Sidorna fungerar därför utan internet, förutom typsnitten som hämtas från Google Fonts.
- **Bokningsformuläret** (`pages/boka-tid.html`) har ingen server. När man skickar kontrolleras fälten och ett färdigt mejl till kontakt@medemus.se öppnas i besökarens e-postprogram. För att ta emot formuläret direkt behövs en formulärtjänst eller en server.
- **Kartan** på Kontakt-sidan är ett foto av entrén med en länk till Google Maps, ingen inbäddad karta.
- **Menyn:** På varje sida glider "Boka tid" in i headern när man scrollar. På mobil ligger knappen i den öppna menyn.

## Komma igång

Öppna `index.html` i webbläsaren, eller kör en lokal server i mappen:

```bash
python3 -m http.server 8000
```

Öppna sedan http://localhost:8000.
