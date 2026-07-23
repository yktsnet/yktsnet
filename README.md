### 曖昧な課題を技術に翻訳し、現場に定着する仕組みをつくる。

学習塾の経営12年（合同会社の設立から清算まで）を経てエンジニアに転じた。いまは SES 企業でエンジニアとのチームで受託開発を担い、CI/CD・IaC・テスト・ドキュメント統一といった開発標準化を主導している。並行してマンション管理会社の外部 CTO として現場の DX を推進している。導入されたのに使われなくなるツールを経営の現場で見てきたので、既存の運用は崩さず、裏側に自動化を差し込む設計を軸にしている。

---

### Works

#### Production

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/nfc-attendance-kit"><b>nfc-attendance-kit</b></a></td>
    <td>NFC 打刻をスプレッドシートに自動集計、実顧客で稼働中（月次工数 −5h）</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/excel-kanri"><b>excel-kanri</b></a></td>
    <td>既存の Excel 帳票運用に Web フォーム・PDF 変換・全文検索を後付け、実顧客で稼働中</td>
  </tr>
</table>

#### Trading Infrastructure

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/bt-lab"><b>bt-lab</b></a></td>
    <td>複数戦略候補を横断検証し、ドローダウンや Recovery Factor で自動選抜する8段パイプライン</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/bt-dynamic"><b>bt-dynamic</b></a></td>
    <td>相場を9セル（トレンド強度×ボラティリティ）でレジーム切替するバックテストコア、PyPI 配布</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/live-dynamic"><b>live-dynamic</b></a></td>
    <td>検証済み戦略を同一 config のまま systemd timer で無人実弾運転する実行層。冪等な発注ゲート・OCO・キルスイッチの安全設計を参照実装として公開</td>
  </tr>
</table>

#### Libraries & Tools

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/folio-agent"><b>folio-agent</b></a></td>
    <td>知識を全同梱する CAG 方式のポートフォリオチャット、npm 公開・Cloudflare Workers</td>
  </tr>
</table>

#### Legacy Migration & AI

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/order-system-migration"><b>order-system-migration</b></a></td>
    <td>WinForms を .NET 10 Web API + React へ移行し、AI エージェントを統合</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/attendance-system-migration"><b>attendance-system-migration</b></a></td>
    <td>WebForms を .NET 10 + React へ移行し、SignalR でリアルタイム監視を実装</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/order-system-rag"><b>order-system-rag</b></a></td>
    <td>帳票 PDF を構造化し、質問の性質で Text-to-SQL / RAG を自動振り分け</td>
  </tr>
</table>

#### Research

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/wiki-guessur"><b>wiki-guessur</b></a></td>
    <td>定義文を消した Wikipedia 記事の同定ベンチマーク。数式 / GBDT / LLM 再判定の4手法 × 5シードで MRR を実測</td>
  </tr>
</table>


### How I build

開発は2フェーズで回している。立ち上げ期は仕様書（PLAN.md / JUDGE.md）が開発を駆動し、リリース時に README へ昇華して役目を終える。保守期は駆動文書を保証台帳（guarantees.md）へ交代させ、「何が壊れてはいけないか」だけを人間が裁可し、テストの実装と執行は AI と CI に任せる（Guarantee-Driven Development）。

実行機構は、設計（対話型 AI）・実装（自律型 AI）・裁可と検証（人間のマージ）を分けた Issue 駆動。危険な操作は運用ルールではなく `.claude/settings.json` の deny で遮断し、実行環境は Nix Flakes で宣言的に統一して CI で検証し続けている。

この仕組み全体を [dotfiles-public](https://github.com/yktsnet/dotfiles-public) として公開しており、汎用 skill は Claude Code の plugin marketplace として導入できる。過程は各リポジトリの Issue と PR にそのまま残している。

