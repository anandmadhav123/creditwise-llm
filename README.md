# CreditWise LLM — Installation & Distribution

[![Version](https://img.shields.io/badge/version-v2.4.0-blue.svg)](https://github.com/anandmadhav123/creditwise-llm)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![VS Code](https://img.shields.io/badge/VS%20Code-%5E1.95.0-purple.svg)](https://code.visualstudio.com/)
[![GitHub Copilot](https://img.shields.io/badge/GitHub%20Copilot-Compatible-black.svg)](https://github.com/features/copilot)

> **Current Release Package:** `creditwise-llm-vscode-2.4.0.vsix`  
> **Version:** `2.4.0`  
> **Distribution Type:** VSIX Extension Release Package (No raw source code)

⚡ **CreditWise LLM** is an autonomous model router, FinOps cost-optimization engine, and AST codebase knowledge graph accelerator designed for **GitHub Copilot** in Visual Studio Code. It dynamically evaluates query complexity, routes tasks across cost-optimized model tiers (Light, Medium, Heavy), and slashes premium token spend by up to 70%.

---

## 📦 Install from VSIX

### Option 1 — VS Code UI

1. Open VS Code.
2. Open the **Extensions** panel (`Ctrl+Shift+X` / `Cmd+Shift+X`).
3. Click the **`...`** (Views and More Actions) menu in the top-right of the Extensions panel.
4. Select **Install from VSIX...**
5. Select `creditwise-llm-vscode-2.4.0.vsix` from this repository and click **Install**.
6. When prompted, reload VS Code (`Cmd+Shift+P` → `Developer: Reload Window`).

### Option 2 — Command Line

Clone this repository and run:

```bash
code --install-extension creditwise-llm-vscode-2.4.0.vsix --force
```

Then reload VS Code.

---

## 🚀 Getting Started

1. **Invoke the Chat Participant in GitHub Copilot:**  
   Open the Copilot Chat panel (`Ctrl+Alt+I` / `Cmd+Option+I`) and address queries to `@creditwise`:
   ```text
   @creditwise refactor this module to extract repeated validation logic into a shared helper
   ```

2. **Open the FinOps Telemetry Dashboard:**  
   - Press `Cmd+Shift+P` (or `Ctrl+Shift+P`) to open the Command Palette.
   - Run `CreditWise LLM: Open Dashboard`.
   - Review live savings metrics, routed models, token compression savings, and execution latency.

3. **Run Pre-Release Model Diagnostics:**  
   - Open Command Palette and run `CreditWise LLM: Run Exhaustive Model & System Diagnostics`.
   - Watch live model discovery, streaming verification, and routing tier checks execute directly in your IDE.

4. **License Management & Pro Activation:**  
   - Free Tier: Includes 50 queries/month. Track remaining balance live in the Status Bar (`$(zap) Free: 50/50`).
   - Upgrade to Pro: Open Command Palette and run `CreditWise LLM: Upgrade to Pro (Lemon Squeezy)` or `CreditWise LLM: Activate License Key`.

---

## 🧠 Dynamic 3-Tier Routing Architecture

| Tier | Complexity Range | Target Models | Best Suited For |
| :---: | :---: | :--- | :--- |
| **Light** | Score < 4.0 | `claude-haiku-4.5`, `gpt-4o-mini` | Syntax lookups, unit conversions, docstrings, text formatting |
| **Medium** | 4.0 ≤ Score < 6.5 | `gemini-3.7-flash`, `gpt-5-mini` | Active feature authoring, test generation, function refactoring, tool calls |
| **Heavy** | Score ≥ 6.5 | `claude-sonnet-5`, `claude-opus-5`, `gpt-5.5` | Distributed systems, lock-free concurrency, security audits, pipeline orchestration |

---

## 🏛️ Repository Structure & Governance

This repository follows the enterprise binary distribution pattern:
- **Binary Distribution Only:** Contains verified `.vsix` release artifacts, documentation, and install telemetry workflows. Raw source code is maintained separately in the development repository.
- **Archive:** Prior versions are archived into `Archive/` upon release of subsequent versions.
- **Install Tracking:** Global installation metrics are recorded via `.github/workflows/track-installs.yml` onto the lightweight `stats` branch.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
