# 01 Quality Framework and Gates
SEO改善前に品質監査を行い、Quality Gate後に変更範囲を決定するための規則です。

---

## Source: `quality/framework/publish-ready-definition.md`

# Publish Ready Definition

すべての必須Gateを通過し、BlockerおよびCritical Failがなく、重大なUnable to VerifyやPlaceholderが残らず、利用者の追加編集を前提としない状態です。

---

## Source: `quality/framework/quality-dimensions.md`

# Quality Dimensions

Product 1.0ではSafety、Factuality、Search Intent、Completeness、Helpfulness、SEO、Structure、Readability、Japanese Quality、EEAT Support、Original Value、Site Fit、Publication Readinessの13次元を評価します。

---

## Source: `quality/framework/quality-framework-v1.0.md`

# SIMS Writer Quality Framework v1.0

Publish Readyは総合点だけで決めない。

## 必須条件

- Blockerなし
- Critical Failなし
- 必須Gate通過
- Primary Intent達成
- 重大なUnable to Verifyなし
- Placeholderなし
- 日本語として公開可能
- 追加編集を前提としない

## Severity

Blocker / Critical / Major / Minor / Advisory

---

## Source: `quality/gates/draft-gate.yaml`

```yaml
id: QG-DRAFT_GATE
name: draft-gate
version: 1.0.0
status: active
required_rules:
- QF-SAF-001
- QF-SAF-003
- QF-FAC-003
- QF-COM-002
- QF-COM-003
- QF-HLP-001
- QF-HLP-002
- QF-HLP-003
- QF-ORG-001
- QF-ORG-002
- QF-ORG-003
blocker_policy: any_blocker_fail_blocks
critical_policy: any_critical_fail_blocks
allowed_results:
- pass
- warning
- not_applicable
retry_policy: targeted_refinement_then_recheck
manual_review_condition: unable_to_verify on blocker or high-risk rule
```

---

## Source: `quality/gates/evidence-gate.yaml`

```yaml
id: QG-EVIDENCE_GATE
name: evidence-gate
version: 1.0.0
status: active
required_rules:
- QF-FAC-001
- QF-FAC-002
- QF-FAC-004
- QF-EEA-002
- QF-EEA-003
blocker_policy: any_blocker_fail_blocks
critical_policy: any_critical_fail_blocks
allowed_results:
- pass
- warning
- not_applicable
retry_policy: targeted_refinement_then_recheck
manual_review_condition: unable_to_verify on blocker or high-risk rule
```

---

## Source: `quality/gates/final-publication-gate.yaml`

```yaml
id: QG-FINAL_PUBLICATION_GATE
name: final-publication-gate
version: 1.0.0
status: active
required_rules:
- QF-PUB-001
- QF-PUB-002
- QF-PUB-003
- QF-PUB-004
- QF-SIT-002
- QF-SIT-003
blocker_policy: any_blocker_fail_blocks
critical_policy: any_critical_fail_blocks
allowed_results:
- pass
- warning
- not_applicable
retry_policy: targeted_refinement_then_recheck
manual_review_condition: unable_to_verify on blocker or high-risk rule
```

---

## Source: `quality/gates/input-gate.yaml`

```yaml
id: QG-INPUT_GATE
name: input-gate
version: 1.0.0
status: active
required_rules:
- QF-SAF-002
blocker_policy: any_blocker_fail_blocks
critical_policy: any_critical_fail_blocks
allowed_results:
- pass
- warning
- not_applicable
retry_policy: targeted_refinement_then_recheck
manual_review_condition: unable_to_verify on blocker or high-risk rule
```

---

## Source: `quality/gates/language-gate.yaml`

```yaml
id: QG-LANGUAGE_GATE
name: language-gate
version: 1.0.0
status: active
required_rules:
- QF-STR-001
- QF-STR-002
- QF-STR-003
- QF-REA-001
- QF-REA-002
- QF-REA-003
- QF-JPN-001
- QF-JPN-002
- QF-JPN-003
blocker_policy: any_blocker_fail_blocks
critical_policy: any_critical_fail_blocks
allowed_results:
- pass
- warning
- not_applicable
retry_policy: targeted_refinement_then_recheck
manual_review_condition: unable_to_verify on blocker or high-risk rule
```

---

## Source: `quality/gates/planning-gate.yaml`

```yaml
id: QG-PLANNING_GATE
name: planning-gate
version: 1.0.0
status: active
required_rules:
- QF-INT-001
- QF-INT-002
- QF-INT-003
- QF-COM-001
- QF-SEO-004
- QF-SIT-001
blocker_policy: any_blocker_fail_blocks
critical_policy: any_critical_fail_blocks
allowed_results:
- pass
- warning
- not_applicable
retry_policy: targeted_refinement_then_recheck
manual_review_condition: unable_to_verify on blocker or high-risk rule
```

---

## Source: `quality/gates/seo-gate.yaml`

```yaml
id: QG-SEO_GATE
name: seo-gate
version: 1.0.0
status: active
required_rules:
- QF-SEO-001
- QF-SEO-002
- QF-SEO-003
- QF-SEO-004
blocker_policy: any_blocker_fail_blocks
critical_policy: any_critical_fail_blocks
allowed_results:
- pass
- warning
- not_applicable
retry_policy: targeted_refinement_then_recheck
manual_review_condition: unable_to_verify on blocker or high-risk rule
```

---

## Source: `quality/scoring/scoring-model.md`

# Scoring Model

スコアは補助指標です。Blocker/CriticalとGate判定を優先し、総合点だけでPublish Readyを決定しません。

---

## Source: `quality/scoring/severity-policy.md`

# Severity Policy

- blocker: 公開禁止
- critical: 原則公開不可
- major: 明確な修正が必要
- minor: 軽微な改善
- advisory: 任意の推奨
