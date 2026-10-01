---
title: RAG & Retrieval
nav_order: 11
permalink: /rag-retrieval/
---

# RAG & retrieval

| Benchmark | What it actually tells you | Link |
|---|---|---|
| MTEB | Multi-task benchmark family for embedding models: retrieval, reranking, STS, classification, clustering, multilingual | [https://huggingface.co/spaces/mteb/leaderboard](https://huggingface.co/spaces/mteb/leaderboard) |
| BEIR | Zero-shot retrieval benchmark across heterogeneous domains and task types | track via aggregators |
| MIRACL | Multilingual retrieval benchmark | track via aggregators |
| LoCoV0 | Long-context retrieval benchmark | track via aggregators |

**Caveat:** Retrieval/embedding quality on these boards doesn't guarantee quality on *your* corpus — domain shift (jargon, document structure, language mix) between benchmark data and production data is common. **Always pair leaderboard results with your own corpus eval.**

## When to check this on a new model release

Step 2 of [release-review-workflow](/AI-benchmarks/release-review-workflow/) for an embeddings release: MTEB + your own corpus eval. Treat MTEB as a candidate shortlist filter, not a final decision — validate top candidates against your actual retrieval task before switching production embedding models.
