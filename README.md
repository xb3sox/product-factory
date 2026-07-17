# AI Product Factory v5

Turn one product idea into live-researched docs that coding agents can build from.

**You need:** a chat app with web search (ChatGPT, Gemini, Claude, or Cursor) + [`PROMPT.md`](PROMPT.md).

## Quick start

1. Enable search/browse (see Requirements).
2. Paste [`PROMPT.md`](PROMPT.md) + your idea → answer ≤3 questions if asked → reply `OK` on `CONFIRM`.
3. Save the seven docs to your product repo.
4. Stitch UI → build one MVP feature per agent run.

```text
Idea → live research + SWOT → confirm once → 7 docs
     → Stitch → coding agent → production
```

## Requirements

| Host | Enable |
| --- | --- |
| ChatGPT | Search/browse; Deep Research; Projects/files |
| Gemini | Google Search grounding; Deep Research |
| Claude | Web search/fetch; Projects/files |
| Cursor | Agent + web/browser/Firecrawl/MCP |
| Other | Search + browse minimum |

No live tools → claims marked `ASSUMPTION`/`UNKNOWN`. Live search required for market/pricing/competitors/regulation.

## Blueprint

Paste [`PROMPT.md`](PROMPT.md), then:

```text
PRODUCT IDEA:
<idea>

OPTIONAL CONTEXT:
<users, pain, constraints, budget, geography, screenshots, or links>
```

Factory infers defaults (`go` accepts `★` picks), researches, shows one `CONFIRM`. Reply `OK` or edit (`drop 2`, `pain is X`), then save:

`RESEARCH.md` · `README.md` · `PRODUCT.md` · `DESIGN.md` · `BUILD.md` · `AGENTS.md` · `DECISIONS.md`

## After blueprint

- Reject if live tools were available but unused.
- RESEARCH shows `as_of`, Tools Used, direct URLs, freshness; sources opened, not snippets; official pricing/features checked.
- SWOT cited or labeled; PRODUCT has 3–5 MVP features, each with evidence + acceptance + kill criteria; screens map to features.

## Build loop

- **Stitch:** `PRODUCT.md` + `DESIGN.md` → visuals only. New feature → PRODUCT first.
- **Prep:** give all seven docs to the agent → repo skeleton, `.env.example`, tests, task list — no features yet.
- **Build:** one MVP feature per run. Paste:

> Follow `AGENTS.md`. Build one MVP feature from `PRODUCT.md` using `DESIGN.md` + `BUILD.md`; consult `RESEARCH.md` for evidence, not requirements. Plan → tests from acceptance criteria → implement → verify tests/typecheck/lint → self-review. Update docs. Log material choices in `DECISIONS.md`. No production deploy without approval.

- **Loop:** Plan → Code → Test → Review → Deploy (human OK). Red tests = not done. Score first slice 1–10; ≤7 → fix before next.
- **Precedence:** `PRODUCT` > `DESIGN` > `BUILD` > `AGENTS`; RESEARCH informs PRODUCT.
- **Human approval:** production deploy, destructive DB, data deletion, secrets, security policy.

## What you get

- Live-cited market + competitor evidence (`CURRENT`/`STALE`/`ASSUMPTION`)
- SWOT + positioning
- 3–5 evidence-backed MVP features with acceptance + kill criteria
- Design, build, agent contract, and decision log ready for coding agents

## License

Free use. No warranty.
