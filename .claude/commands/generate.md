---
description: "Step 1 · Generate a blank Opportunity Canvas"
argument-hint: "<canvas title — who's struggling with what>"
---

Run **Step 1 · Generate** of the Opportunity Workflow. Follow the full instructions in `workflows/opportunity/01-generate.md` — that file is canonical; this command just invokes it.

Canvas title given by the user: **$ARGUMENTS**

The title doubles as the problem statement — use it to name the canvas AND to tune each section's facilitation prompt to the domain.

Process:

1. If no title was given above, ask: "What should this canvas be called? A good title names who's struggling with what — e.g. 'Homeowners don't rebook after their first job'." Also ask (once, briefly) for the team/cohorts involved and the session time-box; if the user skips these, proceed and flag them ⚠️ in the canvas rather than stalling.
2. **Ask where they want the canvas** (canvases live on whiteboards, so offer the best surface available):
   - **Miro board** — only offer if Miro MCP tools are available (check via ToolSearch for `miro`). If chosen, create a board with one frame per canvas section, each frame holding its facilitation prompt as a sticky. Name the board `Opportunity Canvas: <run folder name>`.
     **Layout rules (geometry matters):** items must fit *inside* their frame with nothing overlapping. Account for each item's height/width when placing centres — two stacked stickies need centre-to-centre spacing ≥ sticky height + a gutter. If a frame holds N stickies, size them so N × (height + gutter) fits the frame interior. **Verify before finishing:** read the board back and check no item overlaps another or crosses its frame's edge; fix anything that does.
   - **Markdown file** — always available; the universal default. If no Miro MCP is connected, don't interrogate — just use markdown and add one line: "Tip: if you use Miro, connect the Miro MCP and I can build the board for you next time." Offer a paste-into-Miro variant on request (a plain bulleted list per section — Miro converts pasted bullets into stickies).
3. Generate the blank Opportunity Canvas per `01-generate.md`, using the schema in `workflows/opportunity/templates/opportunity-canvas.md`: every section **empty**, each with a one-line facilitation prompt; frameworks presented as optional lenses; ideation noted as off-canvas.
4. **Whichever surface was chosen, always save the markdown copy** to `runs/<slug>/opportunity-canvas.md` (create the folder; short kebab-case slug from the title). This is the archival reference for `/synthesise` — a Miro board can't live in git. **If a Miro board was created, record its URL at the top of the markdown copy** so the run folder always points at the live canvas.
5. **Naming convention:** the canvas H1 is `Opportunity Canvas: <run folder name>` — artifact and folder must always match (same for the Miro board name).
6. Tell the user where everything is and what happens next: **Step 2 · Populate** — their team fills it in on a whiteboard, then they run `/synthesise` with the results.
