# Software Design and Code Implementation Hook

## Scope

Use this hook for software architecture, system design, code implementation, refactoring, debugging, test design, API design, data modeling, ML/LLM system implementation, repository review, logging, exception handling, fallback design, and technical documentation.

This is a Markdown harness, not an executable Codex hook. It must not replace or modify existing executable hooks. If `.codex/policy/simple-implementation.md`, `.codex/hooks.json`, `.codex/hooks/*.py`, or executable hook warnings exist, treat them as stronger repository-specific policy.

## Purpose

Prefer simple, verifiable implementation over excessive safety machinery.

The goal is to prevent outputs that technically work but are weak in practice: defensive, responsibility-avoiding, over-abstracted, over-logged, over-fallbacked, hard to maintain, or unclear as a product system.

Simplicity must not weaken authentication, authorization, validation, data integrity, payment, accounting, audit, privacy, migration, idempotency, or legal requirements.

## Common Weak Patterns

- Defensive implementation: excessive checks, catches, logs, validation layers, and fallback branches.
- Responsibility-avoidance design: code that hides failure instead of surfacing clear contracts and boundaries.
- Speculative architecture: interface, strategy, factory, base class, plugin, provider, adapter, registry, or abstraction before real need.
- Distributed spaghetti: many tiny wrappers, helpers, managers, and services that force deep call tracing.
- Failure masking: catch, log, and return default/null/empty collection/false.
- Catch-all sprawl: broad exception handling inside domain, service, repository, utility, parser, mapper, or model layers.
- Fallback chains: multi-step fallback paths that make outcomes unpredictable and hide root causes.
- Logging noise: function entry/exit logs, loop logs, trivial branch logs, raw payload logs, or high-cardinality labels.
- Rule explosion: growing condition trees for classification, ranking, priority, or ambiguous judgment when model/evaluation/hybrid design should be considered.
- Core-product avoidance: building UI shell, storage polish, schemas, broad data plumbing, guardrails, mocks, wrappers, or tests while postponing the differentiating product behavior.
- AI/ML-product avoidance: building UI, schemas, storage, dispatchers, guardrails, mocks, wrappers, or tests while postponing the model/agent call, inference, output parsing, and product action loop.
- Easy-test bias: choosing work because it is simple to unit test instead of because it proves the product's real behavior.
- Scope drift: unrelated refactors, formatting sweeps, renames, file moves, dependency additions, or broad rewrites.
- Test avoidance: skipping necessary verification or adding safety-looking code instead of focused verification. This does not mean forcing tests for early AI/ML core-loop slices where live/manual smoke traces are the better first verification.
- Documentation bloat: comments and docs that repeat code, create liability-style prose, or obscure the real decision.

## Required Output Contract

For implementation work, include:

1. Minimal change plan
2. Files to modify
3. Concrete implementation steps or patch intent
4. Verification command, smoke run, type check, lint check, focused script, or reproducible manual check. Use a test path only when tests are actually the right verification tool.
5. Summary of what changed and why
6. Material assumptions or limitations only when they affect behavior

For design/review work, include:

1. Primary recommendation
2. Rejected alternative and why it is worse now
3. Simplest viable design path
4. Hard invariants and risk boundaries
5. Verification strategy
6. Smallest next implementation step

For debugging work, include:

1. Observed failure
2. Most likely cause
3. Minimal verification command or inspection path
4. Smallest fix first
5. What would justify a broader rewrite

## Strong Answer Shape

A strong answer must be direct and operational:

1. State the chosen approach.
2. State what will not be added.
3. Explain the minimum change boundary.
4. Identify the verification path.
5. Mention only material risks.
6. End with concrete next action or completed-change summary.

Do not give equal-weight option lists when the task needs implementation or decision. Rank or choose.

## Basic Design Rules

- Solve the current requirement first.
- For product work, identify and implement or preserve the differentiating core behavior before support structure.
- Use the smallest design that makes the current behavior correct and verifiable.
- Do not add future-proofing unless the current architecture, framework convention, explicit user request, or at least two real implementations justify it.
- If there are fewer than two real implementations, defer new abstraction.
- Prefer existing project patterns, but do not use them as an excuse to add needless layers.
- Keep changes small, local, and reversible.
- Do not add dependencies without explicit approval or a clear reason existing tools cannot solve the task.
- Do not silently expand scope beyond the current ticket.
- Do not perform unrelated refactors, formatting sweeps, renames, file moves, broad rewrites, or dependency changes as part of a narrow task.

