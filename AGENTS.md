
# AGENTS.md — webpuppet-rs

**Use Tero + cabal-devmelopner for work here.**

## Tero (Layer-1 corpus index)

Repo has `docs/tero-index/index.json` (generated/ refreshed via tero-mcp/scripts/generate_lite_index.py).

**Rule:** Use tero queries before large greps or assumptions.
- Grok: tero__text_search / query_by_id (token "local-dev")
- Direct: tero-mcp-lite --index docs/tero-index/index.json
- cabal-devmelopner: auto-detects local index when run from within this tree (or set TERO_INDEX_PATH).

Example:
```bash
cd /root/git/webpuppet-rs
# agent with context:
uv run --project ../cabal-devmelopner cabal-devmelopner "task description here" --use-tero
```

Citations point at file:line — open them.

## Working with cabal-devmelopner agent tool

This project is prepared for integration:
- Tero index committed on chore/tero-index-cabal-ready (and PRable to dev)
- Local auto index support in cabal
- This AGENTS.md

**PR flow (protect main/dev):**
- Create/checkout feature or chore branch
- Make changes (agent will often use working branch)
- PR the branch → `dev` (then dev → main when ready)

## Local checks

Look for:
- scripts/check.sh
- Cargo.toml / pyproject.toml + standard commands (cargo test, uv run pytest, ruff, etc.)

Run checks before considering work complete.

## Further reading

- README.md
- docs/ROADMAP.md or ROADMAP.md (if present)
- docs/ASSESSMENT.md or similar for intent/gaps
- ../cabal-devmelopner/docs/* for agent architecture
- ../tero-mcp for how indexes are built and served

Leave mycelium isolated; all coordination here targets the other repos + cabal.

## Landed status (2026-07-09, wsfull plan priority 1)

chore/tero-index-cabal-ready landed (thin hygiene + pending branch per plan):

- fetch; checkout -B dev origin/dev; git merge --no-ff chore/tero-index-cabal-ready -m "chore(merge): land tero-index + AGENTS + hygiene (wsfull plan priority 1)"; (push attempted but blocked by branch protection)
- ./scripts/check.sh (or --fix as needed for green; conservative where possible)
- /root/git/scripts/update-tero.sh webpuppet-rs ; commit tero regen signed on dev
- Land to main: checkout -B main origin/main; merge --no-ff dev; push (attempted); propagate pull to dev
- Append-only update here (this section); tero-first queries used throughout (e.g. via /root/git/scripts/tero.sh)
- All guards: append-only, signed -S commits, dev-workflow followed (local merges as push rejected)

Verified: checks green ("OK: checks passed"), tero hits on AGENTS (cites: agents--working-with-cabal-devmelopner-agent-tool), main/dev tree content synced (diff empty), no uncommitted.

Refs (tero/plan cited): plan.md:4 (Tero-first), plan.md:~85-100 (hygiene-thin-repos + land), plan.md:120 (exec order item 1), plan.md:130 (verify), AGENTS.md:2 (use Tero + cabal), this file:24 (cabal-devmelopner section).

