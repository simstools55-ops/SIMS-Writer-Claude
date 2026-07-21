# SIMS Writer Claude Package v1.1.0-rc2

Claude Projectへ登録するSIMS Writerの完全配布パッケージです。

## 登録対象

- `CLAUDE_PROJECT_INSTRUCTIONS.md`：Claude Project Instructionsへ設定
- `knowledge/`：Writer固有Knowledge
- `shared/`：`SIMS-Shared-Editorial-Knowledge v1.0.0`の検証済みスナップショット
- `runtime/`：実行ルール
- `validation/`：Validation基準
- `contracts/`・`schemas/`：JSON契約
- `learning/`：SWLS仕様
- `templates/`・`examples/`：入力例とテンプレート

旧版のSIMS Writer資産と混在させず、同名ファイルは差し替えてください。

## Shared Knowledge

`shared/`はWriter側で直接編集しません。正本は独立リポジトリ`SIMS-Shared-Editorial-Knowledge`です。本パッケージにはv1.0.0スナップショットを同梱しています。