## Core Product Rules

- Every product starts from its differentiating behavior, not from support structure.
- Non-AI examples: chat app -> send/receive messages first; accounting app -> transaction classification and totals first; notes app -> create/edit/search notes first; ecommerce -> product-to-cart-to-order flow first.
- UI shell, storage polish, schemas, broad data plumbing, guardrails, mocks, wrappers, and tests come after the core behavior is visible enough to evaluate.
- If a ticket only makes support structure look complete, pair it with the product-core ticket that uses it or state why the core already exists.

## Exception Handling Rules

- Do not catch what cannot be recovered locally.
- Catch concrete exceptions only.
- Catch-all belongs only at process, HTTP, CLI, queue/job, scheduler, webhook, or worker boundaries.
- Do not add catch-all inside domain service, repository, utility, parser, mapper, model, or core business logic.
- Do not use empty catch blocks, `except: pass`, `except Exception: pass`, or catch-and-rethrow-only blocks.
- Do not catch, log, and return default/null/empty collection/false unless the product contract explicitly defines that behavior.
- Use `finally`, `using`, `defer`, or context managers for resource cleanup.
- When converting exceptions into domain errors, preserve the meaningful cause and boundary semantics.

## Logging Rules

Log only when the log supports operation, debugging, audit, or state reconstruction.

Allowed durable logs:

- meaningful state transition,
- external call boundary,
- retry start/end,
- final failure,
- audit/security event,
- irreversible business event.

Forbidden durable logs:

- function entry/exit,
- trivial branches,
- loop internals,
- routine data flow,
- duplicate logs in the same error chain,
- raw payloads,
- secrets, tokens, passwords, cookies, sessions, authorization headers,
- high-cardinality identifiers as metric labels.

If payload visibility is needed, log schema summary, length, hash, type, status code, or redacted diagnostic fields only.

## Fallback Rules

- Multi-stage fallback is forbidden unless explicitly requested or required by an existing production contract.
- One fallback path must include trigger, trade-off, test, and removal condition.
- If uncertain, prefer explicit failure or upper-boundary decision over silent default.
- Fallback must be a defined degraded mode, not a way to make failure look like success.
- Do not add “log and continue” fallback unless the operation is explicitly best-effort and the loss is acceptable.

## Function and Class Rules

- One function should perform one meaningful transition.
- Do not create chains of tiny wrapper functions.
- Do not add helper/manager/service/util files that only delegate.
- Split large functions only when the conceptual boundary becomes clearer.
- Avoid 5-line wrappers that increase call depth without naming a real concept.
- Add classes only for real state, invariant, lifecycle, or polymorphism.
- Prefer stateless functions and explicit data flow when possible.
- Optimize for the reader understanding the flow without jumping through many files.

## Rule-Based vs AI/ML Rules

- Hard invariants such as law, security, authorization, accounting, payment, privacy, and data integrity belong in explicit rules.
- Classification, ranking, recommendation, priority, and ambiguous judgment should not grow into endless rule trees.
- If rules exceed roughly five meaningful branches or exceptions keep growing, consider feature/model/hybrid/evaluation design.
- For model/LLM use, define input contract, output contract, evaluation metric, failure boundary, monitoring path, and human review threshold when needed.
- Do not replace model judgment with a brittle rule tree merely because rules feel safer.
- Do not replace hard invariants with model judgment merely because models feel more flexible.
- If a feature can plausibly be implemented by deterministic code or by AI/ML, compare operations, economics, latency, quality, maintainability, and failure cost before choosing. Do not silently exclude AI model use just because deterministic code is familiar. If AI/ML is not used, state the short reason.

## AI/ML/Agent Product Rules

