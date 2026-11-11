# Roadmap — Finance Intelligence Agent
Stato: DESIGN. Gli item non barrati NON sono implementati.

## Maxi-step 1 — Source intelligence + regole (P0)
- [ ] Definire watchlist, posizione, prezzo, valuta, eventi e provenienza con JSON Schema versionato.
- [ ] Definire disponibilità dati (real-time/delayed/EOD), distribuzione, usi commerciali, costi/provider.
- [ ] Definire pipeline ingest, validazione, dedup, corporate actions e timestamp.
- [ ] Creare fixture *solo sintetiche*, senza dati bancari/personali.
Gate: contratti e test negativi su dato mancante, stale, split, duplicate, simbolo ambiguo.

## Maxi-step 2 — Portfolio & Risk Engine deterministico (P0)
- [ ] P&L realizzato/non realizzato, cost basis, fee, FX, benchmark con definizioni esplicite.
- [ ] Esposizioni titolo/settore/valuta/paese, weight drift e concentrazione.
- [ ] Volatilità, drawdown, scenari e correlazioni con finestre stabilite.
- [ ] Test per timezone, exchange holidays, prezzi zero/mancanti, FX missing, split.
Gate: risultati indipendenti riproducibili su serie sintetiche e edge cases.

## Maxi-step 3 — Research & Signal Quality (P1)
- [ ] News provenance, earnings, guidance, alert engine con idempotenza e cooldown.
- [ ] Classificazione notizia verificata vs ipotesi, ragionamento spiegabile e fonti.
- [ ] Analisi di qualità delle fonti e falsi positivi; niente news causation inventata.
Gate: tutti gli alert hanno fonte/timestamp/rationale e unsubscribe.

## Maxi-step 4 — MVP personale read-only + paper (P1)
- [ ] UI portfolio/watchlist, consenso e storage privato; nessun broker login necessario.
- [ ] Report giornaliero/settimanale, quiet hours, esportazione risultati.
- [ ] Backtest/paper-mode ISOLATO da broker, slippage/fees/survivorship/look-ahead.
Gate: zero ordini reali possibili; privacy review; autorizzazioni minime.

## Maxi-step 5 — Cross-agent reuse & validazione (P2)
- [ ] Riusare in modo pin/versionato job queue e approval dei servizi dell'Agent Core dopo loro certificazione.
- [ ] Benchmark e evidence reali, confronto report/snapshot, policy store/regolamentare.
- [ ] Aggiornare idee/CAP soltanto con nuova evidenza e dedup, eventuale proposta Donor.
Gate: sicurezza, qualità dati, costi/licenze, manutenzione e manual approvals.

Nessuna milestone di broker live trading è autorizzata da questa roadmap.
