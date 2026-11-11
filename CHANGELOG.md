# Changelog
## 2026-11-11 — Snapshot workflow merge identity fixed (CI validated)
- Live Agent Core [rerun #43040897071](https://github.com/riccardopinato/App-Factory-Agent-Core/actions/runs/43040897071) found a shared workflow defect: `git merge --no-edit` could run before `git config user.name/user.email`, producing `Committer identity unknown` when the base advanced.
- Fixed the same snapshot workflow on this repository using [PR #4](https://github.com/riccardopinato/Finance-Intelligence-Agent/pull/4), keeping metadata-only PR workflow, daily cron and `workflow_dispatch` unchanged. The fix is **CI_VERIFIED, NOT independently RUNTIME_VERIFIED** on this repository.
- In the Agent Core donor, [real run #43052705998](https://github.com/riccardopinato/App-Factory-Agent-Core/actions/runs/43052705998) confirmed successful branch merge after the fix; the separate GitHub Actions create-PR admin setting remains blocked there. No product implementation, financial trading, renderer, or Golden promotion.

## 2026-11-11 — Knowledge bootstrap
- Documentate visione Finance Intelligence Agent, separazione da btrader crypto, lifecycle informazioni finanziarie, quality/market data policy, risk metrics, threat model e roadmap.
- Aggiunti schemi JSON di progetto (NON API implementate), esempi interamente sintetici, provenance, evidence.
- Inseriti workflow source-snapshot/CI e politica PR-only. Trading reale e broker API non integrati né autorizzati.
