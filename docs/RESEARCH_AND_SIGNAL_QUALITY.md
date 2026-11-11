# News, ricerca e qualità dei segnali

## Cosa genera un alert utile
Trigger misurabile -> dato e timestamp -> verifica altre fonti se causal claim -> interpretazione separata -> incertezza -> impatto potenziale -> utente decide. Un picco di prezzo NON dimostra da solo quale notizia l'abbia causato.

## Evidenza richiesta per ogni news
publisher, original URL, published_at, event_at se diverso, updated_at, titolo/sintesi originale, instrumento identificato, language, licensing/quote limitations, dedup hash, retrieved_at. Non distribuire lunghi testi protetti da copyright.

## Alert policy
Quiet hours, soglia, frequenza, debounce, cooldown, idempotency, multi-device delivery receipt, retry e opt-out. Se feed stale, sospendere il segnale o marcare NON_VERIFICATO. Non emettere segnale basato su summary LLM non grounded.

## Benchmark
Precision/recall alert, false positives, duplicate news, missing price, earnings surprise, settore-intero vs company-specific, outage provider, orario after-hours. Golden process richiesti solo dopo reuse indipendente.
