---
description: "Step 1 · Generate a blank Opportunity Canvas for your problem area"
argument-hint: "[problem area, e.g. 'checkatrade homeowner repeat usage']"
---

Run **Step 1 · Generate** of the Opportunity Workflow. Follow the full instructions in `workflows/opportunity/01-generate.md` — that file is canonical; this command just invokes it.

Problem area given by the user: **$ARGUMENTS**

Process:

1. If no problem area was given above, ask for it before doing anything else. Also ask (once, briefly) for the team/cohorts involved and the session time-box; if the user skips these, proceed and flag them ⚠️ in the canvas rather than stalling.
2. Generate the blank Opportunity Canvas per `01-generate.md`, using the schema in `workflows/opportunity/templates/opportunity-canvas.md`: every section **empty**, each with a one-line facilitation prompt; frameworks presented as optional lenses; ideation noted as off-canvas.
3. Save it to `runs/<problem-slug>/opportunity-canvas.md` (create the folder; short kebab-case slug from the problem area). Tell the user where it is and what happens next: **Step 2 · Populate** — their team fills it in on a whiteboard, then they run `/synthesise` with the results.
