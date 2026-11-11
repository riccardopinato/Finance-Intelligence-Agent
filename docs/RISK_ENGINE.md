# Analytics & Risk — definizioni e test

## Posizione e P&L
Non sommare rendimenti percentuali di titoli. Su ogni lotto specificare quantità, valuta di base, costo, fee, cash flow, corporate actions e metodo cost basis scelto. Currency conversion con FX point-in-time; la variazione EUR/USD può cambiare il risultato di una posizione USD anche a prezzo in dollari invariato.

## Exposures
Weight = mark-to-market value della posizione / valore totale effettivo, con policy per cash e debito. Sector, country, asset type, currency e beta exposures sono dimensioni diverse; un ETF può nascondere concentrazione di look-through e deve essere marcato come parziale se non verificato.

## Rischio e scenari
- Volatilità annualizzata: dichiarare finestra, frequenza, giorni/anno, tipo rendimenti.
- Drawdown: confronto rispetto all'high water mark lungo percorso osservato.
- Correlazioni: finestre allineate temporalmente e numero di osservazioni; NO affermazioni causali.
- Stress test: shock ipotetici (Nasdaq/tech/semiconduttori, USD/EUR, tassi), correlazione assunta esplicita e sensibilità con data.
- Diversificazione: valutare effettiva esposizione a fattori, non solo numero ticker.

## Esempi NON live
Uno scenario "+/- 10% technology" non è un pronostico. Richiede selezione esplicita dei pesi e delta currency. Non trasferire screenshot/valori personali in fixture pubbliche.

## Backtest / Paper
Commissioni, slippage, corporate actions, survivorship bias, look-ahead, puntuale disponibilità dati, walk-forward/out-of-sample e metriche risk-adjusted. Evitare leakage informativo e promesse di rendimento.
