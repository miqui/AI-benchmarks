---
title: Safety
nav_order: 13
---

# Safety & trustworthiness

| Benchmark | What it actually tells you | Link |
|---|---|---|
| Stanford HELM | Transparent, multidimensional evaluation: scenarios, robustness, fairness, toxicity, efficiency, transparency | https://crfm.stanford.edu/helm |
| DecodingTrust | Trustworthiness across toxicity, bias, robustness, privacy, ethics, fairness | track via aggregators |
| SafetyBench | Multiple-choice safety-knowledge and risk-awareness evaluation | track via aggregators |
| HarmBench | Standardized red-teaming/jailbreak-resistance evaluation | track via aggregators |
| WildGuard | Safety moderation and harmful-content detection evaluation | track via aggregators |

**What it tells you:** Robustness, refusal behavior, bias, and jailbreak resilience. Scale AI's SEAL leaderboard (see [core-leaderboards](core-leaderboards.html)) also includes 20+ safety-alignment benchmarks.

## When to check this on a new model release

Part of step 5 (operational validation) in [release-review-workflow](release-review-workflow.html): prompt-injection resistance and privacy posture specifically. Always cross-check safety claims against your own adversarial testing — safety benchmarks are especially prone to the self-reported-score and vendor-optimization issues covered in [pitfalls](pitfalls.html).
