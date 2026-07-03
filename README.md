曖昧な課題を技術に翻訳し、現場に定着する仕組みをつくる。

学習塾の経営12年（合同会社の設立から清算まで）を経てエンジニアに転じた。いまは SES 企業でテックリードとして、エンジニア2名とのチームで受託開発を担い、CI/CD・IaC・テスト・ドキュメント統一といった開発標準化を主導している。並行してマンション管理会社の外部 CTO として現場の DX を推進している。導入されたのに使われなくなるツールを経営の現場で見てきたので、既存の運用は崩さず、裏側に自動化を差し込む設計を軸にしている。

## Works

実運用しているもの:

| リポジトリ | 概要 |
|---|---|
| [nfc-attendance-kit](https://github.com/yktsnet/nfc-attendance-kit) | NFC カードをかざすだけの勤怠打刻。実顧客で稼働中、月次の勤怠工数を5時間削減。pip 依存ゼロで Raspberry Pi 2 でも動く |
| [cat-feed-tracker](https://github.com/yktsnet/cat-feed-tracker) | 給餌棚の開閉を検知し LINE へ通知する家庭向け IoT。Pico W + FastAPI + PostgreSQL |
| [training-scheduler](https://github.com/yktsnet/training-scheduler) | 新人の手応えをメンターと共有する研修支援ツール。Go + Vue を単一バイナリに固め、SQLite のみで動く |

モダナイゼーションのプロセスを提示するサンプル:

| リポジトリ | 概要 |
|---|---|
| [order-system-migration](https://github.com/yktsnet/order-system-migration) | WinForms を .NET 8 Web API + React へ段階移行し、LangGraph の AI エージェントを統合 |
| [attendance-system-migration](https://github.com/yktsnet/attendance-system-migration) | WebForms を解体し、WebForms では不可能だったリアルタイム打刻監視を SignalR で実装 |
| [order-system-rag](https://github.com/yktsnet/order-system-rag) | 帳票 PDF を構造化し、質問の性質で Text-to-SQL / RAG へ自動で振り分ける |

## How I build

設計（対話型 AI）・実装（自律型 AI）・検証（人間のマージ）を分けた Issue 駆動で開発している。危険な操作は運用ルールではなく設定で遮断する。仕組みは [dotfiles-public](https://github.com/yktsnet/dotfiles-public) に、過程は各リポジトリの Issue と PR にそのまま残している。

## Writing

[Zenn](https://zenn.dev/yktsnet) に構築の記録を書いている。
