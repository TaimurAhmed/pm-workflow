<!--
⚠️ EXAMPLE TEMPLATE — REPLACE WITH YOUR OWN
This is a working skeleton of the empty Opportunity Brief. Claude fills this in
during Synthesise (Stage 3) and outputs it as a formatted .docx. Swap in your
own brief template when ready. Placeholders use {{double-brace}} notation and
⚠️ flags mark where gaps should be surfaced rather than invented.
-->

# {{Opportunity title}}

## Metadata
- **Author:** {{author}}
- **Contributors:** {{contributors}}
- **Date:** {{date}}
- **Status:** Draft

---

## BLUF — Bottom Line Up Front
> *The full thesis in 3–5 lines. A stakeholder who reads only this should understand the opportunity, why it matters to the customer and the business, and what we're asking. State it as an argument, not a summary of sections.*

{{3–5 line thesis}}

---

## SCQA narrative

### Why the customer cares
- **The opportunity (canvas box 1):** {{what the customer is trying to do; the problem in the way; the desire}}
- **Cohorts (canvas box 3):** {{which cohorts, and how the opportunity differs across them}}
- **Empathy evidence (canvas box 2):** {{what they say / think / do / feel — quotes, interviews, research; guesses marked as guesses}}
- **Pains / gains:** {{key pains today; gains a solution would unlock}}

### Why the business cares
- **Impact:** {{what this problem costs the business today}}
- **Potential:** {{the upside of solving it}}

### Competitor analysis (solutions today)

| Alternative | What it does | Strength | Gap it leaves |
|---|---|---|---|
| {{competitor / workaround}} | {{...}} | {{...}} | {{...}} |
| {{...}} | {{...}} | {{...}} | {{...}} |

---

## The opportunity
> *The thesis, tied explicitly back to the customer problem (not the solution). What is the opportunity, and why now?*

{{opportunity thesis}}

- **Market sizing (GMV / TAM):** ⚠️ _Optional — mark "Not covered this iteration" if not done._

---

## How-Might-We questions (mapped to opportunities)

| HMW | Opportunity it addresses (canvas box) |
|---|---|
| How might we {{...}}? | {{opportunity from the canvas, with its box number}} |
| How might we {{...}}? | {{...}} |

---

## HMWs stack-ranked by impact
> *Ordered to tee up ideation. Ideation itself happens off-canvas in the Solution Workflow.*

| Rank | HMW | Impact | Notes |
|---|---|---|---|
| 1 | {{highest-impact HMW}} | High | {{...}} |
| 2 | {{...}} | {{...}} | {{...}} |
| 3 | {{...}} | {{...}} | {{...}} |

---

<!--
Synthesis reminders for Claude:
- Flag gaps as "⚠️ Not yet covered — <why it matters>" rather than inventing content.
- Keep the customer the spine; the opportunity ties back to the customer problem.
- Output as a real .docx (Word heading styles, tables) — see 03-synthesise.md.
-->
