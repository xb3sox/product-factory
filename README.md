# AI Product Factory

Turn one product idea into validated, agent-ready product docs.

```text
Idea → Research → Confirm → Docs → Design → Build → Validate
```

**Handoff:** research tools → chat output → design tools → coding agents

## Quality rules

Check saved docs before Build (step 5). Fail any → re-run Research from step 1.

- Use live research tools when available; else mark `ASSUMPTION` + freshness `UNKNOWN`.
- RESEARCH must show Tools Used, `as_of`, direct URLs, freshness, sources opened, SWOT cited.
- Build only **confirmed MVP scope**. `PRODUCT` > `DESIGN` > `BUILD` > `AGENTS`; RESEARCH informs PRODUCT.
- After each slice: score product value, UX match, technical quality, test quality; average ≥8 and no category <7 to continue.
- Red tests = not done. New scope → update `PRODUCT.md` first.
- Human OK required: production deploy, destructive DB, data deletion, secrets, security/compliance changes.

## Workflow

1. **Research** — enable search/browse in your chat tool. Paste entire [`PROMPT.md`](PROMPT.md) +:

    ```text
    PRODUCT IDEA:
    <idea>

    OPTIONAL CONTEXT:
    <users, pain, constraints, budget, geography, stack, compliance, screenshots, or links>
    ```

2. **Confirm** — reply to ≤3 blocker questions if asked (`go`/`skip` = ★ defaults; **silence ≠ input**). Review one CONFIRM card; reply `OK`/`approve`/`go` or edit lines. **No docs before confirmation.**
3. **Save** — copy seven docs from chat into a **new product repo** (not this factory repo). The product repo becomes the **source of truth**.
4. **Design (optional)** — feed `PRODUCT.md` + `DESIGN.md` to a UI tool (Stitch, Figma AI, etc.). Visuals only. New screen → update `PRODUCT.md` first.
5. **Build** — after Quality rules pass, give all seven docs to a coding agent. Prep repo (skeleton, tests, `.env.example`) before features. Build **one vertical slice at a time:** input → processing → user value → output → measurement. Repeat per MVP item.
6. **Validate** — run each slice against its `PRODUCT.md` validation experiment (metric, threshold, timeframe). Keep, defer, or redesign per kill criteria before the next feature.

## Documents

| File | Purpose |
| --- | --- |
| `RESEARCH.md` | Evidence, competitors, assumptions, risks |
| `PRODUCT.md` | Users, MVP, requirements, success metrics |
| `DESIGN.md` | UX flows, screens, states |
| `BUILD.md` | Architecture and technical plan |
| `AGENTS.md` | Coding agent rules |
| `DECISIONS.md` | Important decisions and changes |
| `README.md` | Product workflow (in your product repo) |

## License

Free use. No warranty.
