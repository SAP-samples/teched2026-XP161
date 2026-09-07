# Part 2, Exercise 3 — Fixed Cost Allocation (~5 minutes)

**Goal:** Allocate a shared resource cost across Apex Holdings business lines using fixed percentages.

**Scenario:** In Part 1, Exercise 6, you identified that **Cloud Foundry Runtime - Standard** under **Sales App 1 – PROD** (Lumina Energy) has a 20 GB overage being charged at consumption rates. In the current Billing tab, 100% of that Cloud Foundry Runtime cost lands on Sales App 1 – PROD — there's no mechanism to split it. But the Finance and HR Operations teams also use this shared runtime environment, and the CFO needs their share reflected in the business line allocation.

> [!TIP]
> **Part 1 ceiling you're crossing here:** Shared resources in the current Billing tab are attributed entirely to the subaccount that hosts them. Fixed distribution lets you define an agreed percentage split — directly on the instance — so each business line sees its real share of the cost.

The agreed split is: **Sales 60%, Finance 25%, HR Operations 15%**.

> [!NOTE]
> Fixed distribution is useful when a shared resource's actual per-team consumption is difficult to measure directly. You define a percentage split based on agreed-upon estimates rather than tracking real-time per-team usage.

## Step 3.1 — Find the Cloud Foundry Runtime Instance

1. In **Group By**, confirm **Account → All Account Entities** is selected.
2. Expand **Lumina Energy → PROD → Sales App 1 – PROD**.
3. Continue expanding to find the **Cloud Foundry Space** inside Sales App 1 – PROD.
4. Inside the space, look for the **Cloud Foundry Runtime** service instance.
   > If no instance is visible at the instance level, apply the fixed allocation at the **Cloud Foundry Space** or **Sales App 1 – PROD** subaccount level instead.
5. Click on the instance (or space/subaccount) to open the details pane.

## Step 3.2 — Apply the Fixed Percentage Split

1. In the **Cost Label Values** multi-select, select all 3 Line of Business values — a **Distribution %** column appears for each.
2. Enter the Apex Holdings agreed split:
   - **Sales:** 60%
   - **Finance:** 25%
   - **HR Operations:** 15%
3. Click **Save**.

**Observe:**
- The cost is now split in the main table: 60% to Sales, 25% to Finance, 15% to HR Operations.
- In the details pane, the cost breakdown reflects the percentage allocation.

## Step 3.3 — View the Full Business Line Cost Distribution

1. In **Group By**, select **Cost Labels → All Cost Labels**.
2. The table now shows the total APEX Holdings cost distribution by Line of Business — combining:
   - Subsidiary-level assignments from Exercise 2 (Lumina Energy → Sales, NexaTech Digital → HR Operations, Crestline Retail → Finance)
   - The subaccount override from Exercise 2 (Finance App 3 – PROD → Finance)
   - The fixed percentage allocation on the Cloud Foundry Runtime instance from this exercise

**Question:** Which business line has the highest total allocated cost across APEX Holdings?

<details>
<summary>Expected answer</summary>

**Sales** — Lumina Energy (the subsidiary with the highest monthly spend, driven by Sales App 1 – PROD's SAP HANA Cloud costs) is fully assigned to Sales, and 60% of the shared Cloud Foundry Runtime cost also flows to Sales.

</details>

> [!TIP]
> This view gives the APEX Holdings CFO a single table showing SAP BTP cost responsibility by business line — directly actionable for internal charge-back, budget planning, and purchasing decisions (like the Cloud Foundry Runtime quota increase from Part 1).

---

[← Exercise 2 — Advanced Breakdown](../ex2-advanced-breakdown/) | [Continue to: Exercise 4 — Second Label Dimension (Optional) →](../ex4-additional-label/)
