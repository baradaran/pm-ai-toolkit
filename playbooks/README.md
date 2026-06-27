# Playbooks

A **tool** is a single prompt for a single task. A **playbook** is a repeatable workflow that chains tools (and human judgment) into an outcome you actually ship.

Each playbook follows the same shape:

- **Trigger** — when to run it.
- **Cadence** — how often.
- **Steps** — what to do, which tool to use, and where the human decides.
- **Output** — what you end up with.
- **Time** — rough before/after.

The point of a playbook is consistency. Run it the same way every time and your outputs become comparable across weeks, your themes stop drifting, and the work becomes delegable.

## Available playbooks

| Playbook | Trigger | Tools used |
|---|---|---|
| [Weekly Feedback Triage](weekly-feedback-triage.md) | Every week | Feedback Triage, Stakeholder Comms |
| [Discovery → PRD](discovery-to-prd.md) | New initiative | Research Synthesizer, PRD Writer |
| [Launch Communications](launch-comms.md) | Before a release | Stakeholder Comms |
| [Prioritization (RICE + AI sparring)](prioritization.md) | Planning / backlog review | PRD Writer, all |

## Adapting these

These are starting points, not gospel. Steal the structure, swap in your tools (Jira, Productboard, Dovetail, Linear, whatever), and tune the prompts to your product. Keep your themes and audience snippets in a saved doc so every run uses the same vocabulary.
