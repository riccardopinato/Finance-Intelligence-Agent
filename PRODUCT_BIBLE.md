# Product Bible — FIN-2026-001
Versione 0.1 (DESIGN) — 11 novembre 2026.

## Esigenza
Raccogliere in uno strumento comprensibile informazioni su azioni, ETF, risultati trimestrali, economia e rischi di un portafoglio, anziché saltare tra grafici/news/report scollegati. Non deve confondere correlazione e causalità o promettere previsioni affidabili senza evidenza.

## MVP senza trading
1. Watchlist e quotazioni con licenze e ritardo dati dichiarati.
2. Import portafoglio opt-in tramite inserimento manuale o CSV locale privato, senza caricare dati nei repo pubblici.
3. Analisi allocazione per posizione, settore, valuta e geografia; P&L e rendimento con ipotesi esplicite.
4. News ed eventi (earning, guidance, corporate actions) collegati a fonti e orari.
5. Alert su soglie, volatilità, evento earnings, e rischi; digest programmabili, no spam.

## Fasi successive
- Scenario analysis: stress tecnologici/semiconduttori, tassi, EUR/USD, indici; scenari illustrativi, non previsioni certe.
- Paper trading e backtesting rigoroso con dati point-in-time, benchmark, costi, fiscalità opzionale ben delimitata.
- UI web desktop per uso personale; in futuro companion Flutter se vantaggio dimostrato.

## Privacy e separazione
- Finance Agent non eredita i token di GitHub/coding agent; database e account separati.
- Nessuna vendita dati personali/posizioni, nessuna telemetria contenuti per default.
- API provider solo dopo audit termini, costi, latenza, permessi e copertura.
- Pausa/disabilitazione alert e cancellazione dati portafoglio con lifecycle verificato.

## Non-obiettivi
- Trading autonomo reale, futures/opzioni/leva in MVP, gestioni patrimoniali per terzi, raccomandazioni personalizzate senza conformità, scraping abusivo o promesse di entrate passive certe.
- No abbonamenti/piani dati a pagamento introdotti per convenienza infrastrutturale senza approvazione.

## KPI ipotizzati da misurare
Dati corretti e freschi, false alert rate, copertura news, latenza report, costi per report, data-source error rate, percentuale alert utili, simulazioni riproducibili. Nessun KPI è certificato ora.
