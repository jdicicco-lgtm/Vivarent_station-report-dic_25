# Vivarent Dashboard — Dicembre 2025

Dashboard statica (HTML/CSS/JS) pronta per GitHub Pages.

## Struttura
```
.
├─ index.html
├─ styles.css
├─ app.js
└─ data/
   ├─ bookings.json
   ├─ occupation.json
   ├─ fleet.json
   ├─ service.json
   ├─ incidents.json
   └─ manifest.json
```

## Come pubblicarla su GitHub Pages (senza build)
1. Crea un repo su GitHub (es. `vivarent-dashboard`).
2. Copia questi file nella root del repo.
3. Vai su **Settings → Pages** e seleziona:
   - Source: `Deploy from a branch`
   - Branch: `main` / root
4. Apri l'URL indicato da GitHub.

## Filtri
- **Agiscono su:** KPI Revenue / Ancillaries / Incidenti / Prenotazioni + donut canali + bar provider + trend + tabella.
- **Non agiscono su:** Occupazione, Flotta, Manutenzione.

## Note KPI
- `Revenue/day` e `Ancillaries/day` sono normalizzati su **somma dei rental days** (campo `durationDays`).

## Rigenerare i JSON
I JSON sono derivati dall'Excel `REPORT DICEMBRE 25.xlsx`. Se vuoi automatizzare la rigenerazione (CI), crea uno script Python che legge l'xlsx e sovrascrive i file in `/data`.
