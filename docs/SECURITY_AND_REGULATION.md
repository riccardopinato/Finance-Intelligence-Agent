# Sicurezza, dati personali e distribuzione

**Default: READ-ONLY.** Nessun endpoint broker/order API, token di trading o permesso di transazione fa parte dell'MVP. Paper-only sandbox senza capacità di inoltrare ordini a mercati.

## Principali rischi
- Financial hallucination: prezzi, notizie, conti e rendimenti non possono essere inventati o ricavati da fonti senza orario.
- Data poisoning/news injection: contenuti di articoli e feed sono input non fidati, non possono cambiare le regole dell'agente.
- Data leakage: posizioni, broker statements e screenshot mai su repo pubblico o log.
- API data licensing: nessun riuso/redistribuzione prima di audit contratto, entitlements, storage e costs.
- Excessive autonomy: il modello non può transare o impostare alert ad alto rischio senza consenso.
- Runtime: quota GPU/CPU, backoff per API rate limit, durable queue, global kill switch, kill switch per provider.

## Normativa
Per commercializzazione e servizi rivolti a terzi serve valutazione specialistica delle normative pertinenti (in Italia/UE almeno MiFID II/CONSOB ove applicabili, GDPR, termini di mercato, marketing, rischio robo-advice). Questa scheda NON dichiara idoneità legale o autorizzazioni.

## Account/cifratura
Portfolio data in storage privato cifrato e account isolation. Token per eventuali read-only providers in secret manager, mai nel codice; proteggere export/delete/backup. Test permission-denied e cross-tenant isolation.
