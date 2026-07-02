# AI-Leveraged PM Workflows

A living, opinionated set of product-management workflows I actually use — designed so an AI assistant (Claude) can help *run* them, not just store templates. Each workflow pairs **collaborative canvases** (for the team) with **synthesised briefs** (for stakeholders), and gives the AI enough context to generate starting artifacts and turn messy collaborative input into polished deliverables.

This repo is two things at once: a **real tool** I use at work, and a **portfolio piece** showing how I think about product discovery and delivery.

---

## Getting started

**You need:** access to Claude (claude.ai, the desktop app, or Claude Code). Nothing to install.

Every workflow runs in **3 stages**. Here's the Opportunity Workflow:

1. **Generate** — paste [`workflows/opportunity/01-generate.md`](workflows/opportunity/01-generate.md) into Claude and tell it your problem area. It hands back a blank Opportunity Canvas.
2. **Populate** — your team fills the canvas in together on a whiteboard. This stage is human; no AI.
3. **Synthesise** — give Claude the filled-in canvas (screenshots, notes) plus [`03-synthesise.md`](workflows/opportunity/03-synthesise.md). It returns a polished Opportunity Brief as a Word doc.

👉 New here? Just do step 1.

---

## Workflow index

Workflows are added incrementally. Status: ✅ complete · 🚧 coming soon.

| Workflow | What it produces | Status |
|---|---|---|
| [Opportunity Workflow](workflows/opportunity/) | Opportunity Canvas → Opportunity Brief | ✅ |
| [Solution Workflow](workflows/solution/) | Solution Canvas → Solution Doc | 🚧 |
| _Future workflows_ | — | 🚧 |

---

## The mental model: a double diamond with canvases at the waists

These workflows map to the classic **double diamond** (discover → define → develop → deliver). The opinionated twist: **my canvases sit at the pinch points — the waists — not stretched across the whole diamonds.**

![Double diamond with the Opportunity Canvas at the convergent close of diamond one and the Solution Canvas at the divergent open of diamond two, ideation bridging the two, and unstructured research and Jira backlog refinement happening off-canvas at the edges.](assets/double-diamond.svg)

- **Opportunity Canvas** sits at the **convergent close of diamond one** — you've done wide discovery and now need to *align on the problem worth solving*.
- **Solution Canvas** sits at the **divergent open of diamond two** — you start *generating and shaping solutions*.
- **Ideation bridges the middle**, carrying you from problem-alignment into solution-divergence.
- The **wide divergent discovery** (unstructured research up front) and the **narrow delivery tail** (Jira tickets, backlog refinement) happen **off-canvas**.

**Why off-canvas at the edges?** Canvases earn their place only at the moments that genuinely need *structured, collaborative alignment*. Early discovery is messy and exploratory by design; late delivery is granular execution. Forcing a canvas onto either just adds ceremony. The waist is where a team most needs to look at one shared surface and agree.

---

## Core philosophy

**1. Canvas for the team, brief for the stakeholder.**
Canvases are *collaborative working surfaces* — they live on a whiteboard (Miro, FigJam, a wall of stickies). They're where the team argues, aligns, and converges. **Briefs** synthesise that messy surface into a *shareable narrative document* a stakeholder can read on their own. Different audiences, different artifacts. The AI's job in synthesis is to translate from one to the other.

**2. Framework-agnostic.**
The point is the **team conversation**, not the framework. JTBD vs. needs vs. pains/gains vs. empathy mapping — use whatever unlocks discussion in the room. The canvas schemas *suggest* lenses; none are mandatory. A framework that produces silence is the wrong framework.

**3. Flag, rationalise, defer — within the time-box.**
When input is incomplete, the AI should **flag the gap**, **briefly explain why it matters**, then **let the PM decide** whether to fill it or defer it. The goal is **reducing decision risk**, not chasing completeness into analysis paralysis. Discovery is time-boxed; "we don't know this yet, and here's the risk that carries" is a valid, documented output.

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
