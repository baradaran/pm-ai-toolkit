# Tool 5 — Stakeholder Comms

**Use it for:** status updates, exec summaries, release notes, launch announcements, and the "rewrite this for a different audience" task.

**Why it matters:** A huge chunk of the PM job is translation — saying the same thing to engineers, execs, sales, and customers in the language each one cares about. AI is excellent at re-leveling and re-framing existing content. You already have the facts; the tax is the rewriting.

**What to keep human:** the facts, the commitments, and the judgment about what to *not* say. AI doesn't know your politics.

---

## Prompt: Weekly status update

```
Write a weekly product status update from my raw notes.
Audience: {{eng team / cross-functional / leadership}}.
Structure: 🟢/🟡/🔴 status → What shipped → In progress → Blocked/risks (with the ask) → Next week.
Tone: factual, concise, no fluff. Surface risks early, don't bury them.
Keep all dates and numbers exactly as I wrote them — do not invent progress.

Raw notes: {{paste}}
```

## Prompt: Exec summary (re-level up)

```
Compress the update below into a 5-bullet exec summary.
Lead with outcomes and decisions needed, not activity. Each bullet ≤ 20 words.
End with "Decisions needed from you:" listing any asks. If there are none, say "FYI only".

Update: {{paste detailed update}}
```

## Prompt: Release notes (3 audiences)

```
From this changelog, write release notes in 3 versions:
1. Customer-facing — benefit-led, friendly, no internal jargon.
2. Sales/CS enablement — what changed, why customers care, what to say.
3. Internal — terse, technical, with flags/links.
Keep feature names and dates exactly as given.

Changelog: {{paste}}
```

## Prompt: "Explain it to X"

```
Rewrite the message below for {{audience: a skeptical CFO / a new engineer / an enterprise customer}}.
Match their concerns and vocabulary. Same facts, different framing. Note what you chose to emphasize and why.

Message: {{paste}}
```

---

## Tips

- **Lock the facts.** The "keep dates/numbers exactly, don't invent progress" rule prevents the most embarrassing failure: an AI-inflated status update.
- Status updates live and die on surfacing risk early. Keep the 🟢🟡🔴 + explicit "the ask" structure.
- For execs, force the "decisions needed" footer — it turns a report into something actionable.
- Save your audience descriptions (your CFO's actual hot buttons, etc.) as reusable snippets.
