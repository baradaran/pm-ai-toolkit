# Tool 3 — Feedback Triage

**Use it for:** classifying, deduping, severity-scoring, and routing incoming feedback at scale — support tickets, feature requests, bug reports, NPS comments, app-store reviews, sales objections.

**Why it matters:** PMs drown in feedback. The bottleneck isn't collecting it — it's deciding what deserves attention. Triage is high-volume and rule-based, which makes it the best-fit AI task in the whole PM workflow. Get this running and you reclaim hours every week and stop missing the signal in the noise.

**What to keep human:** the final prioritization call. Triage *organizes* the queue; you decide what gets built.

---

## The triage model

Every incoming item gets four tags:

| Dimension | Values |
|---|---|
| **Type** | Bug · Feature request · Usability · Question · Praise · Churn risk · Other |
| **Theme** | Your product areas (e.g. Onboarding, Billing, Search, Integrations) |
| **Severity** | P0 blocker · P1 major · P2 minor · P3 cosmetic |
| **Effort signal** | Quick win · Medium · Large / unclear (rough, for routing only) |

Plus: **dedupe** (which items are the same underlying issue) and **sentiment**.

---

## Prompt: Triage a batch

```
You are a product operations analyst. Triage the feedback items below.

For EACH item return a row:
| ID | Type | Theme | Severity (P0-P3) | Sentiment | Effort signal | Dedupe group | One-line summary |

Then provide:
- DEDUPE GROUPS: cluster items that are the same underlying issue; give each group a name and count.
- TOP 5 BY VOLUME: the most-mentioned issues this batch.
- ESCALATE NOW: any P0s, churn-risk signals, or security/privacy/legal mentions — list them explicitly.

Rules:
- Severity reflects user impact, not how loudly it's phrased.
- "Churn risk" = any mention of cancelling, switching, or "deal-breaker".
- If an item is ambiguous, tag it "❓ needs human" rather than guessing.
- Don't editorialize. Just classify.

Themes to use: {{your product areas}}

Feedback items (one per line, prefix with an ID):
{{paste items}}
```

## Prompt: Weekly digest from triaged data

```
From the triaged feedback below, write a 1-page weekly feedback digest for the product team.
Sections: Headline (what changed this week) · Top 5 themes by volume + trend vs last week · New P0/P1s · Notable quotes (verbatim) · Recommended focus.
Be concise and decision-oriented.

Triaged data: {{paste table output}}
```

## Prompt: Route to owners

```
Given the triaged items and this ownership map, assign each item to an owner and suggest a next action (e.g., "create bug", "add to discovery backlog", "reply & close", "escalate").
Ownership map: {{theme → team/person}}
Items: {{paste}}
```

---

## Tips

- **Define your themes once** and reuse them every run, or your categories drift week to week and trends become meaningless.
- **Severity ≠ volume ≠ loudness.** Keep the model honest with the "impact, not phrasing" rule — the angriest ticket is often P2.
- **Escalation is the safety net.** Always include the "ESCALATE NOW" block so P0s and churn/legal signals never get buried in a batch.
- Run it on a cadence — see the [Weekly Feedback Triage playbook](../playbooks/weekly-feedback-triage.md).
- The model can't see your full backlog; the dedupe groups are within-batch. For cross-time dedupe, feed last week's group names as context.
