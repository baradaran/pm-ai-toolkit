# Playbook — Weekly Feedback Triage

**Trigger:** Standing weekly (e.g. Monday morning).
**Cadence:** Weekly.
**Tools used:** [Feedback Triage](../tools/03-feedback-triage.md), [Stakeholder Comms](../tools/05-stakeholder-comms.md).
**Why:** Turns an overflowing, anxiety-inducing feedback inbox into a ranked, deduped, routed list — and a digest the whole team reads. This is the playbook that pays for the whole repo in week one.

---

## Steps

1. **Collect (10 min).** Export the week's feedback from your sources — support tickets, NPS/CSAT comments, app reviews, sales notes, feature requests. Dump into one list, one item per line, each with an ID.

2. **Anonymize (2 min).** Strip names, emails, account IDs. Keep the substance.

3. **Triage (5 min).** Run the **Triage a batch** prompt. Feed in your fixed theme list (same every week — this is what makes trends real). Output: a classified table + dedupe groups + an "escalate now" block.

4. **Human pass on escalations (10 min).** ⚠️ *This is the human step.* Read every P0 and churn-risk item yourself. The model flags candidates; you confirm and act. Create bugs / loop in the right people now.

5. **Digest (3 min).** Run the **Weekly digest** prompt on the triaged data. Feed last week's top themes as context so it can show trend (up/down/new).

6. **Route (5 min).** Run the **Route to owners** prompt with your ownership map. Drop the actions into your tracker.

7. **Decide (human).** Skim the top themes by volume. Decide what, if anything, graduates into discovery. The queue is organized; the call is yours.

---

## Output

- A ranked, deduped, routed feedback table.
- A 1-page digest posted to the team channel.
- Escalations actioned.
- 1–3 candidate themes for discovery.

## Time

~40 min/week, most of it the human judgment steps. Doing this by hand is a half-day and you still miss things.

## Tips

- **Same themes every week.** Drift kills trend analysis.
- Keep a running doc of dedupe-group names so you can dedupe *across* weeks, not just within a batch.
- If volume is huge, triage in batches of ~50 then merge.
