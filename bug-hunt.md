---
title: Bug Hunt Bench
nav_order: 7
permalink: /bug-hunt/
---

# Bug Hunt Bench

Autonomous bug discovery and repair: the agent gets repositories **without being told what's wrong** and must find and fix planted bugs.

## What it evaluates

| Aspect | Detail |
|---|---|
| Task | One agentic round per repository to find and fix **105 planted bugs** across two production TypeScript codebases |
| Grading | Submitted diffs graded blindly against a withheld answer key |
| Leaderboard records | Agent harness, effort setting, number of runs, bugs fixed, per-repository result, extra fixes, wall time, cost, evaluation date |
| Links | [Official leaderboard](https://skillsllm.com/skill/bug-hunt-bench) · [mirror on BenchLM](https://benchlm.ai/benchmarks/bug-hunt-bench) |

## Why it is distinct from [SWE-bench](/AI-benchmarks/coding-agents/)

SWE-bench starts from a real issue description: the agent knows the task it must solve. Bug Hunt asks the agent to inspect a production codebase and locate hidden defects — it exercises several production-relevant behaviors SWE-bench underweights:

- Reading architecture and tracing execution paths without an issue-specific roadmap.
- Turning signals — tests, static analysis, suspicious code, CLI output — into debugging hypotheses.
- Choosing which suspected defects to pursue under a limited run budget.
- Avoiding speculative or low-value changes.
- Producing a correct patch that satisfies hidden evaluation criteria.

For an internal "autonomous repo health" or proactive maintenance agent, Bug Hunt is the closest public analogue.

## Caveats

- **Narrow coverage:** only two TypeScript repositories — a valuable but limited signal. Don't generalize a Bug Hunt ranking to your stack.
- **Not a pure model ranking:** results are a **model + harness + effort** combination. A run from one CLI agent at max effort is not comparable to a different harness with different tools, retry policy, or budget. Always read the run configuration alongside the fix count.
- Compare both the **fix count** and the run configuration: harness, effort/reasoning level, wall-clock time, and cost.

## When to check this on a new model release

When the release targets coding/agent work and autonomous bug discovery matters to your workload: cross-check the Bug Hunt standing against [coding agents](/AI-benchmarks/coding-agents/) results (SWE-bench Verified/Pro, Terminal-Bench, LiveCodeBench) and record the harness/effort configuration with any number you quote. It is step-2 ammunition in the [release-review workflow](/AI-benchmarks/release-review-workflow/), not a standalone verdict.
