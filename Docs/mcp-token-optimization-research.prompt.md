---
description: 'Refresh the MCP token optimization server research — update DOCS/MCP_TOKEN_OPTIMIZATION_SERVERS.md with the latest findings from the past 6 months.'
---

# MCP Token Optimization Research — Refresh

Search GitHub, glama.ai, and the broader MCP ecosystem for **newly released or updated MCP servers** from the past 6 months that specifically focus on:

1. **Token optimization** (reducing tokens sent to/from the LLM)
2. **Context summarization** (condensing outputs before they reach the model)
3. **Dynamic toolset management** (progressive disclosure, schema filtering, on-demand tool loading)

## Research Instructions

- Search GitHub for repositories with topics or keywords: `mcp-server`, `token-optimization`, `context-compression`, `mcp-gateway`, `llm-context`, `semantic-cache`
- Check `glama.ai/mcp/servers` for newly listed servers in the target categories
- Fetch the README for the top candidates to verify their actual token-reduction mechanism
- Exclude servers that only mention token optimization incidentally — require it as a **primary feature**

## Output Format

Update the file `DOCS/MCP_TOKEN_OPTIMIZATION_SERVERS.md` with:

### For each newly discovered server, add a row to the appropriate category table:

| Column | What to fill |
|---|---|
| **Server** | Bold project name |
| **GitHub Link** | `[owner/repo](https://github.com/owner/repo)` |
| **Language** | Primary implementation language |
| **Last Updated** | Month + Year, append `(active)` if commits within 30 days |
| **Use Case** | 1–2 sentence description of what the server does |
| **Token Reduction Mechanism** | Specific technique + any quantified benchmark if available |

### Categories to populate:

1. **Category 1 — Local/Self-Hosted Proxies** — structured output, tool-schema filtering, AST/semantic search
2. **Category 2 — Summarization Middlewares** — condensing file/log/command outputs before LLM ingestion
3. **Category 3 — Gateways with Semantic Caching** — vector stores, session caching, RAG-based retrieval

### Additional updates required:

- Remove any rows where the project has been **abandoned** (no commits in 12+ months, repo archived/deleted)
- Update "Last Updated" dates for servers already listed if they have had recent activity
- Update the **Quick Comparison by Reduction Claimed** table if new benchmarks are available
- Update the `*Last updated: <date>*` footer at the bottom of the file
- Add a **## What's New** section at the top (just below the header) listing servers added or significantly updated in this refresh cycle — remove this section on the next refresh and replace it with a fresh one

## Research Scope

- **Time window**: Past 6 months from today's date
- **Minimum activity signal**: At least one commit or release in the past 6 months
- **Minimum relevance signal**: Token/context optimization must be explicitly described in the README or project description
- **Languages**: Any (TypeScript, Python, Rust, Go, Java, Zig, C#, etc.)

## Quality Bar

Before adding a server, confirm via its README that it either:
- Provides a **quantified reduction benchmark** (e.g., "80% fewer tokens"), OR
- Describes a **named technique** (TOON, semantic chunking, progressive disclosure, abstractive summarization, session caching, vector RAG), OR
- Has **notable GitHub activity** (stars > 20, recent commits, active issues)

Do not add servers based solely on project name or description — verify the actual mechanism from the README content.
