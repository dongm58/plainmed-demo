# PlainMed demo

Interactive demo for **PlainMed**, a COSC 72/272 (Dartmouth, Fall 2026) final project by Michael Dong: plain-language rewrites of Cochrane systematic-review results, with a faithfulness checker that flags sentences a reader should verify against the original.

Live page: https://dongm58.github.io/plainmed-demo/

The page runs entirely from precomputed results in `data.json` (no model runs in the browser).

**Reading aid only, not medical advice.**

## Data and models
- Source abstracts and human plain-language summaries: Cochrane paragraph-level simplification dataset, Devaraj et al. (2021), NAACL, released under CC BY 4.0. The underlying text belongs to Cochrane and is used here for non-commercial research.
- Rewrites: Qwen/Qwen2.5-3B-Instruct (Qwen Research License), plus an extractive baseline.
- Checker: MoritzLaurer/DeBERTa-v3-base-mnli-fever-anli plus a rule for numbers not in the source.
