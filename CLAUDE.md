# CLAUDE.md

Entry point for Claude Code (and any AI assistant) working in this repo. The human-facing overview is in [`README.md`](README.md); this file tells the AI how to *run* the workflows.

## What this repo is

A set of AI-leveraged PM workflows. Each workflow is a folder under `workflows/`. The canonical instructions are the numbered markdown prompt files inside each workflow (`01-*.md`, `02-*.md`, …) — they are self-contained and tool-agnostic. This file just points you at them.

## Operating principles (apply to every workflow)

1. **Canvas for the team, brief for the stakeholder.** Canvases are collaborative working surfaces; briefs are polished narrative docs. Don't blur the two.
2. **Framework-agnostic.** Suggest lenses (JTBD, pains/gains, empathy mapping) but never force one. Optimise for unlocking the team conversation.
3. **Flag, rationalise, defer — within the time-box.** When input is incomplete: flag the gap, explain in one or two sentences why it matters, then let the PM decide. Reduce decision risk; do not chase completeness. Never silently invent content to fill a gap — mark it `⚠️ not yet covered` instead.
4. **Real documents, not markdown-as-docx.** When a step calls for a `.docx`, produce a properly formatted Word file (see below).

## How to run a workflow

1. Read that workflow's `README.md` for the stage overview.
2. For an **AI-assisted stage** (Generate / Synthesise), open the corresponding numbered prompt file and follow it. Each prompt file states its inputs, outputs, and the template(s) it references.
3. **Populate** stages are human-and-team work done offline — your job there is only to prepare inputs or answer questions, not to fabricate the team's content.

## Document generation (.docx)

When a step requires a Word document:

- **Primary path:** use Anthropic's `docx` skill to build a properly formatted `.docx` (headings, styles, tables, page structure). The output must open cleanly in Microsoft Word and Google Docs.
- **Fallback (portable):** if the `docx` skill is unavailable (e.g. someone cloning this repo outside Claude), generate the document with [`python-docx`](https://python-docx.readthedocs.io/). Map each brief section to real Word headings/styles — never just dump markdown into a `.docx` container.

## Available workflows

- `workflows/opportunity/` — ✅ **Opportunity Workflow** (Generate → Populate → Synthesise → Opportunity Brief)
- `workflows/solution/` — 🚧 **Solution Workflow** (stub)
