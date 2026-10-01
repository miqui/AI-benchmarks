---
title: General Reasoning
nav_order: 4
---

# General reasoning & knowledge

| Benchmark | What it actually tells you | Caveat |
|---|---|---|
| MMLU-Pro | Difficult knowledge/reasoning across broad subject areas | Not production-domain accuracy |
| GPQA Diamond | Graduate-level, expert-written science reasoning | Not production-domain accuracy |
| SimpleBench | Simple-seeming but model-breaking common-sense reasoning | Narrow by design; use alongside broader boards |
| Humanity's Last Exam (HLE) | Extremely hard, broad-domain frontier knowledge/reasoning probe | Difficult knowledge/reasoning; not production-domain accuracy |
| LiveBench | Fresh, contamination-resistant general capability across reasoning, math, coding, language, data analysis | Frequently refreshed questions — best used for cross-model relative ranking rather than absolute score tracking over time |

*The source material lists these benchmark names without dedicated individual URLs; track them via the aggregators in [core-leaderboards](core-leaderboards.html) (Artificial Analysis, BenchLM, llm-stats.com) or via LiveBench directly: [https://livebench.ai*](https://livebench.ai*)

## When to check this on a new model release

Step 2 of the [release-review-workflow](release-review-workflow.html) for a "general" release: LiveBench + GPQA Diamond/MMLU-Pro. Useful as a first filter before task-specific validation (coding, multimodal, agents, etc.) — see [pitfalls](pitfalls.html) on why a high score here doesn't predict production performance.
