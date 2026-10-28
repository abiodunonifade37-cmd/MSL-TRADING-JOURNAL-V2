# MSL Edge Flow V2.0

An advanced, mobile-first, dark-theme PWA for a liquidity-based trading workflow. V2 prioritizes reliable editing on touch devices, automatic local saving, and safer workspace backups.

## Features
- Overview dashboard and journal-derived performance metrics
- Illustrative candlestick chart with selectable symbol and timeframe
- Editable liquidity map with automatic local save and manual Save map action
- Model validation checklist for sweep, displacement/MSS, entry area and premium/discount
- Simulated footprint ladder, delta/CVD and volume-profile study
- Synthetic bar-by-bar replay lab with persistent replay notes
- Trade journal with create, edit, delete, search, filtering and screenshot upload
- Screenshot optimization to reduce local storage pressure
- Performance analytics: expectancy, profit factor, average win, drawdown, model breakdown and process insights
- Liquidity Academy with saved lesson completion
- Editable reversal/continuation playbook with automatic local save
- Generic risk-sizing calculator
- JSON workspace export/import and local data reset
- PWA manifest and offline service-worker shell
- V1 local data migration when the old workspace exists in the same browser

## Data and trading limitations
This is **not** a live trading terminal. Candles, footprint, CVD and volume profile are synthetic educational samples. There is no live market feed, broker connection, signal service, cloud sync, or order execution. True bid/ask order flow requires compatible trade/tick data and a defined aggressor-side methodology. The generic risk calculator does not know instrument-specific contract sizes, tick/pip values, broker lot increments, fees or account-currency conversion. Verify these before using a position-size estimate.

## Editing and saving
- Tap any field and enter the value. On mobile, the keyboard should appear for text and number fields.
- Liquidity Map and Model Playbook save automatically after a short pause and also have explicit Save buttons.
- Journal trades, replay notes, lesson completion, model-check selections and flow checklist choices are saved locally.
- Local browser storage is device/browser-specific. Clearing browser data or changing devices can remove or leave data behind; export backups regularly.

## Install / run
For basic use, open `index.html` in a modern browser. PWA installation and service-worker offline caching require HTTPS or localhost. If using Android, open the deployed HTTPS website in Chrome and use the browser menu's **Install app** or **Add to Home screen** option when available. Avoid opening the HTML inside a file-preview app, because some previews disable JavaScript or keyboard interaction.

## Deploy on GitHub Pages
1. Extract the ZIP.
2. Put the contents at the repository root so `index.html` is at the root.
3. Commit and push the files.
4. In GitHub, open **Settings → Pages**, select **Deploy from a branch**, choose the main branch and `/ (root)`.
5. Open the HTTPS Pages URL. If an older build is cached, close the installed app and reload the site; V2 uses a new service-worker cache name.

## Files
- `index.html` — page structure
- `styles.css` — visual design and mobile interaction styles
- `app.js` — workspace logic and local storage
- `manifest.webmanifest` — install metadata
- `sw.js` — offline app shell
- `assets/icon.svg` — app icon
