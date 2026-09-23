# Part 2 — Advanced Cost Allocation (~35 minutes)

## Dana's Follow-Up

You delivered the Part 1 findings. Dana is back.

> *"Good work. Now I need the next level. Subaccount names mean nothing to my board — I need cost center attribution. Lumina, NexaTech, Crestline. And that shared SAC instance you found sitting under NexaTech? That's used by all three divisions. Split it. CC-100 gets 40%, CC-200 35%, CC-300 25%."*

## Where Part 1 Left Off

Part 1's tools are comprehensive — but they hit three ceilings:

- **Visibility stops at the subaccount.** You traced the HANA spike to Sales App 1 – PROD, but couldn't see which service instance inside it is the actual driver.
- **Labels are assigned one by one.** Tagging all 40+ NexaTech Digital subaccounts requires individual updates — and deleted subaccounts take their label history with them.
- **Shared resource costs can't be split.** No mechanism exists to distribute a shared service cost across multiple business units.

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
> **Before starting Part 2**, open the following link. It activates both the Apex Holdings demo account and the **"TechEd Preview"** tab:
>
> <https://emea.cockpit.btp.cloud.sap/cockpit/?idp=ainfvn15r.accounts.ondemand.com&teched-finops-2026-preview=true#>
>
> Log in with the same user and password you used in Part 1.

## Exercises

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 1](ex1-basic-view/) | Basic View — Same Data, New Interface | ~4 min | **Core** |
| [Exercise 2](ex2-advanced-breakdown/) | Advanced View — Granular Breakdown & Label Assignment | ~8 min | **Core** |
| [Exercise 3](ex3-fixed-allocation/) | Advanced View — Fixed Cost Allocation | ~5 min | **Core** |
| [Exercise 4](ex4-additional-label/) | Add a Second Cost Label Dimension | ~5 min | Optional |
| [Exercise 5](ex5-export/) | Export to Excel | ~3 min | Optional |

---

[← Back to Session Overview](../README.md) | [Start with Exercise 1 →](ex1-basic-view/)
