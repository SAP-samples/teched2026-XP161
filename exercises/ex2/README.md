# Exercise 2 — Advanced Cost Allocation (~35 minutes)

## Dana's Follow-Up

You delivered the Exercise 1 findings. Dana is back.

> *"Good work. Now I need the next level. Subaccount names mean nothing to my board — I need cost center attribution. Lumina, NexaTech, Crestline. HANA's our biggest line item — you saw that. And there's a shared HANA Cloud instance — it sits under NexaTech so today 100% of its cost lands on CC-200, but all three cost centers use it. That's not right. Split it: CC-100 gets 40%, CC-200 35%, CC-300 25%."*

> [!WARNING]
> **The features in this exercise are a TechEd Preview — not yet generally available.** They represent the planned direction and may change before release.

## Where Exercise 2 Takes You Further

Exercise 1 gave you the full cost picture. Exercise 2 goes deeper in three areas where more precision is possible:

- **Instance-level visibility.** You traced the HANA spike to Sales App 1 – PROD. Now drill to the specific service instance driving the cost.
- **Fine-grained label allocation.** Allocate cost labels below the subaccount level — down to individual Cloud Foundry spaces and service instances — for precise attribution.
- **Shared resource cost splitting.** Distribute a shared service cost across multiple business units using fixed percentages.

---

<details>
<summary><b>What Exercise 2 Unlocks</b></summary>

The same APEX Holdings data, through a more capable lens.

| Limitation in Exercise 1 | New capability in Exercise 2 |
|---|---|
| Cost breakdown stops at subaccount | **Drill to CF space and service instance** |
| Labels coupled to entity lifecycle — lost on deletion | **Labels persist independently** of account structure |
| Labels assignable only down to subaccount | **Allocate and override labels down to CF space and service instance** |
| No cost splitting for shared resources | **Fixed percentage distribution across cost labels** |

</details>

> [!IMPORTANT]
> **Before starting Exercise 2**, open the following link. It activates both the Apex Holdings demo account and the **"TechEd Preview"** tab:
>
> <https://emea.cockpit.btp.cloud.sap/cockpit/?idp=tdct3ched1.accounts.ondemand.com&teched-finops-2026-preview=true#>
>
> Log in with the same user and password you used in Exercise 1.

## Exercises

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 2.1](ex2.1/) | Basic View — Same Data, New Interface | ~5 min | **Recommended** |
| [Exercise 2.2](ex2.2/) | Advanced View — Granular Breakdown & Label Assignment | ~13 min | **Recommended** |
| [Exercise 2.3](ex2.3/) | Advanced View — Fixed Cost Allocation | ~6 min | **Recommended** |
| [Exercise 2.4](ex2.4/) | Add a Second Cost Label Dimension | ~7 min | Optional |
| [Exercise 2.5](ex2.5/) | Export to Excel | ~4 min | Optional |

---

[← Back to Session Overview](../../README.md) | [Start with Exercise 2.1 →](ex2.1/)
