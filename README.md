[🇬🇧 English](README.md) | [🇯🇵 日本語](README.ja.md)

### Find what's worth fixing in the numbers, build it without changing how people already work, and hand it over so the team can keep it running on their own.

Deciding comes from running a business, building from the shop floor, handing over from teaching. Twelve years running a cram school, and an LLC from founding through liquidation — I closed the books myself, without an accountant, so I can read where the money moves in a business. Now I work at a contract development firm, take on freelance projects of my own, and open-source the tooling they turn out to need.

---

### Works

| Repository | Description | Category | Language |
| --- | --- | --- | --- |
| [nfc-attendance-kit](https://github.com/yktsnet/nfc-attendance-kit) | Auto-aggregates NFC time clock punches into a spreadsheet, running in production for a real client (−5h/month) | Production | Python |
| [excel-kanri](https://github.com/yktsnet/excel-kanri) | Retrofits existing Excel-based paperwork operations with a web form, PDF conversion, and full-text search, running in production for a real client | Production | Python |
| [bt-lab](https://github.com/yktsnet/bt-lab) | An 8-stage pipeline that cross-validates multiple strategy candidates and automatically selects among them by drawdown and Recovery Factor | Trading | Python |
| [bt-dynamic](https://github.com/yktsnet/bt-dynamic) | A backtesting core that switches regimes across 9 cells (trend strength × volatility), distributed on PyPI | Trading | Python |
| [live-dynamic](https://github.com/yktsnet/live-dynamic) | An execution layer that runs validated strategies unattended via systemd timer with the same config, live. Published as a reference implementation for safety design covering idempotent order gating, OCO, and kill switches | Trading | Python |
| [folio-agent](https://github.com/yktsnet/folio-agent) | A CAG-style portfolio chat that bundles all knowledge inline, published on npm and running on Cloudflare Workers | Tools | TypeScript |
| [order-system-migration](https://github.com/yktsnet/order-system-migration) | Migrated WinForms to .NET 10 Web API + React, with an integrated AI agent | Migration & AI | C# |
| [attendance-system-migration](https://github.com/yktsnet/attendance-system-migration) | Migrated WebForms to .NET 10 + React, with real-time monitoring via SignalR | Migration & AI | C# |
| [order-system-rag](https://github.com/yktsnet/order-system-rag) | Structures paperwork PDFs and automatically routes questions between Text-to-SQL and RAG based on their nature | Migration & AI | Python |
| [wiki-guessur](https://github.com/yktsnet/wiki-guessur) | A benchmark for identifying Wikipedia articles with their defining sentences removed. Measures MRR across 4 methods (formula / GBDT / LLM re-ranking) × 5 seeds | Research | Python |

---

### How I build

Development runs in two phases. In the startup phase, spec documents (PLAN.md / JUDGE.md) drive development, then get distilled into the README at release and retire. In the maintenance phase, the driving documents hand off to a guarantee ledger (guarantees.md) — humans authorize only "what must never break," while AI and CI own test implementation and enforcement (Guarantee-Driven Development).

The execution mechanism is issue-driven, separating design (conversational AI), implementation (autonomous AI), and authorization/verification (human merge). Dangerous operations are blocked not by operational rules but by `deny` entries in `.claude/settings.json`, and the execution environment is declaratively unified with Nix Flakes and continuously verified in CI.

This entire system is published as [dotfiles-public](https://github.com/yktsnet/dotfiles-public), and the general-purpose skills can be installed as a Claude Code plugin marketplace. The process is left as-is in each repository's issues and PRs.
