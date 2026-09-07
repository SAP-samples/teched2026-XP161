# Part 2, Exercise 3 — Fixed Cost Allocation (~5 minutes)

**Goal:** Allocate a shared resource cost across Apex Holdings cost centers using fixed percentages.

**Scenario:** APEX Holdings runs a shared **SAP Analytics Cloud (SAC) embedded edition** instance hosted under NexaTech Digital — but used across all three business units for finance reporting, HR analytics, and retail operations. Currently, 100% of the SAC cost lands on NexaTech Digital (CC-200) because that's where the instance is hosted. The CFO needs the cost distributed to reflect actual usage across all three cost centers.

The agreed split is: **CC-100: 40%, CC-200: 35%, CC-300: 25%**.

> [!NOTE]
> Fixed distribution is useful when a shared resource's actual per-team consumption is difficult to measure directly. You define a percentage split based on agreed-upon estimates rather than tracking real-time per-team usage.

## Step 3.1 — Find the SAP Analytics Cloud Instance

1. In **Group By**, confirm **Account → All Account Entities** is selected.
2. Expand **NexaTech Digital → PROD → HR App 3 – PROD**.
3. Continue expanding to find **hr_app_3_prod_space_1** inside HR App 3 – PROD.
4. Inside the space, expand **SAP Analytics Cloud, embedded edition** and click on the **Standard (Time)** instance (`d3a35e06-824a-487b-bd9c-68372aca49fb`).
5. The details pane opens, showing 100% of the SAC cost currently attributed to CC-200 (NexaTech Digital, inherited).

## Step 3.2 — Apply the Fixed Percentage Split

1. In the **Cost Label Values** multi-select, select all 3 Cost Center values — a **Distribution %** column appears for each.
2. Enter the Apex Holdings agreed split:
   - **CC-100:** 40%
   - **CC-200:** 35%
   - **CC-300:** 25%
3. Click **Save**.

**Observe:**

- The cost is now split in the main table: 40% to CC-100, 35% to CC-200, 25% to CC-300.
- In the details pane, the cost breakdown reflects the percentage allocation.

## Step 3.3 — View the Full Cost Center Distribution

1. In **Group By**, select **Cost Labels → All Cost Labels**.
2. The table now shows the total APEX Holdings cost distribution by Cost Center — combining:
   - Subsidiary-level assignments from Exercise 2 (Lumina Energy → CC-100, NexaTech Digital → CC-200, Crestline Retail → CC-300)
   - The subaccount override from Exercise 2 (Finance App 3 – PROD → CC-300)
   - The fixed percentage allocation on the SAC Standard (Time) instance from this exercise
3. Switch **Group By** back to **Account → All Account Entities** and scroll to the bottom of the page. Click the **expand** icon on the **Cost Breakdown** chart to open it in full view. Observe which cost center carries the largest share month over month across the last 12 months, and whether the distribution has shifted.

**Question:** Which cost center has the highest total allocated cost across APEX Holdings?

<details>
<summary>Expected answer</summary>

**CC-100** — it receives the largest cost block from the APEX Holdings hierarchy plus 40% of the shared SAC allocation, giving it the highest total.

</details>

> [!TIP]
> This view gives the APEX Holdings CFO a single table showing SAP BTP cost responsibility by cost center — directly actionable for internal charge-back and budget planning. A resource hosted in one subsidiary can be charged to multiple cost centers without moving it or restructuring the account.

---

[← Exercise 2 — Advanced Breakdown](../ex2-advanced-breakdown/) | [Continue to: Exercise 4 — Second Label Dimension (Optional) →](../ex4-additional-label/)
