# 08 SIMS Feedback Contract v2.1
SIMS Feedback JSON v2.1、reason codes、warning codes、v1互換仕様です。

---

## Source: `contracts/sims-feedback/v2.1/README.md`

# SIMS Feedback JSON Contract v2.1

本文出力と同一のRuntime Stateから生成する機械処理用契約です。`decision`が変更範囲を支配し、重大な前提誤りは`stop_and_rewrite`になります。

## v1互換

v1.x入力は受理し、既存フィールドを`legacy`へ保持しながらv2.1へ正規化します。推定・警告・理由を混同せず、未知フィールドは黙って破棄しません。

---

## Source: `contracts/sims-feedback/v2.1/v1-compatibility.md`

# v1 Compatibility Specification

- `format: SIMS_FEEDBACK_V1` は `SIMS_FEEDBACK` に正規化する。
- `version: 1.0|1.1|1.2` は `2.1` に変換する。
- v1の原値は `legacy` に保持する。
- v2.1必須値が導出不能なら `manual_review_required` とする。
- 互換変換時は `LEGACY_FIELD_MAPPED` をwarning codesへ追加する。
