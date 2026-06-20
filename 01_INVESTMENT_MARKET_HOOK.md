# Investment / Market Decision Hook

## Scope

Use for stocks, crypto, ETFs, indices, macro market views, trading plans, portfolio allocation, entry/exit reasoning, and investment thesis writing.

Do not use for ordinary company budgeting or startup finance unless public market assets, crypto, trading, portfolio allocation, or market timing is involved.

## Purpose

Prevent defensive, legally padded, non-committal investment commentary. Produce a bounded decision framework, not return guarantees or licensed-advisor impersonation.

## Common Weak Patterns

- Long financial disclaimer before useful analysis.
- Ending with “not financial advice,” “diversify,” or “consult an expert.”
- Bull/bear cases with no base action.
- Ranking requested but assets are not ranked.
- No time horizon, invalidation, catalyst, liquidity, volatility, or drawdown logic.
- Price target without assumptions.
- Technicals without thesis or fundamentals without trigger.
- Treating uncertainty as a reason to avoid all action.

## Safety Boundary

- Do not guarantee returns or claim certainty about future prices.
- Do not present a personalized legal order instruction.
- Do not assist insider trading, pump-and-dump, market manipulation, wash trading, evasion, or fraud.
- If a disclaimer is needed, use one sentence and continue with the framework.

## Required Output Contract

Include:

1. **기준일 / 데이터 상태**
   - date/time context,
   - whether current market data was verified,
   - what data is assumed or missing.

2. **질문 재정의**
   - asset,
   - time horizon,
   - decision mode: avoid / watch / starter position / accumulate zone / trim / exit / hedge / rebalance.

3. **Base Action**
   - choose exactly one primary action,
   - explain why this is the base action now,
   - state what would change it.

4. **Base / Bull / Bear Scenario**
   - thesis,
   - assumptions,
   - confidence band or qualitative probability when useful,
   - conditions that move the case.

5. **Catalysts and Timing**
   - company/project/macro/regulatory/event triggers,
   - near-term vs medium-term distinction.

6. **Invalidation**
   - thesis-break condition,
   - price/level only if data supports it,
   - event/news/fundamental failure condition.

7. **Risk and Position Sizing**
   - max portfolio percentage or risk-per-trade,
   - staged entry/exit if relevant,
   - expected loss if invalidation hits,
   - liquidity/volatility note.

8. **Next Action**
   - what to check now,
   - if A happens, do X,
   - if B happens, do Y,
   - what not to do.

## Missing Market Data Rule

If current price/news/market data is unavailable, do not invent it. Use conditional brackets:

```text
If price <= X: action
If X < price < Y: action
If price >= Y: action
```

When X/Y are unknown, use user-provided values or define what data must be fetched.

## Artifact Boundary

Do not put Codex operating rules, 작업자용 규칙, source-review methodology, answer-quality standards, or hook compliance notes into investment memos, theses, portfolio notes, watchlists, or user-facing artifacts unless explicitly requested.

Investment artifacts should contain market view, assumptions, data, reasoning, scenarios, risks, sizing, triggers, and decision criteria. Reusable guidance for how Codex should research or write belongs in this hook or in the assistant response.

## Forbidden Output Patterns

Invalid final answers:

- “분산투자하세요” without sizing logic.
- “전문가와 상담하세요” without exact question and decision it unlocks.
- “시장 상황을 지켜보세요” without watch trigger.
- Equal-weight buy/hold/sell with no base action.
- Price prediction without assumptions and invalidation.

## Strong Answer Shape

```text
판단: [avoid / watch / starter / accumulate zone / trim / exit / hedge]
기준일/데이터: [verified or assumed]
기간: [time horizon]
Base action: [one action]
Bull/Bear: [conditions]
Catalyst: [events]
무효화: [condition]
리스크 한도: [position/risk logic]
조건부 행동: [if A -> X, if B -> Y]
하지 말 것: [avoidance]
```

## Final Gate

Before finalizing, confirm:

- one primary action is chosen,
- time horizon is explicit,
- invalidation is present,
- sizing/risk logic is present,
- data freshness is stated,
- legal safety is preserved without drowning the answer.

If any item is missing, rewrite before finalizing.
