---
title: Coding Agents
nav_order: 6
permalink: /coding-agents/
---

# Coding / software-engineering agents

| Evaluation question | Primary leaderboard | What it catches |
|---|---|---|
| Can it resolve a reported software issue? | [SWE-bench](https://www.swebench.com/) | Issue-to-patch work; official entries report % instances resolved |
| Can it autonomously FIND bugs before being told? | [Bug Hunt Bench](/AI-benchmarks/bug-hunt/) (leaderboard: [skillsllm](https://skillsllm.com/skill/bug-hunt-bench), mirror: [https://benchlm.ai/benchmarks/bug-hunt-bench](https://benchlm.ai/benchmarks/bug-hunt-bench)) | Exploration, diagnosis, repo understanding under ambiguity |
| Can it work through a terminal? | [Terminal-Bench](https://www.tbench.ai/) | Software/systems/data/tool-driven terminal tasks |
| Current coding problems without contamination? | [LiveCodeBench](https://livecodebench.github.io/) | Fresh, time-controlled code generation |
| Accurate code editing across languages? | [Aider leaderboard](https://aider.chat/docs/leaderboards/) | Focused code-editing capability |
| Coding-agent quality/cost/time comparison layer | [Artificial Analysis Coding Agents](https://artificialanalysis.ai/agents/coding-agents) | Quality, cost, token usage, execution time |

Also relevant: OpenHands/agent benchmarks (repo navigation, edit, test, iterate) — verify harness, tool access, and test-leakage controls alongside SWE-bench Verified/Pro.

## Bug Hunt Bench detail

Agent gets one round per repository to find and fix 105 planted bugs across two production TypeScript codebases; diffs graded blindly against a withheld answer key. The leaderboard records harness, effort setting, runs, bugs fixed, per-repo result, extra fixes, wall time, cost, and eval date.

**Caveat:** only two TypeScript repos — narrow signal. Compare fix count **and** run configuration (harness, effort/reasoning level, wall-clock, cost) together, not fix count alone.

## Bug Hunt vs. SWE-bench — the key distinction

- **Bug Hunt Bench** = "investigate → locate → patch" *without* an issue roadmap: requires architecture reading, hypothesis generation, budget allocation, and avoiding speculative changes.
- **SWE-bench** starts from a *known, reported* issue — a narrower, more guided task.

## The model + harness + effort caveat

Bug Hunt (and most agentic coding leaderboards) rank a **model + harness + effort configuration**, not a pure foundation-model capability. "Claude Code at max effort" is not comparable to "another model with a different CLI harness, effort/reasoning level, tool access, retry policy, and budget." Always read the run configuration before comparing numbers across entries.

## When to check this on a new model release

Step 2 of [release-review-workflow](/AI-benchmarks/release-review-workflow/) for a coding release: SWE-bench Verified/Pro + Terminal-Bench + LiveCodeBench, cross-checked against Bug Hunt Bench if autonomous bug discovery matters to your workload. Always record the harness/effort configuration alongside the score, and run your own internal release gate (step 4) mirroring real repos before promoting.
