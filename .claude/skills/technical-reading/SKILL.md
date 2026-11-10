---
name: technical-reading
description: Read a technical text (paper, RFC, design doc, PR, postmortem, docs) for the conversation it joins. Use when asked to read, analyze, critique, or explain what a technical document argues, or before summarizing or responding to one.
---

# Technical reading

Based on *They Say / I Say* (Graff & Birkenstein), ch. 14 and 16: every text is a **response**. You understand it only when you can name what it responds to.

## Steps

1. **Find the they-say.** Locate the view, baseline, prior system, or assumption the author is pushing against. Look in the intro, "related work", "motivation", "background", the problem statement, or a rejected-alternatives section. If it is implicit, reconstruct it: what would a reader believe before reading this? Done when you can write: *"Before this, people assumed/did X."*
2. **Find the I-say.** State the author's own claim in one sentence, in the form *"The author argues Y, in response to X."* Done when Y is a falsifiable or checkable claim, not a topic ("about caching" fails; "a write-through cache cuts p99 by 40% under this workload" passes).
3. **Classify the response** to X: disagree (X is wrong, with reasons), agree with a difference (X holds, plus a new point), or both (X holds in case A, fails in case B).
4. **Separate the voices.** Mark every sentence that reports someone else's view (other papers, a "common belief", a strawman) versus the author's own. Signal phrases: *"it is often assumed", "prior work shows", "one might expect", "however", "we find"*. A claim the author *reports* is not one the author *holds*; most misreadings come from mixing them up.
5. **Find the naysayer.** Locate where the author answers objections: limitations, threats to validity, "one might object", benchmarks they concede. Note any objection they skip.
6. **Find the so-what.** Who should change what they do if Y is true, and why now? Done when you name a concrete audience and a concrete consequence.
7. **Check the evidence against the claim.** Do the data support Y as strongly as stated, or only a narrower Y? Note overreach, missing baselines, and conclusions that go beyond the results.

## Output

Report, in this order: they-say (X), I-say (Y), response type, evidence and its fit, objections handled and skipped, so-what. Quote the author's exact words for Y when the wording matters. Then give your own assessment, labeled as yours.

For a summary of the text, continue with the `technical-summary` skill.
