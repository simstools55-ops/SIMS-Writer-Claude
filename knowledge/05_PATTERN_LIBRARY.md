# 05 Pattern Library
記事タイプ、改善、SEO、根拠、品質回復、セクション設計のPattern Libraryです。

---

## Source: `patterns/sets/product-1.0-pattern-library.md`

# Pattern Library v1.0

- targeted_title_revision: 内容を維持したタイトル改善
- introduction_alignment: 検索意図と導入の整合
- heading_relabel: 本文を変えない見出し明確化
- faq_from_existing_content: 既存情報のFAQ再整理
- stop_and_rewrite: 重大前提誤り時の全面再構成

PatternはQuality Gate後にのみ選択します。

---

## Source: `patterns/policies/conflict-resolution.md`

# Pattern Conflict Resolution

競合時はSafety、Factuality、Decision Evidence、Site Rule、Article Typeの順で解決します。未解決の場合はmanual_reviewへ送ります。

---

## Source: `patterns/policies/decision-pattern-mapping.md`

# Decision to Pattern Mapping

Pattern SelectionはDecision結果を前提とします。Patternを先に選び、後から変更理由を作ることは禁止します。

- no_change / preserve: 原則Patternなし
- revise / add / remove / verify: 対応Patternを選択
- separate_article: Planning Patternのみ
- manual_review / reject: Production Patternを停止

---

## Source: `patterns/policies/selection-policy.md`

# Pattern Selection Policy

