# AGENTS — Finance Intelligence Agent

- Prima di sviluppare: risolvi UNA volta App-Factory-Core/CURRENT.yaml, Master/Golden Index/Registry correnti, Golden pertinenti; pin commit. Product Bible, Roadmap, repository SOURCE e test reali restano fonti differenziate.
- FIN-2026-001 è un prodotto finanziario di intelligence, non btrader crypto né un broker.
- Il repository è pubblico: usare esclusivamente fixture sintetiche, mai holdings reali, dati personali, credenziali, access token, account number, password o chiavi API.
- Ogni market datapoint deve contenere provider, event-time UTC, observation-time, mercato, unità/valuta, corporate-action adjustment, eventuale ritardo e licensing status.
- Un news summary deve distinguere titolo/origine/fatto verificato da interpretazione; collegamento alla fonte obbligatorio, non inferire causalità dal solo prezzo.
- Default operativo: READ_ONLY; paper trading isolato come attività successiva. Trading live/ordini reali/gestione terzi fuori scope, nessuna scorciatoia.
- Calcoli deterministici e test con dataset sintetici versionati, stress, backtest evitando look-ahead/survivorship, slippage e commissioni espliciti.
- Considerare rischi operativi, servizi esterni, privacy e obblighi di distribuzione prima di monetizzazione.
- I comandi agentici su GitHub rispettano least privilege e gate di approvazione; repository separato da coding agent in token, dataset e permessi.
- Ogni modifica sostanziale: branch, PR, exact-head checks, changelog e provenance. Non trasformare CI PASS in mercato/device/Store CERTIFIED.
- Workflow di contesto aggiorna SOLO SHA/metadata dei repository pubblici monitorati in PR; narrativa finanziaria e segnali richiedono revisione umana/source-backed.
