# Exercise 2.3 — Fixed Cost Allocation (~6 minutes)

Dana asked to allocate a shared resource's cost across cost centers.

**Goal:** Allocate a shared resource cost across Apex Holdings cost centers using fixed percentages.

**Scenario:** HANA Cloud is APEX Holdings' largest cost driver (Exercise 1.3). In Exercise 2.2, each HANA instance in Sales App 1 – PROD was attributed to a **single cost center**. The HANA Cloud instance behind **Finance App 3 – PROD** is different: it's a **shared** instance, so no single cost center reflects who really uses it. Today its entire cost is attributed to one cost center — **CC-200** — inherited through the hierarchy from the assignments you made in Exercise 2.2. **Dana** wants it **split across CC-100, CC-200, and CC-300** to reflect actual usage.

The agreed split is: **CC-100: 40%, CC-200: 35%, CC-300: 25%**.

> [!NOTE]
> Fixed distribution is useful when a shared resource's actual per-team consumption is difficult to measure directly. You define a percentage split based on agreed-upon estimates rather than tracking real-time per-team usage.

## Find the SAP HANA Cloud Instance

> Continue in the **TechEd Preview** tab, **Advanced** view.

1. In **Group By**, confirm **Account → All Account Entities** is selected.
2. Expand **NexaTech Digital → PROD → Finance App 3 – PROD**.
3. Continue expanding to find **`finance_app_3_prod_space_1`** inside Finance App 3 – PROD.
4. Inside the space, expand **SAP HANA Cloud** (Service), then expand the **HANA (Capacity Units)** service plan beneath it. Click the instance row — `91d9d4d0-14dd-4aa5-b0a7-afef448aedbd`.
5. The details pane opens, showing the instance's cost currently attributed entirely to **CC-200** (inherited through the hierarchy).

## Apply the Fixed Percentage Split

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

**What is the HANA instance cost per cost center after the split?**

<details>
<summary>Hint</summary>

Click on the donut chart in the details pane header, or view the instance row directly in the main table.

</details>

<details>
<summary>Answer</summary>

| Cost Center | Amount |
|---|---|
| CC-100 | 585.17 USD |
| CC-200 | 512.03 USD |
| CC-300 | 365.73 USD |

</details>

## View the Full Cost Center Distribution

1. In **Group By**, select **Cost Labels → All Cost Labels**. The table now shows the full APEX Holdings cost distribution by Cost Center — combining the subsidiary assignments, instance-level overrides from Exercise 2.2, and the fixed allocation from this exercise.
2. Switch **Group By** back to **Account → All Account Entities**, scroll to the bottom, and expand the **Cost Breakdown** chart to see which cost center carries the largest share over the last 12 months.

> [!TIP]
> This view gives **Dana** a single table showing SAP BTP cost responsibility by cost center — directly actionable for internal charge-back and budget planning. A resource hosted in one subsidiary can be charged to multiple cost centers without moving it or restructuring the account.

---

[← Exercise 2.2 — Advanced Breakdown](../ex2.2/) | [Continue to: Exercise 2.4 — Second Label Dimension (Optional) →](../ex2.4/)
