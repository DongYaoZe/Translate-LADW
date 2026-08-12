# Translation provenance policy

This branch (`rebuild-2026-original-only`) is a clean rebuild of the Chinese translation of *Linear Algebra Done Wrong*.

## Authoritative source

The authoritative English content baseline is `../LADW-2026-recovered`, a mechanical TeX reconstruction from Sergei Treil's official LaTeXML HTML for the 2026-04-30 edition. It is **not** represented as the author's original TeX source; it is used as a faithful structural/content reference to the official 2026 text.

## Chinese translation provenance

Chinese prose on this branch must come from one of the following sources only:

1. the pre-merge `V_9.8.6` translation by Dong Yaoze, retained, corrected, or rewritten where appropriate;
2. fresh Chinese translation/revision made directly from the authoritative English source;
3. clearly marked translator notes written for this project.

The independent repository `LADW-cn-main` is **not a text source** for this branch. Its Chinese sentences, paragraph wording, theorem wording, exercise wording, and figure assets must not be copied into the rebuilt text. Knowledge of issues previously discovered through comparison may be used as an audit checklist, but every repair must be re-derived from the authoritative English source.

## Style goal

The final translation should preserve the translator's recognizable voice and useful original notes while improving mathematical accuracy, Chinese fluency, terminology consistency, and maintainability. Originality should come from the Chinese expression and editorial choices, not from deviating from the author's mathematics.

## Final audit

Before release, compare the rebuilt Chinese files against `LADW-cn-main` only as a contamination audit. Unexpected long identical Chinese passages should be manually reviewed and independently retranslated from the English source unless they are unavoidable conventional terminology, formulas, headings, or short stock phrases.

For this clean rebuild, the final audit on 2026-08-13 stripped TeX syntax, mathematics, Latin text, and punctuation, then searched the nine chapter files for contiguous identical Chinese text. After independently rephrasing every flagged passage from the English source, the result was **0 matches of 32 or more consecutive Han characters** against `LADW-cn-main`. The audit report is kept in the parent project at `../tools/cn_overlap_audit.txt`. This is a provenance/contamination check, not a legal opinion about copyright status.