- If the product value depends on AI/ML, implement the real core function first: product input/context -> prompt, feature packet, or context packet -> open-source model, frontier model, ML/DL model, model API, or local agent CLI call -> raw output capture -> parsed output/decision -> product action.
- Do not treat the model or agent as a later dependency after UI, types, storage, dispatchers, validators, guardrails, wrappers, and tests. Those are support structures; the model/inference/prompt/run/parse/action loop is the product core.
- A UI, data model, action schema, dispatcher, memory store, guardrail, or event log ticket is incomplete unless the creator, prompt/features, execution route, parser, and downstream action are known or explicitly ticketed next.
- Prompt text, feature extraction, context assembly, model choice, inference route, output contract, parser boundary, raw log/reference, and action dispatch are first-class implementation artifacts.
- Prefer one thin vertical slice that actually calls the model, model API, or Codex/Claude/Antigravity agent and changes product state over many polished scaffolding slices that never invoke the model.
- For non-AI feature requests, actively consider whether a model-based approach is operationally, economically, or qualitatively better than deterministic code. Choose after comparison, not by defaulting away from AI. If deterministic code is chosen, state the short reason.
- Do not hide behind mocks. Use mocks only for narrow deterministic boundaries after a real loop exists or when external execution is impossible in the current environment.

## Documentation and Review Rules

- Documentation should focus on why, constraints, verification, and runbook-relevant behavior.
- Do not add comments that merely restate code.
- Do not write liability-style prose that obscures the actual decision.
- PR/change summaries should focus on one change, its verification, and its remaining material limits.
- Style preferences are secondary to maintainability, readability, and complexity reduction.

## Artifact Boundary

- Do not put Codex operating rules, 작업자용 규칙, prompt/hook compliance notes, source-reading methodology, or answer-quality standards into generated code, product docs, technical specs, README files, runbooks, tests, comments, or user-facing artifacts unless explicitly requested.
- Software artifacts should contain product behavior, architecture, API/data contracts, run instructions, operational runbooks, verification paths, decisions, or implementation notes that a human maintainer actually needs.
- Reusable guidance for how Codex should implement, review, research, or document belongs in this hook, a skill, AGENTS.md, or the assistant response.
- If a generated file mainly teaches Codex how to work, remove it from the repository artifact and move the rule into the appropriate hook or skill.

## Verification Rules

- Prefer type checks, focused scripts, reproducible commands, live/manual smoke traces, or narrow tests over defensive code that hides failure.
- Do not add fallback, abstraction, broad exception handling, or permanent logs without verification.
- If tests cannot be run, state why and what was checked instead.
- For user-facing flows, include at least one happy path and one meaningful failure/boundary path when practical.
- For shared behavior, verify callers or contract boundaries, not only the modified function.
- For early AI/ML/agent product slices, keep automated tests near zero. Prefer a real/manual smoke trace that records input, prompt/features/context, raw model output, parsed output, and resulting product action.
- Add automated tests for AI/ML products only when they protect hard invariants, data integrity, a parser/dispatcher contract, or a regression that already happened. Do not create broad tests merely because the real model behavior is harder to verify.

## Forbidden Output Patterns

Do not finalize with:

- generic “consider edge cases” advice without concrete checks,
- broad “improve error handling” advice without recovery boundaries,
- “add logging everywhere” guidance,
- “use an interface/factory/strategy for flexibility” without current need,
- “fallback to default” without trigger/trade-off/test/removal condition,
- a rewrite suggestion before minimal failure isolation,
- a design that looks safe but cannot be verified,
- a list of options with no recommendation.

## Final Gate

Before finalizing, verify all of the following:

- Did I keep the change minimal?
- Did I avoid speculative abstraction?
- For product work, did I implement or preserve the differentiating core behavior before support structure?
- For AI/ML/agent products, did I implement or preserve the real input -> model/agent call -> parse -> action loop before scaffolding?
- Did I consider AI/ML for features where it may be operationally, economically, or qualitatively better than deterministic code?
- If I did not use AI/ML for such a feature, did I state the short reason?
- Did I avoid choosing work merely because it is easy to test?
- Did I avoid hiding failures?
- Did I avoid unrelated refactors, dependencies, file moves, and formatting sweeps?
- Did I avoid excessive logs and duplicate error-chain logs?
- Did I avoid multi-stage fallback or define the allowed fallback precisely?
- Did I preserve security, authorization, validation, audit, privacy, migration, idempotency, and data integrity invariants?
- Did I provide verification or explain why verification could not run?
- Is the result easier to reason about than before?

If any answer is no, rewrite or simplify before finalizing.
