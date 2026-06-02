# Parallect for Claude Code

A [Claude Code](https://claude.com/claude-code) plugin that gives Claude a
**deep-research** skill backed by [Parallect](https://parallect.ai) — a
multi-provider research platform that queries Perplexity, ChatGPT, Claude,
Gemini, and Grok in parallel, then synthesizes their findings into one report
with cross-referenced citations and conflict resolution.

The plugin bundles two things:

- A **`deep-research` skill** that teaches Claude how to run research
  responsibly (budget first, async polling, citations, follow-ons).
- The **Parallect MCP server** config, so the research tools are available the
  moment you install.

## Install

```bash
# Add this repo as a marketplace
/plugin marketplace add parallect/parallect-claude-plugin

# Install the plugin
/plugin install parallect@parallect
```

Once the community marketplace listing is live you'll also be able to:

```bash
/plugin marketplace add anthropics/claude-plugins-community
/plugin install parallect@claude-community
```

## Authenticate

The first time Claude uses a Parallect tool, you'll be asked to connect:

- **OAuth (recommended):** sign in through the browser when prompted. Nothing
  to manage.
- **API key:** create a `par_live_*` key at
  [parallect.ai/settings/keys](https://parallect.ai/settings/keys) and add it to
  your MCP client config as a Bearer token.

New accounts need credits or a payment method before research will run — add
them at [parallect.ai/settings/billing](https://parallect.ai/settings/billing).

## Use

Just ask Claude naturally:

- "Research the latest advances in solid-state batteries"
- "Deep dive on the competitive landscape for AI code editors"
- "Fact-check this claim: software job postings are up 15% year over year"
- "What do we know about the regulatory outlook for stablecoins in the EU?"

Claude will check your balance, agree a budget tier, submit the research, poll
for completion, and deliver a synthesis with citations — then offer follow-ons.

## Budget tiers

| Tier | Max cost | Providers | Best for |
|------|----------|-----------|----------|
| XXS | ~$1 | 1 | Quick factual lookups |
| XS | ~$2 | 1-2 | Brief overviews |
| S | ~$5 | 2 | Standard questions |
| M | ~$15 | 3-4 | Detailed research (default) |
| L | ~$30 | 4-5 | Comprehensive analysis |
| XL | ~$60 | All | Exhaustive multi-provider |

Claude suggests a tier based on the question and confirms before spending.

## Tools

Provided by the Parallect MCP server (`https://parallect.ai/api/mcp/mcp`):

| Tool | Purpose |
|------|---------|
| `research` | Submit a research query (async) |
| `research_status` | Poll job progress |
| `get_results` | Retrieve completed synthesis |
| `follow_up` | Pursue follow-on questions |
| `list_threads` | List recent research threads |
| `get_thread` | Get full thread context |
| `balance` | Check credit balance |
| `usage` | View spend analytics |
| `list_providers` | See available providers and tiers |
| `search_claims` | Search claims across research |
| `get_claim_evidence` | Get the evidence chain for a claim |

## Links

- [Parallect](https://parallect.ai) — dashboard, billing, research history
- [MCP docs](https://parallect.ai/docs/mcp/overview)
- [API reference](https://parallect.ai/docs)

## License

MIT
