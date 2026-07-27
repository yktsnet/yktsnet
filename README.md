[🇬🇧 English](README.md) | [🇯🇵 日本語](README.ja.md)

### Translating ambiguous problems into technology that sticks in the field.

After 12 years running a cram school (from founding the LLC to winding it down), I moved into engineering. I now work at an SES company, leading development standardization — CI/CD, IaC, testing, and unified documentation — as part of an engineering team on contract projects. In parallel, I serve as an external CTO for a condominium management company, driving DX on-site. Having watched tools get introduced only to fall out of use in management settings, my approach centers on leaving existing operations untouched while inserting automation behind the scenes.

---

### Works

#### Production

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/nfc-attendance-kit"><b>nfc-attendance-kit</b></a></td>
    <td>Auto-aggregates NFC time clock punches into a spreadsheet, running in production for a real client (−5h/month)</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/excel-kanri"><b>excel-kanri</b></a></td>
    <td>Retrofits existing Excel-based paperwork operations with a web form, PDF conversion, and full-text search, running in production for a real client</td>
  </tr>
</table>

#### Trading Infrastructure

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/bt-lab"><b>bt-lab</b></a></td>
    <td>An 8-stage pipeline that cross-validates multiple strategy candidates and automatically selects among them by drawdown and Recovery Factor</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/bt-dynamic"><b>bt-dynamic</b></a></td>
    <td>A backtesting core that switches regimes across 9 cells (trend strength × volatility), distributed on PyPI</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/live-dynamic"><b>live-dynamic</b></a></td>
    <td>An execution layer that runs validated strategies unattended via systemd timer with the same config, live. Published as a reference implementation for safety design covering idempotent order gating, OCO, and kill switches</td>
  </tr>
</table>

#### Libraries & Tools

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/folio-agent"><b>folio-agent</b></a></td>
    <td>A CAG-style portfolio chat that bundles all knowledge inline, published on npm and running on Cloudflare Workers</td>
  </tr>
</table>

#### Legacy Migration & AI

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/order-system-migration"><b>order-system-migration</b></a></td>
    <td>Migrated WinForms to .NET 10 Web API + React, with an integrated AI agent</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/attendance-system-migration"><b>attendance-system-migration</b></a></td>
    <td>Migrated WebForms to .NET 10 + React, with real-time monitoring via SignalR</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/order-system-rag"><b>order-system-rag</b></a></td>
    <td>Structures paperwork PDFs and automatically routes questions between Text-to-SQL and RAG based on their nature</td>
  </tr>
</table>

#### Research

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/wiki-guessur"><b>wiki-guessur</b></a></td>
    <td>A benchmark for identifying Wikipedia articles with their defining sentences removed. Measures MRR across 4 methods (formula / GBDT / LLM re-ranking) × 5 seeds</td>
  </tr>
</table>

---

### How I build

Development runs in two phases. In the startup phase, spec documents (PLAN.md / JUDGE.md) drive development, then get distilled into the README at release and retire. In the maintenance phase, the driving documents hand off to a guarantee ledger (guarantees.md) — humans authorize only "what must never break," while AI and CI own test implementation and enforcement (Guarantee-Driven Development).

The execution mechanism is issue-driven, separating design (conversational AI), implementation (autonomous AI), and authorization/verification (human merge). Dangerous operations are blocked not by operational rules but by `deny` entries in `.claude/settings.json`, and the execution environment is declaratively unified with Nix Flakes and continuously verified in CI.

This entire system is published as [dotfiles-public](https://github.com/yktsnet/dotfiles-public), and the general-purpose skills can be installed as a Claude Code plugin marketplace. The process is left as-is in each repository's issues and PRs.
