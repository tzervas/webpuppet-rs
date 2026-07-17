# Security Policy

## Supported versions

| Version        | Supported          |
|----------------|--------------------|
| 0.1.x-alpha    | Yes (pre-release)  |
| older alphas   | No                 |

This project is pre-release software. Security fixes land on the current
development tip (`main`); there is no long-term maintenance of older alphas.

## Reporting a vulnerability

**Do not** open a public GitHub issue for security vulnerabilities.

Please report privately via one of:

1. **GitHub Security Advisories** — repository **Security → Report a vulnerability**
   (preferred when available for this repo).
2. **Maintainer contact** — open a private channel with the repository owner
   listed in [CODEOWNERS](.github/CODEOWNERS) / crate metadata
   (`authors` in `Cargo.toml`).

Include:

- Affected version / commit
- Description and impact
- Reproduction steps or proof-of-concept (non-destructive)
- Any known workarounds

We aim to acknowledge reports within a few business days. Please allow time
for assessment and fix before public disclosure.

## Security model (library)

- **Credentials**: OS keyring / encrypted storage; never commit secrets.
- **Screening**: Input/output security pipeline is enabled by default on
  `WebPuppet::prompt` (injection, PII, secrets, content manipulation).
- **Companion tooling**: For MCP-facing guardrails, pair
  [webpuppet-rs-mcp](https://github.com/tzervas/webpuppet-rs-mcp) with
  [security-mcp](https://github.com/tzervas/security-mcp) wrap mode (bulletin
  `security-mcp/wrap`, **DRAFT** — not STABLE).

### security-mcp integration hook points (consumer readiness)

| Layer | Location | Role |
|-------|----------|------|
| **In-process (default)** | `WebPuppet::prompt` / `prompt_screened` in `src/puppet.rs` | Mandatory `SecurityPipeline` on prompt input and provider output |
| **MCP tool routing (library)** | `src/security/proxy.rs` (`McpSecurityProxy`, `McpServerConfig`) | Optional in-crate proxy model: screen tool args/results before forwarding to a downstream MCP server over stdio/HTTP |
| **Human intervention** | `src/intervention.rs` | Pause/resume for captcha, 2FA, and manual steps (pairs with MCP `webpuppet_intervention_*` tools) |
| **External wrap (operator)** | security-mcp CLI/env (`--wrap`, `--wrap-command`, `SECURITY_MCP_WRAP_*`) | Child process = `webpuppet-mcp`; security-mcp screens `tools/call` args before forward — **contract DRAFT** on security-mcp `main` |

This repository does **not** ship security-mcp or auto-start wrap; fleet operators wire
the child command and acknowledge the DRAFT bulletin in their own deployment docs.

Historical audit notes (point-in-time): [SECURITY_AUDIT.md](SECURITY_AUDIT.md).

## Local supply-chain checks

When installed:

```bash
cargo audit
cargo deny check
```

Day-to-day quality gate (no network audit tools required):

```bash
./scripts/check.sh
```
