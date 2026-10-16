[🇯🇵 日本語](README.md) | [🇬🇧 English](README.en.md)

### 事業の数字から直すべきものを決め、現場のやり方を変えずに作り、人が回せる形にして渡して残す。

決めるところは経営から、作るところは現場から、渡すところは教育から来ている。学習塾を12年、合同会社を設立から清算まで。税理士を立てず決算まで見ていたので、事業の金がどこを通っているかを自分で読める。いまは受託開発の会社に勤めつつ、個人でも受託を受け、必要になった仕組みを OSS にしている。

---

### Works

| Repository | Description | Tag |
| --- | --- | --- |
| [nfc-attendance-kit](https://github.com/yktsnet/nfc-attendance-kit) | NFC 打刻をスプレッドシートに自動集計、実顧客で稼働中（月次工数 −5h） | `iot` |
| [excel-kanri](https://github.com/yktsnet/excel-kanri) | Excel 帳票運用に Web フォーム・PDF 変換・全文検索を後付け、実顧客で稼働中 | `modernization` |
| [order-system-migration](https://github.com/yktsnet/order-system-migration) | WinForms を .NET 10 Web API + React へ移行し、AI エージェントを統合 | `modernization` |
| [folio-agent](https://github.com/yktsnet/folio-agent) | 知識を全同梱する CAG 方式のポートフォリオチャット、npm 公開・Cloudflare Workers | `chatbot` |
| [sdlc-kit](https://github.com/yktsnet/sdlc-kit) | 1人で固めた開発の型を、チームのリポジトリへ1コマンドで取り込める配布キット | `team` |

---

### How I build

開発は2フェーズで回している。立ち上げ期は仕様書（PLAN.md / JUDGE.md）が開発を駆動し、リリース時に README へ昇華して役目を終える。保守期は駆動文書を保証台帳（guarantees.md）へ交代させ、「何が壊れてはいけないか」だけを人間が裁可し、テストの実装と執行は AI と CI に任せる（Guarantee-Driven Development）。

実行機構は、設計（対話型 AI）・実装（自律型 AI）・裁可と検証（人間のマージ）を分けた Issue 駆動。危険な操作は運用ルールではなく `.claude/settings.json` の deny で遮断し、実行環境は Nix Flakes で宣言的に統一して CI で検証し続けている。この仕組み全体と、それを動かす skill を [dotfiles-public](https://github.com/yktsnet/dotfiles-public) として公開している。過程は各リポジトリの Issue と PR にそのまま残している。
