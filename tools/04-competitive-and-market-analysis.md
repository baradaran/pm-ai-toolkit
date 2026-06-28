# Tool 4 — Competitive & Market Analysis

**Use it for:** structured competitor teardowns, positioning maps, feature-gap analysis, and turning scattered market notes into a coherent view.

**Why it matters:** PMs are expected to "know the landscape" but rarely have time to do it rigorously. AI gives you structure and speed for the synthesis. It does **not** give you facts — so this tool leans hard on *you supplying the data* and the model *organizing* it.

**What to keep human — and this one is critical:** *As of June 2026 (this review), and consistent with the latest reviews,* models without live, cited retrieval will confidently hallucinate competitor features, pricing, and funding. **Don't trust a model's unaided recall of facts about specific companies** — treat that as today's reality, not a permanent verdict (retrieval and grounding are improving quickly). Either way, the safe workflow is the same: feed it real data you've gathered (their site, G2 reviews, pricing page) and have it *structure* that, and verify everything that ships.

---

## Prompt: Competitor teardown (from data you provide)

```
You are a competitive intelligence analyst. Using ONLY the source material I paste below, build a teardown of {{competitor}}.

Structure:
- Positioning — who they target, their core promise (quote their own words)
- Key capabilities — what they do, mapped to our product areas: {{your areas}}
- Pricing & packaging — as stated in the source
- Strengths / weaknesses — based on the reviews provided
- Where they beat us / where we beat them

Rules:
- Use ONLY the pasted source. If something isn't in it, write "not in source" — do not fill from memory.
- Separate facts (from source) from inferences (your analysis), and label inferences.

Source material:
{{paste their pricing page, homepage copy, G2/Capterra reviews, etc.}}
Our product: {{describe}}
```

## Prompt: Feature-gap matrix

```
Build a feature comparison matrix.
Rows = capabilities (use my list). Columns = us + the competitors below.
Fill each cell from the source data I provide: ✅ full / 🟡 partial / ❌ none / ? unknown.
Then: list the 3 gaps where we're behind that matter most for {{target segment}}, and 3 where we lead.
Mark every "?" — don't guess.

Capabilities: {{list}}
Source data per competitor: {{paste}}
```

## Prompt: Positioning sharpener

```
Given our product and the competitive set below, draft 3 distinct positioning statements
(format: For [segment] who [need], [product] is the [category] that [unique value], unlike [alt] which [gap]).
For each, note the segment it wins with and the risk. Then recommend one.

Us: {{paste}}
Competitors & their positioning: {{paste}}
```

---

## Tips

- **The cardinal rule:** the model organizes data, it does not supply it. The "ONLY the pasted source" constraint is what keeps this tool from becoming a confident liar.
- Gather sources first: pricing pages, homepage copy, recent G2/Capterra reviews, changelogs. Paste those in. That's where the real signal is anyway.
- If you use a model with live web access, still demand citations and click through them. "It said so" is not analysis.
- Re-run the teardown quarterly; competitors move.
