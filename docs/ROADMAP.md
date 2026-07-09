# webpuppet-rs — Product Roadmap

**Status:** Living (2026-07-08)  
**North star:** Safe-by-default **library** for legitimate browser automation — isolated profiles, hard permissions, optional security pipeline — consumed by MCP front, not by unconstrained agents.

Companion: [ASSESSMENT.md](ASSESSMENT.md).

---

## Waves

### Wave A — Safety baseline

| ID | Work |
|----|------|
| W-A1 | Isolated browser profile default (no user profile unless explicit) |
| W-A2 | Permission hardwire inside `WebPuppet` (not only MCP edge) |
| W-A3 | Secrets via keyring/env only |
| W-A4 | SECURITY.md: ToS, allowlist, logging redaction |

### Wave B — Security integration

| ID | Work |
|----|------|
| W-B1 | Triage `claude/review-security-integration-k2KXP` vs security-mcp peer |
| W-B2 | Prefer **external** security-mcp calls over vendoring detectors twice |
| W-B3 | Hook points: `before_navigate`, `before_type`, `after_extract` |

### Wave C — API stability

| ID | Work |
|----|------|
| W-C1 | Freeze public library API 0.2 |
| W-C2 | Examples for research-only workflows |
| W-C3 | Coordinate version with webpuppet-rs-mcp |

---

## Library API plan (target)

```rust
pub struct PuppetConfig {
    pub profile: ProfileMode, // Ephemeral | NamedPath | ExplicitUser(danger)
    pub permissions: PermissionSet,
    pub security: SecurityMode, // Off | ExternalMcp { endpoint } | InProcess
}

impl WebPuppet {
    pub async fn new(cfg: PuppetConfig) -> Result<Self>;
    pub async fn navigate(&mut self, url: &Url) -> Result<()>;
    pub async fn screenshot(&mut self, path: &Path) -> Result<()>;
    pub async fn extract_text(&mut self, sel: &str) -> Result<String>;
    // Provider-specific helpers stay feature-gated
}
```

**Permissions (hard fail):** navigation hosts allowlist, download deny-by-default, clipboard opt-in.

---

## PR plan

1. Docs assessment + roadmap  
2. Ephemeral profile default  
3. Internal permission checks  
4. Security branch triage  
5. 0.2 API freeze  

---

## Non-goals

- Bypassing auth/ToS  
- Being cabal’s default tool  
- Silent full-desktop control  
