---
title: Core Leaderboards
nav_order: 2
---

# Core leaderboards

The 12 boards worth knowing, plus aggregators and discovery indexes.

| Leaderboard | Best for | What it actually tells you | Link |
|---|---|---|---|
| LMArena / Arena | General chat quality and human preference | Large-scale blinded, pairwise user preference. First signal for conversation, writing, instruction following, common reasoning. Not a substitute for task-specific eval. | https://arena.ai/leaderboard |
| Artificial Analysis | Practical model selection | Broad dashboard comparing frontier and open models across intelligence, speed, price, context, API/deployment properties. Turns "benchmark winner" into an architecture decision. | https://artificialanalysis.ai |
| Scale AI SEAL / Leaderboards | Expert-driven reasoning, coding, agents, safety | Curated suite of demanding expert evaluations incl. agentic coding and frontier reasoning; 20+ benchmarks incl. safety alignment. | https://labs.scale.com/leaderboard |
| LiveBench | Fresh, contamination-resistant general capability | Frequently refreshed questions across reasoning, math, coding, language, data analysis. | https://livebench.ai |
| Hugging Face Open LLM Leaderboard | Open-weight LLMs | Standardized harness for open models; essential for self-hostable candidates. | https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard |
| SWE-bench | Repo-level software engineering | Agent resolves real GitHub issues in real repos. Prioritize Verified and stronger contamination-aware variants; inspect harness, scaffold, tools. | https://www.swebench.com |
| Terminal-Bench | CLI-based coding agents | Agents in realistic shell environments; relevant to Codex/Claude Code/Gemini CLI workflows. | https://www.tbench.ai |
| Aider Polyglot Benchmark | Code-editing quality | Narrow measure of code editing across languages; not end-to-end agent reliability. | https://aider.chat/docs/leaderboards/ |
| MTEB | Embeddings, retrieval, RAG | Multi-task benchmark family for embedding models: retrieval, reranking, STS, classification, clustering, multilingual. Pair with own corpus evals. | https://huggingface.co/spaces/mteb/leaderboard |
| LMSYS / Vision Arena | Vision-language human preference | Head-to-head preference for visual understanding and multimodal chat. | https://arena.ai |
| VLMEvalKit leaderboard | Vision-language benchmark coverage | Broad, reproducible VLM evaluation across many visual QA and reasoning datasets. | https://github.com/open-compass/VLMEvalKit |
| HELM | Transparent, multidimensional evaluation | Stanford CRFM: scenarios, robustness, fairness, toxicity, efficiency, transparency. | https://crfm.stanford.edu/helm |

## Aggregators and discovery indexes

- **Artificial Analysis** — see above.
- **BenchLM** — tracks hundreds of models with benchmark-level breakdowns. https://benchlm.ai/
- **AI Release Tracker** — discovery index of new releases and benchmarks. https://aireleasetracker.com/benchmark
- **AOE AI Technology Radar** — model/platform leaderboard radar. https://ai-radar.aoe.com/models-platforms/model_leaderboards/
- **llm-stats.com** — cross-model stats aggregator. https://llm-stats.com/
- **Vellum LLM Leaderboard** — aggregator. https://www.vellum.ai/llm-leaderboard

## When to check this on a new model release

Always — this is step 1 of the [release-review-workflow](release-review-workflow.html). Start with Arena + Artificial Analysis for the broad capability/price/speed profile before drilling into category-specific pages.
