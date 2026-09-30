[🇯🇵 日本語](README.md) | [🇬🇧 English](README.en.md)

### Find what's worth fixing in the numbers, build it without changing how people already work, and hand it over so the team can keep it running on their own.

Deciding comes from running a business, building from the shop floor, handing over from teaching. Twelve years running a cram school, and an LLC from founding through liquidation — I closed the books myself, without an accountant, so I can read where the money moves in a business. Now I work at a contract development firm, take on freelance projects of my own, and open-source the tooling they turn out to need.

---

### Works

| Repository | Description | Tag |
| --- | --- | --- |
| [nfc-attendance-kit](https://github.com/yktsnet/nfc-attendance-kit) | Auto-aggregates NFC time clock punches into a spreadsheet, running in production for a real client (−5h/month) | `iot` |
| [excel-kanri](https://github.com/yktsnet/excel-kanri) | Adds web forms, PDF conversion, and full-text search to existing Excel paperwork, in production for a real client | `modernization` |
| [order-system-migration](https://github.com/yktsnet/order-system-migration) | Migrated a legacy WinForms app to .NET 10 Web API + React and integrated an AI agent into it | `modernization` |
| [attendance-system-migration](https://github.com/yktsnet/attendance-system-migration) | Migrated a legacy WebForms app to .NET 10 + React, adding real-time monitoring via SignalR | `modernization` |
| [order-system-rag](https://github.com/yktsnet/order-system-rag) | Structures paperwork PDFs and automatically routes questions between Text-to-SQL and RAG based on their nature | `chatbot` |
| [folio-agent](https://github.com/yktsnet/folio-agent) | A CAG-style portfolio chat that bundles all knowledge inline, published on npm and running on Cloudflare Workers | `chatbot` |
| [sdlc-kit](https://github.com/yktsnet/sdlc-kit) | A distribution kit that imports a solo-hardened dev process into team repos in one command | `team` |
| [ladder-kit](https://github.com/yktsnet/ladder-kit) | An engineer ladder for teams developing with AI agents, putting evaluation and hiring on one 5×5 scale | `team` |
| [live-dynamic](https://github.com/yktsnet/live-dynamic) | Runs validated strategies live and unattended on the same config, with idempotent order gating, OCO, and kill switches | `trading` |
| [etax-prep](https://github.com/yktsnet/etax-prep) | A ledger for salaried workers with side-business income: enter amounts and accounts, get totals ready for tax filing | `finance` |

---

### How I build

Development runs in two phases. In the startup phase, spec documents (PLAN.md / JUDGE.md) drive development, then get distilled into the README at release and retire. In the maintenance phase, the driving documents hand off to a guarantee ledger (guarantees.md) — humans authorize only "what must never break," while AI and CI own test implementation and enforcement (Guarantee-Driven Development).

The execution mechanism is issue-driven, separating design (conversational AI), implementation (autonomous AI), and authorization/verification (human merge). Dangerous operations are blocked not by operational rules but by `deny` entries in `.claude/settings.json`, and the execution environment is declaratively unified with Nix Flakes and continuously verified in CI.

This entire system is published as [dotfiles-public](https://github.com/yktsnet/dotfiles-public), and the general-purpose skills can be installed as a Claude Code plugin marketplace. The process is left as-is in each repository's issues and PRs.
