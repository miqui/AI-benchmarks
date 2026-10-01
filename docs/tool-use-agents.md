---
title: Tool Use & Agents
nav_order: 10
---

# Tool use & agents

| Benchmark | What it actually tells you |
|---|---|
| ToolBench | Function-calling breadth across many real-world APIs |
| BFCL (Berkeley Function Calling Leaderboard) | Function-calling accuracy and schema adherence across call types |
| tau-bench | Stateful, multi-turn agentic task completion in realistic domains (e.g. retail/airline) |
| GAIA | General AI assistant tasks requiring reasoning, tool use, and web/file interaction |
| Toolathlon | Multi-tool, multi-step agentic task completion — relevant to MCP (Model Context Protocol) workflows |

**What it tells you:** Function calling, schema adherence, tool selection, stateful workflows.

**Relevance to MCP:** Toolathlon and BFCL are the most directly relevant to MCP-based tool orchestration — check schema adherence and multi-tool sequencing specifically, not just single-call accuracy.

*Track current standings via the aggregators in [core-leaderboards](core-leaderboards.html).*

## When to check this on a new model release

Step 2 of [release-review-workflow](release-review-workflow.html) for an agentic release: GAIA/tau-bench/Toolathlon + your own internal tool-call trace eval. This is also where the step-4 internal release gate matters most — OpenAPI/MCP tool selection, OAuth-aware calls, schema validation, and API error repair rarely show up fully in public boards.
