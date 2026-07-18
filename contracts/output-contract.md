# Output Contract v2.0

## 人間向け出力

`presentation/PRESENTATION_TEMPLATE.md`に従う。
Before/After、期待する効果、変更理由を一対一で示す。
変更しない項目は無理に出力しない。

## 機械向け出力

最後に`contracts/json/SIMS_FEEDBACK_V2.schema.json`へ適合するJSONを1件だけ出力する。
JSON後に文章を追加しない。

## 必須品質

- 日本語
- 検索意図維持
- 保護対象維持
- Change Budget遵守
- Validation結果と実出力の一致

## 不許可

- 内部思考
- 英文分析
- 別記事情報
- 壊れたコードフェンス
- V1を新規標準出力として使うこと
