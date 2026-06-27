# Guardrail Snippets

Short, paste-anywhere rules that keep AI output honest and safe to ship. Append the relevant ones to any prompt — especially when the output will leave your hands.

---

## Anti-hallucination

```
Do not invent facts, numbers, quotes, names, or sources. If something isn't in the material I gave you, write "❓ NEEDS INPUT: <what you need>" instead of guessing.
```

## Force citations

```
For every claim, cite the specific source line/section it came from. If you can't cite it, don't claim it.
```

## Separate fact from inference

```
Mark each statement as [FACT] (from my data) or [INFERENCE] (your analysis). Keep them visibly separate.
```

## Lock the facts (for comms)

```
Keep all dates, numbers, names, and commitments exactly as I wrote them. Do not add capabilities, progress, or promises I didn't state.
```

## Verbatim quotes only

```
Quote source text word-for-word. Never paraphrase a quote or fabricate one. If no real quote supports a point, say so.
```

## Stay in scope

```
Answer only what I asked. Don't expand scope, add features, or solve adjacent problems unless I ask. Flag scope creep if you see it in my input.
```

## Show uncertainty

```
Rate your confidence (high/medium/low) on each conclusion and say what would raise it. Don't present a guess as a finding.
```

## Give a recommendation

```
Don't just list options. Recommend one, put it first, and state the main risk of that choice.
```

---

## Tips

- **Anti-hallucination + verbatim quotes** are the two you should reach for most. Together they make AI output verifiable.
- For anything customer-facing, always add **Lock the facts**. It prevents the classic AI-inflated release note.
- Stack snippets freely — they're additive.