1. Decision Action PlanにactionがあるComponentのみ候補化する。
2. no_change、preserve、deferの対象には生成Patternを適用しない。
3. Safety、Evidence、Primary Intent、改善目的、Sectionの順で優先する。
4. Non-Applicabilityまたは入力不足の場合は選択しない。
5. 選択理由とPattern Versionを記録する。

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-001-keyword-stuffing.yaml`

```yaml
{
  "id": "PT-ANT-001",
  "name": "Keyword Stuffing",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "キーワードを不自然に詰め込む",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEO-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEO-001"
  ],
  "related_knowledge": [
    "KN-SEO-002"
  ],
  "related_quality_rules": [
    "QF-SEO-002"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-002-competitor-heading-copy.yaml`

```yaml
{
  "id": "PT-ANT-002",
  "name": "Competitor Heading Copy",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "競合見出しをそのまま模倣する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-002"
  ],
  "related_knowledge": [
    "KN-CDS-003"
  ],
  "related_quality_rules": [
    "QF-ORG-002"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-003-faq-inflation.yaml`

```yaml
{
  "id": "PT-ANT-003",
  "name": "FAQ Inflation",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "必要性なくFAQを増やす",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-FAQ-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-FAQ-001"
  ],
  "related_knowledge": [
    "KN-WRI-005"
  ],
  "related_quality_rules": [
    "QF-REA-003"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-004-full-rewrite-without-evaluation.yaml`

```yaml
{
  "id": "PT-ANT-004",
  "name": "Full Rewrite Without Evaluation",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "評価なしで全文書き換えする",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-002"
  ],
  "related_knowledge": [
    "KN-OPS-001"
  ],
  "related_quality_rules": [
    "QF-SIT-002"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-005-year-update-without-evidence.yaml`

```yaml
{
  "id": "PT-ANT-005",
  "name": "Year Update Without Evidence",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "根拠なく年号だけ更新する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-001"
  ],
  "related_quality_rules": [
    "QF-FAC-001"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-006-generic-introduction.yaml`

```yaml
{
  "id": "PT-ANT-006",
  "name": "Generic Introduction",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "どの記事にも使える一般論で始める",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-001"
  ],
  "related_knowledge": [
    "KN-WRI-001"
  ],
  "related_quality_rules": [
    "QF-INT-002"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-007-excessive-bullet-lists.yaml`

```yaml
{
  "id": "PT-ANT-007",
  "name": "Excessive Bullet Lists",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "説明が必要な箇所まで箇条書きにする",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-002"
  ],
  "related_knowledge": [
    "KN-WRI-002"
  ],
  "related_quality_rules": [
    "QF-REA-001"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-008-fabricated-experience.yaml`

```yaml
{
  "id": "PT-ANT-008",
  "name": "Fabricated Experience",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "未経験の内容を体験談として書く",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-004"
  ],
  "related_quality_rules": [
    "QF-ORG-003"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-009-all-queries-in-one-article.yaml`

```yaml
{
  "id": "PT-ANT-009",
  "name": "All Queries in One Article",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "全クエリを1記事へ詰め込む",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEP-001"
  ],
  "related_knowledge": [
    "KN-CDS-003"
  ],
  "related_quality_rules": [
    "QF-INT-003"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/anti_pattern/PT-ANT-010-prompt-only-quality-rule.yaml`

```yaml
{
  "id": "PT-ANT-010",
  "name": "Prompt-Only Quality Rule",
  "category": "anti_pattern",
  "version": "1.0.0",
  "status": "active",
  "problem": "品質ルールをPromptだけに保持する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-PUB-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "detect_condition",
    "block_or_warn",
    "apply_alternative_pattern"
  ],
  "expected_outputs": [
    "prohibition_record"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-PUB-001"
  ],
  "related_knowledge": [
    "KN-PRD-002"
  ],
  "related_quality_rules": [
    "QF-PUB-003"
  ],
  "risks": [
    "quality_degradation"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/article/PT-ART-001-how-to-article.yaml`

```yaml
{
  "id": "PT-ART-001",
  "name": "How-to Article",
  "category": "article",
  "version": "1.0.0",
  "status": "active",
  "problem": "手順記事で実行順序が不明確になる。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "article_structure"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-WRI-003"
  ],
  "related_quality_rules": [
    "QF-HLP-001",
    "QF-COM-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/article/PT-ART-002-troubleshooting-article.yaml`

```yaml
{
  "id": "PT-ART-002",
  "name": "Troubleshooting Article",
  "category": "article",
  "version": "1.0.0",
  "status": "active",
  "problem": "原因切り分けと復旧手順が混在する。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "article_structure"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-CDS-001",
    "KN-FAC-003"
  ],
  "related_quality_rules": [
    "QF-HLP-003",
    "QF-SAF-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/article/PT-ART-003-comparison-article.yaml`

```yaml
{
  "id": "PT-ART-003",
  "name": "Comparison Article",
  "category": "article",
  "version": "1.0.0",
  "status": "active",
  "problem": "比較軸がないまま候補を列挙する。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "article_structure"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-CDS-002"
  ],
  "related_quality_rules": [
    "QF-HLP-002",
    "QF-STR-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/article/PT-ART-004-definition-article.yaml`

```yaml
{
  "id": "PT-ART-004",
  "name": "Definition Article",
  "category": "article",
  "version": "1.0.0",
  "status": "active",
  "problem": "定義記事が一般論だけになる。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "article_structure"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-WRI-002"
  ],
  "related_quality_rules": [
    "QF-INT-002",
    "QF-HLP-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/article/PT-ART-005-cost-article.yaml`

```yaml
{
  "id": "PT-ART-005",
  "name": "Cost Article",
  "category": "article",
  "version": "1.0.0",
  "status": "active",
  "problem": "費用記事で前提条件や計算根拠が欠ける。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "article_structure"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-FAC-002"
  ],
  "related_quality_rules": [
    "QF-FAC-002",
    "QF-HLP-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/article/PT-ART-006-cause-and-solution-article.yaml`

```yaml
{
  "id": "PT-ART-006",
  "name": "Cause and Solution Article",
  "category": "article",
  "version": "1.0.0",
  "status": "active",
  "problem": "原因と解決策の対応関係が不明になる。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "article_structure"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-WRI-003"
  ],
  "related_quality_rules": [
    "QF-STR-003",
    "QF-HLP-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/article/PT-ART-007-settings-guide.yaml`

```yaml
{
  "id": "PT-ART-007",
  "name": "Settings Guide",
  "category": "article",
  "version": "1.0.0",
  "status": "active",
  "problem": "設定案内で画面順序や注意事項が欠ける。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "article_structure"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-WRI-003",
    "KN-FAC-003"
  ],
  "related_quality_rules": [
    "QF-HLP-001",
    "QF-SAF-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/evidence/PT-EVD-001-official-source-first.yaml`

```yaml
{
  "id": "PT-EVD-001",
  "name": "Official Source First",
  "category": "evidence",
  "version": "1.0.0",
  "status": "active",
  "problem": "重要事実を非公式情報だけで判断する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "source_selection"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-001"
  ],
  "related_quality_rules": [
    "QF-FAC-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/evidence/PT-EVD-002-time-sensitive-fact-verification.yaml`

```yaml
{
  "id": "PT-EVD-002",
  "name": "Time-Sensitive Fact Verification",
  "category": "evidence",
  "version": "1.0.0",
  "status": "active",
  "problem": "変化する情報を確認せず最新と断定する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "verified_claims"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-001"
  ],
  "related_quality_rules": [
    "QF-FAC-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/evidence/PT-EVD-003-numeric-claim-verification.yaml`

```yaml
{
  "id": "PT-EVD-003",
  "name": "Numeric Claim Verification",
  "category": "evidence",
  "version": "1.0.0",
  "status": "active",
  "problem": "数値や計算の根拠がない",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "verified_numbers"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-002"
  ],
  "related_quality_rules": [
    "QF-FAC-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/evidence/PT-EVD-004-fact-and-opinion-separation.yaml`

```yaml
{
  "id": "PT-EVD-004",
  "name": "Fact and Opinion Separation",
  "category": "evidence",
  "version": "1.0.0",
  "status": "active",
  "problem": "経験や推測を事実として表現する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "claim_classification"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-004"
  ],
  "related_quality_rules": [
    "QF-FAC-004"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/evidence/PT-EVD-005-unable-to-verify-handling.yaml`

```yaml
{
  "id": "PT-EVD-005",
  "name": "Unable-to-Verify Handling",
  "category": "evidence",
  "version": "1.0.0",
  "status": "active",
  "problem": "確認不能事項を推測で埋める",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001",
      "DEC-PUB-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "unverified_action"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001",
    "DEC-PUB-001"
  ],
  "related_knowledge": [
    "KN-FAC-003"
  ],
  "related_quality_rules": [
    "QF-PUB-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/evidence/PT-EVD-006-experience-claim-labeling.yaml`

```yaml
{
  "id": "PT-EVD-006",
  "name": "Experience Claim Labeling",
  "category": "evidence",
  "version": "1.0.0",
  "status": "active",
  "problem": "存在しない体験を創作する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "experience_claims"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-004"
  ],
  "related_quality_rules": [
    "QF-EEA-001",
    "QF-ORG-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/improvement/PT-IMP-001-preserve-and-revise.yaml`

```yaml
{
  "id": "PT-IMP-001",
  "name": "Preserve and Revise",
  "category": "improvement",
  "version": "1.0.0",
  "status": "active",
  "problem": "有効要素を残さず全面置換する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "improvement_plan"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-001"
  ],
  "related_knowledge": [
    "KN-OPS-001"
  ],
  "related_quality_rules": [
    "QF-SIT-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/improvement/PT-IMP-002-targeted-revision-before-full-rewrite.yaml`

```yaml
{
  "id": "PT-IMP-002",
  "name": "Targeted Revision Before Full Rewrite",
  "category": "improvement",
  "version": "1.0.0",
  "status": "active",
  "problem": "部分修正で足りるのに全文改稿する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "targeted_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-002"
  ],
  "related_knowledge": [
    "KN-OPS-002"
  ],
  "related_quality_rules": [
    "QF-PUB-004"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/improvement/PT-IMP-003-outdated-information-refresh.yaml`

```yaml
{
  "id": "PT-IMP-003",
  "name": "Outdated Information Refresh",
  "category": "improvement",
  "version": "1.0.0",
  "status": "active",
  "problem": "古い情報の更新範囲が不明確",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001",
      "DEC-IMP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "fact_update_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001",
    "DEC-IMP-001"
  ],
  "related_knowledge": [
    "KN-FAC-001"
  ],
  "related_quality_rules": [
    "QF-FAC-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/improvement/PT-IMP-004-content-gap-completion.yaml`

```yaml
{
  "id": "PT-IMP-004",
  "name": "Content Gap Completion",
  "category": "improvement",
  "version": "1.0.0",
  "status": "active",
  "problem": "不足情報を無制限に追加する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "content_gap_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-001"
  ],
  "related_knowledge": [
    "KN-CDS-001"
  ],
  "related_quality_rules": [
    "QF-COM-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/improvement/PT-IMP-005-heading-reorganization.yaml`

```yaml
{
  "id": "PT-IMP-005",
  "name": "Heading Reorganization",
  "category": "improvement",
  "version": "1.0.0",
  "status": "active",
  "problem": "見出しだけを競合記事に合わせて変更する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "heading_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-002"
  ],
  "related_knowledge": [
    "KN-WRI-004"
  ],
  "related_quality_rules": [
    "QF-STR-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/improvement/PT-IMP-006-introduction-replacement.yaml`

```yaml
{
  "id": "PT-IMP-006",
  "name": "Introduction Replacement",
  "category": "improvement",
  "version": "1.0.0",
  "status": "active",
  "problem": "導入だけの問題を全文改稿で解決する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "introduction_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-001"
  ],
  "related_knowledge": [
    "KN-WRI-001"
  ],
  "related_quality_rules": [
    "QF-INT-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/improvement/PT-IMP-007-faq-addition-or-reduction.yaml`

```yaml
{
  "id": "PT-IMP-007",
  "name": "FAQ Addition or Reduction",
  "category": "improvement",
  "version": "1.0.0",
  "status": "active",
  "problem": "FAQを常に追加する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-FAQ-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "faq_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-FAQ-001"
  ],
  "related_knowledge": [
    "KN-WRI-005"
  ],
  "related_quality_rules": [
    "QF-REA-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/improvement/PT-IMP-008-metadata-only-improvement.yaml`

```yaml
{
  "id": "PT-IMP-008",
  "name": "Metadata-Only Improvement",
  "category": "improvement",
  "version": "1.0.0",
  "status": "active",
  "problem": "本文変更不要なのに本文まで改稿する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEO-001",
      "DEC-SEO-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "metadata_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEO-001",
    "DEC-SEO-002"
  ],
  "related_knowledge": [
    "KN-SEO-003"
  ],
  "related_quality_rules": [
    "QF-SEO-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/planning/PT-PLN-001-primary-intent-identification.yaml`

```yaml
{
  "id": "PT-PLN-001",
  "name": "Primary Intent Identification",
  "category": "planning",
  "version": "1.0.0",
  "status": "active",
  "problem": "主要検索意図を明確にせず構成へ進む。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "search_intent_model"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-SEO-001",
    "KN-CDS-001"
  ],
  "related_quality_rules": [
    "QF-INT-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/planning/PT-PLN-002-main-answer-definition.yaml`

```yaml
{
  "id": "PT-PLN-002",
  "name": "Main Answer Definition",
  "category": "planning",
  "version": "1.0.0",
  "status": "active",
  "problem": "記事の中心回答が曖昧になる。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "main_answer"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-SEO-002",
    "KN-CDS-002"
  ],
  "related_quality_rules": [
    "QF-INT-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/planning/PT-PLN-003-content-scope-boundary.yaml`

```yaml
{
  "id": "PT-PLN-003",
  "name": "Content Scope Boundary",
  "category": "planning",
  "version": "1.0.0",
  "status": "active",
  "problem": "関連意図を広げすぎて主題がぼやける。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001",
      "DEC-SEP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "content_scope",
    "out_of_scope"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001",
    "DEC-SEP-001"
  ],
  "related_knowledge": [
    "KN-CDS-003"
  ],
  "related_quality_rules": [
    "QF-INT-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/planning/PT-PLN-004-required-content-mapping.yaml`

```yaml
{
  "id": "PT-PLN-004",
  "name": "Required Content Mapping",
  "category": "planning",
  "version": "1.0.0",
  "status": "active",
  "problem": "必要情報の抜けが発生する。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "content_requirements"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-CDS-001"
  ],
  "related_quality_rules": [
    "QF-COM-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/planning/PT-PLN-005-existing-value-identification.yaml`

```yaml
{
  "id": "PT-PLN-005",
  "name": "Existing Value Identification",
  "category": "planning",
  "version": "1.0.0",
  "status": "active",
  "problem": "既存記事の強い要素を誤って削除する。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-001",
      "DEC-IMP-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "preserve_inventory"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-001",
    "DEC-IMP-002"
  ],
  "related_knowledge": [
    "KN-OPS-001",
    "KN-OPS-002"
  ],
  "related_quality_rules": [
    "QF-SIT-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/planning/PT-PLN-006-evidence-planning.yaml`

```yaml
{
  "id": "PT-PLN-006",
  "name": "Evidence Planning",
  "category": "planning",
  "version": "1.0.0",
  "status": "active",
  "problem": "確認すべき事実を生成後まで特定しない。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "evidence_plan"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-001",
    "KN-FAC-002"
  ],
  "related_quality_rules": [
    "QF-FAC-001",
    "QF-FAC-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/planning/PT-PLN-007-separate-article-intent-detection.yaml`

```yaml
{
  "id": "PT-PLN-007",
  "name": "Separate Article Intent Detection",
  "category": "planning",
  "version": "1.0.0",
  "status": "active",
  "problem": "別記事向け意図を同一記事に混在させる。",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "separate_article_candidates"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEP-001"
  ],
  "related_knowledge": [
    "KN-SEO-005",
    "KN-CDS-003"
  ],
  "related_quality_rules": [
    "QF-INT-003",
    "QF-SEO-004"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/quality_recovery/PT-QRC-001-primary-intent-recovery.yaml`

```yaml
{
  "id": "PT-QRC-001",
  "name": "Primary Intent Recovery",
  "category": "quality_recovery",
  "version": "1.0.0",
  "status": "active",
  "problem": "初稿が主要意図を満たさない",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "revised_content_plan"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-SEO-001"
  ],
  "related_quality_rules": [
    "QF-INT-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/quality_recovery/PT-QRC-002-unsupported-claim-removal.yaml`

```yaml
{
  "id": "PT-QRC-002",
  "name": "Unsupported Claim Removal",
  "category": "quality_recovery",
  "version": "1.0.0",
  "status": "active",
  "problem": "根拠のない主張が残る",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "claim_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-001"
  ],
  "related_quality_rules": [
    "QF-FAC-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/quality_recovery/PT-QRC-003-structure-simplification.yaml`

```yaml
{
  "id": "PT-QRC-003",
  "name": "Structure Simplification",
  "category": "quality_recovery",
  "version": "1.0.0",
  "status": "active",
  "problem": "構造が複雑で要点が分散する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "structure_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-002"
  ],
  "related_knowledge": [
    "KN-WRI-004"
  ],
  "related_quality_rules": [
    "QF-STR-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/quality_recovery/PT-QRC-004-redundancy-reduction.yaml`

```yaml
{
  "id": "PT-QRC-004",
  "name": "Redundancy Reduction",
  "category": "quality_recovery",
  "version": "1.0.0",
  "status": "active",
  "problem": "同じ説明が繰り返される",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "redundancy_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-001"
  ],
  "related_knowledge": [
    "KN-WRI-002"
  ],
  "related_quality_rules": [
    "QF-REA-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/quality_recovery/PT-QRC-005-japanese-naturalization.yaml`

```yaml
{
  "id": "PT-QRC-005",
  "name": "Japanese Naturalization",
  "category": "quality_recovery",
  "version": "1.0.0",
  "status": "active",
  "problem": "日本語が直訳調・AI調になる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "language_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-001"
  ],
  "related_knowledge": [
    "KN-WRI-002"
  ],
  "related_quality_rules": [
    "QF-JPN-001",
    "QF-JPN-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/quality_recovery/PT-QRC-006-faq-de-duplication.yaml`

```yaml
{
  "id": "PT-QRC-006",
  "name": "FAQ De-Duplication",
  "category": "quality_recovery",
  "version": "1.0.0",
  "status": "active",
  "problem": "FAQが本文と重複する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-FAQ-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "faq_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-FAQ-001"
  ],
  "related_knowledge": [
    "KN-WRI-005"
  ],
  "related_quality_rules": [
    "QF-REA-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/quality_recovery/PT-QRC-007-title-body-alignment-recovery.yaml`

```yaml
{
  "id": "PT-QRC-007",
  "name": "Title-Body Alignment Recovery",
  "category": "quality_recovery",
  "version": "1.0.0",
  "status": "active",
  "problem": "タイトルの約束と本文が一致しない",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEO-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "title_or_body_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEO-001"
  ],
  "related_knowledge": [
    "KN-SEO-002"
  ],
  "related_quality_rules": [
    "QF-SEO-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/quality_recovery/PT-QRC-008-existing-value-restoration.yaml`

```yaml
{
  "id": "PT-QRC-008",
  "name": "Existing Value Restoration",
  "category": "quality_recovery",
  "version": "1.0.0",
  "status": "active",
  "problem": "改善後に元記事の価値が失われる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "restoration_patch"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-001"
  ],
  "related_knowledge": [
    "KN-OPS-001"
  ],
  "related_quality_rules": [
    "QF-SIT-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/section/PT-SEC-001-answer-first-introduction.yaml`

```yaml
{
  "id": "PT-SEC-001",
  "name": "Answer-First Introduction",
  "category": "section",
  "version": "1.0.0",
  "status": "active",
  "problem": "導入で結論が遅れる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "introduction"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-001"
  ],
  "related_knowledge": [
    "KN-WRI-001"
  ],
  "related_quality_rules": [
    "QF-INT-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/section/PT-SEC-002-problem-recognition-introduction.yaml`

```yaml
{
  "id": "PT-SEC-002",
  "name": "Problem Recognition Introduction",
  "category": "section",
  "version": "1.0.0",
  "status": "active",
  "problem": "読者の状況を無視した導入になる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "introduction"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-001"
  ],
  "related_knowledge": [
    "KN-WRI-001"
  ],
  "related_quality_rules": [
    "QF-HLP-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/section/PT-SEC-003-step-by-step-procedure.yaml`

```yaml
{
  "id": "PT-SEC-003",
  "name": "Step-by-Step Procedure",
  "category": "section",
  "version": "1.0.0",
  "status": "active",
  "problem": "手順の順序や操作単位が曖昧になる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "procedure_section"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-002"
  ],
  "related_knowledge": [
    "KN-WRI-003"
  ],
  "related_quality_rules": [
    "QF-COM-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/section/PT-SEC-004-comparison-criteria.yaml`

```yaml
{
  "id": "PT-SEC-004",
  "name": "Comparison Criteria",
  "category": "section",
  "version": "1.0.0",
  "status": "active",
  "problem": "比較基準が後出しになる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-STR-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "comparison_section"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-STR-002"
  ],
  "related_knowledge": [
    "KN-CDS-002"
  ],
  "related_quality_rules": [
    "QF-HLP-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/section/PT-SEC-005-warning-and-exception.yaml`

```yaml
{
  "id": "PT-SEC-005",
  "name": "Warning and Exception",
  "category": "section",
  "version": "1.0.0",
  "status": "active",
  "problem": "重要な注意や例外が本文に埋もれる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-EVD-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "warning_component"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-EVD-001"
  ],
  "related_knowledge": [
    "KN-FAC-003"
  ],
  "related_quality_rules": [
    "QF-COM-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/section/PT-SEC-006-faq-complement.yaml`

```yaml
{
  "id": "PT-SEC-006",
  "name": "FAQ Complement",
  "category": "section",
  "version": "1.0.0",
  "status": "active",
  "problem": "FAQが本文の言い換えになる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-FAQ-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "faq"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-FAQ-001"
  ],
  "related_knowledge": [
    "KN-WRI-005"
  ],
  "related_quality_rules": [
    "QF-COM-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/section/PT-SEC-007-non-repetitive-conclusion.yaml`

```yaml
{
  "id": "PT-SEC-007",
  "name": "Non-Repetitive Conclusion",
  "category": "section",
  "version": "1.0.0",
  "status": "active",
  "problem": "まとめが本文の反復だけになる",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-IMP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "conclusion"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-IMP-001"
  ],
  "related_knowledge": [
    "KN-WRI-006"
  ],
  "related_quality_rules": [
    "QF-REA-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/section/PT-SEC-008-internal-link-context.yaml`

```yaml
{
  "id": "PT-SEC-008",
  "name": "Internal Link Context",
  "category": "section",
  "version": "1.0.0",
  "status": "active",
  "problem": "内部リンクが脈絡なく挿入される",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-LNK-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "internal_link_context"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-LNK-001"
  ],
  "related_knowledge": [
    "KN-SEO-006"
  ],
  "related_quality_rules": [
    "QF-SIT-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/seo/PT-SEO-001-low-ctr-high-rank-title-improvement.yaml`

```yaml
{
  "id": "PT-SEO-001",
  "name": "Low CTR High Rank Title Improvement",
  "category": "seo",
  "version": "1.0.0",
  "status": "active",
  "problem": "順位に対してCTRが低い記事のタイトル改善",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEO-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "seo_title"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEO-001"
  ],
  "related_knowledge": [
    "KN-SEO-003"
  ],
  "related_quality_rules": [
    "QF-SEO-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/seo/PT-SEO-002-title-and-h1-role-separation.yaml`

```yaml
{
  "id": "PT-SEO-002",
  "name": "Title and H1 Role Separation",
  "category": "seo",
  "version": "1.0.0",
  "status": "active",
  "problem": "SEOタイトルとH1の役割が無意味に重複する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEO-001",
      "DEC-SEO-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "seo_title",
    "h1"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEO-001",
    "DEC-SEO-002"
  ],
  "related_knowledge": [
    "KN-SEO-004"
  ],
  "related_quality_rules": [
    "QF-SEO-001"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/seo/PT-SEO-003-main-query-natural-placement.yaml`

```yaml
{
  "id": "PT-SEO-003",
  "name": "Main Query Natural Placement",
  "category": "seo",
  "version": "1.0.0",
  "status": "active",
  "problem": "主クエリが不自然に反復される",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEO-001",
      "DEC-STR-002"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "query_placement_plan"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEO-001",
    "DEC-STR-002"
  ],
  "related_knowledge": [
    "KN-SEO-002"
  ],
  "related_quality_rules": [
    "QF-SEO-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/seo/PT-SEO-004-supporting-query-coverage.yaml`

```yaml
{
  "id": "PT-SEO-004",
  "name": "Supporting Query Coverage",
  "category": "seo",
  "version": "1.0.0",
  "status": "active",
  "problem": "補助クエリを機械的に見出し化する",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SCP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "supporting_query_map"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SCP-001"
  ],
  "related_knowledge": [
    "KN-SEO-001"
  ],
  "related_quality_rules": [
    "QF-SEO-003"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/seo/PT-SEO-005-cannibalization-separation.yaml`

```yaml
{
  "id": "PT-SEO-005",
  "name": "Cannibalization Separation",
  "category": "seo",
  "version": "1.0.0",
  "status": "active",
  "problem": "既存記事との意図重複を見逃す",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEP-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "cannibalization_action"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEP-001"
  ],
  "related_knowledge": [
    "KN-SEO-005"
  ],
  "related_quality_rules": [
    "QF-SEO-004"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/seo/PT-SEO-006-internal-link-relevance.yaml`

```yaml
{
  "id": "PT-SEO-006",
  "name": "Internal Link Relevance",
  "category": "seo",
  "version": "1.0.0",
  "status": "active",
  "problem": "語句一致だけで内部リンクを選ぶ",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-LNK-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "internal_link_recommendations"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-LNK-001"
  ],
  "related_knowledge": [
    "KN-SEO-006"
  ],
  "related_quality_rules": [
    "QF-SIT-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```

---

## Source: `patterns/definitions/seo/PT-SEO-007-meta-description-intent-summary.yaml`

```yaml
{
  "id": "PT-SEO-007",
  "name": "Meta Description Intent Summary",
  "category": "seo",
  "version": "1.0.0",
  "status": "active",
  "problem": "ディスクリプションが本文価値を表さない",
  "context": "Decision Action Planで当該処理が必要と判定された場合に適用する。",
  "applicability": {
    "decision_results": [
      "DEC-SEO-001"
    ],
    "conditions": [
      "required_inputs_available"
    ]
  },
  "non_applicability": [
    "decision_result_is_no_change",
    "required_inputs_missing"
  ],
  "required_inputs": [
    "writing_request",
    "decision_action_plan",
    "knowledge_assembly"
  ],
  "optional_inputs": [
    "source_content_snapshot",
    "performance_data",
    "site_knowledge"
  ],
  "method": [
    "confirm_decision_evidence",
    "apply_pattern_method",
    "validate_expected_output"
  ],
  "expected_outputs": [
    "meta_description"
  ],
  "quality_criteria": [
    "decision_intent_preserved",
    "related_quality_rules_pass"
  ],
  "related_decisions": [
    "DEC-SEO-001"
  ],
  "related_knowledge": [
    "KN-SEO-002"
  ],
  "related_quality_rules": [
    "QF-PUB-002"
  ],
  "risks": [
    "over_application",
    "context_mismatch"
  ],
  "examples": [
    "golden_case_required"
  ],
  "counterexamples": [
    "no_change_decision"
  ],
  "reviewed_at": "2026-07-17",
  "next_review_at": "2027-01-17",
  "owner": "product-governance"
}
```
