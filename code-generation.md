---
title: Code Generation
nav_order: 8
permalink: /code-generation/
---

# Code generation

| Benchmark | What it actually tells you | Link |
|---|---|---|
| LiveCodeBench | Fresh, time-controlled code generation; contamination-resistant current signal | [https://livecodebench.github.io/](https://livecodebench.github.io/) |
| BigCodeBench | Broader, more realistic function/task-level coding coverage | track via [core-leaderboards](/AI-benchmarks/core-leaderboards/) aggregators |
| HumanEval+ | Hardened/extended version of the classic function-completion benchmark | track via aggregators |
| MBPP+ | Hardened/extended "Mostly Basic Python Problems" benchmark | track via aggregators |

**Caveat:** Function/task-level coding only — prefer LiveCodeBench/BigCodeBench for current signal over the older HumanEval/MBPP bases, which are more saturated and contamination-prone.

## When to check this on a new model release

Use for pure code-generation quality, distinct from agentic coding (see [coding-agents](/AI-benchmarks/coding-agents/)) which measures multi-step repo-level work. Check this when the task is single-function/single-file code generation rather than end-to-end software engineering.
