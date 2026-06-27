# PM AI Toolkit

> A practical, opinionated toolkit for product managers who want to actually *use* AI in the daily job — not chase hype.

This repo gives you **5 tools** (reusable prompt systems) and a set of **playbooks** for the work PMs do every week: writing specs, making sense of research, triaging feedback, sizing up competitors, and keeping stakeholders aligned.

Everything here is copy-paste ready. Drop the prompts into Claude, ChatGPT, Gemini, or whatever you use. The point isn't the tool — it's the *workflow*.

**🌐 Browsable site:** https://baradaran.github.io/pm-ai-toolkit/

---

## What PMs should actually use AI for (the argument)

There's a lot of noise about "AI for PMs." Most of it is either toy demos or tools that replace a step you didn't need help with. Here's the honest take.

**AI is genuinely good at the parts of the PM job that are high-volume, language-heavy, and judgment-light:**

- **Summarizing and clustering** — turning 200 support tickets, 12 interview transcripts, or a noisy Slack thread into themes. This is the single highest-ROI use. Do this first.
- **First drafts** — PRDs, one-pagers, release notes, status updates. AI gets you from blank page to 70%. You bring the 30% that's actually product judgment.
- **Triage and routing** — labeling, deduping, and severity-scoring incoming feedback so you spend your attention on the 10% that matters.
- **Reframing and pressure-testing** — "argue against this", "what would a skeptical exec ask", "what am I missing". AI as a sparring partner, not an oracle.

**AI is bad at — and you should NOT delegate — the core of the job:**

- Deciding *what* to build and *why* (prioritization is judgment + politics + strategy).
- Anything requiring real customer empathy or context only you have.
- Final numbers, commitments, or anything that ships to a customer without your review.

**Rule of thumb:** Use AI to compress the time between *information* and *insight*, and between *insight* and *first draft*. Keep the decisions.

### What to use *right now* (no excuses)

| If you only adopt one thing | Do this |
|---|---|
| This week | [Feedback Triage](tools/03-feedback-triage.md) — it pays for itself immediately |
| This month | [Research Synthesizer](tools/02-research-synthesizer.md) — stop hand-summarizing interviews |
| Before your next spec | [PRD & Spec Writer](tools/01-prd-and-spec-writer.md) |

---

## The 5 tools

1. **[PRD & Spec Writer](tools/01-prd-and-spec-writer.md)** — turn a rough idea into a structured PRD, one-pager, or RFC.
2. **[Research Synthesizer](tools/02-research-synthesizer.md)** — interviews, surveys, reviews, and tickets → themes, quotes, and opportunities.
3. **[Feedback Triage](tools/03-feedback-triage.md)** — classify, dedupe, severity-score, and route incoming feedback at scale.
4. **[Competitive & Market Analysis](tools/04-competitive-and-market-analysis.md)** — structured teardowns, positioning, and gap analysis.
5. **[Stakeholder Comms](tools/05-stakeholder-comms.md)** — status updates, exec summaries, release notes, and the "explain it to X" rewrite.

## The playbooks

Tools are the *what*. Playbooks are the *when and how* — step-by-step workflows that chain tools together.

- [Weekly Feedback Triage](playbooks/weekly-feedback-triage.md)
- [Discovery → PRD](playbooks/discovery-to-prd.md)
- [Launch Communications](playbooks/launch-comms.md)
- [Prioritization (RICE + AI sparring)](playbooks/prioritization.md)

See [playbooks/README.md](playbooks/README.md) for how playbooks work.

## Reusable prompt building blocks

The pattern is always **persona + context + task + guardrails**. The [prompts/](prompts/) folder holds the building blocks:

- [System prompts](prompts/system-prompts.md) — personas (Pragmatic PM, Research Analyst, Skeptical Reviewer, Comms Editor).
- [Guardrail snippets](prompts/guardrail-snippets.md) — paste-anywhere rules to stop hallucination and force citations.
- [Context blocks](prompts/context-blocks.md) — fill-once templates for your product, areas, and audiences.

---

## How to use this repo

1. Pick the tool that matches your task.
2. Copy the prompt. Fill in the `{{placeholders}}`.
3. Paste your real data (anonymize anything sensitive — see below).
4. Iterate: AI's first answer is a draft, not a verdict.

### Ground rules

- **Never paste regulated, PII, or customer-identifying data** into a tool you don't control. Strip names, emails, account IDs first.
- **Always review before it leaves your hands.** AI drafts; you ship.
- **Cite your sources.** When AI synthesizes research, make it quote the underlying data so you can verify.

---

## Contributing

Found a prompt that consistently works? Open a PR. Keep it: real-world tested, copy-paste ready, and honest about limitations.

## License

MIT — see [LICENSE](LICENSE).
