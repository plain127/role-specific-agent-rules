# Research / Analysis Rigor Hook

## Scope

Use for research tasks, literature reviews, market research, competitive analysis, technical/industry investigation, claim verification, report writing, and reasoning audits.

## Purpose

Prevent smooth but weak analysis: unsupported claims, vague citations, overgeneralization, cherry-picking, false certainty, or confirmation-only reasoning.

## Common Weak Patterns

- “Studies show” without source.
- Summary without claim-level evidence.
- Only confirming the user's preferred thesis.
- No counterargument or disconfirming evidence.
- No source quality ranking.
- No date/freshness control.
- Turning weak evidence into broad conclusion.
- Mixing fact, inference, assumption, and opinion.
- No uncertainty level or verification path.

## Safety Boundary

- Do not fabricate sources, quotes, papers, statistics, benchmarks, or dates.
- If current information may have changed, verify before stating it as fact.
- If evidence is insufficient, say what is missing and provide an exact research plan.

## Required Output Contract

Include:

1. **Research Question**
   - exact question,
   - scope,
   - excluded areas.

2. **Claim Map**
   - claim,
   - evidence,
   - source/data basis,
   - confidence.

3. **Evidence Quality**
   - A: primary source, official data, paper, filing,
   - B: reputable secondary analysis,
   - C: media/report/blog with unclear methodology,
   - D: anecdote/community claim.

4. **Fact / Inference / Assumption Split**
   - facts verified,
   - inferences made,
   - assumptions requiring confirmation.

5. **Counterevidence**
   - strongest opposing view,
   - what would change the conclusion.

6. **Conclusion**
   - clear answer,
   - confidence level,
   - practical implication.

7. **Verification Path**
   - sources to check,
   - data needed,
   - next research step.

## Source Rule

No source, no factual certainty.

If browsing/source access is unavailable, label claims as:

- provided context,
- prior knowledge,
- inference,
- assumption,
- needs verification.

## Artifact Boundary

Do not put Codex operating rules, 작업자용 규칙, research-process methodology, answer-quality standards, or hook compliance notes into research reports, evidence tables, briefs, memos, or user-facing artifacts unless explicitly requested.

Research artifacts should contain question, sources, evidence, confidence, inference, contradiction, recommendation, and remaining unknowns. Reusable guidance for how Codex should research or write belongs in this hook or in the assistant response.

## Forbidden Output Patterns

Invalid final answers:

- unsupported “facts,”
- fake citations,
- generic summaries with no evidence ranking,
- only one-sided confirmation,
- conclusions stronger than evidence,
- “more research is needed” with no exact research task.

## Strong Answer Shape

```text
결론: [clear answer]
신뢰도: [high/medium/low + why]
Claim map:
- Claim 1: [evidence/source quality/confidence]
- Claim 2: [evidence/source quality/confidence]
사실/추론/가정: [split]
반대 근거: [strongest counterpoint]
실무적 의미: [what to do]
검증 경로: [next checks]
```

## Final Gate

Before finalizing, confirm:

- facts and inferences are separated,
- source/data quality is ranked,
- counterevidence is included,
- conclusion confidence matches evidence,
- verification path is concrete,
- no fake or vague citations are present.

If missing, rewrite before finalizing.
