# Parallect Search Depth Reference

Read this when recommending a depth or when the user asks about pricing/options.

Parallect exposes five **search depths** in the dashboard. Present these names
to the user; the `research` MCP tool takes the mapped `budgetTier`. You bill at
**actual usage** — the prices below are the standard/typical amount, not a cap.

| Depth | Price | Time | `budgetTier` | Best for |
|-------|-------|------|-------------|----------|
| Nano | $1.50 | 5-8 min | XXS | Quick fact-check, single-answer lookup |
| Lite | $2.50 | 8-15 min | XS | Light research with multiple sources |
| **Normal** (default) | $5.00 | 12-20 min | M | Verified daily-driver research across 5 providers |
| Deep | $15 | 12-30 min | L | Parallel research across 7 providers, cross-referenced |
| Max | $30 | 15-45 min | XL | Every provider in parallel, deepest synthesis (investment-grade) |

All depths run multi-provider synthesis. Higher depths add more providers and
deeper cross-referencing. **Normal is the default** — only go cheaper for quick
lookups or deeper when the topic genuinely needs breadth.

## Choosing a depth

| Question | Depth |
|----------|-------|
| "What is X?" / quick fact-check | Nano |
| "Give me a quick read on X" | Lite |
| Most research (default) | Normal |
| Broad, cross-referenced deep dive / due diligence | Deep |
| Exhaustive, leave nothing out | Max |

## Providers

**Do NOT hardcode or recall provider/model names — they change.** Call
`list_providers` (optionally with a `budgetTier`) for the live list of
providers, their current models, strengths, and the per-tier cost cap. Present
exactly what it returns.

Provider strengths (stable, qualitative — exact model versions come from
`list_providers`, not this file):

| Provider | Best at |
|----------|---------|
| Perplexity | Citation density, search breadth, speed |
| Gemini | Google Search grounding, structured data |
| OpenAI | Deep reasoning chains, nuanced analysis |
| Grok | Real-time X/social data, web search |
| Anthropic (Claude) | Synthesis quality, careful reasoning |
