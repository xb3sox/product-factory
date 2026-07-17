# AI Product Factory v5

Turn a product idea into research-backed docs that coding agents can build from.

Workflow sources in this repo:

| File | Role |
| --- | --- |
| [`PROMPT.md`](PROMPT.md) | Master prompt: interview defaults, live research, SWOT, feature scoring, seven-doc contract |
| [`RUN.md`](RUN.md) | Operator guide: tool preflight, blueprint, quality check, design + build loop |

## Flow

```text
Idea → live research + SWOT → confirm once → 7 docs
     → Stitch → coding agent → production
```

Happy path: paste idea → optional ≤3 picks → one `CONFIRM` → save docs. No serial interview. No manual Google paste.

## Quick start

1. Enable live search/browse on your host (ChatGPT, Gemini, Claude, or Cursor).
2. Paste [`PROMPT.md`](PROMPT.md) + your idea (see [`RUN.md`](RUN.md) for the paste template).
3. Reply `OK` on the Confirm card (or edit a line).
4. Save the seven outputs into your product project root:
   - `RESEARCH.md` · `README.md` · `PRODUCT.md` · `DESIGN.md` · `BUILD.md` · `AGENTS.md` · `DECISIONS.md`
5. Stitch UI from PRODUCT + DESIGN, then build **one MVP feature per agent run** using `AGENTS.md`.

## What you get

- Live-cited market/competitor evidence with freshness labels (`CURRENT` / `STALE` / `ASSUMPTION`)
- SWOT + positioning
- 3–5 evidence-backed MVP features with acceptance + kill criteria
- Design, architecture, agent contract, and decision log ready for coding agents

Precedence after confirmation: `PRODUCT` > `DESIGN` > `BUILD` > `AGENTS`. `RESEARCH` informs PRODUCT; it does not override accepted decisions.

## License

Use freely for your own products. No warranty.
