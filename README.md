### 曖昧な課題を技術に翻訳し、現場に定着する仕組みをつくる。

学習塾の経営12年（合同会社の設立から清算まで）を経てエンジニアに転じた。いまは SES 企業でエンジニア2名とのチームで受託開発を担い、CI/CD・IaC・テスト・ドキュメント統一といった開発標準化を主導している。並行してマンション管理会社の外部 CTO として現場の DX を推進している。導入されたのに使われなくなるツールを経営の現場で見てきたので、既存の運用は崩さず、裏側に自動化を差し込む設計を軸にしている。

### Tech Stack

<img src="https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python"> <img src="https://img.shields.io/badge/-Go-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go"> <img src="https://img.shields.io/badge/-C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt="C#"> <img src="https://img.shields.io/badge/-TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript"> <img src="https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React"> <img src="https://img.shields.io/badge/-Vue-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white" alt="Vue"> <img src="https://img.shields.io/badge/-FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI"> <img src="https://img.shields.io/badge/-Laravel-FF2D20?style=flat-square&logo=laravel&logoColor=white" alt="Laravel"> <img src="https://img.shields.io/badge/-LangGraph-1C3C3C?style=flat-square&logo=langchain&logoColor=white" alt="LangGraph"> <img src="https://img.shields.io/badge/-Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Gemini"> <img src="https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL"> <img src="https://img.shields.io/badge/-Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white" alt="Raspberry Pi"> <img src="https://img.shields.io/badge/-Cloudflare-F38020?style=flat-square&logo=cloudflare&logoColor=white" alt="Cloudflare"> <img src="https://img.shields.io/badge/-NixOS-5277C3?style=flat-square&logo=nixos&logoColor=white" alt="NixOS"> <img src="https://img.shields.io/badge/-Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker">

### Works

#### 実運用しているもの

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/nfc-attendance-kit"><b>nfc-attendance-kit</b></a></td>
    <td>NFC 打刻 → スプレッドシート自動集計。実顧客で稼働中（月次工数 −5h）。pip 依存ゼロで Raspberry Pi 2 でも動く</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/cat-feed-tracker"><b>cat-feed-tracker</b></a></td>
    <td>給餌棚の開閉検知 → LINE 通知。Pico W + FastAPI + PostgreSQL</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/training-scheduler"><b>training-scheduler</b></a></td>
    <td>新人の手応えを共有する研修支援ツール。Go + Vue 単一バイナリ、SQLite のみ</td>
  </tr>
</table>

#### ライブラリ・ツール

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/folio-agent"><b>folio-agent</b></a></td>
    <td>静的サイト用ポートフォリオチャット（npm公開）。ビルド時に知識を全同梱するCAG方式。Cloudflare Workers + LangGraph.js</td>
  </tr>
</table>

#### モダナイゼーション + AI 統合

<table>
  <tr>
    <td><a href="https://github.com/yktsnet/order-system-migration"><b>order-system-migration</b></a></td>
    <td>WinForms → .NET 8 Web API + React。LangGraph AI エージェントを統合</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/attendance-system-migration"><b>attendance-system-migration</b></a></td>
    <td>WebForms → .NET 8 + React。SignalR でリアルタイム打刻監視を実装</td>
  </tr>
  <tr>
    <td><a href="https://github.com/yktsnet/order-system-rag"><b>order-system-rag</b></a></td>
    <td>帳票 PDF を Azure AI Document Intelligence で構造化し、質問の性質で Text-to-SQL / RAG へ自動振り分け</td>
  </tr>
</table>


### How I build

設計（対話型 AI）・実装（自律型 AI）・検証（人間のマージ）を分けた Issue 駆動で開発している。危険な操作は運用ルールではなく設定で遮断する。仕組みは [dotfiles-public](https://github.com/yktsnet/dotfiles-public) に、過程は各リポジトリの Issue と PR にそのまま残している。

---

[![Portfolio](https://img.shields.io/badge/Portfolio-ykts.net-5de4c7?style=flat-square)](https://ykts.net)
[![Zenn](https://img.shields.io/badge/Zenn-yktsnet-3EA8FF?style=flat-square&logo=zenn&logoColor=white)](https://zenn.dev/yktsnet)
