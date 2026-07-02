# Stage 1 — Generate (🤖 Claude)

> 📋 **This is a prompt.** Paste it into Claude along with your problem area / product context. (You can also just read it to understand the stage.)

**Goal:** produce a *blank, well-structured* Opportunity Canvas the team can populate. You are creating the working surface, not filling it in.

**Input:** the canvas schema in [`templates/opportunity-canvas.md`](templates/opportunity-canvas.md), plus any context the PM gives you (the rough problem area, the product, the team).

**Output:** a clean, empty Opportunity Canvas — ready to drop onto a whiteboard (Miro / FigJam) or hand to the team.

**Surface — offer the best one available, in this order:**
1. **Miro board** (only if a Miro MCP is connected): one frame per section, each with its facilitation prompt as a sticky. Board named `Opportunity Canvas: <run folder name>`.
   *Layout rules:* everything fits **inside** its frame, nothing overlaps — spacing between stacked stickies must account for the sticky's actual height, not just its centre. After building, **read the board back and verify** no item overlaps another or crosses a frame edge; fix before reporting done. Record the board URL at the top of the archival markdown copy.
2. **Markdown file** — the universal default; works everywhere. If no Miro MCP is available, use this without interrogating the user (one-line tip that connecting the Miro MCP unlocks board creation is fine). On request, also give a paste-into-Miro variant: a plain bulleted list per section — Miro turns pasted bullets into stickies.

**Always keep a markdown copy** at `runs/<slug>/opportunity-canvas.md` regardless of surface — it's the archival reference for Synthesise. **Naming:** the canvas H1 (and Miro board name) is `Opportunity Canvas: <run folder name>` — artifact and folder always match.

---

## Prompt

> You are helping a product manager run the **Generate** stage of the Opportunity Workflow. Produce a **blank Opportunity Canvas** for their team to fill in collaboratively.
>
> Use the schema in `templates/opportunity-canvas.md`. For each section:
> - Keep it **empty** — do not invent content. This is a working surface for the *team*.
> - Include a **one-line facilitation prompt** (the question the team should answer in that section).
> - Where the schema suggests a framework (JTBD, pains/gains, empathy mapping), present it as an **optional lens**, not a requirement. Remind the team: *use whatever unlocks the conversation.*
>
> Before generating, ask the PM only what you genuinely need: the **problem area / product**, the **team / cohorts** involved, and any **time-box** for the session. If they don't answer, proceed with neutral placeholders and flag what's missing.
>
> Output the canvas as clean markdown with each section as a heading and an empty, prompted body. If asked, additionally describe a Miro frame layout (one frame per section, arranged left-to-right top-to-bottom in schema order).

---

## Section order to generate (from the schema)

1. Customer problem (framework-agnostic)
2. User & customer cohorts
3. Solutions today (competitor / alternatives)
4. Why the business should care (challenges + potential impact; optional value/time calc)
5. Adoption strategy (per cohort)
6. Pain/gain + JTBD / empathy pass
7. Impact stack-rank (tees up ideation)

## Do / Don't

- ✅ Leave every section **empty** with a facilitation prompt.
- ✅ Mark optional sections (value/time calc, GMV/TAM) as optional.
- ✅ Note that **ideation happens off-canvas** — the canvas ends at the stack-rank.
- ❌ Don't pre-fill the team's answers.
- ❌ Don't force a single framework.
