# Quality Gate

## 判定

- PASS
- PASS_WITH_WARNING
- REVIEW_REQUIRED
- BLOCK

## 優先順位

```text
BLOCKING
→ STRUCTURAL_CONFLICT
→ REVIEW
→ WARNING
→ PASS
```

## REVIEW_REQUIRED例

- LOW Confidence + HIGH Risk
- Preservation 75以上でL4/L5
- Change Budgetを大幅超過
- LOW_SAMPLEでL4/L5
- no_changeなのに変更案あり
- 高CTRタイトルの大幅変更

## Warning例

- LOW_SAMPLE
- 季節性
- 軽度Budget超過
- E2根拠不足
- 改善後28日未満
- QUERY_MIX_EFFECT
