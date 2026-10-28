# Castagnacopo – le castagne di Caprese Michelangelo

Sito per prenotare le castagne: https://castagnacopo.boneggio.it

## Pagine
- `index.html` – pagina pubblica per ordinare i sacchi da 1, 2, 3 e 5 kg.
- `report.html` – pannello di gestione (accesso con password e verifica in due passaggi).
- `riscossioni.html` – pagina dei referenti ("I miei ordini"), con link personale.
- `preparazione.html` – pagina di chi prepara i sacchetti, con link personale.

## Come funziona
- Le pagine sono statiche e vengono pubblicate da GitHub Pages dal ramo `main`.
- I dati passano da un Cloudflare Worker (cartella `worker/`, pubblicato da Workers Builds) e stanno in un database Cloudflare D1 (`worker/schema.sql`).
- Password, chiavi e token non sono nel codice: stanno nel database (la password del pannello solo come impronta SHA-256).
