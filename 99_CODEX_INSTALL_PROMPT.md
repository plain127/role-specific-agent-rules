# Prompt to Ask Codex to Install Markdown Domain Harness v2

Copy this prompt into Codex when installing this pack.

```text
Install the markdown-only domain hook harness in this repository.

Important:
- Do not modify the existing software design / code implementation hook.
- Do not create Python hook scripts.
- Do not create executable hook files.
- Do not modify `.codex/hooks.json` unless I explicitly ask.
- This is a markdown harness pack only.
- Keep `AGENTS.md` small to reduce token cost and context rot.
- Move detailed rules into referenced markdown files.
- Do not put Codex operating rules, 작업자용 규칙, hook compliance notes, or documentation methodology into user-facing generated artifacts unless explicitly requested; put reusable worker guidance in the relevant hook, skill, or assistant response.

Create or update:

1. `AGENTS.md`
2. `.codex/domain-hooks/00_INDEX.md`
3. `.codex/domain-hooks/00_COMMON_HARNESS_RULES.md`
4. `.codex/domain-hooks/01_INVESTMENT_MARKET_HOOK.md`
5. `.codex/domain-hooks/02_BUSINESS_MANAGEMENT_HOOK.md`
6. `.codex/domain-hooks/03_PRODUCT_IDEA_PLANNING_HOOK.md`
7. `.codex/domain-hooks/04_MARKETING_GROWTH_HOOK.md`
8. `.codex/domain-hooks/05_FINANCE_MANAGEMENT_HOOK.md`
9. `.codex/domain-hooks/06_RESEARCH_ANALYSIS_HOOK.md`
10. `.codex/domain-hooks/07_CREATIVE_IMAGE_HOOK.md`
11. `.codex/domain-hooks/08_OPERATIONS_PROCESS_HOOK.md`
12. `.codex/harness/README.md`
13. `.codex/harness/solo-fullstack-workflow.md`
14. `.codex/harness/session-sync.md`
15. `.codex/harness/role-skills.md`
16. `.codex/harness/final-response.md`

Purpose:
- These are not executable hooks.
- They are domain-specific markdown harness policies.
- `AGENTS.md` should route to `.codex/domain-hooks/00_INDEX.md` for non-code professional work.
- Each domain hook must remain independent.
- Do not merge all hooks into one universal instruction.
- The hooks should reduce vague, defensive, non-committal, responsibility-avoiding, or generic outputs.

Preserve:
- Existing software/code implementation hook remains untouched.
- For software tasks, use the existing software hook and `.codex/policy/simple-implementation.md` if present.
- For non-software tasks, select the matching markdown domain hook.
- Safety, law, privacy, and security remain binding.
- If a task is allowed, do not hide behind disclaimers; produce concrete executable output.
```
