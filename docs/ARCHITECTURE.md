# Architettura di riferimento (non codice prodotto)

```text
Public/contracted market data + official filings + vetted news
 -> Provider adapters (rate-limit, licensing, retries)
 -> Provenance/timezone/market-calendar validation
 -> Canonical events & prices (immutable source receipt)
 -> Adjustments: split, dividends, symbol change, currency
 -> Read-only query & portfolio engine
       |-- Allocation, cost basis & P&L
       |-- Risk, scenario, benchmark
       |-- News evidence/research
       |-- Signals + explanation
 -> Alert gateway (dedup, cooldown, consent)
 -> User dashboard / scheduled digest
 -> Separate sandbox for paper trading (NO broker routes)
```

## Boundaries
Data ingestion non autorizza trading; parser di news non autorizza scrittura su conto. Non dare al Finance Agent lo stesso PAT GitHub/LLM/coding del core developer. Authenticated user data in private store (TBD), non in Git.
Provider di market data e info regolamentate non equivalgono a provider di esecuzione ordini.

## Modello concettuale
Ticker con exchange/venue/currency e historical identity; quote con event_time/ingested_time/delay/source; position con units, lots and fees; FX fix con time/market source; corporate action con ratio/effective date e reference; evidence con URL hash e publisher timestamp.
Un modello generativo può aiutare a scrivere report ma numeri, citazioni e ordini delle operazioni devono essere calcolati e verificati in modo deterministico.

## Integrazione Agent Factory
AGF fornisce *se certificato* task orchestration, retry e notification abstractions; FIN mantiene security boundary, schema, risk domain e storage. Un AGF non può leggere i dati finanziari senza autorizzazione specifica.
