# webpuppet-rs — Assessment & Gap Analysis

**Date:** 2026-07-16 (TLC refresh; original 2026-07-08)  
**Crate:** `webpuppet` (browser automation library)  
**MCP front:** separate repo `webpuppet-rs-mcp`  
**Security partner:** `security-mcp` (still recommended for multi-agent cabal use)

---

## 1. Role

Rust library for programmatic browser control (research, QA, automation). High ToS/risk surface — must stay **opt-in**, permissioned, and screened.

---

## 2. Maturity: **3 / 5**

| Area | Notes |
|------|--------|
| Core automation | Alpha-capable (`0.1.5-alpha`) |
| Security hardwire | **Mandatory pipeline on main** (`SecurityPipeline` on `prompt`) |
| Profile isolation | Still weak / real profile reuse risk |
| Docs vs code | Improved; local CI parity documented |
| Fit as cabal default | **No** |

---

## 3. Branches

| Branch | Notes |
|--------|--------|
| `main` | Integration / publish tip (prefer this) |
| `dev` / `testing` | May lag `main` — re-sync before using as base |
| Historical security-integration branches | Superseded by merges on main; triage leftovers only |

---

## 4. Gaps

| Gap | Sev |
|-----|-----|
| Session/profile isolation | High |
| Permission enforcement only at edges | High |
| HITL / display-mode depth vs docs | Med |
| Clear “library only / MCP only” guidance | Med |
| `origin/dev` lagging `main` | Med (process) |

**Resolved since 2026-07-08 notes:** mandatory screening pipeline is on main;
secrecy 0.10 API compatibility landed; linux x64 CI routes to self-hosted podman fleet.

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
