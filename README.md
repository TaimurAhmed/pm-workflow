# AI-Leveraged PM Workflows

A living, opinionated set of product-management workflows I actually use — designed so an AI assistant (Claude) can help *run* them, not just store templates. Each workflow pairs **collaborative canvases** (for the team) with **synthesised briefs** (for stakeholders), and gives the AI enough context to generate starting artifacts and turn messy collaborative input into polished deliverables.

This repo is two things at once: a **real tool** I use at work, and a **portfolio piece** showing how I think about product discovery and delivery.

---

## Getting started

### Setup (one-time)

1. **Install Claude Code** — follow [these instructions](https://docs.claude.com/en/docs/claude-code/overview). (Or skip this and use [claude.ai](https://claude.ai) — see the note at the bottom.)
2. **Clone this repo:**
   ```bash
   git clone https://github.com/TaimurAhmed/ai-pm-workflows.git
   ```
3. **Open it in Claude Code:**
   ```bash
   cd ai-pm-workflows && claude
   ```
   Claude reads [`CLAUDE.md`](CLAUDE.md) automatically, so it already knows how to run the workflows.

### Run your first workflow (Opportunity)

1. **Step 1 · Generate** — ask Claude: *"Run Step 1 of the Opportunity Workflow for [your problem area]."* It hands back a blank Opportunity Canvas.
2. **Step 2 · Populate** — your team fills the canvas in together on a whiteboard. This stage is human; no AI.
3. **Step 3 · Synthesise** — give Claude the filled-in canvas (screenshots, notes) and ask it to run Step 3. It returns a polished Opportunity Brief as a Word doc.

👉 New here? Just do the setup, then **Step 1 · Generate**.

> **No Claude Code?** You don't need it. Open any prompt file (e.g. [`01-generate.md`](workflows/opportunity/01-generate.md)), copy its contents into [claude.ai](https://claude.ai), and paste your inputs underneath.

---

## Workflow index

Workflows are added incrementally. Status: ✅ complete · 🚧 coming soon.

| Workflow | What it produces | Status |
|---|---|---|
| [Opportunity Workflow](workflows/opportunity/) | Opportunity Canvas → Opportunity Brief | ✅ Complete |
| [Solution Workflow](workflows/solution/) | Solution Canvas → Solution Doc | 🚧 Coming soon |
| _Future workflows_ | — | 🚧 Coming soon |

---

## The mental model: a double diamond with canvases at the waists

These workflows map to the classic **double diamond** (discover → define → develop → deliver). **My canvases sit at the pinch points — the waists — not stretched across the whole diamonds.**

![Double diamond with the Opportunity Canvas at the convergent close of diamond one and the Solution Canvas at the divergent open of diamond two, ideation bridging the two, and unstructured research and Jira backlog refinement happening off-canvas at the edges.](assets/double-diamond.svg)

- **Opportunity Canvas** sits at the **convergent close of diamond one** — you've done the wide divergent discovery and now need to *align on the problem worth solving*.
- **Solution Canvas** sits at the **divergent open of diamond two** — you start *generating and shaping solutions*.
- **Ideation bridges the middle**, carrying you from problem-alignment into solution-divergence.
- The **wide divergent discovery** (e.g. user research, data mining, canvassing the team for opinions) and the **narrow delivery tail** (e.g. Jira tickets, backlog refinement) happen **off-canvas**.

**Why off-canvas at the edges?** Canvases earn their place only at the moments that need *structured, collaborative alignment*. Wide discovery is messy and exploratory by design; the delivery tail is granular execution — forcing a canvas onto either just adds ceremony. I may build AI workflows for those ends later, but that work rarely transfers between organisations, so it's not where I chose to invest first.

---

## Core philosophy

**1. Canvas for the team, brief for the stakeholder.**
Canvases are messy collaborative surfaces (the whiteboard); briefs are the polished narrative a stakeholder reads alone. The AI translates one into the other.

**2. Framework-agnostic.**
JTBD, pains/gains, empathy mapping — use whatever unlocks the conversation. The framework serves the discussion, not the other way round.

**3. Flag, rationalise, defer — within the time-box.**
When input is thin, the AI flags the gap, says why it matters, and lets the PM decide. The goal is reducing decision risk, not chasing completeness.

---

## How the AI leverage works

Every workflow is built so Claude can help run it. Two stages of each workflow are AI-assisted:

- **Generate** — Claude produces a *blank, well-structured artifact* (e.g. an Opportunity Canvas) for the team to populate.
- **Synthesise** — Claude takes the *populated, messy* artifact (screenshots, meeting transcripts, chat logs) plus a template and produces a *polished deliverable* (e.g. an Opportunity Brief as a formatted `.docx`).

The instructions that drive this live as **markdown prompt files** inside each workflow folder (canonical, tool-agnostic — paste into any Claude), with a thin [`CLAUDE.md`](CLAUDE.md) so the repo also "just works" when opened in Claude Code.

> **Document generation note:** the Synthesise step produces a **properly formatted Word document**, not markdown renamed to `.docx`. See each workflow's `03-synthesise.md` for how this is done — Anthropic's `docx` skill is the primary path; `python-docx` is noted as a portable fallback.

---

## Repo structure

```
ai-pm-workflows/
├── README.md                  ← you are here
├── CLAUDE.md                  ← entry point for Claude Code
└── workflows/
    ├── opportunity/           ← ✅ Opportunity Workflow
    │   ├── README.md
    │   ├── 01-generate.md
    │   ├── 02-populate.md
    │   ├── 03-synthesise.md
    │   └── templates/
    │       ├── opportunity-canvas.md
    │       └── opportunity-brief.template.md
    └── solution/              ← 🚧 Solution Workflow (stub)
        └── README.md
```

---

## License & attribution

Licensed under [MIT](LICENSE).

The Opportunity Canvas schema is inspired by **Jeff Patton's [Opportunity Canvas](https://www.jpattonassociates.com/opportunity-canvas/)**. Narrative structuring draws on **SCQA** (Barbara Minto's *Pyramid Principle*) and **BLUF** (bottom line up front). These are adapted, not reproduced — credit to the originators.
