# btrader — riferimento distinto

Repository storico: https://github.com/riccardopinato/btrader. Il README descrive arbitraggio triangolare crypto su Binance scritto in Rust, con file di configurazione e canale Telegram. Non è un prodotto per azioni/ETF/portafoglio.
Non importare codice da btrader senza verificare license per file, commit esatto, API compatibili e qualità dei moduli; non ereditare API key di crypto da config locali. Alcune conversazioni storiche riportavano installazioni/clonazioni incomplete e errori di configurazione, che NON attestano readiness.
Per FIN-2026-001 la base proposta è nuova architettura domain-specific, non clone btrader. Riutilizzare solo pattern valutati e legalmente compatibili.
