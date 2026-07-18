# 02 Evidence Verification and Consistency
事実確認、根拠、数値、時点依存情報、本文とJSONの一貫性を扱います。

---

## Source: `knowledge/factuality/evidence-verification-v1.0.md`

# Evidence Verification v1.0

数値、日付、仕様、引用、制度、製品情報は根拠の有無と鮮度を確認します。確認不能な主張は創作せず、削除・保留・警告のいずれかに分類します。

---

## Source: `knowledge/writing/consistency-audit-v1.0.md`

# Consistency Audit v1.0

タイトル、検索意図、導入、見出し、本文、FAQ、結論、変更フラグ、JSONを横断確認します。本文とJSONは同じRuntime Stateから生成し、別々の判断を行いません。

---

## Source: `knowledge/factuality/KN-FAC-001-verify-time-sensitive-claims.md`

---
id: KN-FAC-001
title: Verify Time-Sensitive Claims
category: factuality
knowledge_type: rule_basis
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-QLT-001
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-FAC-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Verify Time-Sensitive Claims

## Statement

料金・仕様・制度・最新機能など変化しうる重要情報は、確認日付きの信頼できるSourceで検証する。

## Rationale

古い情報を最新情報として断定することを防ぐため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/factuality/KN-FAC-002-numeric-claims-need-basis.md`

---
id: KN-FAC-002
title: Numeric Claims Need Basis
category: factuality
knowledge_type: rule_basis
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-QLT-001
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-FAC-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Numeric Claims Need Basis

## Statement

数値・割合・期間・料金は、出典、計算過程、条件のいずれかを示せる状態にする。

## Rationale

根拠不明の数字は説得力ではなく誤情報リスクを増やすため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/factuality/KN-FAC-003-separate-fact-and-opinion.md`

---
id: KN-FAC-003
title: Separate Fact and Opinion
category: factuality
knowledge_type: editorial_principle
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-QLT-001
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-FAC-004
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Separate Fact and Opinion

## Statement

確認済み事実、一般的傾向、編集判断、体験を区別して表現する。

## Rationale

異なる確度の情報を同じ断定調で扱うと誤解を生むため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/factuality/KN-FAC-004-unable-to-verify-must-remain-visible.md`

---
id: KN-FAC-004
title: Unable to Verify Must Remain Visible
category: factuality
knowledge_type: warning
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-PRD-002
- SRC-QLT-001
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-PUB-003
- QF-FAC-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Unable to Verify Must Remain Visible

## Statement

重要情報を確認できない場合は、削除・限定表現・要確認のいずれかで扱い、推測で埋めない。

## Rationale

検証不能を隠すとPublish Ready判定が不正確になるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/factuality/KN-FAC-005-no-unsupported-performance-forecast.md`

---
id: KN-FAC-005
title: No Unsupported Performance Forecast
category: factuality
knowledge_type: rule
version: 1.0.0
status: active
authority_level: B
confidence: verified
source_ids:
- SRC-KNW-001
applicability:
  request_types:
  - existing_article_improvement
exceptions: []
related_quality_rules: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# KN-FAC-005 No Unsupported Performance Forecast

## Rule

CTRやクリック数の具体的な改善幅は、比較可能な実測データまたは明示された根拠がない限り予測しない。

## Safe expression

- 「CTR改善余地がある」
- 「再測定で確認する」
- 「母数が小さいため定量予測は困難」

## Unsafe expression

- 根拠なしに「2〜3%へ改善」
- 根拠なしに「+1〜2クリック」

---

## Source: `quality/rules/factuality/QF-FAC-003-internal-consistency.yaml`

```yaml
id: QF-FAC-003
name: Internal Consistency
dimension: factuality
severity: critical
version: 1.0.0
status: active
requirement: 記事内の数値、結論、条件、用語は相互に矛盾してはならない。
evaluation_method: deterministic_or_model_assisted
pass_condition: 重要な主張が記事内で一貫している。
fail_condition: 同一記事内で重要情報が矛盾している。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```
