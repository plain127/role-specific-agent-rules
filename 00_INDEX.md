# Domain Hook Index

These are independent markdown harnesses for non-code Codex work. Do not merge them. Load the smallest matching hook.

## Routing Table

| Task | Primary hook |
|---|---|
| Stocks, crypto, ETFs, indices, trading, market thesis, portfolio allocation | `01_INVESTMENT_MARKET_HOOK.md` |
| Company strategy, management, hiring, org design, operating model, expansion | `02_BUSINESS_MANAGEMENT_HOOK.md` |
| Product ideas, MVP, feature planning, startup validation, roadmap, wedge | `03_PRODUCT_IDEA_PLANNING_HOOK.md` |
| Marketing, growth, funnel, positioning, copy, campaigns, acquisition, retention | `04_MARKETING_GROWTH_HOOK.md` |
| Budgeting, runway, cash flow, capital allocation, pricing finance, unit economics | `05_FINANCE_MANAGEMENT_HOOK.md` |
| Research, literature review, competitive analysis, claim verification, evidence synthesis | `06_RESEARCH_ANALYSIS_HOOK.md` |
| Image prompts, visual direction, art direction, thumbnails, posters, brand visuals | `07_CREATIVE_IMAGE_HOOK.md` |
| SOPs, process design, workflow, delegation, cadence, execution systems, runbooks | `08_OPERATIONS_PROCESS_HOOK.md` |
| Software architecture, implementation, refactoring, debugging, API/data design, technical docs | `09_SOFTWARE_DESIGN_CODE_IMPLEMENTATION_HOOK.md` |
| Fiction, scripts, webnovels, game narrative, dark creative work, intense allowed creative direction | `10_CREATIVE_FREEDOM_AND_BOUNDARY_HOOK.md` |

## Loading Rule

For any non-code professional task:

1. Read `00_COMMON_HARNESS_RULES.md`.
2. Select exactly one primary hook.
3. Read the selected hook.
4. Use one secondary hook only for a clearly separate section.
5. Apply the selected hook's Final Gate before answering.

## Boundaries

- Software/code tasks use `09_SOFTWARE_DESIGN_CODE_IMPLEMENTATION_HOOK.md` for markdown planning/review,
  while executable repository hooks and repository-specific policy remain stronger.
- Investment-market rules apply only when public securities, crypto, trading, market timing, or portfolio allocation is involved.
- Finance-management rules apply to budgeting, runway, cash control, pricing economics, and capital allocation outside market trading.
- Creative-image rules apply only when the user asks for visual direction, image generation, prompts, thumbnails, posters, or art direction.
- Creative-freedom rules apply to allowed fictional, narrative, or creator work where genre intensity should not be flattened.
- Do not put Codex operating rules, 작업자용 규칙, hook compliance notes, or document-generation methodology into user-facing project artifacts unless explicitly requested; put reusable worker guidance in the relevant hook, skill, AGENTS.md, or assistant response.

## Fallback if Files Cannot Be Read

Use this compact fallback:

- Pick one recommendation.
- Rank options and reject weaker alternatives.
- State assumptions briefly.
- Include numbers, timeline, owner, metric, artifact, or kill condition.
- Do not end with generic disclaimers or “it depends.”
- If blocked, give the closest safe executable alternative.
