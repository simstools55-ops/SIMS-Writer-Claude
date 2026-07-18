# 07 Operations and Product Rules
既存価値の維持、変更範囲、内部リンク、公開準備、失敗の明示に関する運用規則です。

---

## Source: `knowledge/operations/KN-OPS-001-targeted-revision-before-full-rewrite.md`

---
id: KN-OPS-001
title: Targeted Revision Before Full Rewrite
category: operations
knowledge_type: operational_principle
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-PRD-002
- SRC-OPS-001
applicability:
  request_types:
  - existing_article_improvement
exceptions: []
related_quality_rules:
- QF-SIT-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Targeted Revision Before Full Rewrite

## Statement

既存記事の問題が部分的なら、対象箇所の修正を全文再生成より優先する。

## Rationale

追加編集量と回帰リスクを抑えやすいため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/operations/KN-OPS-002-track-before-and-after.md`

---
id: KN-OPS-002
title: Track Before and After
category: operations
knowledge_type: process
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-DOM-001
- SRC-PRD-002
applicability:
  request_types:
  - existing_article_improvement
exceptions: []
related_quality_rules:
- QF-SIT-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Track Before and After

## Statement

既存記事改善では、保存・修正・追加・削除した要素と理由を追跡する。

## Rationale

改善の妥当性と回帰を後から検証できるようにするため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/operations/KN-OPS-003-do-not-promote-single-outcomes.md`

---
id: KN-OPS-003
title: Do Not Promote Single Outcomes
category: operations
knowledge_type: warning
version: 1.0.0
status: active
authority_level: C
confidence: medium
source_ids:
- SRC-KNW-001
applicability:
  request_types:
  - learning
exceptions: []
related_quality_rules: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Do Not Promote Single Outcomes

## Statement

一件の成功・失敗を、そのまま一般的KnowledgeやPatternへ昇格しない。

## Rationale

検索成果には外部要因があり、再現性を確認する必要があるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/operations/KN-OPS-004-separate-user-output-and-feedback.md`

---
id: KN-OPS-004
title: Separate User Output and Feedback
category: operations
knowledge_type: principle
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

# KN-OPS-004 Separate User Output and Feedback

## Rule

利用者が読む改善案と、システムが読むFeedback JSONを別レイヤーとして扱う。

## Required behavior

- 利用者向けは Before / After / 理由を中心にする。
- Feedback JSONは変更フラグ、変更値、要約、警告に限定する。
- 全文は明示要求時だけ出力する。
- JSONは必ず最後に置き、その後に文章を出さない。

## Evidence

2026-07-17の実記事テスト8件で、全文とJSONの重複、JSON順序違反、利用者が修正箇所を見つけにくい問題が再発した。A000007の部分出力形式が最も高い利用者評価を得た。

---

## Source: `knowledge/operations/KN-OPS-005-change-flags-must-match-output.md`

---
id: KN-OPS-005
title: Change Flags Must Match Output
category: operations
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

# KN-OPS-005 Change Flags Must Match Output

## Rule

`SIMS_FEEDBACK_V1.changes` は実際に出力・適用した変更と一致させる。

## Examples

- 新しい本文ブロックを追加: `body=true`
- FAQだけを追加: `faq=true`, `body=false`
- 内部リンクを評価しただけ: `internal_links=false`
- 検証済みリンクを実際に挿入: `internal_links=true`

変更フラグを手書き判断だけに依存せず、Before/Afterと追加要素から導出する。

---

## Source: `knowledge/operations/KN-OPS-006-internal-link-three-way-classification.md`

---
id: KN-OPS-006
title: Internal Link Three-way Classification
category: operations
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

# KN-OPS-006 Internal Link Three-way Classification

## Rule

内部リンク候補は `採用 / 保留 / 不採用` の3分類で評価する。

- 採用: 検索意図と本文の流れが一致し、URLと記事タイトルを確認済みで、実際に挿入する。
- 保留: 関連性はあるがURL・タイトル・設置根拠のいずれかが未確認。
- 不採用: 検索意図または本文の流れに合わない。

URLまたはタイトルを確認できない候補はHTMLリンクとして出力しない。

---

## Source: `knowledge/operations/KN-OPS-007-improvement-necessity-judgment.md`

# KN-OPS-007 改善必要度を先に判定する

記事改善では、必ず変更案を出すのではなく、最初に次の3段階で必要度を判定する。

- improvement_recommended: 改善推奨
- minor_improvement: 軽微改善
- maintain_current: 現状維持推奨

順位・CTR・検索意図整合性が良好な記事は、変更による悪化リスクを考慮して現状維持を選べる。上位表示しているがCTRや導入に改善余地がある記事は、本文を維持してタイトル・導入など限定範囲だけを修正する。

---

## Source: `knowledge/operations/KN-OPS-008-editorial-change-accountability.md`

# KN-OPS-008 編集変更の説明責任

差分出力では、変更箇所ごとにBefore、After、理由、期待する効果を示す。変更しない主要箇所について説明が必要な場合は、変更しない理由を明示する。期待する効果は読者理解や検索結果での伝わりやすさなど定性的に記述し、根拠のないCTR・順位・クリック数を予測しない。

---

## Source: `knowledge/product/KN-PRD-001-publish-ready-is-the-default.md`

---
id: KN-PRD-001
title: Publish Ready Is the Default
category: product
knowledge_type: editorial_principle
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-PRD-001
- SRC-PRD-002
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-PUB-004
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Publish Ready Is the Default

## Statement

標準成果物は下書きではなく、そのまま公開できる完成稿とする。

## Rationale

利用者の追加編集を前提にすると、製品品質を生成速度へすり替えるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/product/KN-PRD-002-evidence-over-assumption.md`

