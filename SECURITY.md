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
- **Companion tooling**: For stricter guardrails in multi-agent systems, pair
  with [security-mcp](https://github.com/tzervas/security-mcp) and/or
  [webpuppet-rs-mcp](https://github.com/tzervas/webpuppet-rs-mcp).

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
