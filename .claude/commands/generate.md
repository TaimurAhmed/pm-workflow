---
description: "Step 1 · Generate a blank Opportunity Canvas"
argument-hint: "<canvas title — who's struggling with what>"
---

Run **Step 1 · Generate** of the Opportunity Workflow. Follow the full instructions in `workflows/opportunity/01-generate.md` — that file is canonical; this command just invokes it.

Canvas title given by the user: **$ARGUMENTS**

The title doubles as the problem statement — use it to name the canvas AND to tune each section's facilitation prompt to the domain.

Process:

1. If no title was given above, ask: "What should this canvas be called? A good title names who's struggling with what — e.g. 'Homeowners don't rebook after their first job'." Also ask (once, briefly) for the team/cohorts involved and the session time-box; if the user skips these, proceed and flag them ⚠️ in the canvas rather than stalling.
2. Generate the blank Opportunity Canvas per `01-generate.md`, using the schema in `workflows/opportunity/templates/opportunity-canvas.md`: every section **empty**, each with a one-line facilitation prompt; frameworks presented as optional lenses; ideation noted as off-canvas.
3. Save it to `runs/<problem-slug>/opportunity-canvas.md` (create the folder; short kebab-case slug from the problem area). Tell the user where it is and what happens next: **Step 2 · Populate** — their team fills it in on a whiteboard, then they run `/synthesise` with the results.
