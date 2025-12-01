# CRS Score

Applicazione web per la gestione delle gare e delle performance dei bikers (CRS Factory Racing).

## Contenuto del progetto

- `index.html`  
  File principale dell'app (usa la versione funzionante che hai già, ad esempio `index_2.6.html` rinominato in `index.html`).

- `manifest.webmanifest`  
  File di configurazione PWA (nome app, icone, colori, start URL).

- `service-worker.js`  
  Service Worker minimale per supporto PWA (install / activate / fetch).

- `crs-icon.png`  
  Icona dell'app (sostituire con icona reale 512x512).

- `BANNER.jpg`  
  Immagine di banner usata nell'interfaccia (sostituire con grafica definitiva).

## Setup GitHub Pages

1. Crea un nuovo repository su GitHub.
2. Carica tutti i file:
   - `index.html` (la tua versione funzionante: rinomina il tuo `index_2.6.html` in `index.html`)
   - `manifest.webmanifest`
   - `service-worker.js`
   - `crs-icon.png`
   - `BANNER.jpg`
   - `README.md`
3. Vai su **Settings → Pages**.
4. In **Source**, seleziona:
   - Branch: `main`
   - Folder: `/ (root)`
5. Salva: GitHub genererà un URL del tipo  
   `https://<tuo-username>.github.io/<nome-repo>/`

## Collegamento con Google Apps Script

L'app comunica con la Web App di Google Apps Script tramite la costante `API_URL` dentro `index.html`.

Lo script Apps Script deve:
- usare lo stesso URL deployato che hai inserito in `API_URL`
- puntare al file `CoyoteRace_DB`
- avere i fogli:
  - `USERS`
  - `BIKERS`
  - `RACERS`

Dopo ogni modifica allo script Apps Script, ricordati di fare:
**Deploy → Gestisci deploy → Modifica → Nuova versione → Aggiorna**.
