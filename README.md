# AI Product Factory v5

Turn a product idea into research-backed docs that coding agents can build from.

| File | Role |
| --- | --- |
| [`PROMPT.md`](PROMPT.md) | Master prompt: interview defaults, live research, SWOT, feature scoring, seven-doc contract |

This README is the operator guide.

## Flow

```text
Idea → live research + SWOT → confirm once → 7 docs
     → Stitch → coding agent → production
```

Happy path: idea → `OK` → files. No serial interview. No manual research.

## 0. Tool preflight

Before paste: live search + page browsing on.

| Host | Enable |
| --- | --- |
| ChatGPT | Search/browse; Deep Research; Projects/files |
| Gemini | Google Search grounding; Deep Research |
| Claude | Web search/fetch; Projects/files |
| Cursor | Agent mode + web/browser/Firecrawl/MCP |
| Other | Search + browse minimum; deep research/files if offered |

No manual research/search-result paste. Factory calls tools + logs `RESEARCH.md`. No live tools → claims `ASSUMPTION`/`UNKNOWN`; live-search host required for current market/pricing/competitor/regulation confidence.

## 1. Blueprint

Paste [`PROMPT.md`](PROMPT.md), then:

```text
PRODUCT IDEA:
<idea>

OPTIONAL CONTEXT:
<users, pain, constraints, budget, geography, screenshots, or links>
```

1. Infer defaults; optional ≤3-question batch (`go` accepts `★`).
2. Research → one `CONFIRM`. Reply `OK` or edit (`drop 2`, `pain is X`).
3. Save: `RESEARCH.md` · `README.md` · `PRODUCT.md` · `DESIGN.md` · `BUILD.md` · `AGENTS.md` · `DECISIONS.md`

## 2. Quality check

- RESEARCH: `as_of`, Tools Used, direct URLs, confidence/freshness; opened sources not snippets; official live pricing/features.
- SWOT cited/assumed; PRODUCT 3–5 MVP each with evidence + acceptance + kill criteria; CONFIRM risks match docs; screens map to features.
- Live tools available but unused → reject + rerun tool-enabled.

## 3. Design + build

**Stitch:** `PRODUCT.md` + `DESIGN.md` → visuals only. New feature → PRODUCT first. `PRODUCT` > `DESIGN`.

**Prep:** seven docs → Cursor / Claude Code / Codex / OpenCode. Repo structure, `.env.example`, test skeleton, task list. No features yet. `RESEARCH.md` = evidence; `PRODUCT.md` = accepted behavior.

**Build:** same agent, **one MVP feature per run**. Paste:

> Follow `AGENTS.md`. Build one MVP feature from `PRODUCT.md` using `DESIGN.md` + `BUILD.md`; consult `RESEARCH.md` for evidence, not requirements. Plan → tests from acceptance criteria → implement → verify tests/typecheck/lint → self-review. Update docs. Log material choices in `DECISIONS.md`. No production deploy without approval.

Loop: Plan → Code → Test → Review → Deploy only with human approval. Red tests = not done. Never whole product one run.

Rules: `PRODUCT` > `DESIGN` > `BUILD` > `AGENTS`; RESEARCH informs PRODUCT. Human OK: production deploy, destructive DB, data deletion, secrets, security policy. After feature: update docs; fix upstream. Score first slice 1–10 (MVP, AC, UX, local, verify, agent); ≤7 → fix that slice before next.

## What you get

- Live-cited market/competitor evidence with freshness labels (`CURRENT` / `STALE` / `ASSUMPTION`)
- SWOT + positioning
- 3–5 evidence-backed MVP features with acceptance + kill criteria
- Design, architecture, agent contract, and decision log ready for coding agents

Precedence after confirmation: `PRODUCT` > `DESIGN` > `BUILD` > `AGENTS`. `RESEARCH` informs PRODUCT; it does not override accepted decisions.

## License

Use freely for your own products. No warranty.
