# Finance Intelligence Agent — azioni, ETF, mercati e portafoglio

**ID:** FIN-2026-001 · **Tipo:** agente specializzato di analisi finanziaria · **Stato:** DESIGN / KNOWLEDGE BOOTSTRAP, non trading bot attivo. Aggiornato 11/11/2026.

> Questo repository è **pubblico**. Non caricare posizioni reali, screenshot del portafoglio, report bancari, email, token, credenziali broker, API key o dati finanziari personali.

## Visione
Un assistente verificabile per seguire titoli, ETF e portafogli: acquisisce dati con provenienza e timestamp, distingue fatti/news da ipotesi, misura esposizioni e rischi, produce alert intelligibili e permette scenari/paper trading. Riusa l'orchestratore **separato** [App-Factory-Agent-Core](https://github.com/riccardopinato/App-Factory-Agent-Core), senza condividere credenziali e permessi tra finanza e coding.

## Mappe del contesto
- [Product Bible](PRODUCT_BIBLE.md) — scopo, persone, confini e decisioni.
- [Roadmap](ROADMAP.md) — 5 maxi-step con gate misurabili.
- [Architecture](docs/ARCHITECTURE.md) — pipeline dati e separazione tool.
- [Market Data Policy](docs/MARKET_DATA_POLICY.md) — licenze, freshness, corporate actions.
- [Analytics & Risk](docs/RISK_ENGINE.md) — P&L, esposizione, stress test, modello operativo.
- [Signals & Research](docs/RESEARCH_AND_SIGNAL_QUALITY.md) — fonti, classificazioni, valutazione.
- [Safety & Regulation](docs/SECURITY_AND_REGULATION.md) — read-only, paper-only, dati riservati.
- [Provenance](docs/PROVENANCE.md) · [Evidence](evidence/README.md) · [Automation policy](docs/AUTO_UPDATE_POLICY.md).

## Cosa esiste davvero?
| Area | Livello | Nota |
|---|---|---|
| Documentazione architetturale | SOURCE_ADDED | Bootstrap in questa PR |
| Script sincronizzazione commit pubblici | SOURCE_ADDED / CI_PENDING | `scripts/sync_context.py` |
| Feed di borsa/quotazioni | NOT_INTEGRATED | Nessun provider approvato |
| Dashboard, watchlist, performance, alert | ROADMAP | Non sono applicazioni funzionanti |
| Broker e trading reale | OUT_OF_SCOPE | Nessun ordine autorizzato |
| Modello AI | NOT_INTEGRATED | Agent Core esterno ancora da certificare |

## Collegamenti
Dossier centrale proposto: [Ideas PR #90](https://github.com/riccardopinato/Idee-app-Archivi-riferimenti/pull/90). Factory: [CURRENT.yaml](https://github.com/riccardopinato/App-Factory-Core/blob/main/CURRENT.yaml), baseline fissata per questo bootstrap `ee72dbb1b0de2cd71bc4aac42c350853c6915159` (Master v27, Golden Index 29).
Il [repo btrader](https://github.com/riccardopinato/btrader) è arbitraggio crypto/Binance in Rust, un dominio diverso e **non è** l'implementazione di questo agente azionario.

## Regola di prodotto
Nessuna promessa di rendimento, nessuna indicazione automatica “compra/vendi” non spiegata, nessuna esecuzione di ordini: prima osservazione, validazione dei dati e simulazioni. Ogni dato mostrato avrà fonte, valuta, timestamp, delay se pertinente e spiegazione delle limitazioni.
