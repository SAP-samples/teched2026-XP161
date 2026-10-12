# Exercise 2.3 — Fixed Cost Allocation (~5 minutes)

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
- The **donut chart** in the details pane header visualizes the distribution across cost centers at a glance.
- In the details pane, the cost breakdown reflects the percentage allocation.

**What is the SAC instance cost per cost center after the split?**

<details>
<summary>Hint</summary>

Click on the donut chart in the details pane header, or view the instance row directly in the main table.

</details>

<details>
<summary>Answer</summary>

| Cost Center | Amount |
|---|---|
| CC-100 | 1,349.06 USD |
| CC-200 | 1,541.78 USD |
| CC-300 | 963.62 USD |

</details>

## Step 3.3 — View the Full Cost Center Distribution

1. In **Group By**, select **Cost Labels → All Cost Labels**. The table now shows the full APEX Holdings cost distribution by Cost Center — combining the subsidiary assignments, instance-level overrides from Exercise 2.2, and the fixed allocation from this exercise.
2. Switch **Group By** back to **Account → All Account Entities**, scroll to the bottom, and expand the **Cost Breakdown** chart to see which cost center carries the largest share over the last 12 months.

> [!TIP]
> This view gives the APEX Holdings CFO a single table showing SAP BTP cost responsibility by cost center — directly actionable for internal charge-back and budget planning. A resource hosted in one subsidiary can be charged to multiple cost centers without moving it or restructuring the account.

---

[← Exercise 2.2 — Advanced Breakdown](../ex2.2/) | [Continue to: Exercise 2.4 — Second Label Dimension (Optional) →](../ex2.4/)
