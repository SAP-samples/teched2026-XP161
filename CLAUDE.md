# CLAUDE.md — TechEd 2026 XP161

This is the canonical working directory for TechEd 2026 XP161 exercise content.
All TechEd editing happens here — never in the product repo (`git-repos/product`).

## Repository

- **Remote:** `https://github.tools.sap/I031851/teched2026-xp161`
- **Push rule:** Push to remote only on explicit request ("push to GitHub", "push to TechEd repo")

## Exercise Structure

```
1_setup/                         — Getting Started (~5 min)
2_cost-visibility-and-control/   — Part 1: Cost Visibility and Control (~55 min)
3_advanced-cost-allocation/      — Part 2: Advanced Cost Allocation (~35 min)
4_ask-joule/                     — Part 3: Ask Joule (~30 min)
```

## APEX Holdings Mock Data — Key Facts

- **Date shift:** APEX data shifts +1 month each month. At TechEd (October 2026), data
  currently labeled Aug 2026 in exports will show as Sep 2026 (previous month).
- **Q3 2026 vs Q2 2026 increase:** ~25% (Dana's quote in setup README)
- **HR App 4 – TEST:** $40,527.64 in previous month — exceeds the $40,000 budget
- **SAP HANA Cloud spike:** Sales App 1 – PROD (Lumina Energy) — first month of HANA charges
- **CF Runtime overage:** 80 GB usage, 60 GB prepaid quota, 20 GB overage
- **CC-200 (NexaTech Digital)** is the highest cost center: $205,219.28

## HANA Instance IDs (Sales App 1 – PROD, sales_app_1_prod_space_1)

| Instance | Share | Cost Label |
|---|---|---|
| `7ba838b5-0328-4145-a27f-bed7a6dc8a8b` (existing) | ~60% | CC-100 (inherited) |
| `cce2dd07-0931-4355-95c8-aa037a88f83c` (new) | ~25% | CC-200 (override) |
| `30eeba60-2008-4dc9-bf2b-9db1f358e8a4` (new) | ~15% | CC-300 (override) |

## Open Items

- HANA instance data pending Alex's confirmation — check `3_advanced-cost-allocation/ex3-fixed-allocation/README.md`
  and `3_advanced-cost-allocation/ex4-additional-label/README.md` for any remaining TODOs
- Issue 2 (CF Runtime attribution in Part 2 narrative) still needs a fix
