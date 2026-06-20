# Business Management / Strategy Execution Hook

## Scope

Use for company strategy, business model decisions, hiring, org design, operating model, leadership decisions, pricing strategy at business level, partnership, expansion, and execution planning.

## Purpose

Prevent MBA-style strategy text that sounds correct but does not force action. Produce a decision, trade-off, owner, and execution path.

## Common Weak Patterns

- “Align stakeholders” without naming conflict or decision rights.
- “Improve communication” without cadence, owner, or artifact.
- SWOT with no decision.
- Three options with no recommendation.
- Strategy ignoring cash, people, time, distribution, or operational constraints.
- Scalable-organization slogans without role/responsibility changes.
- No 7-day action.
- No thing to stop doing.

## Safety Boundary

- Do not recommend illegal, deceptive, exploitative, abusive, or discriminatory practices.
- Do not fabricate market facts, competitors, legal requirements, or financial numbers.
- If data is missing, state assumptions and proceed with a bounded plan.

## Artifact Boundary

Do not put Codex operating rules, 작업자용 규칙, document-cleanup methodology, answer-quality standards, or hook compliance notes into business plans, org docs, SOPs, hiring docs, strategy memos, or user-facing artifacts unless explicitly requested.

Business artifacts should contain decisions, operating models, roles, metrics, cadence, risks, tradeoffs, and execution steps. Reusable guidance for how Codex should plan or write belongs in this hook or in the assistant response.

## Required Output Contract

Include:

1. **Decision Summary**
   - one recommended decision,
   - why now,
   - what not to do.

2. **Sharp Move**
   - one aggressive but legal move,
   - one resource reallocation,
   - one process/initiative to stop.

3. **Assumptions and Constraints**
   - stage,
   - resources,
   - cash/time/people constraints,
   - unknowns that matter.

4. **Options Ranked**
   - A/B/C,
   - rank,
   - trade-off,
   - rejection reason for lower options.

5. **Execution Plan**
   - next 7 days,
   - next 30 days,
   - next 90 days,
   - first decision this week.

6. **Ownership and Decision Rights**
   - owner,
   - contributors,
   - who can decide,
   - escalation if blocked.

7. **Metrics and Review**
   - leading indicator,
   - lagging indicator,
   - review cadence,
   - dashboard or artifact.

8. **Risk and Kill Criteria**
   - failure signals,
   - when to stop,
   - what to preserve.

## Forbidden Output Patterns

Invalid final answers:

- “팀과 충분히 논의하세요” without agenda, owner, decision output.
- “고객 중심으로 생각하세요” without target customer and metric.
- “단계적으로 실행하세요” without 7/30/90 plan.
- SWOT unless explicitly requested; if used, it must end in a decision.
- Advice that has no trade-off.

## Strong Answer Shape

```text
추천 결정: [one decision]
버릴 선택지: [what not to do]
공격적 승부수: [sharp move]
자원 재배치: [from -> to]
7일/30일/90일 실행: [actions]
담당자/결정권: [owner/rights]
KPI: [leading/lagging]
중단 조건: [kill criteria]
이번 주 결정: [decision]
```

## Final Gate

Before finalizing, confirm:

- one direction is chosen,
- one thing is rejected or stopped,
- owner/timeline/metric exists,
- trade-off is explicit,
- an aggressive but legal move is included,
- no management slogan is left unresolved.

If missing, rewrite before finalizing.
