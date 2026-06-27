# Playbook — Prioritization (RICE + AI sparring)

**Trigger:** Backlog review, planning, or roadmap building.
**Cadence:** Per planning cycle.
**Tools used:** all — but mostly AI as a *sparring partner*, not a decider.
**Why:** Prioritization is where PMs are most tempted to "let AI decide" — and most wrong to. The decision is judgment + strategy + politics, none of which the model has. Use AI to make your reasoning explicit and to attack it, not to produce the answer.

> ⚠️ **Read this first.** Do not ask AI to "rank my backlog" and ship the result. The numbers will look authoritative and be meaningless — the model can't know your reach, your strategy, or your constraints. Use it to *structure and stress-test* your own scoring.

---

## Steps

1. **List candidates (human).** The items up for prioritization, each with a one-line description.

2. **Draft RICE inputs (human, AI-assisted).** For each item, you provide Reach, Impact, Confidence, Effort. Use AI to *challenge* your inputs:

   ```
   For each item below I've estimated RICE (Reach, Impact 0.25-3, Confidence %, Effort person-months).
   Don't change my numbers. Instead, for each: name the single biggest reason my estimate could be wrong, and what evidence would resolve it. Flag any Confidence above 80% that isn't backed by data I mentioned.
   Items: {{paste items + your scores + the evidence you have}}
   ```

3. **Compute (mechanical).** RICE = (Reach × Impact × Confidence) ÷ Effort. A spreadsheet does this; AI doesn't need to.

4. **Stress-test the ranking (AI sparring).**

   ```
   Here's my prioritized list with rationale. Play three critics:
   a skeptical exec, a frustrated customer, and a pragmatic eng lead.
   What does each think we got wrong? What's the strongest case for moving something up or down? What are we ignoring that isn't on the list at all?
   List: {{paste ranked list + rationale}}
   ```

5. **Check for strategy fit (human).** RICE optimizes for local value. Manually overlay: does the top of the list move our actual strategic goal this cycle? Reorder if not. **Strategy beats score.**

6. **Decide and document (human).** Lock the priorities. Write the *why* — especially where you overrode the score. That rationale is what you'll defend later.

---

## Output

A prioritized list where every ranking has a stated rationale, the high-confidence claims are evidence-backed, and the obvious objections are already answered.

## Time

A couple of focused hours. The AI steps make your reasoning legible — the lasting value is the documented rationale.

## Tips

- **AI never sets the priority.** It pressure-tests yours. Keep that line bright.
- Watch the confidence inflation. The step-2 prompt exists specifically to catch "90% confident" estimates with no data behind them.
- Frameworks (RICE, here) are scaffolding for judgment, not a substitute. The override step is the most important one.
