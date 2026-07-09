# webpuppet-rs — Tero Index (Layer 1)

> **Honesty:** Empirical/Declared — lite heading/line heuristic over markdown in webpuppet-rs via tero-mcp/scripts/generate_lite_index.py; source files are ground truth. Generated 2026-07-09.
> Use this index to find where to Read, not as authoritative ground truth.

- **Items:** 143
- **Flagged:** 0
- **item_tag:** `Empirical/Declared`
- **Machine index:** [`index.json`](./index.json)
- **Manifest:** [`MANIFEST.toml`](./MANIFEST.toml)

## doc (132 entries)

| Anchor | Kind | Id | Title | File:Line | Status | Summary |
|---|---|---|---|---|---|---|
| `contributing` | section | — | Contributing to webpuppet | `CONTRIBUTING.md:1` | — | Thank you for your interest in contributing to webpuppet! This document provides guidelines for contributing to the project. |
| `contributing--development-setup` | section | — | Development Setup | `CONTRIBUTING.md:5` | — | - Rust 1.75+ (latest stable recommended) |
| `contributing--prerequisites` | section | — | Prerequisites | `CONTRIBUTING.md:7` | — | - Rust 1.75+ (latest stable recommended) |
| `contributing--setup` | section | — | Setup | `CONTRIBUTING.md:13` | — | 1. Fork and clone the repository |
| `contributing--platform-support` | section | — | Platform Support | `CONTRIBUTING.md:19` | — | This project focuses on modern platforms and environments: |
| `contributing--code-standards` | section | — | Code Standards | `CONTRIBUTING.md:39` | — | We follow [Conventional Commits](https://www.conventionalcommits.org/): |
| `contributing--commit-messages` | section | — | Commit Messages | `CONTRIBUTING.md:41` | — | We follow [Conventional Commits](https://www.conventionalcommits.org/): |
| `contributing--branch-naming` | section | — | Branch Naming | `CONTRIBUTING.md:70` | — | Follow this pattern: type/description-in-kebab-case |
| `contributing--code-style` | section | — | Code Style | `CONTRIBUTING.md:79` | — | - Use rustfmt for formatting: cargo fmt |
| `contributing--pull-request-process` | section | — | Pull Request Process | `CONTRIBUTING.md:86` | — | 1. Ensure all tests pass: cargo test |
| `contributing--before-submitting` | section | — | Before Submitting | `CONTRIBUTING.md:88` | — | 1. Ensure all tests pass: cargo test |
| `contributing--pr-guidelines` | section | — | PR Guidelines | `CONTRIBUTING.md:96` | — | - Use a clear, descriptive title |
| `contributing--review-process` | section | — | Review Process | `CONTRIBUTING.md:103` | — | - All PRs require review before merging |
| `contributing--security` | section | — | Security | `CONTRIBUTING.md:109` | — | - Do not create public issues for security vulnerabilities |
| `contributing--reporting-security-issues` | section | — | Reporting Security Issues | `CONTRIBUTING.md:111` | — | - Do not create public issues for security vulnerabilities |
| `contributing--security-guidelines` | section | — | Security Guidelines | `CONTRIBUTING.md:117` | — | - All user input must be validated and sanitized |
| `contributing--testing` | section | — | Testing | `CONTRIBUTING.md:124` | — | - Unit tests: Test individual components |
| `contributing--test-categories` | section | — | Test Categories | `CONTRIBUTING.md:126` | — | - Unit tests: Test individual components |
| `contributing--test-requirements` | section | — | Test Requirements | `CONTRIBUTING.md:132` | — | - New features must include tests |
| `contributing--running-tests` | section | — | Running Tests | `CONTRIBUTING.md:138` | — | cargo test |
| `contributing--run-all-tests` | other | — | Run all tests | `CONTRIBUTING.md:140` | — | cargo test |
| `contributing--run-specific-test-category` | other | — | Run specific test category | `CONTRIBUTING.md:143` | — | cargo test --test integration |
| `contributing--run-with-output` | other | — | Run with output | `CONTRIBUTING.md:146` | — | cargo test -- --nocapture |
| `contributing--license` | section | — | License | `CONTRIBUTING.md:150` | — | By contributing, you agree that your contributions will be licensed under the MIT License. |
| `readme` | other | — | webpuppet | `README.md:1` | — | Web Browser Programmatic Automation & Control Library |
| `readme--purpose-use-cases` | section | — | Purpose & Use Cases | `README.md:9` | — | webpuppet is a quality-of-life tool for developers and researchers who need programmatic web browser control for legitimate automation use cases: |
| `readme--architecture` | section | — | Architecture | `README.md:22` | — | webpuppet is designed as a foundational library that can be integrated into larger research automation systems. The library itself provides core automation cap… |
| `readme--security-model` | section | — | Security Model | `README.md:26` | — | - Primary Library: webpuppet (this crate) - provides browser automation and session management |
| `readme--overview` | section | — | Overview | `README.md:34` | — | webpuppet enables programmatic browser automation and control through native browser APIs when traditional methods (like API-only access) are unavailable or re… |
| `readme--features` | section | — | Features | `README.md:44` | — | - Multi-Provider Support: Built-in support for multiple web interfaces (Claude, Grok, Gemini, ChatGPT, Perplexity, NotebookLM, Kaggle) |
| `readme--installation` | section | — | Installation | `README.md:55` | — | Add to your Cargo.toml: |
| `readme--feature-flags` | section | — | Feature Flags | `README.md:73` | — | — |
| `readme--usage` | section | — | Usage | `README.md:88` | — | use webpuppet::{WebPuppet, Provider, PromptRequest}; |
| `readme--basic-prompt` | section | — | Basic Prompt | `README.md:90` | — | use webpuppet::{WebPuppet, Provider, PromptRequest}; |
| `readme--multi-provider-query` | section | — | Multi-Provider Query | `README.md:120` | — | use webpuppet::{WebPuppet, Provider, PromptRequest}; |
| `readme--conversation-mode` | section | — | Conversation Mode | `README.md:152` | — | use webpuppet::{WebPuppet, Provider, PromptRequest}; |
| `readme--authentication-flow` | section | — | Authentication Flow | `README.md:186` | — | On first use with each provider: |
| `readme--configuration` | section | — | Configuration | `README.md:210` | — | use webpuppet::{Config, WebPuppet}; |
| `readme--provider-capabilities` | section | — | Provider Capabilities | `README.md:230` | — | Capabilities are declared per provider in code (not runtime UI detection yet). For programmatic access, use WebPuppet::providercapabilities(). |
| `readme--security` | section | — | Security | `README.md:243` | — | - Credentials: Stored in OS keyring, never in plaintext files |
| `readme--limitations` | section | — | Limitations | `README.md:251` | — | - Pre-release software: APIs may change without notice |
| `readme--content-security-screening` | section | — | Content Security Screening | `README.md:259` | — | The library includes built-in security screening for AI responses: |
| `readme--detected-security-issues` | section | — | Detected Security Issues | `README.md:291` | — | — |
| `readme--custom-screening-configuration` | section | — | Custom Screening Configuration | `README.md:304` | — | use webpuppet::{WebPuppet, ScreeningConfig}; |
| `readme--architecture-2` | section | — | Architecture | `README.md:326` | — | webpuppet/ |
| `readme--system-requirements` | section | — | System Requirements | `README.md:347` | — | - Rust: 1.75.0 or newer (latest stable recommended) |
| `readme--troubleshooting` | section | — | Troubleshooting | `README.md:358` | — | // Force re-authentication |
| `readme--session-expired` | section | — | Session Expired | `README.md:360` | — | // Force re-authentication |
| `readme--rate-limited` | section | — | Rate Limited | `README.md:367` | — | The library automatically handles rate limits with exponential backoff. If you're consistently hitting limits, increase the delay: |
| `readme--browser-not-found` | section | — | Browser Not Found | `README.md:377` | — | use std::path::PathBuf; |
| `readme--license` | section | — | License | `README.md:387` | — | MIT License - See [LICENSE](../../LICENSE) for details. |
| `readme--disclaimer` | section | — | Disclaimer | `README.md:391` | — | This tool is for educational and research purposes only. Use of this tool to automate web interfaces may violate the terms of service of the respective provide… |
| `readme--status-roadmap` | section | — | Status & roadmap | `README.md:395` | — | - [Assessment & gaps](docs/ASSESSMENT.md) |
| `roadmap` | note | — | webpuppet: Next Enhancement Roadmap | `ROADMAP.md:1` | — | Current Status: v0.1.0-alpha.3 - Multi-browser support, cross-platform detection |
| `roadmap--version-0.2.0-development-plan` | section | — | Version 0.2.0 Development Plan | `ROADMAP.md:2` | — | Current Status: v0.1.0-alpha.3 - Multi-browser support, cross-platform detection |
| `roadmap--platform-strategy` | section | — | Platform Strategy | `ROADMAP.md:9` | — | Target Platforms (Modern Focus): |
| `roadmap--phase-1-core-reliability-stability` | section | — | Phase 1: Core Reliability & Stability 🔧 | `ROADMAP.md:34` | — | Timeline: 2-3 weeks |
| `roadmap--1.1-error-handling-recovery` | section | — | 1.1 Error Handling & Recovery | `ROADMAP.md:37` | — | - Robust Connection Management |
| `roadmap--1.2-performance-optimization` | section | — | 1.2 Performance Optimization | `ROADMAP.md:53` | — | - Resource Management |
| `roadmap--1.3-comprehensive-testing` | section | — | 1.3 Comprehensive Testing | `ROADMAP.md:64` | — | - Integration Test Suite |
| `roadmap--phase-2-advanced-features` | section | — | Phase 2: Advanced Features 🚀 | `ROADMAP.md:77` | — | Timeline: 3-4 weeks |
| `roadmap--2.1-enhanced-provider-support` | section | — | 2.1 Enhanced Provider Support | `ROADMAP.md:80` | — | - Universal File Handling |
| `roadmap--2.2-advanced-automation` | section | — | 2.2 Advanced Automation | `ROADMAP.md:96` | — | - Workflow Engine |
| `roadmap--2.3-monitoring-observability` | section | — | 2.3 Monitoring & Observability | `ROADMAP.md:107` | — | - Metrics Collection |
| `roadmap--phase-3-enterprise-features` | section | — | Phase 3: Enterprise Features 📈 | `ROADMAP.md:120` | — | Timeline: 4-5 weeks |
| `roadmap--3.1-multi-user-team-support` | section | — | 3.1 Multi-User & Team Support | `ROADMAP.md:123` | — | - User Management |
| `roadmap--3.2-integration-ecosystem` | section | — | 3.2 Integration Ecosystem | `ROADMAP.md:134` | — | - MCP Server Implementation |
| `roadmap--3.3-advanced-security` | section | — | 3.3 Advanced Security | `ROADMAP.md:150` | — | - Audit & Compliance |
| `roadmap--phase-4-platform-deployment` | section | — | Phase 4: Platform & Deployment 🌐 | `ROADMAP.md:163` | — | Timeline: 3-4 weeks |
| `roadmap--4.1-container-cloud-native` | section | — | 4.1 Container & Cloud Native | `ROADMAP.md:166` | — | - Docker Support |
| `roadmap--4.2-configuration-management` | section | — | 4.2 Configuration & Management | `ROADMAP.md:177` | — | - Configuration Management |
| `roadmap--technical-debt-maintenance` | section | — | Technical Debt & Maintenance 🛠️ | `ROADMAP.md:190` | — | Ongoing throughout all phases |
| `roadmap--code-quality` | section | — | Code Quality | `ROADMAP.md:193` | — | - Refactoring Priorities |
| `roadmap--documentation-developer-experience` | section | — | Documentation & Developer Experience | `ROADMAP.md:204` | — | - API Documentation |
| `roadmap--risk-assessment-mitigation` | section | — | Risk Assessment & Mitigation | `ROADMAP.md:217` | — | 1. Provider UI Changes: Continuous monitoring and rapid response team |
| `roadmap--high-risk-items` | section | — | High-Risk Items | `ROADMAP.md:219` | — | 1. Provider UI Changes: Continuous monitoring and rapid response team |
| `roadmap--mitigation-strategies` | section | — | Mitigation Strategies | `ROADMAP.md:224` | — | - Provider Monitoring: Automated UI change detection |
| `roadmap--success-metrics` | section | — | Success Metrics | `ROADMAP.md:231` | — | - Reliability: 99.5% uptime for supported providers |
| `roadmap--technical-metrics` | section | — | Technical Metrics | `ROADMAP.md:233` | — | - Reliability: 99.5% uptime for supported providers |
| `roadmap--user-experience-metrics` | section | — | User Experience Metrics | `ROADMAP.md:238` | — | - Ease of Use: New user onboarding in <10 minutes |
| `roadmap--business-metrics` | section | — | Business Metrics | `ROADMAP.md:243` | — | - Integration Success: MCP server adoption in production environments |
| `securityaudit` | section | — | Security Audit Report | `SECURITY_AUDIT.md:1` | ✅ PASSED | Date: January 6, 2026 |
| `securityaudit--webpuppet-v0.1.0-alpha.2` | section | — | webpuppet v0.1.0-alpha.2 | `SECURITY_AUDIT.md:2` | — | Date: January 6, 2026 |
| `securityaudit--executive-summary` | section | — | Executive Summary | `SECURITY_AUDIT.md:8` | — | This report documents the security review performed on webpuppet, a browser automation library for AI provider web interfaces. The project has undergone compre… |
| `securityaudit--security-architecture` | section | — | Security Architecture | `SECURITY_AUDIT.md:12` | — | - Encryption Algorithm: AES-256-GCM for sensitive data at rest |
| `securityaudit--1.-cryptographic-implementation` | section | — | 1. Cryptographic Implementation | `SECURITY_AUDIT.md:14` | — | - Encryption Algorithm: AES-256-GCM for sensitive data at rest |
| `securityaudit--2.-supply-chain-security` | section | — | 2. Supply Chain Security | `SECURITY_AUDIT.md:20` | — | - Dependency Scanning: 335 dependencies verified against known vulnerability databases |
| `securityaudit--3.-content-security-controls` | section | — | 3. Content Security Controls | `SECURITY_AUDIT.md:26` | — | - Input Validation: All user inputs validated and sanitized |
| `securityaudit--risk-analysis-duplicate-dependencies` | section | — | Risk Analysis: Duplicate Dependencies | `SECURITY_AUDIT.md:32` | — | The dependency tree contains multiple versions of certain crates, particularly in the Windows ecosystem and random number generation libraries. This creates po… |
| `securityaudit--problem-statement` | section | — | Problem Statement | `SECURITY_AUDIT.md:34` | — | The dependency tree contains multiple versions of certain crates, particularly in the Windows ecosystem and random number generation libraries. This creates po… |
| `securityaudit--risk-assessment-mitigation` | section | — | Risk Assessment & Mitigation | `SECURITY_AUDIT.md:43` | — | HIGH PRIORITY - Resolved: |
| `securityaudit--monitoring-remediation-plan` | section | — | Monitoring & Remediation Plan | `SECURITY_AUDIT.md:58` | — | 1. Quarterly Reviews: Monitor for resolution of temporary exceptions |
| `securityaudit--mcp-server-compatibility-assessment` | section | — | MCP Server Compatibility Assessment | `SECURITY_AUDIT.md:64` | — | ✅ Pure Library Crate: No binary artifacts, suitable for integration |
| `securityaudit--library-design` | section | — | Library Design | `SECURITY_AUDIT.md:66` | — | ✅ Pure Library Crate: No binary artifacts, suitable for integration |
| `securityaudit--security-considerations-for-mcp-usage` | section | — | Security Considerations for MCP Usage | `SECURITY_AUDIT.md:72` | — | ✅ No Privilege Escalation: Library operates within user context only |
| `securityaudit--recommended-mcp-integration-patterns` | section | — | Recommended MCP Integration Patterns | `SECURITY_AUDIT.md:78` | — | - Use WebPuppet::new().build() for basic automation |
| `securityaudit--test-results` | section | — | Test Results | `SECURITY_AUDIT.md:84` | — | cargo audit: ✅ PASSED (0 vulnerabilities) |
| `securityaudit--vulnerability-scanning` | section | — | Vulnerability Scanning | `SECURITY_AUDIT.md:86` | — | cargo audit: ✅ PASSED (0 vulnerabilities) |
| `securityaudit--secret-detection` | section | — | Secret Detection | `SECURITY_AUDIT.md:92` | — | Regex Patterns Tested: 15+ |
| `securityaudit--dependency-analysis` | section | — | Dependency Analysis | `SECURITY_AUDIT.md:99` | — | Total Dependencies: 335 |
| `securityaudit--compliance-status` | section | — | Compliance Status | `SECURITY_AUDIT.md:107` | — | - ✅ OWASP Top 10: No critical web application vulnerabilities |
| `securityaudit--security-standards` | section | — | Security Standards | `SECURITY_AUDIT.md:109` | — | - ✅ OWASP Top 10: No critical web application vulnerabilities |
| `securityaudit--license-compliance` | section | — | License Compliance | `SECURITY_AUDIT.md:114` | — | - ✅ Approved Licenses: MIT, Apache-2.0, BSD variants, Unicode-3.0, ISC, MPL-2.0, CDLA-Permissive-2.0 |
| `securityaudit--deployment-recommendations` | section | — | Deployment Recommendations | `SECURITY_AUDIT.md:119` | — | 1. Environment Variables: Store sensitive config in environment, not files |
| `securityaudit--production-hardening` | section | — | Production Hardening | `SECURITY_AUDIT.md:121` | — | 1. Environment Variables: Store sensitive config in environment, not files |
| `securityaudit--mcp-server-integration` | section | — | MCP Server Integration | `SECURITY_AUDIT.md:127` | — | 1. Resource Limits: Set appropriate timeouts and memory limits |
| `securityaudit--conclusion` | section | — | Conclusion | `SECURITY_AUDIT.md:133` | — | webpuppet has successfully passed comprehensive security review and is ready for production deployment. The library demonstrates strong security posture with d… |
| `assessment` | note | — | webpuppet-rs — Assessment & Gap Analysis | `docs/ASSESSMENT.md:1` | — | Date: 2026-07-08 |
| `assessment--1.-role` | section | — | 1. Role | `docs/ASSESSMENT.md:10` | — | Rust library for programmatic browser control (research, QA, automation). High ToS/risk surface — must stay opt-in, permissioned, and preferably screened. |
| `assessment--2.-maturity-23-5` | section | — | 2. Maturity: **2–3 / 5** | `docs/ASSESSMENT.md:16` | — | — |
| `assessment--3.-branches` | section | — | 3. Branches | `docs/ASSESSMENT.md:28` | — | — |
| `assessment--4.-gaps` | section | — | 4. Gaps | `docs/ASSESSMENT.md:38` | — | — |
| `assessment--5.-integration` | section | — | 5. Integration | `docs/ASSESSMENT.md:50` | — | See [ROADMAP.md](ROADMAP.md). Root [../ROADMAP.md](../ROADMAP.md) may hold older notes — this docs/ roadmap is the cabal-era plan. |
| `assessment--tero-index` | section | — | Tero index | `docs/ASSESSMENT.md:60` | — | Layer-1 citation index: [docs/tero-index/](tero-index/) (index.json, INDEX.md, MANIFEST.toml). |
| `localchecks` | section | — | Local checks (CI parity) | `docs/LOCAL_CHECKS.md:1` | — | GitHub Actions workflows in this repo are manual only (workflowdispatch). |
| `localchecks--run-everything-the-remote-job-would-run` | section | — | Run everything the remote job would run | `docs/LOCAL_CHECKS.md:6` | — | ./scripts/check.sh |
| `localchecks--tero-index` | section | — | Tero index | `docs/LOCAL_CHECKS.md:19` | — | python3 ../tero-mcp/scripts/generateliteindex.py --root "$(pwd)" |
| `localchecks--from-a-checkout-that-can-see-the-generator-sibling-tero-mcp-recommended` | other | — | from a checkout that can see the generator (sibling tero-mcp recommended): | `docs/LOCAL_CHECKS.md:22` | — | python3 ../tero-mcp/scripts/generateliteindex.py --root "$(pwd)" |
| `localchecks--or` | other | — | or: | `docs/LOCAL_CHECKS.md:24` | — | python3 scripts/generateteroindex.sh   # if present as a thin wrapper |
| `localchecks--remote-optional` | section | — | Remote (optional) | `docs/LOCAL_CHECKS.md:30` | — | In GitHub: Actions → CI → Run workflow. |
| `roadmap-2` | note | — | webpuppet-rs — Product Roadmap | `docs/ROADMAP.md:1` | Living (2026-07-08) | Status: Living (2026-07-08) |
| `roadmap--waves` | section | — | Waves | `docs/ROADMAP.md:10` | — | — |
| `roadmap--wave-a-safety-baseline` | section | — | Wave A — Safety baseline | `docs/ROADMAP.md:12` | — | — |
| `roadmap--wave-b-security-integration` | section | — | Wave B — Security integration | `docs/ROADMAP.md:21` | — | — |
| `roadmap--wave-c-api-stability` | section | — | Wave C — API stability | `docs/ROADMAP.md:29` | — | — |
| `roadmap--library-api-plan-target` | section | — | Library API plan (target) | `docs/ROADMAP.md:39` | — | pub struct PuppetConfig { |
| `roadmap--pr-plan` | section | — | PR plan | `docs/ROADMAP.md:61` | — | 1. Docs assessment + roadmap |
| `roadmap--non-goals` | section | — | Non-goals | `docs/ROADMAP.md:71` | — | - Bypassing auth/ToS |
| `readme-2` | other | — | Tero index (Layer 1) | `docs/tero-index/README.md:1` | — | Machine + human citation index for this repository. |
| `readme--regenerate` | section | — | Regenerate | `docs/tero-index/README.md:13` | — | python3 /path/to/tero-mcp/scripts/generateliteindex.py --root $(pwd) |
| `readme--or-if-tero-mcp-is-a-sibling` | other | — | or if tero-mcp is a sibling: | `docs/tero-index/README.md:17` | — | python3 ../tero-mcp/scripts/generateliteindex.py --root $(pwd) |
| `readme--serve-locally` | section | — | Serve locally | `docs/tero-index/README.md:21` | — | export TEROTOKENS=local-dev:refresh |

## changelog (11 entries)

| Anchor | Kind | Id | Title | File:Line | Status | Summary |
|---|---|---|---|---|---|---|
| `changelog` | entry | — | Changelog | `CHANGELOG.md:1` | — | All notable changes to this project will be documented in this file. |
| `changelog--unreleased` | section | — | [Unreleased] | `CHANGELOG.md:8` | — | - BREAKING: Renamed crate from embeddenator-webpuppet to webpuppet |
| `changelog--changed` | section | — | Changed | `CHANGELOG.md:10` | — | - BREAKING: Renamed crate from embeddenator-webpuppet to webpuppet |
| `changelog--0.1.0-alpha.3-2025-01-19` | section | — | [0.1.0-alpha.3] - 2025-01-19 | `CHANGELOG.md:15` | — | - Multi-browser support: Extended from 4 to 8 browser types (Brave, Chrome, Chromium, Edge, Opera, Vivaldi, Firefox, Safari) |
| `changelog--added` | section | — | Added | `CHANGELOG.md:17` | — | - Multi-browser support: Extended from 4 to 8 browser types (Brave, Chrome, Chromium, Edge, Opera, Vivaldi, Firefox, Safari) |
| `changelog--changed-2` | section | — | Changed | `CHANGELOG.md:26` | — | - CI: Bumped softprops/action-gh-release from 1 to 2 |
| `changelog--0.1.0-alpha.2-2024-12-20` | section | — | [0.1.0-alpha.2] - 2024-12-20 | `CHANGELOG.md:34` | — | - Comprehensive security hardening and MCP server preparation |
| `changelog--added-2` | section | — | Added | `CHANGELOG.md:36` | — | - Comprehensive security hardening and MCP server preparation |
| `changelog--security` | section | — | Security | `CHANGELOG.md:42` | — | - Implemented maximum security hardening measures |
| `changelog--0.1.0-alpha.1-2024-12-19` | section | — | [0.1.0-alpha.1] - 2024-12-19 | `CHANGELOG.md:46` | — | - Initial alpha release |
| `changelog--added-3` | section | — | Added | `CHANGELOG.md:48` | — | - Initial alpha release |

