# 04 Writing and Content Design
公開品質の日本語記事を作るための構成・文章・完全性の規則です。

---

## Source: `knowledge/writing/KN-WRI-001-answer-first-introduction.md`

---
id: KN-WRI-001
title: Answer-First Introduction
category: writing
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
- condition: 物語・体験を主目的とする記事
  behavior: 記事目的に適した導入を優先する。
related_quality_rules:
- QF-INT-002
- QF-REA-003
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Answer-First Introduction

## Statement

導入文では、読者が最初に知りたい答えまたは判断の要点を早めに示す。

## Rationale

背景説明だけが続く導入は読者を待たせるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/writing/KN-WRI-002-one-section-one-purpose.md`

---
id: KN-WRI-002
title: One Section One Purpose
category: writing
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
- QF-STR-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# One Section One Purpose

## Statement

一つの見出しは一つの読者課題または説明目的に集中させる。

## Rationale

複数目的を混在させると見出し構造と理解が崩れるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/writing/KN-WRI-003-procedure-must-reach-completion.md`

---
id: KN-WRI-003
title: Procedure Must Reach Completion
category: writing
knowledge_type: process
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-QLT-001
applicability:
  request_types:
  - how_to
  - troubleshooting
  - settings_guide
exceptions: []
related_quality_rules:
- QF-COM-003
- QF-HLP-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Procedure Must Reach Completion

## Statement

手順記事は、開始条件から完了確認まで実行可能な順序で説明する。

## Rationale

途中で終わる手順は読者の目的を達成できないため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/writing/KN-WRI-004-faq-must-add-new-value.md`

---
id: KN-WRI-004
title: FAQ Must Add New Value
category: writing
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
- QF-REA-003
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# FAQ Must Add New Value

## Statement

FAQは本文の言い換えではなく、追加疑問・例外・短い確認に使う。

## Rationale

本文重複のFAQは冗長化し、記事価値を増やさないため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/writing/KN-WRI-005-conclusion-without-repetition.md`

---
id: KN-WRI-005
title: Conclusion Without Repetition
category: writing
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
- QF-REA-003
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Conclusion Without Repetition

## Statement

まとめは本文の全項目を繰り返さず、結論と次の行動を簡潔に示す。

## Rationale

長い再掲は読後の判断を遅らせるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/writing/KN-WRI-006-natural-japanese-over-formulaic-politeness.md`

---
id: KN-WRI-006
title: Natural Japanese Over Formulaic Politeness
category: writing
knowledge_type: editorial_principle
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-QLT-001
applicability:
  request_types:
  - ja-JP
exceptions: []
related_quality_rules:
- QF-JPN-001
- QF-JPN-003
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Natural Japanese Over Formulaic Politeness

## Statement

過剰な丁寧表現や定型的AI表現より、意味が明確で自然な日本語を優先する。

## Rationale

形式的な丁寧さは文章を冗長・不自然にすることがあるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/content-design/KN-CDS-001-define-content-scope.md`

---
id: KN-CDS-001
title: Define Content Scope
category: content-design
knowledge_type: decision_heuristic
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-DOM-001
- SRC-QLT-001
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-INT-003
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Define Content Scope

## Statement

記事で扱う範囲と扱わない範囲をContent Planで明示する。

## Rationale

境界がない計画は情報の追加が止まらず、主題が散漫になるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/content-design/KN-CDS-002-map-required-content-before-drafting.md`

---
id: KN-CDS-002
title: Map Required Content Before Drafting
category: content-design
knowledge_type: process
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-DOM-001
- SRC-QLT-001
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-COM-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Map Required Content Before Drafting

## Statement

本文生成前に、Primary Intentを満たす必須情報をContent Requirementへ整理する。

## Rationale

生成後に不足を補うより、計画段階で必要情報を確定した方が品質が安定するため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/content-design/KN-CDS-003-reader-level-controls-explanation-depth.md`

---
id: KN-CDS-003
title: Reader Level Controls Explanation Depth
category: content-design
knowledge_type: decision_heuristic
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-DOM-001
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-HLP-002
- QF-REA-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Reader Level Controls Explanation Depth

