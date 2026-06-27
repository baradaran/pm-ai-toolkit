# Tool 2 — Research Synthesizer

**Use it for:** turning raw research — interview transcripts, survey open-text, app reviews, support tickets, sales call notes — into themes, supporting quotes, and prioritized opportunities.

**Why it matters:** This is the single highest-ROI use of AI for PMs. Synthesis is slow, repetitive, and exactly what models are good at. Hand-coding 15 transcripts takes a day; this takes 20 minutes and you spend the saved time on the interviews themselves.

**What to keep human:** deciding which opportunity to act on. AI surfaces the patterns; you weigh them against strategy.

---

## Prompt: Synthesize interviews into themes

```
You are a UX researcher. Analyze the raw notes/transcripts below.

Output:
1. THEMES — 4-7 recurring themes. For each: a one-line name, how many participants raised it, and a 1-sentence summary.
2. EVIDENCE — under each theme, 2-3 direct verbatim quotes with the participant ID. Do NOT paraphrase quotes. If you can't find a real quote, say so.
3. SURPRISES — anything that contradicted our assumptions.
4. OPPORTUNITIES — for each major theme, the job-to-be-done and a possible product response.
5. CONFIDENCE — note where the sample is too small to conclude.

Rules:
- Quote only what's actually in the text. Never invent a quote.
- Distinguish what users SAID from what they DID.
- Flag leading questions if you see them.

Research data:
{{paste transcripts / notes — anonymized}}
```

## Prompt: Cluster survey open-text

```
Cluster the free-text survey responses below into themes.
For each theme: a label, the % of responses it covers, a representative quote, and sentiment (positive/negative/mixed).
List anything that doesn't fit as "Other". Don't force-fit.

Responses:
{{paste open-text — one per line}}
```

## Prompt: Build an opportunity map

```
From the synthesized themes below, build an opportunity solution tree.
Desired outcome → opportunities (user needs/pains) → possible solutions.
Rank opportunities by (frequency × severity). Mark which are validated vs. assumed.

Themes: {{paste output from the synthesis prompt}}
```

---

## Tips

- **Anonymize first.** Replace names with P1, P2… and strip company/account identifiers before pasting.
- **Force verbatim quotes.** The "never invent a quote" rule is non-negotiable — it's how you keep synthesis trustworthy and verifiable.
- For large corpora, synthesize in batches of ~5 transcripts, then run a final "synthesize these summaries" pass.
- Pair this with [Feedback Triage](03-feedback-triage.md) when the source is high-volume tickets rather than interviews.
