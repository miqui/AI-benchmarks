---
title: Pitfalls
nav_order: 16
---

# Practical cautions & pitfalls

No leaderboard is definitive. Keep these in mind whenever a number looks too clean.

## Contamination

Benchmarks whose test sets leak into training data (directly or via near-duplicate web content) inflate scores without reflecting real capability gains. Prefer fresh, time-controlled/contamination-resistant benchmarks (LiveBench, LiveCodeBench) for current signal over older, more saturated sets (classic HumanEval/MBPP, GSM8K).

## Self-reported scores

Many leaderboard entries are vendor-submitted, not independently reproduced. Vendors can optimize for benchmarks specifically (prompt tuning, scaffold tuning, selective reporting). Always check whether a score is independently verified before treating it as ground truth.

## Composite-rank caution

Avoid composite "best model" boards as primary truth — a single blended ranking encodes *someone else's* weighting of categories that may not match your priorities (example: artificialwatch.com/benchmarks normalizes ranks from several boards into one index). Prefer category-specific boards relevant to your actual use case.

## Harness confounds

Agentic benchmarks (SWE-bench, Bug Hunt Bench, Terminal-Bench, GAIA, tau-bench) rank a **model + harness + effort/reasoning-level + tool access + retry policy + compute budget** combination, not a pure foundation-model capability. Two entries using the same base model but different harnesses or effort settings are not comparable. See [coding-agents](coding-agents.html) for the detailed Bug Hunt Bench example.

## "5th place can win in production"

A model ranked 5th on a capability leaderboard can be the best production choice once you weight:
- JSON/schema adherence
- p95 latency
- stable tool calling
- data handling and context window fit
- cost per *successful* workflow (not just cost per token)

Triangulate: human preference ([core-leaderboards](core-leaderboards.html)) + fresh contamination-resistant tests ([general-reasoning](general-reasoning.html)) + real agent evals ([tool-use-agents](tool-use-agents.html), [coding-agents](coding-agents.html)) + multimodal ([multimodal](multimodal.html)) + deployment economics ([efficiency-economics](efficiency-economics.html)) — then run your own internal release gate (step 4 of [release-review-workflow](release-review-workflow.html)) before trusting any single board's ranking for a production decision.
