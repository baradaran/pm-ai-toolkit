# Playbook — Launch Communications

**Trigger:** A feature/release is ~1–2 weeks out.
**Cadence:** Per launch.
**Tools used:** [Stakeholder Comms](../tools/05-stakeholder-comms.md).
**Why:** Every launch needs the same set of messages for different audiences. Drafting them from one source of truth keeps the facts consistent and saves the repetitive rewriting.

---

## Steps

1. **Single source of truth (human).** Write the canonical facts once: what shipped, who it's for, the benefit, the date, known limitations, links. Everything else derives from this — so it must be correct.

2. **Customer-facing release notes (Stakeholder Comms).** Run the 3-audience release-notes prompt → customer version. Benefit-led, no jargon.

3. **Sales/CS enablement (same prompt).** → the "what to say" version. Add objection handling if needed.

4. **Internal announcement (same prompt).** → terse technical version with flags and links.

5. **Exec FYI (Stakeholder Comms).** Run the exec-summary prompt → 5 bullets, outcomes first.

6. **Re-level for any special audience.** Use "Explain it to X" for a big enterprise customer or a skeptical stakeholder.

7. **Human review (⚠️ required).** Check every claim, date, and commitment against the source of truth. AI must not introduce a capability you didn't ship or a date you didn't promise. Then send.

---

## Output

A consistent comms pack — customer notes, enablement, internal note, exec FYI — all traceable to one source of truth.

## Time

~30 min instead of half a day of rewriting the same thing five ways.

## Tips

- One source of truth, always. The moment audiences diverge from different drafts, you get contradictions in public.
- Limitations are part of the message. Don't let the upbeat customer version quietly drop the known caveats.
- Save your audience profiles (your top accounts, your exec's priorities) for reuse across launches.
