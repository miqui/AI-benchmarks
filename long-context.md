---
title: Long Context
nav_order: 9
permalink: /long-context/
---

# Long context

| Benchmark | What it actually tells you |
|---|---|
| RULER | Synthetic multi-task long-context evaluation across retrieval, aggregation, tracing |
| LongBench v2 | Realistic long-document task suite (QA, summarization, reasoning over long inputs) |
| InfiniteBench | Very-long-context (100K+ token) task suite |
| Needle-in-a-Haystack (NIAH) variants | Synthetic retrieval probes for whether a specific fact can be found in a long input |

**Caveat:** Recall/reasoning with long inputs — synthetic retrieval (especially NIAH) can overstate usable context; a model finding one needle doesn't mean it reasons well across the *whole* long context under real multi-fact, multi-hop conditions.

*Track current standings via the aggregators in [core-leaderboards](/AI-benchmarks/core-leaderboards/).*

## When to check this on a new model release

When the advertised context window increases, or your workload depends on long-document reasoning (not just single-fact retrieval). Validate NIAH-style claims against LongBench v2 or RULER before trusting a long context-window number for multi-hop or aggregation tasks.
