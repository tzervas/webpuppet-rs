# webpuppet-rs — Assessment & Gap Analysis

**Date:** 2026-07-08  
**Crate:** `webpuppet` (browser automation library)  
**MCP front:** separate repo `webpuppet-rs-mcp`  
**Security partner:** `security-mcp` (pairing incomplete on main)

---

## 1. Role

Rust library for programmatic browser control (research, QA, automation). High ToS/risk surface — must stay **opt-in**, permissioned, and preferably screened.

---

## 2. Maturity: **2–3 / 5**

| Area | Notes |
|------|--------|
| Core automation | Alpha-capable |
| Security hardwire | Incomplete; large paused branch exists |
| Profile isolation | Weak / real profile reuse risk |
| Docs vs code (security manages both) | Aspirational |
| Fit as cabal default | **No** |

---

## 3. Branches

| Branch | Notes |
|--------|--------|
| `main` (docs base) | Current publish tip |
| Old `dev`/`testing` | Historically **behind** main — do not prefer without re-sync |
| **`claude/review-security-integration-k2KXP`** | Large security pipeline integration — **triage** |

---

## 4. Gaps

| Gap | Sev |
|-----|-----|
| Mandatory screening not on main | High |
| Session/profile isolation | High |
| Permission enforcement only at edges | High |
| HITL APIs incomplete vs docs | Med |
| Clear “library only / MCP only” guidance | Med |

---

## 5. Integration

| Mode | Recommendation |
|------|----------------|
| Direct crate in cabal | **No** default |
| Via webpuppet-rs-mcp | Wave D only, never default-on |
| Behind security-mcp | Required for any cabal enablement |

See [ROADMAP.md](ROADMAP.md). Root [../ROADMAP.md](../ROADMAP.md) may hold older notes — this docs/ roadmap is the cabal-era plan.

## Tero index

Layer-1 citation index: [docs/tero-index/](tero-index/) (`index.json`, `INDEX.md`, `MANIFEST.toml`).
