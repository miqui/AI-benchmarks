---
title: Home
nav_order: 1
permalink: /
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

Full detail: [release-review-workflow](release-review-workflow.html).

## Compact 8-bookmark set

| # | Leaderboard | Best for | Link |
|---|---|---|---|
| 1 | Arena | Human preference | https://arena.ai/leaderboard |
| 2 | Artificial Analysis | Performance / speed / cost | https://artificialanalysis.ai |
| 3 | LiveBench | Fresh general capability | https://livebench.ai |
| 4 | Scale Leaderboard | Expert frontier / agent / safety | https://labs.scale.com/leaderboard |
| 5 | SWE-bench | Repo-level software engineering | https://www.swebench.com |
| 6 | Terminal-Bench | Terminal/CLI coding agents | https://www.tbench.ai |
| 7 | MTEB | Embeddings and retrieval | https://huggingface.co/spaces/mteb/leaderboard |
| 8 | HF Open LLM Leaderboard | Open-weight models | https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard |

## Map of this reference

See the sidebar for all capability pages: [core-leaderboards](core-leaderboards.html), [open-models](open-models.html), [general-reasoning](general-reasoning.html), [math](math.html), [coding-agents](coding-agents.html), [code-generation](code-generation.html), [long-context](long-context.html), [multimodal](multimodal.html), [tool-use-agents](tool-use-agents.html), [rag-retrieval](rag-retrieval.html), [multilingual](multilingual.html), [safety](safety.html), [efficiency-economics](efficiency-economics.html), [pitfalls](pitfalls.html).

No leaderboard is definitive — see [pitfalls](pitfalls.html) before trusting any single number.
