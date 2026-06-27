# Reusable Prompt Snippets

The tools and playbooks are task-specific. This folder holds the **building blocks** — snippets you paste *into* any prompt to control behavior, plus reusable context blocks you fill in once and reuse everywhere.

## Files

- [system-prompts.md](system-prompts.md) — role/system prompts that set the model up as a specific kind of PM collaborator.
- [guardrail-snippets.md](guardrail-snippets.md) — short rules you append to any prompt to stop hallucination, force citations, etc.
- [context-blocks.md](context-blocks.md) — fill-once templates (your product, your users, your audiences) that you paste into every session.

## How to use them

1. Start a session with a **system prompt** (sets the persona).
2. Paste your **context block** (product, users, constraints) so the model isn't guessing.
3. Use a tool or playbook prompt for the task.
4. Append **guardrail snippets** whenever the output will leave your hands.

Think of it as: *persona + context + task + guardrails.*
