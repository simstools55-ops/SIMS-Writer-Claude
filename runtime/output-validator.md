# Output Validator

出力直前に以下をYES/NOで内部確認します。

- ArticleIDは一致しているか。
- URLは一致しているか。
- 依頼モードに従っているか。
- 改善後タイトルは検索意図を維持しているか。
- protected_elementsを壊していないか。
- Change Budget内か。
- Before/Afterは対応しているか。
- 全文の冒頭と末尾があるか。
- 英語分析文がないか。
- JSONはSchemaに従うか。

1つでも重大なNOがあればQuality Gateへ戻します。
