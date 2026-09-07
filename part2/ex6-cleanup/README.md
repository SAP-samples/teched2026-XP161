# Part 2, Exercise 6 — Clean Up — Optional (~3 minutes)

> [!TIP]
> **This exercise is optional.** Complete it to restore the Apex Holdings demo account to its initial state.

> [!NOTE]
> Deleting cost labels only affects what is visible in the TechEd Preview. It does not impact any services, billing data, or business processes.

## Steps (UI reset)

1. In **Group By**, select **Cost Labels → All Cost Labels**.
2. Click **Manage Cost Labels**.
3. Delete the **"Cost Center"** label key — this removes the key definition and all assignments (Lumina Energy → CC-100, NexaTech Digital → CC-200, Crestline Retail → CC-300, Finance App 3 – PROD override, Backup Vault → CC-100, SAP Analytics Cloud Standard (Time) fixed allocation).
4. If you completed Exercise 4, delete the **"Region"** label key as well.
5. Confirm each deletion and click **Save**.

**Expected result:** The demo account returns to its initial state — only the default Sample labels remain.

---

## Part 2 Summary

### 🎯 Key Takeaways

- ✅ The TechEd Preview tab shows the same Apex Holdings data as the standard Billing tab, with a new level of granularity (CF space and service instance)
- ✅ You assigned the three highest-spend APEX Holdings subsidiaries to cost centers: Lumina Energy → CC-100, NexaTech Digital → CC-200, Crestline Retail → CC-300
- ✅ Labels inherit from subsidiary to subaccount — **Sales App 1 – PROD** inherited CC-100 from Lumina Energy; **HR App 4 – TEST** inherited CC-200 from NexaTech Digital
- ✅ Override at any level: Finance App 3 – PROD was reassigned from CC-200 to CC-300 without restructuring the account
- ✅ Label assignments survive entity deletion — **Backup Vault** was decommissioned last month but its costs remained attributed: the label assignment persisted independently of the subaccount lifecycle

---

[← Exercise 5 — Export to Excel](../ex5-export/) | [Continue to: Part 3 — FinOps with Joule →](../../part3/README.md)
