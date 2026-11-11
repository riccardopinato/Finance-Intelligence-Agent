# Esempio completamente sintetico — NON posizione reale

Portfolio didattico fittizio (valori inventati SOLO per test): 2 posizioni «ACME» e «BETA», prezzo e valuta interamente sintetici. Gli esempi non descrivono il portafoglio del proprietario e non costituiscono consigli.
Usare fixture con:
1. Apre in EUR, acquisisce una posizione sintetica in USD e una in EUR.
2. Dà al primo titolo uno split 2:1, confermando che il valore non raddoppia.
3. Applica una variazione del cambio sintetica e mostra P&L FX separato.
4. Simula una data di mercato chiusa e un feed stale: bloccare la valutazione o segnalarlo.
5. Applica un drawdown e confronta benchmark senza usare prezzi futuri.
6. Paper trading calcola fee/slippage senza chiamare endpoint reali.
NON usare tickers/quantità presi da screenshot o import personali.
