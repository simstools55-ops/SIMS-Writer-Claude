# 03 SEO Knowledge
検索意図、タイトル、見出し、CTR、クエリ利用、カニバリ、内部リンクの判断基準です。

---

## Source: `knowledge/seo/seo-knowledge-v1.0.md`

# SEO Knowledge v1.0

検索意図適合、情報利得、明確なタイトル、読者の疑問解消を優先します。CTRだけを目的に誇張せず、品質監査で変更不要と判定した箇所は維持します。

---

## Source: `knowledge/seo/KN-SEO-001-primary-intent-before-structure.md`

---
id: KN-SEO-001
title: Primary Intent Before Structure
category: seo
knowledge_type: decision_heuristic
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-QLT-001
applicability:
  request_types:
  - new_article
  - existing_article_improvement
exceptions: []
related_quality_rules:
- QF-INT-001
- QF-INT-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Primary Intent Before Structure

## Statement

見出し構成を作る前に、メインクエリのPrimary Intentを明確にする。

## Rationale

検索意図が未確定の構成は情報量があっても主目的を外しやすいため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/seo/KN-SEO-002-main-answer-must-be-explicit.md`

---
id: KN-SEO-002
title: Main Answer Must Be Explicit
category: seo
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
exceptions:
- condition: 比較条件により答えが変わる場合
  behavior: 単一結論ではなく、先に判断軸と条件を示す。
related_quality_rules:
- QF-INT-002
- QF-HLP-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Main Answer Must Be Explicit

## Statement

記事の主要な答えを読者が早い段階で把握できるよう明示する。

## Rationale

答えを探させる構成は離脱と不満を招くため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/seo/KN-SEO-003-title-must-match-article-promise.md`

---
id: KN-SEO-003
title: Title Must Match Article Promise
category: seo
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
- QF-SEO-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Title Must Match Article Promise

## Statement

SEOタイトルは本文が実際に提供する価値と一致させる。

## Rationale

検索結果で形成した期待と本文がずれると、有用性と信頼を損なうため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/seo/KN-SEO-004-natural-query-usage.md`

---
id: KN-SEO-004
title: Natural Query Usage
category: seo
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
- QF-SEO-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Natural Query Usage

## Statement

メインクエリと関連語は、日本語として自然な箇所に必要量だけ使用する。

## Rationale

機械的反復は可読性を下げ、読者価値へ貢献しないため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/seo/KN-SEO-005-separate-out-of-scope-intent.md`

---
id: KN-SEO-005
title: Separate Out-of-Scope Intent
category: seo
knowledge_type: decision_heuristic
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
- QF-INT-003
- QF-SEO-004
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Separate Out-of-Scope Intent

## Statement

主題から外れる検索意図は、別記事候補として分離する。

## Rationale

すべてのクエリを一記事へ混在させると主題と構造がぼやけるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/seo/KN-SEO-006-ctr-improvement-requires-body-alignment.md`

---
id: KN-SEO-006
title: CTR Improvement Requires Body Alignment
category: seo
knowledge_type: operational_principle
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-QLT-001
applicability:
  request_types:
  - ctr_improvement
exceptions: []
related_quality_rules:
- QF-SEO-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# CTR Improvement Requires Body Alignment

## Statement

CTR改善のタイトル変更は、本文内容と検索意図の整合を確認して行う。

## Rationale

クリックだけを狙う表現は期待外れと品質低下を招くため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/seo/KN-SEO-007-main-query-field-is-pure.md`

---
id: KN-SEO-007
title: Main Query Field Is Pure
category: seo
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

# KN-SEO-007 Main Query Field Is Pure

## Rule

`new_values.main_query` には検索クエリ文字列だけを格納する。

メインクエリを本文やタイトルから推定した場合も、注記を同じフィールドへ混在させず、`main_query_source="estimated"` と `estimated_fields=["main_query"]` で明示し、補足説明は `information` に記録する。

---

## Source: `knowledge/seo/KN-SEO-008-comparison-intent-consistency.md`

# KN-SEO-008 比較記事の結論整合性

比較記事では、比較項目、比較表または要約、各商品をおすすめする人、最終結論を一貫させる。比較結果と推奨商品が矛盾してはならない。価格だけで優劣を決めず、内容量、使用回数、用途など本文で確認できる条件を併記する。

---

## Source: `quality/rules/seo/QF-SEO-001-title-intent-alignment.yaml`

```yaml
id: QF-SEO-001
name: Title Intent Alignment
dimension: seo
severity: critical
version: 1.0.0
status: active
requirement: SEO TitleはPrimary Intentと本文の実内容に一致しなければならない。
evaluation_method: deterministic_or_model_assisted
pass_condition: タイトルの約束を本文が満たしている。
fail_condition: タイトルと本文が不一致または誇張である。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge:
- KN-SEO-003
- KN-SEO-006
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/seo/QF-SEO-002-natural-query-usage.yaml`

```yaml
id: QF-SEO-002
name: Natural Query Usage
dimension: seo
severity: major
version: 1.0.0
status: active
requirement: メインクエリと関連語は自然な日本語として使用する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 不自然な反復や語句詰め込みがない。
fail_condition: キーワードを機械的に反復している。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge:
- KN-SEO-004
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/seo/QF-SEO-003-heading-topic-alignment.yaml`

```yaml
id: QF-SEO-003
name: Heading Topic Alignment
dimension: seo
severity: major
version: 1.0.0
status: active
requirement: 各見出しは記事主題とSection目的に整合する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 見出しだけで論理的な記事の流れが分かる。
fail_condition: 主題と無関係な見出しや重複見出しがある。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/seo/QF-SEO-004-cannibalization-risk-check.yaml`

```yaml
id: QF-SEO-004
name: Cannibalization Risk Check
dimension: seo
severity: major
version: 1.0.0
status: active
requirement: 既存記事と検索意図が重複する可能性を確認する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 重複リスクが評価され、必要なら分離されている。
fail_condition: 同一意図の記事を無評価で追加・拡張している。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge:
- KN-SEO-005
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/search-intent/QF-INT-001-primary-intent-must-be-answered.yaml`

```yaml
id: QF-INT-001
name: Primary Intent Must Be Answered
dimension: search-intent
severity: blocker
version: 1.0.0
status: active
requirement: 記事はメインクエリのPrimary Intentへ直接回答しなければならない。
evaluation_method: deterministic_or_model_assisted
pass_condition: 主要な疑問への答えが本文に明示されている。
fail_condition: 主題がずれ、主要な疑問に答えていない。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge:
- KN-SEO-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/search-intent/QF-INT-002-main-answer-must-be-explicit.yaml`

```yaml
id: QF-INT-002
name: Main Answer Must Be Explicit
dimension: search-intent
severity: critical
version: 1.0.0
status: active
requirement: Main Answerは読者が見つけやすい位置に明示する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 導入または主要節で結論が明確である。
fail_condition: 結論が暗黙的、または記事末まで判別できない。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge:
- KN-SEO-001
- KN-SEO-002
- KN-WRI-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/search-intent/QF-INT-003-out-of-scope-intent-separation.yaml`

```yaml
id: QF-INT-003
name: Out-of-Scope Intent Separation
dimension: search-intent
severity: major
version: 1.0.0
status: active
requirement: 別記事にすべき検索意図を混在させず、範囲外として分離する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 主題の範囲が明確で不要な意図が混在しない。
fail_condition: 複数の異なる意図を一記事へ詰め込んでいる。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge:
- KN-SEO-005
- KN-CDS-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```
