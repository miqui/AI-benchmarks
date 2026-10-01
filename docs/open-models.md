---
title: Open Models
nav_order: 3
---

# Open models

| Benchmark | What it actually tells you | Link |
|---|---|---|
| Hugging Face Open LLM Leaderboard | Standardized harness results across open-weight models; the essential reference for self-hostable candidates. | https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard |

## Open-weight guidance

- Open-weight models need the same triangulation as closed models: don't trust a single composite score. Cross-check against [core-leaderboards](core-leaderboards.html) (Arena, LiveBench, Artificial Analysis) which include open models alongside frontier ones.
- Self-hostability changes the economics calculus — pair leaderboard results with [efficiency-economics](efficiency-economics.html) (your own load tests, hosting cost, throughput) rather than relying on hosted-API pricing comparisons.
- Licensing and fine-tunability matter as much as raw score for open models; the leaderboard doesn't capture license terms — check them separately per model card.

## When to check this on a new model release

When the release is open-weight (or you're evaluating self-hosting), use this leaderboard for a standardized comparison point, then validate with [general-reasoning](general-reasoning.html), [coding-agents](coding-agents.html), or whichever capability page matches your use case, plus your own release gate (step 4 of [release-review-workflow](release-review-workflow.html)).
