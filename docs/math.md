---
title: Math
nav_order: 5
---

# Math & formal reasoning

| Benchmark | What it actually tells you | Caveat |
|---|---|---|
| AIME | Competition-level math problem solving | Symbolic/contest problem solving; less predictive of tool-using workflows |
| HMMT | Harder competition math (Harvard-MIT Math Tournament) | Same as AIME — contest style, not workflow-predictive |
| MATH-500 | Curated hard math problem subset | Symbolic reasoning depth, not applied/agentic math |
| GSM8K | Grade-school arithmetic word problems | Largely saturated by frontier models; low signal for differentiating top models today |

*Track current standings via the aggregators in [core-leaderboards](core-leaderboards.html) and LiveBench's math slice: https://livebench.ai*

## When to check this on a new model release

Check if the release targets reasoning/math capability explicitly, or if your workload includes quantitative/symbolic tasks. Treat strong math scores as necessary-not-sufficient: pair with [coding-agents](coding-agents.html) or [tool-use-agents](tool-use-agents.html) if the real task involves using math inside a larger workflow (per [pitfalls](pitfalls.html), contest math doesn't predict tool-using performance).
