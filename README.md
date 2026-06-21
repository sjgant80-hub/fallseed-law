# FallSeed Law Firm

> **A Progressive Web App (PWA) seed for UK Law firms.**
> One HTML file. Four base tools + LLM-agnostic build engine + Fork Seed packager. MIT. Sovereign.

**Live:** https://sjgant80-hub.github.io/fallseed-law/

## What this is

`fallseed-law` is a single HTML file you can save to your desktop or install as a PWA. It bundles:

- The four base tools of the Law wedge (anchor / onboard / paper / practice)
- A build engine that generates new tools on demand using any LLM (WebLLM in-browser, ollama / LM Studio local, Groq / OpenRouter free cloud, or BYOK paid)
- A Fork Seed packager that lets you mutate the seed for a different vertical or client

## Vertical context

Solicitors · conveyancing · litigation (UK).

## Base tools

| Role | Tool | Purpose |
|---|---|---|
| anchor | [`falllegal`](https://sjgant80-hub.github.io/falllegal/) | Matter register · client/matter records · time recording · WIP · billing · SRA Accounts Rules ledgers · conflict / CDD register |
| onboard | [`falllegalonboard`](https://sjgant80-hub.github.io/falllegalonboard/) | Client onboarding · CDD / KYC · source-of-funds · PEP screen · conflict check · engagement letter · costs information |
| paper | [`falllegalpaper`](https://sjgant80-hub.github.io/falllegalpaper/) | Engagement letter · costs information · client care · complaints procedure · CFA / DBA / fixed-fee templates · S.69 statutory bills |
| practice | [`falllegalpractice`](https://sjgant80-hub.github.io/falllegalpractice/) | File reviews · SRA Accounts Rules reconciliation · AML risk assessment · complaints log · CPD tracker · indemnity renewals · 5-week recs |

## Architecture

- **One HTML file** — no build step, no server, no install
- **IDB primary** — every record lives in `IndexedDB` (`fallseed-law-v2`) on your device
- **BroadcastChannel mesh** — `fall-law` for cross-tool sync; `fall-signal` for global hello
- **P3 audit chain** — `prevHash` + SHA-256 chained entries on every mutation
- **8-provider LLM cascade** — WebLLM (T1) → ollama / LM Studio (T2) → Groq / OpenRouter free / Google / Cerebras (T3-free) → Anthropic (T3-paid)
- **Streaming** — SSE token-by-token output
- **Fork Seed packager** — serialises a mutated SEED back into a new self-contained HTML

## Sovereignty

- MIT-licensed
- No telemetry, no analytics, no tracking
- All data stays on your device (IDB) — nothing posted unless you wire an external LLM
- Works offline once installed as PWA
- One-time payment; upgrades optional

## Cosmology

Prime **1033**, spine-clean mod 127. Mesh channel **`fall-law`**. Bundle roles **anchor / onboard / paper / practice**. Seal **◊·κ=1**.

Part of the FallSeed family — see [www.ai-nativesolutions.com](https://www.ai-nativesolutions.com).

## Licence

MIT © Simon Gant.
