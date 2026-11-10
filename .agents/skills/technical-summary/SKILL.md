---
name: technical-summary
description: Summarize technical material (papers, specs, threads, codebases, meetings, incident reports) faithfully, and quote it correctly. Use when asked to summarize, give a TL;DR, write an abstract or related-work section, or report what a source says.
---

# Technical summary

Based on *They Say / I Say* (Graff & Birkenstein), ch. 2–3 and 5.

## Steps

1. **Play the believing game.** Before judging, restate the source as its author would: their problem, their claim, their reasons, in their strongest form. Test: would the author sign off on this paragraph? Read the source with the `technical-reading` steps first if you haven't identified its they-say and I-say.
2. **Pick the focus from your purpose.** A summary serves the point you (or the user) will make next. Keep what bears on that point; drop the rest. Done when every sentence in the summary earns its place for that purpose, and nothing that would change the reader's picture of the source has been dropped.
3. **Write it with precise verbs.** Use a verb that names the action the author takes: *argues, shows, measures, proposes, assumes, concedes, rejects, extends, warns, recommends*. "Says" or "talks about" hide whether the source proved something or merely asserted it. Match the verb to the evidence: *measures* only for measurements, *shows* only for demonstrated results, *claims* for unverified assertions.
4. **Keep the source's terms.** Use their names for things (system names, metrics, definitions). If you translate jargon, give the original term once.
5. **Mark the voices.** Every sentence is either the source's view or yours; the reader must be able to tell which, every time. Attribute with *"the authors report...", "according to the spec..."*; label your own view with *"I'd note...", "this summary's reading is..."*.
6. **Quote sparingly, and sandwich every quote.** Quote only when the exact wording matters (a definition, a guarantee, a surprising claim, something you'll dispute). Before the quote: who says it and in what context. After: what it means and why it matters here. A quote with no explanation after it is unfinished.

## Failure modes to check before finishing

- **Closest-cliché drift**: the summary says what sources on this topic *usually* say instead of what this one says. Fix: check each claim against the actual text.
- **Strawman**: the source sounds weaker or sillier than it is. Fix: redo step 1.
- **List summary**: a sequence of "then they say... then they say..." with no thread. Fix: lead with the central claim, then hang the supporting points from it.
- **Unattributed opinion**: your judgment reads as the source's. Fix: step 5.

## Shape

- TL;DR: one sentence of the form *"[Source] [precise verb] [claim], in response to [what it pushes against]."*
- Longer: TL;DR first, then key evidence, then limitations the source states, then (labeled) your assessment.
