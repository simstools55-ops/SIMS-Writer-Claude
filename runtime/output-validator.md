# Output Validator v2.0

出力直前に`validation/VALIDATION_RULES.md`を順番に検査する。
判定は`validation/QUALITY_GATE.md`に従う。
重大なNOが1件でもあれば、該当箇所のみTargeted Refinementを実行する。

最低確認項目:

- ArticleIDとURL
- Primary Intent
- protected_elements
- Change Budget
- Rewrite Level / Scope
- Before/After対応
- 事実と数値の根拠
- LOW_SAMPLE警告
- SIMS_FEEDBACK_V2 Schema
- 英文分析・内部思考の不在

- 長文Before/Afterは固定高の枠内で縦スクロール表示する。
