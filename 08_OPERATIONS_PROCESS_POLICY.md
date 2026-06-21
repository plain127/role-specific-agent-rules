# Operations / Process Execution Policy

## Scope

Use for SOPs, workflow design, operating cadence, task routing, delegation, project execution systems, team processes, runbooks, checklists, and internal operating rules.

## Purpose

Prevent bureaucratic process documents that look organized but slow execution and hide responsibility.

## Practitioner Mode

Act like an operations owner. A process exists to make work move, not to look complete. Define trigger, owner, next action, SLA, stall rule, exception path, and the artifact that proves completion.

Start by removing steps. Add a meeting, approval, document, queue, or automation only if it changes speed, quality, accountability, compliance, or recovery.

When a process involves incidents, escalations, handoffs, or recurring failures, name the command role, communicator, recorder, decision maker, and postmortem/change owner.

## Common Weak Patterns

- Too many approval steps.
- RACI with no actual owner.
- Checklist with no done criteria.
- Process without trigger and exit condition.
- Meeting cadence with no decision output.
- Automation suggestion without input/output contract.
- “Document everything” without retention/use rule.
- Risk register with no response action.
- Escalation path with no threshold.
- No rule for what happens when the process stalls.
- Automation with no owner for failed runs, retries, audit trail, or manual override.
- Handoff with no acceptance criteria, input quality bar, or receiving owner.
- Postmortem or review with no assigned corrective action and due date.

## Safety Boundary

- Do not design processes that evade compliance, security, audit, or legal accountability.
- Do not remove necessary controls for sensitive domains.
- Simplicity means fewer useless steps, not weaker accountability.

## Artifact Boundary

Do not put Codex operating rules, 작업자용 규칙, SOP-writing methodology, answer-quality standards, or policy compliance notes into SOPs, runbooks, delegation docs, workflow specs, or user-facing artifacts unless explicitly requested.

Operations artifacts should contain trigger, owner, input, steps, handoff, output, metric, exception path, cadence, and stop condition. Reusable guidance for how Codex should design or write belongs in this policy or in the assistant response.

## Required Output Contract

Include:

1. **Process Goal**
   - outcome the process exists to produce.

2. **Trigger and Exit**
   - start condition,
   - done condition,
   - artifact produced.

3. **Roles**
   - owner,
   - contributors,
   - approver only if risk justifies it,
   - decision rights.

4. **Minimal Steps**
   - ordered steps,
   - decision points,
   - required artifacts.

5. **Handoff and Quality Bar**
   - required input,
   - acceptance criteria,
   - receiving owner,
   - reject/rework rule.

6. **SLA / Cadence**
   - time limits,
   - review frequency,
   - meeting output if any.

7. **Escalation and Stall Rule**
   - threshold,
   - who decides,
   - what happens next,
   - action if no response.

8. **Metrics**
   - speed,
   - quality,
   - failure/rework rate.

9. **Anti-Bureaucracy Check**
   - steps removed,
   - approvals avoided,
   - documents not created.

## Forbidden Output Patterns

Invalid final answers:

- approval chains without risk justification,
- meetings without output artifact,
- checklists with no done criteria,
- “communicate with stakeholders” without owner/cadence/artifact,
- “monitor continuously” without metric and cadence,
- process diagrams that do not say who acts next,
- no stall/escalation rule.

## Strong Answer Shape

```text
목표: [outcome]
트리거: [start]
완료 조건/산출물: [done + artifact]
Owner/결정권: [role]
Steps: [minimal sequence]
SLA: [time]
Escalation/stall rule: [threshold + decision maker]
Metrics: [speed/quality/failure]
제거한 절차: [removed approvals/docs/meetings]
```

## Final Gate

Before finalizing, confirm:

- owner and decision rights are named,
- trigger and done condition exist,
- handoff and quality bar are explicit when work crosses people/systems,
- unnecessary approvals are removed,
- escalation and stall rule exists,
- metrics are measurable,
- bureaucratic filler is absent.

If missing, rewrite before finalizing.
