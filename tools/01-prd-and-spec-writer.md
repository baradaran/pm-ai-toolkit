# Tool 1 — PRD & Spec Writer

**Use it for:** turning a rough idea, a Slack thread, or a meeting note into a structured PRD, one-pager, or technical RFC.

**Why it matters:** The blank page is where specs die. AI gets you to a structured 70% draft in minutes. Your job becomes editing and adding judgment — not formatting.

**What to keep human:** the actual decisions (scope cuts, trade-offs, success metrics that matter), and anything about *why* this is worth doing.

---

## Prompt: Draft a PRD

```
You are an experienced product manager. Write a PRD from the rough input below.

Use this structure:
1. Problem — who has it, how painful, evidence we have
2. Goal & success metrics — one primary metric, 2-3 guardrails
3. Non-goals — what we are explicitly NOT doing
4. Proposed solution — high level, then key user flows
5. Requirements — functional, prioritized as Must / Should / Could
6. Open questions & risks
7. Rollout — phasing, what's behind a flag, how we measure

Rules:
- If something is missing from my input, write "❓ NEEDS INPUT: <question>" instead of inventing it. Do not make up metrics or evidence.
- Keep it tight. A PRD is a decision tool, not an essay.
- Flag any requirement that smells like scope creep.

Rough input:
{{paste your idea, notes, thread, or bullet points}}

Context:
- Product: {{what your product is}}
- Users: {{who this is for}}
- Constraints: {{timeline, tech, team size}}
```

## Prompt: One-pager (for exec buy-in)

```
Turn the input below into a one-page proposal for a busy executive.
Structure: The ask (1 sentence) → Why now → What we'll do → What we need → What success looks like.
Lead with the ask. No jargon. Max 350 words. Mark any unsupported claim with ❓.

Input: {{paste PRD or notes}}
```

## Prompt: Pressure-test a draft

```
You are a skeptical staff engineer and a skeptical sales lead reviewing this spec.
List the 5 hardest questions each would ask, and where the spec is weakest.
Then suggest the 3 highest-leverage edits. Be blunt.

Spec: {{paste draft}}
```

---

## Tips

- Always include the "❓ NEEDS INPUT" rule. It stops the model from hallucinating evidence and metrics — the #1 PRD failure mode.
- Run the **pressure-test** prompt before you share. It catches the obvious gaps reviewers would catch anyway.
- Keep your product/users/constraints context in a saved snippet so you paste it every time.
