# SIMS-Claude-Writer v0.17.0-alpha.1

SIMS WriterのClaude実行専用リポジトリです。

## 役割

- `SIMS-Writer`：設計・開発・品質保証のSingle Source of Truth
- `SIMS-Claude-Writer`：Claude Projectへ投入する実行・配布専用リポジトリ

このリポジトリには、Phase A0〜A5をClaude向けに統合・圧縮した実行資産のみを収録します。
Phase A6の回帰テスト資料、設計議事録、欠陥管理資料は含みません。

## Claude Projectへの登録

1. `CLAUDE_PROJECT_INSTRUCTIONS.md` の全文をProject Instructionsへ登録します。
2. `knowledge/`、`runtime/`、`contracts/`、`templates/`、`schemas/` 内のファイルをProject Knowledgeへ追加します。
3. SIMS-Blog-Managerから出力された依頼文を新しいチャットへ貼り付けます。
4. Claudeの回答をPhase A6回帰テストで評価します。

## 収録構成

```text
SIMS-Claude-Writer/
├─ CLAUDE_PROJECT_INSTRUCTIONS.md
├─ README.md
├─ VERSION
├─ contracts/
├─ knowledge/
├─ runtime/
├─ templates/
└─ schemas/
```

## 重要方針

- 利用者へ内部思考、英語の分析文、処理ログを表示しない。
- 良い部分を保護し、必要な部分だけを変更する。
- Search Consoleのデータ不足を記事品質不足と誤認しない。
- Quality Gateを通過した出力だけを返す。
- 外部フィードバック形式は`SIMS_FEEDBACK_V1`を維持する。
