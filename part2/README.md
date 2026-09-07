# Part 2 — Preview: Upcoming Cost and Usage FinOps Capabilities (~35 minutes)

## Where Part 1 Left Off

In Part 1 you worked through APEX Holdings' existing FinOps capabilities — billing verification, cost monitoring, cross-charging, budgets, and optimization. They are comprehensive. But as you investigated costs, you hit three ceilings that the current Billing tab cannot cross:

**Ceiling 1 — Visibility stops at the subaccount.**
In Exercise 3 you traced the SAP HANA Cloud cost spike to **Sales App 1 – PROD** (Lumina Energy). That's as deep as you could go. You couldn't see which Cloud Foundry space or which HANA service instance inside that subaccount is the actual driver — whether it's one runaway instance or distributed across several.

**Ceiling 2 — Labels are bound to entities, assigned one by one.**
In Exercise 4 you saw **Department** labels on individual subaccounts — set one by one when each account was configured. To assign a cost center to all 40+ NexaTech Digital subaccounts, you'd need to update each individually. And when a subaccount is deleted — like the orphaned ones you saw in the account hierarchy — its label history disappears with it.

**Ceiling 3 — Shared resource costs can't be split.**
In Exercise 6 you found that Cloud Foundry Runtime – Standard (Sales App 1 – PROD) is being overcharged at consumption rates. That runtime is actually shared by the Sales, Finance, and HR teams. But 100% of its cost lands on Sales App 1 – PROD with no mechanism to distribute it by team.

---

## What Part 2 Unlocks

The same APEX Holdings data, through a more capable lens.

> [!WARNING]
> This preview is **not yet generally available**. Features shown here represent the planned direction and may change before GA release.

| Limitation in Part 1 | New capability in Part 2 |
|---|---|
| Cost breakdown stops at subaccount | **Drill to CF space and service instance** |
| Labels coupled to entity lifecycle — lost on deletion | **Labels persist independently** of account structure |
| Label assignment one subaccount at a time | **Assign at any directory level — all children inherit** |
| No cost splitting for shared resources | **Fixed percentage distribution across cost labels** |

> [!IMPORTANT]
> **Before starting Part 2**, use the URL provided by your facilitator. It activates both the Apex Holdings demo account and the **"TechEd Preview"** tab (`teched-finops-2026-preview=true`).

## Exercises

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 1](ex1-basic-view/) | Basic View — Same Data, New Interface | ~4 min | **Core** |
| [Exercise 2](ex2-advanced-breakdown/) | Advanced View — Granular Breakdown & Label Assignment | ~8 min | **Core** |
| [Exercise 3](ex3-fixed-allocation/) | Advanced View — Fixed Cost Allocation | ~5 min | **Core** |
| [Exercise 4](ex4-additional-label/) | Add a Second Cost Label Dimension | ~5 min | Optional |
| [Exercise 5](ex5-export/) | Export to Excel | ~3 min | Optional |
| [Exercise 6](ex6-cleanup/) | Clean Up | ~3 min | Optional |

---

[← Back to Session Overview](../README.md) | [Start with Exercise 1 →](ex1-basic-view/)
