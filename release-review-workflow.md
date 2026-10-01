---
title: Release-Review Workflow
nav_order: 16
permalink: /release-review-workflow/
---

# Release-review workflow

The full 5-step checklist to run whenever a new model (or a new version of an existing model) is released.

1. **Start with Arena + Artificial Analysis.** Human preference, capability profile, context window, pricing, throughput, availability. See [core-leaderboards](/AI-benchmarks/core-leaderboards/) and [efficiency-economics](/AI-benchmarks/efficiency-economics/).

2. **Validate in the relevant category:**
   - **General** → [LiveBench](/AI-benchmarks/general-reasoning/) + GPQA Diamond/MMLU-Pro
   - **Coding** → [SWE-bench Verified/Pro + Terminal-Bench + LiveCodeBench](/AI-benchmarks/coding-agents/)
   - **Multimodal** → [MMMU-Pro + DocVQA/ChartQA + Vision Arena](/AI-benchmarks/multimodal/)
   - **Embeddings** → [MTEB + own corpus eval](/AI-benchmarks/rag-retrieval/)
   - **Agents** → [GAIA/tau-bench/Toolathlon + internal tool-call trace eval](/AI-benchmarks/tool-use-agents/)

3. **Read the evaluation protocol, not just the number.** Model version/date, prompting policy, reasoning mode, tools enabled, agent scaffold, retries, test-time compute, cost cap, vendor-reported vs. independently reproduced. This is the single most-skipped step and the source of most mis-ranked comparisons (see [coding-agents](/AI-benchmarks/coding-agents/)'s model+harness+effort caveat).

4. **Run an internal release gate.** 25–100 versioned tests mirroring actual workloads:
   - OpenAPI/MCP tool selection
   - OAuth-aware calls
   - Schema validation
   - API error repair
   - Incident analysis
   - Code changes
   - Policy-sensitive tasks

   Capture: quality, tool-call correctness, latency, token use, cost, failure mode.

5. **Promote only after operational validation.** Rate-limit behavior, structured-output reliability, prompt-injection resistance, privacy posture, regional availability, observability. Run a **staging canary behind a model gateway** before full rollout.

See [pitfalls](/AI-benchmarks/pitfalls/) for the failure modes this workflow is designed to catch.
