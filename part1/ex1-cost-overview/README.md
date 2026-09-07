# Exercise 1 — Cost and Usage Overview (approx. 10 minutes)

The **Overview** tab is the central entry point for FinOps in SAP BTP. It brings together monthly cost intelligence, contract status, prepaid quota, automated recommendations, and cost distribution in a single page.

In this exercise you will navigate the Overview tab card by card — building the picture of APEX Holdings' financial situation before diving deeper in the exercises that follow.

---

## Card 1 — Monthly Cost Summary

The **Monthly Cost Summary** card at the top of the Overview shows the current month's spend at a glance.

1. Locate the **Monthly Cost Summary** card.
2. Review each field:
   - **Total Cost Last Month** — the finalized list-price spend for the completed previous month. This is the number Dana Mercer is reacting to.
   - **Total Forecasted Cost for Current Month** — an estimate of this month's spend based on usage so far. It updates continuously as the month progresses.
   - **Trend indicator** — compares this month's forecast against last month's actual. A red upward arrow signals the 40% increase Dana mentioned.
   - **Average Monthly Cost for Last 12 Months** — the mean monthly spend over the past year. Use this as the baseline to judge whether the current month is an anomaly or part of a longer trend.
   - **Highest Monthly Cost for Last 12 Months** — the single most expensive month in the past year. If the current month's forecast exceeds this, APEX Holdings is about to set a new record.
   - **Lowest Monthly Cost for Last 12 Months** — the cheapest month in the past year. Useful for understanding seasonal patterns or identifying months where cost reduction measures worked.

> [!NOTE]
> The current month's cost is an estimate until the billing cycle closes. Once closed, it becomes finalized and will no longer show as estimated.

---

## Card 2 — Cloud Platform Enterprise Agreement

The **Cloud Platform Enterprise Agreement** card shows APEX Holdings' CPEA contract — the cloud credit pool that backs all consumption-based spending.

1. Locate the **Cloud Platform Enterprise Agreement** card.
2. The card shows a **progress bar** for the current contract phase. The percentage label on the bar tells you at a glance how far into the phase budget APEX Holdings is. Below the bar you can see the total cloud credits for this phase and how much has been consumed.
3. **Enable the forecast:** toggle on **"Show Forecast"**.
   - The card now shows a cost projection through the end of the contract.
   - **Forecasted Cost Overage** (shown in red) — the amount projected to exceed the cloud credit balance. APEX Holdings' current consumption rate leads to overage starting in **January 2027** — approximately 3 months from now.
   - This early warning gives lead time to act: either purchase additional credits at contract rates, or reduce consumption before list-price overage charges begin.
4. Click the **expand icon** to open the detailed monthly trend graph.
   - Each bar shows the monthly spend against the cloud credit pool.
   - The red bars extending into future months show the projected overage period — starting January 2027.
   - The expanded view also shows **contract phase details**: start and end dates of the current phase and its total credit allocation.
5. Close the expanded view.

> [!TIP]
> Clicking **"Show Forecast"** early in the month gives you lead time to act — either by purchasing additional credits at contract rates or by reducing consumption before overage charges at list price begin.

---

## Card 3 — Last Month's Prepaid Quota Consumption

APEX Holdings uses a **hybrid commercial model** — a subscription component that includes prepaid quotas for specific services, combined with CPEA cloud credits for consumption. You can find the full commercial model details in the **Overview footer** (scroll to the bottom of the page and click "Important information about your billing and usage data").

The **Last Month's Prepaid Quota Consumption** card shows how much of the subscription-included quota APEX Holdings consumed last month.

1. Locate the **Last Month's Prepaid Quota Consumption** card.
2. Review the services listed. For each service you can see:
   - **Prepaid Quota** — the subscription entitlement for that service last month
   - **Prepaid Quota Used** — how much of that entitlement was consumed (shown as a percentage bar)
   - Services over 100% have exceeded their quota and are generating consumption overage charges
3. Click **"View in Billing Tab"** to open the Billing view filtered to services with prepaid quota.
4. In the Billing tab, locate the **Prepaid Quota** column:
   - **Prepaid Quota** — the subscription-included entitlement
   - **Prepaid Quota Used** — units consumed against that entitlement
   - **Charged Usage** — units consumed beyond the quota, billed at list price against cloud credits
5. Return to the **Overview** tab (use the browser back button or the Overview tab).

> We will investigate the specific service exceeding its quota in Exercise 6 (Optimization).

---

## Card 4 — Cost and Usage Recommendations

The **Cost and Usage Recommendations** section surfaces automated alerts based on APEX Holdings' cost patterns and configured thresholds. APEX Holdings has **4 active recommendations** today.

1. Locate the **Cost and Usage Recommendations** section.
2. You will see the first few recommendations listed. Click **"Show more"** to expand and see all 4.
3. Review the recommendation types — Apex has recommendations across three categories:
   - **Budget exceeded** — a subaccount or service has crossed a configured budget threshold
   - **Cloud credit overage forecasted** — the system predicts CPEA credits will be exhausted before contract end
   - **Cost spike** — an unusual cost increase detected compared to historical patterns
4. Find the **4th recommendation** (a cost spike recommendation). Click **"View subaccount costs in Billing tab"**.
5. You are now in the Billing tab filtered to the relevant subaccount. Click on **"Budgeting Hub – TEST"** in the table to select it.
6. Scroll down to the **cost graph** below the table.
   - You can see the month-over-month cost trend for Budgeting Hub – TEST.
   - Identify the month where the cost spike occurred — a bar significantly higher than the surrounding months.

> [!NOTE]
> Budgeting Hub – TEST belongs to the **Crestline Retail** subsidiary (Finance department, EMEA region, contact: alex.yamamoto@apex.com). In Exercise 4 you will explore how to use labels to track ownership and cross-charge this cost.

7. Return to the **Overview** tab.

---

## Card 5 — Cost Breakdown and Cost Distribution

The final two sections of the Overview provide complementary visual perspectives on APEX Holdings' spend.

1. Locate the **Cost Breakdown** section:
   - Shows the **top service plans** and **top subaccounts** ranked by cost, with a **monthly bar chart** for each entry covering the last 12 months.
   - This is a trend view — you can see not just who costs the most today, but how that cost has moved month by month over the past year. A growing bar chart signals acceleration; a flat one indicates stable spend.
   - Use this to quickly identify the biggest cost drivers and spot which of them are trending upward.

2. Locate the **Cost Distribution** section:
   - Shows pie charts for **service plans** and **subaccounts**, based on **cumulative costs over the last 12 months**.
   - This is a proportional view — it answers "what percentage of our total annual spend went to each service or subaccount?" rather than showing monthly fluctuations.
   - Use this to understand the overall cost composition of APEX Holdings' BTP portfolio and identify concentration risk (e.g., one service dominating 60% of spend).

---

## Summary

### 🎯 Key Takeaways

- ✅ The Overview tab consolidates the full APEX Holdings cost picture in one page
- ✅ Monthly Cost Summary shows finalized vs. estimated spend and the trend direction
- ✅ The CPEA card with forecast tells you when cloud credits will be exhausted — early warning for contract management
- ✅ Prepaid Quota Consumption shows subscription utilization — services over quota generate additional charges against cloud credits
- ✅ Automated recommendations surface budget breaches, overage forecasts, and cost spikes proactively
- ✅ Cost Breakdown and Distribution give a ranked and proportional view of the top cost drivers

---

[← Previous: Exercise 0 - Getting Started](../../ex0/) | [Continue to: Exercise 2 - Billing Verification (Optional) →](../ex2-billing-verification/)
