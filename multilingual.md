---
title: Multilingual
nav_order: 13
permalink: /multilingual/
---

# Multilingual

| Benchmark | What it actually tells you |
|---|---|
| Global-MMLU | Knowledge/reasoning quality across many languages and locales, with cultural-sensitivity annotations |
| FLORES-200 | Machine translation quality across 200 languages |
| Multilingual MTEB | Embedding/retrieval quality across languages (subset of the MTEB family — see [rag-retrieval](/AI-benchmarks/rag-retrieval/)) |
| MGSM | Grade-school math reasoning translated across languages |

**What it tells you:** Quality across languages/locales — critical when a model's English-language benchmark scores don't reflect performance in the languages your users actually use.

*Track current standings via the aggregators in [core-leaderboards](/AI-benchmarks/core-leaderboards/).*

## When to check this on a new model release

If your product serves non-English users, validate here before trusting English-only benchmark results (Arena, LiveBench, MMLU-Pro, etc.) as representative — a strong English-language release can still underperform in target languages.
