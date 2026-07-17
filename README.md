# AI Product Factory v5

Turn one idea into live-researched docs that coding agents can build from.

```text
Idea → CONFIRM → 7 docs → check → prep → build loop
```

## What you get

- Live-cited market + competitor research with SWOT and positioning
- 3–5 evidence-backed MVP features with acceptance + kill criteria
- Design, build, agent contract, and decision log ready for coding agents

## Steps

1. **Enable search**

    | Host | Enable |
    | --- | --- |
    | ChatGPT | Search/browse; Deep Research; Projects/files |
    | Gemini | Google Search grounding; Deep Research |
    | Claude | Web search/fetch; Projects/files |
    | Cursor | Agent + web/browser/Firecrawl/MCP |
    | Other | Search + browse minimum |

2. **Blueprint** — paste the **entire** [`PROMPT.md`](PROMPT.md), then the idea block below:

    ```text
    PRODUCT IDEA:
    <idea>

    OPTIONAL CONTEXT:
    <users, pain, constraints, budget, geography, stack, compliance, screenshots, or links>
    ```

3. **Reply**

    **3a Blockers** — if the factory asks ≤3 questions, reply `go` or `skip` to accept ★ defaults, pick an option, or type `Other: …`. Silence is not input.

    **3b CONFIRM** — the factory shows one card (user/buyer, pain, positioning, MVP list, sources, tools, risks, `as_of`). Reply `OK`, `approve`, or `go` to accept. Edit inline: `drop 2`, `add X`, `pain is Y`. Files come **only after you accept**.

4. **Save** — copy the seven docs from chat into a **new product repo** (not this factory repo). The output `README.md` is your **product** readme.

    `RESEARCH.md` · `README.md` · `PRODUCT.md` · `DESIGN.md` · `BUILD.md` · `AGENTS.md` · `DECISIONS.md`

5. **Build**

    **5a Stitch (optional)** — feed `PRODUCT.md` + `DESIGN.md` to Stitch or a similar UI tool for visuals only.

    **5b Prep** — give all seven docs to a coding agent and paste:

    > Read all seven docs. Create repo skeleton, `.env.example`, test setup, and CI stub. Follow `BUILD.md` + `AGENTS.md`. No product features yet.

    **5c Build** — one MVP feature per run. Paste:

    > Follow `AGENTS.md`. Build one MVP feature from `PRODUCT.md` using `DESIGN.md` + `BUILD.md`; consult `RESEARCH.md` for evidence, not requirements. Plan → tests from acceptance criteria → implement → verify tests/typecheck/lint → self-review. Update docs. Log material choices in `DECISIONS.md`. No production deploy without approval.

    **Loop:** repeat 5c per feature. Rate first slice 1–10; score ≤7 → fix before next. New scope → update `PRODUCT.md` first.

## Check before you build

Run these before step 5. Reject and redo the blueprint if any fail.

- Live tools were used (if available). No tools → claims marked `ASSUMPTION` + freshness `UNKNOWN`.
- RESEARCH shows Tools Used, `as_of`, direct URLs, freshness (`CURRENT`/`STALE`/`UNKNOWN`); sources opened, not snippets; official pricing/features checked; SWOT cited.
- PRODUCT has 3–5 MVP features with evidence + acceptance + kill criteria. Screens map to features.
- Precedence: `PRODUCT` > `DESIGN` > `BUILD` > `AGENTS`; RESEARCH informs PRODUCT.
- Human OK required: production deploy, destructive DB, data deletion, secrets, security policy.

## License

Free use. No warranty.