## Statement

読者の知識レベルに合わせ、用語説明と手順の細かさを調整する。

## Rationale

説明不足と過剰説明の両方を避けるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `quality/rules/japanese/QF-JPN-001-natural-japanese.yaml`

```yaml
id: QF-JPN-001
name: Natural Japanese
dimension: japanese
severity: critical
version: 1.0.0
status: active
requirement: 直訳調や意味の通らない表現を避け、自然な日本語にする。
evaluation_method: deterministic_or_model_assisted
pass_condition: 日本語話者が追加修正せず理解できる。
fail_condition: 不自然な語順・助詞・直訳調が残る。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge:
- KN-WRI-006
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/japanese/QF-JPN-002-expression-consistency.yaml`

```yaml
id: QF-JPN-002
name: Expression Consistency
dimension: japanese
severity: major
version: 1.0.0
status: active
requirement: 表記、用語、敬体・常体、数字表現を記事内で統一する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 主要表現に一貫性がある。
fail_condition: 表記揺れや文体混在が目立つ。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/japanese/QF-JPN-003-ai-like-phrase-reduction.yaml`

```yaml
id: QF-JPN-003
name: AI-Like Phrase Reduction
dimension: japanese
severity: major
version: 1.0.0
status: active
requirement: 内容のない定型句、過剰な総括、機械的な語尾を減らす。
evaluation_method: deterministic_or_model_assisted
pass_condition: 各文が具体的な意味を持つ。
fail_condition: AI的な抽象句や定型句が頻出する。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge:
- KN-WRI-006
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/structure/QF-STR-001-valid-heading-hierarchy.yaml`

```yaml
id: QF-STR-001
name: Valid Heading Hierarchy
dimension: structure
severity: major
version: 1.0.0
status: active
requirement: 見出し階層は飛び級や複数H1を避け、論理構造を保つ。
evaluation_method: deterministic_or_model_assisted
pass_condition: H1が一つでH2・H3が正しく配置される。
fail_condition: 見出し階層が破綻している。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/structure/QF-STR-002-one-section-one-purpose.yaml`

```yaml
id: QF-STR-002
name: One Section One Purpose
dimension: structure
severity: major
version: 1.0.0
status: active
requirement: 一つのSectionは主要目的を一つに限定する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 各Sectionの目的が明確で重複が少ない。
fail_condition: 一つのSectionに無関係な複数目的が混在する。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge:
- KN-WRI-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/structure/QF-STR-003-logical-information-order.yaml`

```yaml
id: QF-STR-003
name: Logical Information Order
dimension: structure
severity: critical
version: 1.0.0
status: active
requirement: 情報は読者の理解と実行に適した順序で配置する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 前提、回答、手順、注意が自然に進む。
fail_condition: 結論や手順の順序が理解を妨げる。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/completeness/QF-COM-001-required-content-coverage.yaml`

```yaml
id: QF-COM-001
name: Required Content Coverage
dimension: completeness
severity: critical
version: 1.0.0
status: active
requirement: Content Planで必須とされた情報をすべて含める。
evaluation_method: deterministic_or_model_assisted
pass_condition: 必須Content Requirementが充足している。
fail_condition: 主要手順・説明・判断情報が欠落している。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge:
- KN-CDS-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/completeness/QF-COM-002-exception-and-warning-coverage.yaml`

```yaml
id: QF-COM-002
name: Exception and Warning Coverage
dimension: completeness
severity: major
version: 1.0.0
status: active
requirement: 重要な例外、注意点、適用外条件を必要に応じて説明する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 誤解や失敗を防ぐ例外・注意が含まれる。
fail_condition: 重要な例外を省略し誤解を生む。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/completeness/QF-COM-003-action-completion.yaml`

```yaml
id: QF-COM-003
name: Action Completion
dimension: completeness
severity: critical
version: 1.0.0
status: active
requirement: 手順記事は読者が目的を完了できるところまで説明する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 開始から完了確認まで実行可能である。
fail_condition: 途中で説明が終わり、目的を達成できない。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge:
- KN-WRI-003
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```
