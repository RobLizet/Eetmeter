# Voedingstracker

Zelfstandige PWA om calorieën, eiwitten, koolhydraten, vet en gewicht bij te houden.
Werkt volledig lokaal (localStorage) en offline; alleen barcode scannen/zoeken heeft internet nodig (Open Food Facts, gratis, geen API-key).

## Deployen via GitHub (web interface)

1. Maak een nieuwe repo op github.com, bv. `voedingstracker`.
2. Upload deze 5 bestanden naar de root van de repo:
   `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`
3. Ga naar **Settings → Pages** in de repo.
4. Bij "Build and deployment" kies **Deploy from a branch**, branch `main`, map `/ (root)`. Opslaan.
5. Na ~1 minuut is de app live op `https://JOUWGEBRUIKERSNAAM.github.io/voedingstracker/`.
6. Open die URL op je telefoon → menu → "Toevoegen aan startscherm" om als app te installeren.

## Scannen

Barcode scannen gebruikt de `BarcodeDetector`-API van de browser (werkt op Chrome/Android). Als dat niet wordt ondersteund, val je automatisch terug op zoeken of handmatig invoeren.

## Back-up

Alle data staat in localStorage van de browser. Ga naar **Doelen → Gegevens → Exporteren** om regelmatig een JSON-back-up te downloaden.
