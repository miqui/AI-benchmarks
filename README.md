# AI-benchmarks

A durable, markdown reference of the most popular AI leaderboards and benchmarks — what each one actually tells you, its caveats, and how to use it when evaluating a new model release.

Served as a GitHub Pages site (Jekyll + just-the-docs) from `docs/`: **https://miqui.github.io/AI-benchmarks/**

## Repo map

```
AI-benchmarks/
├── README.md                       # this file
├── _config.yml                     # Jekyll / just-the-docs config
└── docs/
    ├── index.md                    # START HERE: 5-step release-review checklist + 8-bookmark set
    ├── core-leaderboards.md        # the 12 core boards + aggregators/discovery indexes
    ├── open-models.md              # HF Open LLM Leaderboard + open-weight guidance
    ├── general-reasoning.md        # MMLU-Pro, GPQA Diamond, SimpleBench, HLE, LiveBench
    ├── math.md                     # AIME, HMMT, MATH-500, GSM8K
    ├── coding-agents.md            # SWE-bench, Terminal-Bench, Bug Hunt Bench, LiveCodeBench, Aider, AA Coding Agents
    ├── code-generation.md          # LiveCodeBench, BigCodeBench, HumanEval+, MBPP+
    ├── long-context.md             # RULER, LongBench v2, InfiniteBench, NIAH variants
    ├── multimodal.md               # MMMU/MMMU-Pro, MathVista, ChartQA, DocVQA, Video-MME, Vision Arena, VLMEvalKit
    ├── tool-use-agents.md          # ToolBench, BFCL, tau-bench, GAIA, Toolathlon
    ├── rag-retrieval.md            # MTEB, BEIR, MIRACL, LoCoV0
    ├── multilingual.md             # Global-MMLU, FLORES-200, multilingual MTEB, MGSM
    ├── safety.md                   # HELM, DecodingTrust, SafetyBench, HarmBench, WildGuard
    ├── efficiency-economics.md     # Artificial Analysis, pricing/latency, own load tests
    ├── release-review-workflow.md  # the full 5-step workflow incl. internal release gate
    └── pitfalls.md                 # contamination, self-reported scores, composite-rank caution, harness confounds
```

## How to update this repo on a new model release

1. Open `docs/release-review-workflow.md` and run the 5-step checklist against the new model.
2. For each relevant capability page, check whether the leaderboard has since added the model; no content changes are usually needed — these pages link to *living* leaderboards, they don't snapshot scores.
3. Only edit page content when: a benchmark is deprecated/superseded, a new benchmark becomes a core reference, a link changes, or a caveat needs updating based on something learned during the release review (e.g. a harness confound discovered in practice).
4. Keep every URL exactly as sourced — do not invent or guess links.
5. Open a PR (branch protection requires 1 approval before merge into `main`).

## GitHub Pages limits (respected here)

Pure markdown docs are trivially within GitHub Pages limits:
- Repo size ≤ 1 GB
- Published site ≤ 1 GB
- Bandwidth: 100 GB/month soft limit

## License

Content is a curated reference of publicly available benchmark leaderboards; links point to their original sources.
