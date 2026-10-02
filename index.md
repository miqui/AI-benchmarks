---
title: Home
nav_order: 1
permalink: /
layout: page
---

# AI Benchmarks — a durable leaderboard reference

This site tracks the benchmarks and leaderboards worth checking on every new model release. It links to *living* leaderboards rather than snapshotting scores, so it stays useful without constant maintenance.

## Start here: the 5-step release-review checklist

1. **Start broad.** Check Arena + Artificial Analysis: human preference, capability profile, context window, pricing, throughput, availability.
2. **Validate in the relevant category:**
   - general → LiveBench + GPQA Diamond / MMLU-Pro
   - coding → SWE-bench Verified/Pro + Terminal-Bench + LiveCodeBench
   - multimodal → MMMU-Pro + DocVQA/ChartQA + Vision Arena
   - embeddings → MTEB + your own corpus eval
   - agents → GAIA/tau-bench/Toolathlon + internal tool-call trace eval
3. **Read the evaluation protocol, not just the number:** model version/date, prompting policy, reasoning mode, tools enabled, agent scaffold, retries, test-time compute, cost cap, vendor-reported vs. independently reproduced.
4. **Run an internal release gate:** 25–100 versioned tests mirroring actual workloads (OpenAPI/MCP tool selection, OAuth-aware calls, schema validation, API error repair, incident analysis, code changes, policy-sensitive tasks). Capture quality, tool-call correctness, latency, token use, cost, failure mode.
5. **Promote only after operational validation:** rate-limit behavior, structured-output reliability, prompt-injection resistance, privacy posture, regional availability, observability — run a staging canary behind a model gateway.

Full detail: [release-review-workflow](/AI-benchmarks/release-review-workflow/).

## Compact 9-bookmark set

| # | Leaderboard | Best for | Link |
|---|---|---|---|
| 1 | Arena | Human preference | [https://arena.ai/leaderboard](https://arena.ai/leaderboard) |
| 2 | Artificial Analysis | Performance / speed / cost | [https://artificialanalysis.ai](https://artificialanalysis.ai) |
| 3 | Arena Pareto frontier | Quality vs price frontier — best model at each budget | [https://arena.ai/leaderboard/text/pareto](https://arena.ai/leaderboard/text/pareto) |
| 4 | LiveBench | Fresh general capability | [https://livebench.ai](https://livebench.ai) |
| 5 | Scale Leaderboard | Expert frontier / agent / safety | [https://labs.scale.com/leaderboard](https://labs.scale.com/leaderboard) |
| 6 | SWE-bench | Repo-level software engineering | [https://www.swebench.com](https://www.swebench.com) |
| 7 | Terminal-Bench | Terminal/CLI coding agents | [https://www.tbench.ai](https://www.tbench.ai) |
| 8 | MTEB | Embeddings and retrieval | [https://huggingface.co/spaces/mteb/leaderboard](https://huggingface.co/spaces/mteb/leaderboard) |
| 9 | HF Open LLM Leaderboard | Open-weight models | [https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) |

## Map of this reference

See the sidebar for all capability pages: [core-leaderboards](/AI-benchmarks/core-leaderboards/), [open-models](/AI-benchmarks/open-models/), [general-reasoning](/AI-benchmarks/general-reasoning/), [math](/AI-benchmarks/math/), [coding-agents](/AI-benchmarks/coding-agents/), [bug-hunt](/AI-benchmarks/bug-hunt/), [code-generation](/AI-benchmarks/code-generation/), [long-context](/AI-benchmarks/long-context/), [multimodal](/AI-benchmarks/multimodal/), [tool-use-agents](/AI-benchmarks/tool-use-agents/), [rag-retrieval](/AI-benchmarks/rag-retrieval/), [multilingual](/AI-benchmarks/multilingual/), [safety](/AI-benchmarks/safety/), [efficiency-economics](/AI-benchmarks/efficiency-economics/), [pitfalls](/AI-benchmarks/pitfalls/).

No leaderboard is definitive — see [pitfalls](/AI-benchmarks/pitfalls/) before trusting any single number.
