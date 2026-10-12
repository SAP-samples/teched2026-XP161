# Exercise 2 — Advanced Cost Allocation (~35 minutes)

## Dana's Follow-Up

You delivered the Exercise 1 findings. Dana is back.

> *"Good work. Now I need the next level. Subaccount names mean nothing to my board — I need cost center attribution. Lumina, NexaTech, Crestline. And that shared SAC instance you found sitting under NexaTech? That's used by all three divisions. Split it. CC-100 gets 40%, CC-200 35%, CC-300 25%."*

## Where Exercise 2 Takes You Further

Exercise 1 gave you the full cost picture. Exercise 2 goes deeper in three areas where more precision is possible:

- **Instance-level visibility.** You traced the HANA spike to Sales App 1 – PROD. Now drill to the specific service instance driving the cost.
- **Scalable label assignment.** Assign a label at the directory level and have all subaccounts beneath it inherit it automatically — including future ones.
- **Shared resource cost splitting.** Distribute a shared service cost across multiple business units using fixed percentages.

---

## What Exercise 2 Unlocks

The same APEX Holdings data, through a more capable lens.

> [!WARNING]
> This preview is **not yet generally available**. Features shown here represent the planned direction and may change before GA release.

| Limitation in Exercise 1 | New capability in Exercise 2 |
|---|---|
| Cost breakdown stops at subaccount | **Drill to CF space and service instance** |
| Labels coupled to entity lifecycle — lost on deletion | **Labels persist independently** of account structure |
| Label assignment one subaccount at a time | **Assign at any directory level — all children inherit** |
| No cost splitting for shared resources | **Fixed percentage distribution across cost labels** |

> [!IMPORTANT]
> **Before starting Exercise 2**, open the following link. It activates both the Apex Holdings demo account and the **"TechEd Preview"** tab:
>
> <https://emea.cockpit.btp.cloud.sap/cockpit/?idp=tdct3ched1.accounts.ondemand.com&teched-finops-2026-preview=true#>
>
> Log in with the same user and password you used in Exercise 1.

## Exercises

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 2.1](ex2.1/) | Basic View — Same Data, New Interface | ~4 min | **Core** |
| [Exercise 2.2](ex2.2/) | Advanced View — Granular Breakdown & Label Assignment | ~8 min | **Core** |
| [Exercise 2.3](ex2.3/) | Advanced View — Fixed Cost Allocation | ~5 min | **Core** |
| [Exercise 2.4](ex2.4/) | Add a Second Cost Label Dimension | ~5 min | Optional |
| [Exercise 2.5](ex2.5/) | Export to Excel | ~3 min | Optional |

---

[← Back to Session Overview](../../README.md) | [Start with Exercise 2.1 →](ex2.1/)