---
id: KN-PRD-002
title: Evidence Over Assumption
category: product
knowledge_type: rule_basis
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
- QF-FAC-001
- QF-FAC-002
- QF-FAC-004
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Evidence Over Assumption

## Statement

事実・評価・改善提案は、可能な限り確認可能な根拠に基づける。

## Rationale

推測を事実として扱うと、記事の信頼性と読者の安全を損なうため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/product/KN-PRD-003-preserve-proven-value.md`

---
id: KN-PRD-003
title: Preserve Proven Value
category: product
knowledge_type: operational_principle
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-PRD-002
- SRC-QLT-001
applicability:
  request_types:
  - existing_article_improvement
exceptions: []
related_quality_rules:
- QF-SIT-002
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Preserve Proven Value

## Statement

既存記事改善では、有効な内容を特定してから変更範囲を決める。

## Rationale

全面書き換えは独自情報・検索評価・内部リンクを失う危険があるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `knowledge/product/KN-PRD-004-fail-explicitly.md`

---
id: KN-PRD-004
title: Fail Explicitly
category: product
knowledge_type: rule_basis
version: 1.0.0
status: active
authority_level: A
confidence: verified
source_ids:
- SRC-PRD-002
applicability:
  request_types:
  - all
exceptions: []
related_quality_rules:
- QF-PUB-003
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
---

# Fail Explicitly

## Statement

入力不足・検証不能・処理失敗を正常完了として扱わない。

## Rationale

問題を隠した成果物は公開判断を誤らせるため。

## Application Notes

- 適用時はRequest Contextと例外条件を確認する。
- Quality Ruleの判定根拠として利用する場合は、Knowledge IDとVersionを記録する。

---

## Source: `quality/rules/publication/QF-PUB-001-no-placeholder.yaml`

```yaml
id: QF-PUB-001
name: No Placeholder
dimension: publication
severity: blocker
version: 1.0.0
status: active
requirement: 完成稿にプレースホルダー、TODO、仮文を残してはならない。
evaluation_method: deterministic_or_model_assisted
pass_condition: 未置換文字列や作業メモがない。
fail_condition: 要確認、後で追加、XXX等が残る。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/publication/QF-PUB-002-complete-metadata.yaml`

```yaml
id: QF-PUB-002
name: Complete Metadata
dimension: publication
severity: critical
version: 1.0.0
status: active
requirement: 必要なSEO Title、Meta Description、H1等を確定する。
evaluation_method: deterministic_or_model_assisted
pass_condition: 要求されたMetadataがすべて存在する。
fail_condition: 必須Metadataが空または仮状態である。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: true
manual_review_required: false
related_knowledge: []
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/publication/QF-PUB-003-no-unresolved-blocking-issue.yaml`

```yaml
id: QF-PUB-003
name: No Unresolved Blocking Issue
dimension: publication
severity: blocker
version: 1.0.0
status: active
requirement: BlockerまたはCritical Failを残したまま公開可能判定しない。
evaluation_method: deterministic_or_model_assisted
pass_condition: 重大Issueがすべて解消されている。
fail_condition: 重大Issueが残るのにpublish_readyである。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge:
- KN-PRD-004
- KN-FAC-004
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```

---

## Source: `quality/rules/publication/QF-PUB-004-additional-editing-not-required.yaml`

```yaml
id: QF-PUB-004
name: Additional Editing Not Required
dimension: publication
severity: critical
version: 1.0.0
status: active
requirement: 標準成果物は利用者の追加編集を前提としない完成状態とする。
evaluation_method: deterministic_or_model_assisted
pass_condition: そのまま公開でき、残る事項はAdvisoryのみである。
fail_condition: 文章・構成・事実の追加修正が必要である。
warning_condition: 判定に必要な情報が不足する場合はunable_to_verifyまたはwarningとする。
auto_fix_eligible: false
manual_review_required: false
related_knowledge:
- KN-PRD-001
related_patterns: []
reviewed_at: '2026-07-17'
next_review_at: '2027-01-17'
```
