# Part 2, Exercise 5 — Clean Up — Optional (~3 minutes)

> [!TIP]
> **This exercise is optional.** Complete it to restore the Apex Holdings demo account to its initial state.

> [!NOTE]
> Deleting cost labels only affects what is visible in the TechEd Preview. It does not impact any services, billing data, or business processes.
>
> **Fastest reset:** Add `?resetCostLabels=true` to the cockpit URL. This removes all label assignments and definitions instantly without going through the UI.

## Steps (UI reset)

1. In **Group By**, select **Cost Labels → All Cost Labels**.
2. Click **Manage Cost Labels**.
3. Delete the **"Line of Business"** label key — this removes the key definition and all assignments (Lumina Energy → Sales, NexaTech Digital → HR Operations, Crestline Retail → Finance, Finance App 3 – PROD override, Cloud Foundry Runtime fixed allocation).
4. If you completed Exercise 4, delete the **"Cost Owner"** label key as well.
5. Confirm each deletion and click **Save**.

**Expected result:** The demo account returns to its initial state — only the default Sample labels remain.

---

## Part 2 Summary

### 🎯 Key Takeaways

- ✅ The TechEd Preview tab shows the same Apex Holdings data as the standard Billing tab, with a new level of granularity (CF space and service instance)
- ✅ You assigned Apex costs to real business lines: Sales (Lumina Energy), HR Operations (NexaTech Digital), Finance (Crestline Retail)
- ✅ Labels inherit from subsidiary to subaccount — **Sales App 1 – PROD** inherited Sales from Lumina Energy; **HR App 4 – TEST** inherited HR Operations from NexaTech Digital
- ✅ Override at any level: Finance App 3 – PROD was reassigned from HR Operations to Finance without restructuring the account

---

[← Exercise 4 — Additional Label](../ex4-additional-label/) | [Continue to: Part 3 — FinOps with Joule →](../../part3/README.md)
