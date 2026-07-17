# AI Product Factory v5

Turn one idea into live-researched docs that coding agents can build from.

**Need:** chat app with web search + [`PROMPT.md`](PROMPT.md).

## Steps

1. **Enable search** — ChatGPT Search · Gemini grounding · Claude web · Cursor Agent/MCP
2. **Paste** [`PROMPT.md`](PROMPT.md) + your idea:

    ```text
    PRODUCT IDEA:
    <idea>

    OPTIONAL CONTEXT:
    <users, pain, constraints, budget, geography, links>
    ```

3. **Reply** — ≤3 questions if asked (`go`/`skip` = ★ defaults) → `OK` on `CONFIRM` (or edit: `drop 2`, `pain is X`)
4. **Save** seven files: `RESEARCH.md` · `README.md` · `PRODUCT.md` · `DESIGN.md` · `BUILD.md` · `AGENTS.md` · `DECISIONS.md`
5. **Build** — Stitch UI from `PRODUCT` + `DESIGN` → prep repo (skeleton, tests, no features) → one MVP feature per run. Paste:

    > Follow `AGENTS.md`. Build one MVP feature from `PRODUCT.md` using `DESIGN.md` + `BUILD.md`; consult `RESEARCH.md` for evidence, not requirements. Plan → tests from acceptance criteria → implement → verify tests/typecheck/lint → self-review. Update docs. Log material choices in `DECISIONS.md`. No production deploy without approval.

## Rules

- Reject if live tools were available but unused. No tools → `ASSUMPTION` + freshness `UNKNOWN`.
- RESEARCH: Tools Used, `as_of`, direct URLs, sources opened (not snippets), pricing/features checked, SWOT cited.
- 3–5 MVP features with evidence + acceptance + kill criteria. Screens map to features.
- Precedence: `PRODUCT` > `DESIGN` > `BUILD` > `AGENTS`; RESEARCH informs PRODUCT. Red tests = not done. Score ≤7 → fix before next.
- Human OK: production deploy, destructive DB, data deletion, secrets, security policy.

## License

Free use. No warranty.
