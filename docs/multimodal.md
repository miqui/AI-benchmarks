---
title: Multimodal
nav_order: 9
---

# Multimodal

| Benchmark / board | What it actually tells you | Link |
|---|---|---|
| MMMU / MMMU-Pro | College-level multimodal understanding and reasoning across disciplines | track via aggregators |
| MathVista | Visual math reasoning (charts, diagrams, geometry) | track via aggregators |
| ChartQA | Chart understanding and question answering | track via aggregators |
| DocVQA | Document image question answering (forms, scans, layouts) | track via aggregators |
| Video-MME | Multimodal understanding over video input | track via aggregators |
| LMSYS / Vision Arena | Head-to-head human preference for visual understanding and multimodal chat | https://arena.ai |
| VLMEvalKit leaderboard | Broad, reproducible VLM evaluation across many visual QA and reasoning datasets | https://github.com/open-compass/VLMEvalKit |

**What this family tells you:** Visual/document/chart/math/video understanding. No single board covers all modalities equally — triangulate per modality that matters to your use case (document-heavy vs. chart-heavy vs. video).

## When to check this on a new model release

Step 2 of [release-review-workflow](release-review-workflow.html) for a multimodal release: MMMU-Pro + DocVQA/ChartQA + Vision Arena. If your workload is document-specific, weight DocVQA/ChartQA higher than general Arena preference.
