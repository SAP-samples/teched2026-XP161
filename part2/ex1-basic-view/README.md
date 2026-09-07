# Part 2, Exercise 1 — Basic View (~4 minutes)

**Goal:** Orient yourself in the TechEd Preview tab and confirm it shows the same Apex Holdings cost data you worked with in Part 1.

**Scenario:** In Part 1 you identified two critical issues in the Apex Holdings account:
- **SAP HANA Cloud - HANA** costs spiked in the previous month, driven by **Sales App 1 – PROD** under the **Lumina Energy** subsidiary
- **HR App 4 – TEST** under the **NexaTech Digital** subsidiary exceeded its 40,000 USD budget

In Part 2 you will use the new Billing Preview to see the same data with a more powerful lens — and then allocate those costs to Apex's business lines.

## Accessing the TechEd Preview

> [!NOTE]
> **Your facilitator will provide the URL for Part 2** (`teched-finops-2026-preview=true`). It activates both the Apex Holdings demo account and the **"TechEd Preview"** tab.

1. Open the URL provided by your facilitator for Part 2.
2. Log in with the same credentials used in Part 1.
3. Navigate to **Costs and Usage**.
4. Click the **"TechEd Preview"** tab — it appears alongside the standard tabs (Billing, Usage, Budgets, Overview).

## Steps

1. In the left sidebar, confirm **"Basic"** is selected (pre-selected by default).
2. In the **Period** section, set **Month** to **Previous Month** — the same month you analyzed in Part 1.
3. Use the **Group By** dropdown to explore:
   - Select **Services → All Services**. Confirm **SAP HANA Cloud - HANA** appears at the top — the highest-cost service from Part 1, Exercise 3.
   - Switch to **Account → Directories & Subaccounts**. Confirm you can see the 5 Apex Holdings subsidiaries: **Atlas Industries**, **Lumina Energy**, **HarborCare Health**, **Crestline Retail**, and **NexaTech Digital**.
4. In the left sidebar under **Filter**, expand **Services** and select **SAP HANA Cloud - HANA** to narrow the view to HANA costs only.
5. Clear the filter before continuing to Exercise 2.

> **Two UI changes from the standard Billing tab:**
> - Filters have moved to the **left sidebar** (instead of the table header)
> - **Group By** is a new dropdown that controls row aggregation — this also applies in the Advanced view

---

[← Part 2 Overview](../README.md) | [Continue to: Exercise 2 — Advanced View: Cost Breakdown & Labels →](../ex2-advanced-breakdown/)
