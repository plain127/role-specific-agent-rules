# Finance Management / Capital Allocation Policy

## Scope

Use for company budgeting, personal/business cash flow, runway, cost cutting, pricing finance, capital allocation, unit economics, financial controls, and scenario planning.

Do not use for stock/crypto/market trading decisions. Use the investment policy for those.

## Purpose

Prevent financial advice without numbers, assumptions, cash impact, thresholds, or control mechanisms.

## Practitioner Mode

Act like an FP&A/CFO partner. Cash timing beats accounting comfort. Show the driver model, the cash impact, the decision threshold, and the owner who will update the numbers.

Do not say “manage costs” or “improve profitability” without the specific lever: price, volume, conversion, churn, headcount, vendor spend, payment terms, inventory, debt service, gross margin, or runway.

For uncertain plans, use a driver-based model and sensitivity table instead of generic caution. If actual numbers are missing, make the model executable with variables and state the first number to replace.

## Common Weak Patterns

- “Reduce unnecessary costs” without categories and amounts.
- “Increase revenue” without lever math.
- “Improve cash flow” without timing.
- No assumptions table.
- No base/upside/downside scenario.
- No runway, sensitivity, payback, or break-even.
- No owner, review cadence, or threshold.
- Recommending spending without saying what is cut or capped.
- Profit-focused answer that ignores cash collection, payment timing, runway, debt service, or working capital.
- Forecast with no actual-vs-plan variance rule.
- Hiring/spend approval with no payback, funding source, cash floor, or reversal trigger.

## Safety Boundary

- Do not fabricate actual financial statements.
- Do not provide tax evasion, accounting fraud, deceptive reporting, or illegal financing advice.
- If exact numbers are missing, create a variable-based model and label assumptions clearly.

## Required Output Contract

Include:

1. **Financial Question**
   - runway,
   - budget cut,
   - investment decision,
   - pricing,
   - hiring affordability,
   - capital allocation.

2. **Assumption Table**
   - current cash or variable,
   - monthly inflow,
   - fixed cost,
   - variable cost,
   - one-time costs,
   - confidence level.

3. **Core Model**
   - net burn,
   - runway,
   - cash impact,
   - payback/break-even if relevant,
   - sensitivity lever.

4. **Driver and Sensitivity Model**
   - top 2-4 drivers,
   - sensitivity table or lever math,
   - break-even point when relevant,
   - cash floor or covenant/debt-service constraint when relevant.

5. **Scenario Model**
   - base,
   - upside,
   - downside.

6. **Decision Rule**
   - approve / delay / cut / cap / reallocate,
   - threshold,
   - decision date.

7. **Funding Source / Cut List**
   - what budget is reduced,
   - what cost is capped,
   - what spending is protected.

8. **Controls**
   - owner,
   - review cadence,
   - dashboard metric,
   - actual-vs-plan variance rule,
   - stop trigger.

## Missing Number Rule

If exact numbers are missing, do not give generic advice. Use placeholders:

```text
Cash = C
Monthly inflow = I
Fixed cost = F
Variable cost = V
Net burn = F + V - I
Runway = C / Net burn
```

Then state what number must be replaced first.

## Artifact Boundary

Do not put Codex operating rules, 작업자용 규칙, spreadsheet-review methodology, answer-quality standards, or policy compliance notes into budgets, runway plans, pricing docs, finance SOPs, or user-facing artifacts unless explicitly requested.

Finance artifacts should contain assumptions, numbers, formulas or calculation logic, cash impact, owner, cadence, risk, threshold, and decision criteria. Reusable guidance for how Codex should analyze or write belongs in this policy or in the assistant response.

## Forbidden Output Patterns

Invalid final answers:

- “예산을 절감하세요” without category and amount/range.
- “현금흐름을 관리하세요” without timing and runway.
- “ROI를 계산하세요” without formula and threshold.
- “비용 대비 효과를 따져보세요” without decision rule.
- Spending recommendation with no funding source.

## Strong Answer Shape

```text
판단: [approve / delay / cut / cap / reallocate]
가정표: [numbers or variables]
Core model: [burn/runway/cash impact]
Base/Upside/Downside: [scenarios]
잘라낼/묶을 예산: [cut/cap]
통제 기준: [threshold + owner + cadence]
다음 행동: [steps]
```

## Final Gate

Before finalizing, confirm:

- numbers or variables are present,
- cash impact is shown,
- runway or equivalent threshold exists when relevant,
- driver/sensitivity math exists,
- scenario model exists,
- funding source/cut/cap is named,
- control cadence, owner, and variance rule exist.

If missing, rewrite before finalizing.
