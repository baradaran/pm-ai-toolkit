# Tool 6 — AI Prototyping

**Use it for:** turning a spec — or even a single sentence — into a **clickable prototype** you can put in front of users, eng, and execs, without waiting on a design/build cycle.

**Why it matters:** This is the fastest-rising AI use for PMs in 2026, and for good reason. The old loop was: idea → spec → design → eng spike → *then* feedback, costing days or weeks. AI prototyping collapses it to hours. You validate the concept *before* committing real engineering. A clickable mock kills more bad ideas (and sells more good ones) than any doc.

**What to keep human:** the product decision the prototype is meant to test, and the judgment to **never ship the generated code to production unreviewed**. These are validation artifacts, not releases.

> Tools that do this: **v0 (Vercel)**, **Lovable**, **Bolt**, **Replit**. The prompts below are tool-agnostic — paste into whichever you use.

---

## Prompt: Spec → prototype brief

```
You are a product designer. Turn the spec below into a clear prototyping brief I can hand to an AI app builder (v0/Lovable/Replit).

Output:
- Screens needed (list, in user-flow order)
- For each screen: key UI elements, the primary action, and what data it shows
- The single happy-path flow to make clickable first
- States to include: empty, loading, error, success
- What to FAKE (stub data, mocked responses) vs. what must feel real
- Explicitly OUT of scope for this prototype

Keep it to what's needed to validate the core hypothesis: {{the one thing you're testing}}.

Spec: {{paste PRD or feature description}}
```

## Prompt: Generate the prototype

```
Build a clickable prototype based on this brief. Use realistic placeholder data so it feels real in a demo. Prioritize the happy path; stub the rest. Mobile-responsive. Keep it simple and fast — this is for user validation, not production.

Brief: {{paste output from the brief prompt}}
```

## Prompt: Turn a prototype into a test plan

```
I'm about to test this prototype with {{number}} target users ({{describe them}}).
Give me: the hypothesis we're testing, 5 task-based scenarios to ask them to complete, what to watch for, and 4 non-leading questions. Keep it unmoderated-test friendly.

Prototype/flow: {{describe or paste screens}}
```

---

## Tips

- **Prototype to learn, not to ship.** Decide the *one* hypothesis first; build only enough to test it. Scope discipline is everything here.
- **Fake aggressively.** Stub data and mock responses make a prototype feel real in minutes. Don't wire up real backends to validate a concept.
- **The generated code is a draft, not a release.** If something validates, hand it to engineering as a reference — don't deploy it as-is.
- Feeds naturally from [PRD & Spec Writer](01-prd-and-spec-writer.md) and into the [Discovery → PRD](../playbooks/discovery-to-prd.md) loop: prototype *before* you finalize the spec to de-risk it.
