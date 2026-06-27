# Playbook — Discovery → PRD

**Trigger:** A new initiative gets greenlit for discovery.
**Cadence:** Per initiative.
**Tools used:** [Research Synthesizer](../tools/02-research-synthesizer.md), [PRD & Spec Writer](../tools/01-prd-and-spec-writer.md), [Competitive & Market Analysis](../tools/04-competitive-and-market-analysis.md).
**Why:** Gets you from "we should look into X" to a reviewable PRD without losing the connection to evidence. The chain forces every requirement to trace back to a real user signal.

---

## Steps

1. **Frame the question (human).** Write the one-sentence problem and the riskiest assumption. Don't skip — everything downstream inherits this framing.

2. **Gather signal.** Pull existing research: past interviews, relevant triaged feedback (from the [Weekly Triage](weekly-feedback-triage.md) output), support trends, sales asks.

3. **Synthesize (Research Synthesizer).** Run the synthesis prompt across the gathered material → themes, verbatim quotes, opportunities. Demand real quotes so the PRD can cite evidence.

4. **Build the opportunity map (Research Synthesizer).** Outcome → opportunities → possible solutions, ranked by frequency × severity. Mark validated vs. assumed.

5. **Scan the landscape (Competitive Analysis).** If relevant, run a quick teardown of how others solve this — *from real source data only*. Note table stakes vs. differentiation.

6. **Decide scope (human).** ⚠️ Pick the opportunity and the cut. This is the irreducible product judgment. AI gave you the map; you choose the route.

7. **Draft the PRD (PRD Writer).** Run the PRD prompt with your chosen scope + the synthesized evidence as context. Let it mark every gap with "❓ NEEDS INPUT".

8. **Fill the gaps (human).** Answer the ❓s. Add the success metric that actually matters. Add what you know that the data doesn't.

9. **Pressure-test (PRD Writer).** Run the skeptical-reviewer prompt. Fix the top 3 weaknesses before sharing.

---

## Output

A PRD that's grounded in cited evidence, scoped by a human, and pre-hardened against the obvious objections.

## Time

A day or two instead of a week — and the synthesis is more thorough than you'd do by hand.

## Tips

- The quotes are the gold. A PRD that quotes real users survives review; one that asserts survives nothing.
- Keep synthesis and drafting as separate steps. Don't let the model jump from raw notes to PRD — you lose the evidence trail.
