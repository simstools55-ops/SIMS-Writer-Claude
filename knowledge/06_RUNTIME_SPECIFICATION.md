# 06 Runtime Specification
Quality AuditからPublication PackagingまでのRuntime順序と状態管理です。本文とJSONは同じRuntime Stateから生成します。

---

## Source: `runtime/overview/runtime-core-v1.0.md`

# SIMS Writer Runtime Core v1.0

## 責務
- 入力を内部Requestへ正規化する
- Repository資産のVersionを固定する
- Decision Action Planを経てPatternを選択する
- Stage状態とエラーを記録する
- Quality Gateに基づき公開状態を制御する

## 非責務
- Knowledge・Pattern・Quality Ruleの意味を独自に変更しない
- 特定LLMの都合をProduct Coreへ持ち込まない
- Alpha段階で公開品質の記事生成を装わない

---

## Source: `runtime/orchestration/orchestrator-specification.md`

# Orchestrator Specification

OrchestratorはStage順序、状態、再試行、停止、再開地点を管理します。正式KnowledgeやQuality判断の内容は保持しません。

- Blocked Stageの後続は実行しない
- Execution中の資産Versionは固定する
- 同一Requestの再実行は新しいexecution_idを付与する
- Errorは共通Error Contractへ変換する

---

## Source: `runtime/context/runtime-context-policy.md`

# Runtime Context Policy

優先順はOutput Contract、Safety、Primary Intent、Decision Action Plan、必須Knowledge、必須Pattern、Source Content、補助情報です。必須資産を削ってContext上限へ合わせてはなりません。

---

## Source: `runtime/pipeline/01-intake.md`

# Stage 1: Intake

## 目的
外部入力を不変Snapshotとして受信する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/02-normalization.md`

# Stage 2: Normalization

## 目的
外部入力をWriting Requestへ正規化する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/03-source_acquisition.md`

# Stage 3: Source Acquisition

## 目的
既存記事と根拠Sourceの取得状態を記録する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/04-knowledge_assembly.md`

# Stage 4: Knowledge Assembly

## 目的
Requestに必要なKnowledgeを選択する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/05-content_planning.md`

# Stage 5: Content Planning

## 目的
検索意図・範囲・構造を計画する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/06-decision_evaluation.md`

# Stage 6: Decision Evaluation

## 目的
変更要否と対象Componentを決定する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/07-pattern_selection.md`

# Stage 7: Pattern Selection

## 目的
Decision Action Planに必要なPatternだけを選択する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/08-content_production.md`

# Stage 8: Content Production

## 目的
Model Adapterを通じてDraftを生成する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/09-quality_validation.md`

# Stage 9: Quality Validation

## 目的
Quality RuleとGateでDraftを評価する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/10-refinement.md`

# Stage 10: Refinement

## 目的
Issueに対し対象限定の修正を行う。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/pipeline/11-publication_packaging.md`

# Stage 11: Publication Packaging

## 目的
最終成果物と公開判定を構造化する。

## 状態
`pending / running / passed / passed_with_warning / failed / blocked / skipped / manual_review_required`

## 原則
入力と出力はContractで検証し、失敗を正常完了として扱いません。

---

## Source: `runtime/policies/asset-version-lock-policy.md`

# Asset Version Lock Policy

Execution開始時にContract、Knowledge、Decision、Pattern、Quality、RuntimeのVersion一覧をManifestへ固定します。実行途中のRepository変更を混在させません。

---

## Source: `runtime/policies/manual-review-policy.md`

# Manual Review Policy

`manual_review_required`は、安全性、YMYL相当の重大判断、重大な事実確認不足、出力契約の解消不能な競合、Blocker残存など、人手確認なしでは成果物を安全に提示できない場合に限定します。

次の不足だけでは処理全体を停止しません。

- `main_query`不足：タイトル等から推定し、推定不能ならクエリ依存処理だけを保留してWarning
- `article_catalog`不足：内部リンク候補選定だけをSKIP
- 外部Source取得不能：既存入力で改善可能な項目を継続しWarning

任意入力や補助データの不足はGraceful Degradationで処理し、fatal errorへ昇格させません。

---

## Source: `runtime/policies/retry-policy.md`

# Retry Policy

一時障害・Schema欠落・出力Component欠落のみ再試行可能です。入力不足、未対応Version、安全上の停止は再試行しません。Alphaでは各Stage最大1回です。
