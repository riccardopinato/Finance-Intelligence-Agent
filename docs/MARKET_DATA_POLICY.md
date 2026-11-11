# Market data — policy di acquisizione e qualità

## Provider onboarding — obbligatorio
Per ogni provider registrare: link termini/licenza commerciale, utilizzo/display/redistribuzione, budget/rate-limit, storico disponibile, eventuale delayed/non-real-time, copertura venue, ritardo effettivo, SLA, calendari, split/dividend adjustment, quote valuta, cancellazione, fallback, costi.
Nessun provider attualmente è stato selezionato, acquistato o integrato. **Non presumere che una API gratuita possa alimentare un prodotto commerciale.**

## Data contracts
- `event_time_utc`: tempo della transazione/chiusura rilevante, non orario di scraping.
- `ingested_at_utc`: timestamp di ricezione, sempre distinguibile.
- `time_basis`: OPEN/MID/CLOSE/BID/ASK/INDICATIVE/EOD coerente col dato.
- `as_of`: data di riferimento della serie; non mischiare prezzi aggiustati e non.
- `provider_id`, `source_url`, `license_review`, `is_delayed`: obbligatori.
- `symbol` senza exchange/ISIN/identità persistente non è chiave universale affidabile.

## Quality rules
Monotonicity/idempotency event keys, reject wrong currency/unit, detect gap/stale/outlier with explanatory statuses; avoid silent interpolation for P&L, validate FX fixing and dividends. Salvare provenance di correzioni e corporate actions.
Market close/holiday/after-hours nel fuso locale della borsa, UI in Europe/Rome solo per display; non far cambiare la data economica col fuso visuale.
