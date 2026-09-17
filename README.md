# BoekhoudPro PWA Mobile v1.1.0

Installeerbare lokale boekhoudapp voor een gecontroleerde proof of concept.

## Starten op Windows

1. Pak het ZIP-bestand uit.
2. Start `start-app.cmd`.
3. Microsoft Edge opent op `http://localhost:8080`.
4. Selecteer in de app **Installeer app** of gebruik in Edge **Apps > BoekhoudPro installeren**.

Python 3 moet lokaal beschikbaar zijn. Alternatief: voer in de projectmap `python -m http.server 8080` uit en open `http://localhost:8080`.

## Starten op macOS/Linux

Voer `./start-app.sh` uit, of `python3 -m http.server 8080`, en open `http://localhost:8080`.

## Mobiele interface

- iPhone-vriendelijke bovenbalk en vaste onderste navigatie
- Veilige schermmarges voor notch en home-indicator
- Grote touchdoelen en kaartweergave voor tabellen
- Snelle acties voor import, controle en rapportage
- Camera-/fotokiezer als voorbereid invoerkanaal
- Mobiele review-sheet voor goedkeuren en afkeuren

Let op: foto-OCR is nog niet lokaal ingebouwd. Afbeeldingen kunnen worden gekozen, maar voor herkenning is een toekomstige Copilot/API-koppeling nodig. UBL/XML en Copilot JSON worden nu volledig verwerkt.

## Functies

- UBL 2.1 XML-import
- Copilot JSON-import met schemaVersion 1.0
- Validatie van totalen, btw, datums, rekeningen en dubbele facturen
- Conceptstatussen: wacht op controle, goedgekeurd, afgekeurd en ongeldig
- Expliciete goedkeuring vóór definitieve boeking
- Journaal, grootboek, proefbalans, balans en winst-en-verliesrekening
- Leveranciersregistratie
- IndexedDB voor lokale opslag
- Audittrail en CSV-export
- JSON-back-up en herstel
- Offline caching via service worker

## Belangrijk

Dit is een lokale PoC en geen gecertificeerd boekhoudpakket. De gebruiker blijft verantwoordelijk voor grootboekkeuze, btw-behandeling, periode, activering en finale goedkeuring. Voor gedeeld of productiegebruik zijn centrale authenticatie, serverdatabase, autorisaties, back-ups en beveiligingsreview nodig.

## Projectstructuur

- `index.html`: gebruikersinterface
- `styles.css`: vormgeving
- `app.js`: workflows, validatie en rapportages
- `db.js`: IndexedDB-opslag
- `ubl.js`: UBL 2.1-parser
- `manifest.webmanifest`: installatiegegevens
- `service-worker.js`: offline cache
- `icons/`: app-iconen
- `samples/`: voorbeeldbestanden
