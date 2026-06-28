# Opportunity Workflow ✅

**Where it sits:** the convergent close of **diamond one** — you've done wide, unstructured discovery and now need to *align the team on the problem worth solving* before ideating.

**What it produces:**
1. A populated **Opportunity Canvas** (the team's shared working surface)
2. A polished **Opportunity Brief** as a formatted `.docx` (the stakeholder's narrative doc)

**Inspired by** Jeff Patton's [Opportunity Canvas](https://www.jpattonassociates.com/opportunity-canvas/), adapted with a framework-agnostic problem framing and a pain/gain + JTBD pass.

---

## The three stages

| Stage | Who | What happens | File |
|---|---|---|---|
| **1. Generate** | 🤖 Claude | Produces a blank, well-structured Opportunity Canvas for the team to fill in. | [`01-generate.md`](01-generate.md) |
| **2. Populate** | 👥 Team | The team fills the canvas in offline, collaboratively (Miro / whiteboard). | [`02-populate.md`](02-populate.md) |
| **3. Synthesise** | 🤖 Claude | Takes the messy populated canvas (screenshots, transcripts, chat) + the brief template and produces the Opportunity Brief `.docx`. | [`03-synthesise.md`](03-synthesise.md) |

> **Ideation happens off-canvas.** The canvas closes with a simple impact stack-rank that *tees up* ideation — but the divergent solution-generation itself belongs to the next workflow, not this one.

---

## Canvas schema (overview)

The full schema lives in [`templates/opportunity-canvas.md`](templates/opportunity-canvas.md). Sections, in order:

1. **Customer problem** — framework-agnostic statement of the problem.
2. **User & customer cohorts** — who has this problem.
3. **Solutions today** — how it's solved now (competitor / alternatives analysis).
4. **Why the business should care** — challenges + potential impact (optional value/time calc).
5. **Adoption strategy** — per cohort, how they'd discover & adopt a solution.
6. **Pain/gain + JTBD / empathy pass** — deepen the problem understanding.
7. **Impact stack-rank** — simple prioritisation that tees up ideation.

---

## Brief structure (overview)

The full template lives in [`templates/opportunity-brief.template.md`](templates/opportunity-brief.template.md). Sections:

1. **Metadata** — title, author, contributors, date.
2. **BLUF** — full thesis in 3–5 lines.
3. **SCQA narrative** — why the customer cares (problem → segments → JTBD → pains/gains) → why the business cares (impact → potential) → competitor analysis.
4. **The opportunity** — the thesis, tied back to the customer (optional GMV/TAM; mark "not covered this iteration" if skipped).
5. **HMWs** — How-Might-We questions mapped to customer problems.
6. **HMWs stack-ranked** — by impact, to tee up ideation.

---

## ⚠️ Template files you supply

Two template files are referenced here. Working **example** versions ship in `templates/` so the workflow runs out of the box — **replace them with your own** when ready (each file is marked at the top):

- [`templates/opportunity-canvas.md`](templates/opportunity-canvas.md) — the canvas schema Claude generates from.
- [`templates/opportunity-brief.template.md`](templates/opportunity-brief.template.md) — the empty brief Claude fills during Synthesise.
