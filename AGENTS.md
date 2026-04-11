# AGENTS.md

## What this repo is

**Documentation-only** safety kit: preventing irreversible crypto transfer mistakes. Not a trading bot or wallet product.

## Principles (do not violate in edits)

1. **Neutral and tool-agnostic** — no endorsing specific wallets, exchanges, or tokens.
2. **Technically accurate** — base claims on protocol mechanics, not hype.
3. **Preventive** — emphasize verification before send.

## Layout

- `README.md` — overview and table of contents
- `docs/` — numbered topic guides (fundamentals → glossary)
- `tools/` — supporting checklists / references
- `CONTRIBUTING.md` — how to contribute

## When editing docs

- Keep language **clinical and practical**; avoid FUD or investment advice.
- Cross-link related sections instead of pasting duplicate paragraphs.
- Prefer updating the canonical section under `docs/` and linking from `README.md`.

## Doc file map (for agents)

| Topic | File |
|------|------|
| Why transfers fail | `docs/01-fundamentals/why-transfers-fail.md` |
| Networks & asset confusion | `docs/02-networks-and-assets/common-confusion.md` |
| Passkeys & account abstraction | `docs/03-wallet-security/passkeys-and-aa.md` |
| CEX deposit/withdraw | `docs/04-exchange-safety/deposit-withdrawal-checklist.md` |
| Bridges & DeFi risk | `docs/05-defi-and-bridges/bridge-risk-model.md` |
| MEV / sandwich / advanced | `docs/06-advanced-risks/mev-and-sandwich.md` |
| After a mistake | `docs/07-incident-response/what-to-do-after-mistake.md` |
| Glossary | `docs/08-glossary/terms.md` |
