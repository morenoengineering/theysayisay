---
name: technical-writing
description: Write or revise argument-driven technical prose (design docs, RFCs, proposals, papers, PR descriptions, ADRs, blog posts, review comments) using the they-say/I-say structure. Use when asked to write, draft, edit, or strengthen a technical document or its argument.
---

# Technical writing

Based on *They Say / I Say* (Graff & Birkenstein), ch. 1, 4–10 and 16. Good technical writing is a **response**: it states what others believe or do, then what you claim, why, and why it matters.

## Steps

1. **Open with the they-say.** Start from what the reader already believes or does: the current system, the standard approach, prior work, the team's assumption, the bug report. Keep it short and get to your claim fast. If nothing is being said yet, use the implied or "standard" view: *"The obvious approach is X."* Done when a reader new to the topic knows what you are responding to by the end of the first paragraph.
2. **State the I-say in one sentence**, and say how it relates to the they-say:
   - Disagree, with reasons: *"X assumes A, but our traces show B, so X fails when..."*. A contradiction without reasons is not an argument.
   - Agree with a difference: *"X is right about A; it also implies B, which nobody has acted on."*
   - Both: *"X holds for read-heavy loads but breaks for writes, because..."*
   Done when the claim is specific enough that someone could disagree with it.
3. **Mark the voices.** Readers must always know whose view a sentence states. Attribute the others' views (*"the current design assumes..."*, *"proponents of X argue..."*) and own yours (*"I propose...", "we measured..."*). Use "I" or "we" freely where it clarifies who claims what.
4. **Summarize opponents fairly.** Describe the alternative the way its best advocate would (see the `technical-summary` skill). A strawman makes your claim look weak, not strong.
5. **Bring in the naysayer.** Name the strongest objection a skeptical reviewer would raise, in its strongest form, then answer it: refute it, concede and narrow your claim, or accept it as a known limitation. Typical naysayers: cost, complexity, migration risk, "we tried that", a missing baseline, a workload you didn't test. Done when the top objection a skeptical reviewer would raise is answered in the text.
6. **Answer so-what and who-cares.** Name who is affected and what changes for them: latency for users, on-call load, cost, unblocked work, a wrong belief corrected. Say it explicitly, early, and again in the conclusion.
7. **Calibrate claims to evidence** (the sciences chapter). Say what the data *mean*, then hedge exactly as much as the evidence warrants: *"the data suggest"* for correlation or small samples, *"shows"* for demonstrated results, *"we expect"* for predictions. State the conditions under which the result holds.
8. **Connect the parts.** Each paragraph should follow from the last. Use transitions that name the logical relation (*therefore, however, for example, in contrast, as a result*), pointing words that refer back (*this bottleneck, that tradeoff*), and repeat key terms exactly instead of swapping in synonyms. In technical writing a new word reads as a new concept.
9. **Add metacommentary.** Tell the reader how to read the document: a title that states the claim, a one-paragraph summary up front, roadmap sentences (*"Section 3 covers the migration plan"*), and clarifiers (*"this is not a proposal to drop X, only to stop defaulting to it"*). Done when someone who reads only the title and first paragraph knows the claim and the ask.
10. **Write plainly.** Use the plainest word that is exact. Mix in direct, everyday phrasing when it makes a point clearer; formal does not mean dense.

## Revision checklist

Run when revising, yours or someone else's draft. Report each item as pass/fail with the fix:

- They-say present and in the first paragraph?
- I-say stated in one disputable sentence?
- Every sentence attributable to a clear voice?
- Strongest objection raised and answered?
- So-what names an audience and a consequence?
- Claims hedged to match evidence?
- Key terms consistent; transitions name the relation?
- Title and opening carry the claim?

## Template skeleton

```
Title: <the claim, not the topic>

<They-say: the current belief/system/approach, 1–3 sentences.>
<I-say: your claim and how it relates, 1 sentence.> <So-what, 1 sentence.>

## Why <claim>          — reasons and evidence, hedged to fit
## Alternatives         — fair summary of each, and why not
## Objections           — the naysayer, answered
## What changes         — who is affected, the ask, next steps
```
