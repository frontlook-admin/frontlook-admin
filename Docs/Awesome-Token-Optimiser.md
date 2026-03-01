# MCP Servers for Token Optimization, Context Summarization & Dynamic Toolset Management

> Researched from GitHub — September 2025 to March 2026

---

## Category 1 — Local/Self-Hosted Proxies

> Servers that use structured output, tool filtering, or semantic search to hide/reduce schema verbosity.

| Server | GitHub Link | Language | Last Updated | Use Case | Token Reduction Mechanism |
|---|---|---|---|---|---|
| **Pare** | [Dave-London/Pare](https://github.com/Dave-London/Pare) | TypeScript | Mar 2026 (active) | Wraps git, npm, docker, test runners — returns schema-validated JSON instead of raw terminal output. 240 tools across 28 packages. | Converts verbose CLI stdout to compact structured JSON. Env-var tool filtering (`PARE_GIT_TOOLS=status,log`) limits which tool schemas are exposed. Benchmarks: docker build **95%**, git log **92%**, npm install **83%**, vitest **80%** reduction. |
| **CortexAST** | [cortex-works/cortex-ast](https://github.com/cortex-works/cortex-ast) | Rust | Mar 2026 (active) | AI-native code intelligence backend. Semantic codebase navigation, AST analysis, blast-radius, cross-file vector search over past decisions. | `map_overview` mode returns "near-zero tokens" symbol maps. `deep_slice` uses a configurable token budget with vector-ranked results. Rules fetched dynamically per file-path context rather than sending all rules upfront. |
| **Agentic-MCP-Skill** | [bioeu/Agentic-MCP-Skill](https://github.com/bioeu/Agentic-MCP-Skill) | TypeScript | Mar 2026 (active) | Progressive disclosure and script linkage for Claude Code interactions. | Validates and optimizes MCP token usage by exposing skills/tools on-demand (progressive disclosure) rather than loading all schemas into context at once. |
| **LLM-Tools** | [samestrin/llm-tools](https://github.com/samestrin/llm-tools) | Go | Feb 2026 | High-performance Go toolset for LLM agents with token-optimized search and persistent project memory. | Token-optimized search returns only the most relevant hits; persistent memory prevents re-exploring already-discovered context in subsequent agent calls. |

---

## Category 2 — Summarization Middlewares

> Servers that condense large file, command, or log outputs before they reach the LLM.

| Server | GitHub Link | Language | Last Updated | Use Case | Token Reduction Mechanism |
|---|---|---|---|---|---|
| **token-optimizer-mcp** | [ooples/token-optimizer-mcp](https://github.com/ooples/token-optimizer-mcp) | TypeScript | Nov 2025 (v5.0.1) | Intelligent token optimizer for Claude Code. Hooks into the MCP lifecycle. | Claims **95%+** reduction via caching (`smart_read`), compression, and smart tool intelligence. Per-hook/per-action granular analytics. Abstractive summarization module included. |
| **Chomper** | [IcHiGo-KuRoSaKiI/Chomper](https://github.com/IcHiGo-KuRoSaKiI/Chomper) | Python | Jan 2026 | Document parser for 36+ formats (PDF, DOCX, EPUB, CSV, code files, email, etc.) for AI systems. | **TOON (Token-Optimized Object Notation)** format reduces output by ~**40%** vs JSON. Default summary mode returns only the first 5,000 chars; full text requires explicit opt-in. Pagination via `get_document_chunk`. Semantic chunking for RAG. |
| **Stump** | [hegner123/stump](https://github.com/hegner123/stump) | Zig | Jan 2026 | Token-efficient directory tree visualization for LLM consumption. | Produces condensed directory tree output optimized for LLMs — claims **50%+** reduction vs standard `tree` output. |
| **Jankins** | [thecturner/jankins](https://github.com/thecturner/jankins) | Python | Nov 2025 | Token-optimized Jenkins MCP server for CI/CD triage. | Smart log handling trims and summarizes Jenkins build logs before returning to the LLM. Advanced triage mode surfaces only failure lines, not full verbose logs. |
| **Datadog MCP Server** | [waabox/datadog-mcp-server](https://github.com/waabox/datadog-mcp-server) | Java | Feb 2026 | LLM-optimized Datadog APM, logs, and metrics server. | Returns structured, token-efficient summaries of traces/logs specifically designed for AI debugging — not raw unfiltered Datadog data. |
| **mcp-master-puppeteer** | [flrngel/mcp-master-puppeteer](https://github.com/flrngel/mcp-master-puppeteer) | TypeScript | Nov 2025 | Browser automation with minimal token output. | Returns only the minimal structured page data needed for the agent's goal rather than dumping full DOM or screenshots. |

---

## Category 3 — Gateways with Semantic Caching

> Servers that cache context semantically or use vector stores to avoid redundant token-heavy lookups.

| Server | GitHub Link | Language | Last Updated | Use Case | Token Reduction Mechanism |
|---|---|---|---|---|---|
| **token-optimizer-mcp** *(also Cat. 2)* | [ooples/token-optimizer-mcp](https://github.com/ooples/token-optimizer-mcp) | TypeScript | Nov 2025 | Session-level caching for Claude Code tool calls. | `smart_read` caching stores file reads in session cache — repeated reads to the same files cost zero new tokens. Cache hit rate tracked per action. |
| **Pinecone Assistant MCP** | [john-walkoe/pinecone_assistant_mcp](https://github.com/john-walkoe/pinecone_assistant_mcp) | Python | Feb 2026 | Generic RAG gateway using Pinecone vector store. YAML-configurable domains, cross-MCP integration. Reference implementation: USPTO patent search (MPEP). | Strategic multi-search with semantic caching — retrieves only relevant document chunks from the vector store rather than loading full documents. Token optimization flag built-in. |
| **TOON-JSON Conversion MCP** | [arindam-b/toon-json-conversion-mcp](https://github.com/arindam-b/toon-json-conversion-mcp) | Python | Jan 2026 | Converts standard JSON payloads to TOON format before returning to the LLM. | TOON (Token-Optimized Object Notation) is a compact representation of JSON. Acts as a conversion gateway — plugs into any pipeline to shrink verbose JSON API responses before they consume context. |
| **claude-cartographer** | [cristinaaponte/claude-cartographer](https://github.com/cristinaaponte/claude-cartographer) | Python | Mar 2026 (active) | Codebase navigation map for Claude Code — creates and maintains semantic indexes of large codebases. | Claims **95%+** token reduction when navigating large codebases. Agents query the semantic map rather than reading files directly. |

---

## Key Observations

- **TOON format** appears across multiple independent projects (Chomper, toon-json-conversion-mcp) as an emerging compact notation for LLM-targeted output — roughly **40% more compact** than standard JSON.
- **Pare** is the most production-ready and actively maintained option for structured CLI output (320+ releases, 64 stars, daily commit cadence as of Mar 2026).
- **token-optimizer-mcp** (ooples) spans all three categories, functioning as a full-stack optimizer covering caching + compression + abstractive summarization.
- **CortexAST** is the most sophisticated option for codebase-specific token control, combining vector search, dynamic rule fetching, and token-budgeted query modes.
- **Progressive disclosure** (exposing only relevant tool schemas on demand) is an emerging pattern in Agentic-MCP-Skill and Pare's tool-filtering env vars.

---

## Quick Comparison by Reduction Claimed

| Server | Claimed Reduction | Mechanism |
|---|---|---|
| token-optimizer-mcp | 95%+ | Caching + compression + summarization |
| claude-cartographer | 95%+ | Semantic codebase index |
| Pare (docker build) | 95% | Structured JSON output |
| Pare (git log) | 92% | Structured JSON output |
| Pare (npm install) | 83% | Structured JSON output |
| Stump | 50%+ | Directory tree compression |
| Chomper (TOON) | ~40% | TOON format vs JSON |

---

*Last updated: March 1, 2026*
