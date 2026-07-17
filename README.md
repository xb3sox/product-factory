# AI Product Factory v5

Turn one idea into live-researched docs coding agents can build from.

```text
Idea → CONFIRM → 7 docs → check → stitch → prep → build loop
```

**Need:** chat + web search + [`PROMPT.md`](PROMPT.md).

## Steps

1. **Search** — ChatGPT Search/Deep Research · Gemini grounding · Claude web · Cursor Agent/MCP · Other: search + browse min
2. **Blueprint** — paste entire [`PROMPT.md`](PROMPT.md) +:

    ```text
    PRODUCT IDEA:
    <idea>

    OPTIONAL CONTEXT:
    <users, pain, constraints, budget, geography, stack, compliance, screenshots, or links>
    ```

3. **Reply** — **3a** ≤3 blocker Qs: `go`/`skip` = ★, option, or `Other: …`; silence ≠ input. **3b** CONFIRM: `OK`/`approve`/`go` accept; `drop 2`/`add X`/`pain is Y` edit. Files after accept only.
4. **Save** — copy 7 docs from chat → **new product repo** (not this repo; output `README.md` = product readme):

    `RESEARCH.md` · `README.md` · `PRODUCT.md` · `DESIGN.md` · `BUILD.md` · `AGENTS.md` · `DECISIONS.md`

5. **Build** (pass Check first)

    **5a Stitch (optional)** — attach `PRODUCT.md` + `DESIGN.md`, paste:

    > Mock every MVP screen from DESIGN.md. Match tokens/components/states (loading/empty/error). Visuals only — no code. New screen → update PRODUCT + DESIGN first.

    **5b Prep** — all 7 docs to agent, paste:

    > Read all seven docs. Create repo skeleton, `.env.example`, test setup, and CI stub. Follow `BUILD.md` + `AGENTS.md`. No product features yet.

    **5c Build** — one MVP/run, paste:

    > Follow `AGENTS.md`. Build one MVP feature from `PRODUCT.md` using `DESIGN.md` + `BUILD.md`; consult `RESEARCH.md` for evidence, not requirements. Plan → tests from acceptance criteria → implement → verify tests/typecheck/lint → self-review. Update docs. Log material choices in `DECISIONS.md`. No production deploy without approval.

    Loop: repeat 5c. Score first slice 1–10; ≤7 fix before next. Red tests = not done. New scope → `PRODUCT.md` first.

## Check before build

Fail any → re-run step 2.

- Live tools used if available; else `ASSUMPTION` + freshness `UNKNOWN`
- RESEARCH: Tools Used, `as_of`, URLs, `CURRENT`/`STALE`/`UNKNOWN`, sources opened, pricing/features checked, SWOT cited
- PRODUCT: 3–5 MVP, evidence + acceptance + kill criteria; screens ↔ features
- Precedence: `PRODUCT` > `DESIGN` > `BUILD` > `AGENTS`; RESEARCH informs PRODUCT
- Human OK: prod deploy, destructive DB, data deletion, secrets, security policy

## License

Free use. No warranty.
