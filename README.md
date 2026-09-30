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
| [attendance-system-migration](https://github.com/yktsnet/attendance-system-migration) | WebForms を .NET 10 + React へ移行し、SignalR でリアルタイム監視を実装 | `modernization` |
| [order-system-rag](https://github.com/yktsnet/order-system-rag) | 帳票 PDF を構造化し、質問の性質で Text-to-SQL / RAG を自動振り分け | `chatbot` |
| [folio-agent](https://github.com/yktsnet/folio-agent) | 知識を全同梱する CAG 方式のポートフォリオチャット、npm 公開・Cloudflare Workers | `chatbot` |
| [sdlc-kit](https://github.com/yktsnet/sdlc-kit) | 1人で固めた開発の型を、チームのリポジトリへ1コマンドで取り込める配布キット | `team` |
| [ladder-kit](https://github.com/yktsnet/ladder-kit) | エージェントで開発を回すチームの評価ラダー。5軸5段階で評価と採用を1本の物差しに乗せる | `team` |
| [live-dynamic](https://github.com/yktsnet/live-dynamic) | 検証済み戦略を同じ config で無人実弾運転する実行層。冪等な発注ゲート・OCO・キルスイッチを実装 | `trading` |
| [etax-prep](https://github.com/yktsnet/etax-prep) | 給与と副業の事業所得を合算する帳簿。金額と勘定科目の入力だけで確定申告用の集計まで出す | `finance` |

---

### How I build

開発は2フェーズで回している。立ち上げ期は仕様書（PLAN.md / JUDGE.md）が開発を駆動し、リリース時に README へ昇華して役目を終える。保守期は駆動文書を保証台帳（guarantees.md）へ交代させ、「何が壊れてはいけないか」だけを人間が裁可し、テストの実装と執行は AI と CI に任せる（Guarantee-Driven Development）。

実行機構は、設計（対話型 AI）・実装（自律型 AI）・裁可と検証（人間のマージ）を分けた Issue 駆動。危険な操作は運用ルールではなく `.claude/settings.json` の deny で遮断し、実行環境は Nix Flakes で宣言的に統一して CI で検証し続けている。

この仕組み全体を [dotfiles-public](https://github.com/yktsnet/dotfiles-public) として公開しており、汎用 skill は Claude Code の plugin marketplace として導入できる。過程は各リポジトリの Issue と PR にそのまま残している。
