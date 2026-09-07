# Exercise 1 - Cost and Usage Overview (approx. 10 minutes)

## Exercise 1.1 - Understanding Prepaid Quota

Before exploring the dashboard, it is important to understand how SAP BTP billing works when you have both a subscription and a consumption-based contract.

> [!NOTE]
> **Prepaid Quota explained**
>
> SAP BTP offers several commercial models. APEX Holdings uses a **hybrid model** that combines:
> - A **subscription component** — APEX pays upfront for a fixed quota of specific services (e.g., 40 GB of Cloud Foundry Runtime per month). This prepaid quota is consumed at no additional charge.
> - A **consumption-based component (CPEA/BTPEA)** — backed by cloud credits. Any usage beyond the prepaid quota is charged against those cloud credits at list price.
>
> Usage works in two layers:
> - **Layer 1 — Prepaid quota (free to consume):** The subscription covers a fixed amount of each entitled service. Consuming within this limit generates no additional bill.
> - **Layer 2 — Consumption overage (charged):** Any usage that exceeds the prepaid quota is charged at list price against the CPEA/BTPEA cloud credits.
>
> Example: APEX Holdings has a prepaid quota of 40 GB for Cloud Foundry Runtime. If consumption reaches 60 GB, the first 40 GB is covered by the subscription and the remaining 20 GB is billed at consumption rates against cloud credits.
>
> **Why does this matter?** Monitoring prepaid quota utilization is a core FinOps practice. Maximizing use of your prepaid quota and avoiding unexpected overages directly reduces your cloud bill.

1. In the **Costs and Usage** header, click the **"Important information about your billing and usage data"** link in the Global Account Info card.
2. Confirm that Apex Holdings is licensed for both the **subscription-based** and **consumption-based** commercial models — this is why prepaid quota applies.
3. Close the information panel.

## Exercise 1.2 - Exploring the Overview Tab

The **Overview** tab is the central entry point for FinOps in SAP BTP. It consolidates key cost insights and automated recommendations in one place.

1. Confirm you are on the **Overview** tab (default landing page).
2. Review the **Monthly Cost Summary** card:
   - See the **Total Forecasted Cost for current month** and compare it against the previous month.
   - Note the trend direction — has cost increased or decreased?
3. Review the **Last Month's Prepaid Quota Consumption** card:
   - This shows how much of Apex Holdings' prepaid quota was consumed last month across services.
   - Note which services are approaching or exceeding their quota.
4. Review the **Cost and Usage Recommendations** section:
   - **Budgets Exceeded** — subaccounts or cost centers that have crossed their budget threshold.
   - **Cloud Credit Overage Forecasted** — a warning if the system predicts Apex will exceed cloud credit allocation before the contract ends.
   - **Cost Spikes** — unusual cost increases compared to historical patterns.

> [!NOTE]
> Recommendations are generated automatically from your account's cost patterns and configured thresholds. Acting on them promptly prevents budget overruns and avoids overage charges.

5. Review the **Cost Breakdown** and **Cost Distribution** cards:
   - The **Cost Breakdown** shows your top-cost service plans and subaccounts side by side.
   - The **Cost Distribution** pie charts give an at-a-glance view of how costs are spread across the account.

## Exercise 1.3 - Navigating to the Billing Tab to View Prepaid Quota

1. Click the **"View in Billing Tab"** link from the **Last Month's Prepaid Quota Consumption** card.
   You are now on the **Billing → View by Service** tab for the previous month, filtered to show services with prepaid quota.

2. Locate the **Prepaid Quota** column in the table.
   - This column shows the quota your subscription entitles you to for each service in the selected month.
   - Sort the **Prepaid Quota** column in **descending order** to see the services with the largest prepaid quotas at the top.

3. Compare the **Prepaid Quota**, **Usage**, and **Charged Usage** columns for the top services:
   - **Usage** — total resource units consumed.
   - **Prepaid Quota** — units covered by subscription (no additional charge).
   - **Charged Usage** — units consumed beyond the prepaid quota (billed at list price).

4. Identify a service where **Charged Usage > 0**. This means Apex Holdings has exceeded its prepaid quota for that service and is being billed for the overage.

   <details>
   <summary><b>Which service has charged usage this month?</b></summary>

   **Cloud Foundry Runtime - Standard**

   *This service has exceeded its prepaid quota, generating charged usage that appears on the balance statement. This is the optimization opportunity explored in Exercise 6.*
   </details>

5. Click the **ⓘ information icon** next to any column header to read the definition. Understanding these columns is essential for billing verification (Exercise 2).

## Summary

### 🎯 Key Takeaways

- ✅ Understand how prepaid quota and consumption-based billing work together
- ✅ Navigate the Overview tab as the central FinOps dashboard
- ✅ Use automated recommendations to prioritize FinOps actions
- ✅ Navigate to the Billing tab and read the Prepaid Quota consumption column

---

[← Previous: Exercise 0 - Getting Started](../ex0/) | [Continue to: Exercise 2 - Billing Verification (Optional) →](../ex2/)
