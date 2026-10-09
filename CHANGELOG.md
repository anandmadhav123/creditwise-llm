# Changelog

All notable changes to the **CreditWise LLM** extension will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [2.4.0] - 2026-10-08

### Added
- **Global Rebranding to CreditWise LLM**:
  - Rebranded extension from `CreditWise LLM` (`creditWise`, `@creditwise`, `creditwise-llm`) to `CreditWise LLM` (`creditWise`, `@creditwise`, `creditwise-llm`).
  - Added `@creditwise` chat participant for autonomous model routing.
  - Renamed provider modules to `CreditWiseModelProvider.ts` and `CreditWiseModelProviderV2.ts`.
- **Licensing & Quota Management**:
  - Integrated `LicenseManager` singleton with Lemon Squeezy software licensing API.
  - Integrated `QuotaManager` singleton tracking monthly query consumption on the Free tier.
  - Added Free vs. Pro quota gate in `@creditwise` chat participant and Language Model Provider.
  - Added dedicated Status Bar item displaying live Free tier query balance (`$(zap) Free: X/50`) or Pro status (`$(star-full) CreditWise Pro`).
  - Added 7-day offline grace period for licensed Pro users.
  - Added configurable monthly quota limit via `creditWise.freeMonthlyQuota` (default: 50).
- **Backward Compatibility & Dual Command Registration**:
  - Maintained complete backward compatibility by registering both `creditWise.*` and `creditWise.*` command identifiers.
  - Added storage migration fallbacks for both `creditWise.monthlyQuota` and `creditWise.licenseInfo`.
  - Added configuration fallbacks across all `creditWise.*` settings.
- **Unit Testing Suite**:
  - Added `test/licensing.test.js` validating Free tier query limits, Pro bypass, reset behavior, and storage key migration.

### Changed
- Updated local loopback server (`127.0.0.1:3456`) `/v1/models` endpoint to return `creditwise-llm*` model identifiers alongside legacy aliases.
- Updated Graphify agent tools to `creditWise_queryGraph`, `creditWise_getNeighbors`, and `creditWise_findPath`.
- Rewrote `package.json` with new publisher (`creditwise-llm`), package name (`creditwise-llm-vscode`), and command palette contributions.

---

## [2.3.2] - 2026-09-28

### Fixed
- **Truthful Token Telemetry**: Corrected token savings calculation to differentiate between raw wire tokens and actual structural context compression.
- **Pipeline Orchestration Routing**: Fixed complexity classifier to score multi-step CI/CD and AI DLC pipeline orchestration prompts accurately into the Heavy tier.

---

## [2.3.0] - 2026-09-25

### Added
- **Graphify Codebase Knowledge Graph**: AST structural analysis integration to eliminate unnecessary raw file token consumption during chat sessions.
- Dynamic subscription model scanning and real-time tier classification.

---

## [2.2.0] - 2026-09-15

### Added
- **Outcome Learning**: Local tracking of model escalations and errors with automated penalty adjustments for struggling models.
- **Conversation Stickiness**: Retains higher model tiers across multi-turn refactoring sessions.

---

## [2.1.0] - 2026-09-01

### Added
- **Next-Gen FinOps Console (V2)**: Full-editor interactive dashboard with Dark/Light theme toggles and token telemetry breakdowns.

---

## [2.0.0] - 2026-08-15

### Added
- **Autonomous Multi-Tier Routing Engine**: Dynamic Light / Medium / Heavy tier routing with local loopback proxy (`http://127.0.0.1:3456`) for native Agent mode support.
