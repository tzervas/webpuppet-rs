# Local checks (CI parity)

Local quality gates are the preferred day-to-day source of truth. GitHub Actions
CI also runs the same script on push/PR to `main`/`dev`/`develop` and via
`workflow_dispatch` (self-hosted podman fleet for linux x64).

## Run everything the remote job would run

```bash
./scripts/check.sh
```

This runs, in order:

1. `cargo fmt --check`
2. `cargo clippy --all-targets --all-features -- -D warnings`
3. `cargo build --all-features`
4. `cargo test --all-features --verbose`

Optional:

```bash
./scripts/check.sh --fix  # apply rustfmt instead of --check
```

## Tero index

```bash
# from a checkout that can see the generator (sibling tero-mcp recommended):
python3 ../tero-mcp/scripts/generate_lite_index.py --root "$(pwd)"
# or:
python3 scripts/generate_tero_index.sh   # if present as a thin wrapper
```

Artifacts land in `docs/tero-index/` (`index.json`, `INDEX.md`, `MANIFEST.toml`, `README.md`).

## Remote (optional)

In GitHub: **Actions → CI → Run workflow** (manual), or open a PR / push to a
watched branch for automatic runs.
