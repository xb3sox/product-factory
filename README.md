# How to Use the Master Prompt

## 1. Add Your Product Idea

Copy the full master prompt and replace:

```text
[PASTE PRODUCT IDEA HERE]
```

with your product idea.

Example:

```text
An AI-powered project management app for small remote teams.
```

## 2. Paste It Into ChatGPT or Gemini

Start a new chat and paste the complete prompt.

For best results, use a model with:

- Web browsing
- File generation
- Long context
- Advanced reasoning

## 3. Answer the Interview

The AI will ask short questions one at a time.

You can reply with:

```text
Recommended
```

to accept the suggested option.

Or reply with:

```text
All recommended
```

to let the AI choose all remaining options.

## 4. Approve the Product Direction

The AI will show a summary of:

- Product concept
- Target users
- MVP features
- Recommended technology
- Assumptions
- Main risks

Reply with:

```text
Approve
```

Or request a change:

```text
Change: Add a mobile app to the MVP
```

## 5. Download the Generated Files

After approval, the AI will generate the full product package.

Prefer downloading it as a ZIP file.

The package will include:

```text
/
├── README.md
├── AGENTS.md
├── CLAUDE.md
├── GEMINI.md
├── PLANS.md
├── docs/
└── prompts/
```

## 6. Create the Design

Open:

```text
prompts/STITCH.md
```

Copy its prompts into Google Stitch to generate the product screens and design system.

Review and refine the design before development.

## 7. Prepare the Code Repository

Create or open your project repository.

Add all generated Markdown files to the repository root while keeping the same folder structure.

Example:

```text
your-project/
├── AGENTS.md
├── PLANS.md
├── docs/
├── prompts/
└── source-code/
```

## 8. Start Building

Open:

```text
prompts/BUILD.md
```

Give it to your coding agent, such as:

- Codex
- Claude Code
- Gemini CLI
- Cursor
- Replit Agent

The agent will read the product documents and start with the next task in:

```text
PLANS.md
```

## 9. Build One Task at a Time

For each development session, ask the agent:

```text
Read AGENTS.md and PLANS.md. Implement the next ready task, verify it fully, and update the documentation.
```

Continue until all MVP tasks are complete.

## Complete Workflow

```text
Product idea
↓
Master prompt
↓
Short interview
↓
Approve direction
↓
Research and product documents
↓
Google Stitch design
↓
Coding-agent implementation
↓
Testing and verification
↓
Production deployment
```
