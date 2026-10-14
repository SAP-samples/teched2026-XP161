# Exercise 1.1 — Cost and Usage Overview (approx. 10 minutes)

The **Overview** tab is the central entry point for FinOps in SAP BTP. It brings together monthly cost intelligence, contract status, prepaid quota, automated recommendations, and cost distribution in a single page.

In this exercise you will navigate the Overview tab card by card — building the picture of APEX Holdings' financial situation before diving deeper in the exercises that follow.

> [!NOTE]
> The current month is still in progress, so any current-month cost shown on this page is an estimate until the billing cycle closes. Once closed, it is finalized and no longer marked as estimated.

---

## Monthly Cost Summary

The **Monthly Cost Summary** card combines current-month metrics with statistical benchmarks from the last 12 months — giving you both where you are now and the historical context to judge whether it's normal.

1. Locate the **Monthly Cost Summary** card.
2. The card shows current-month metrics — month-to-date spend and a full-month forecast — alongside key benchmarks from the last 12 months: the average, the highest, and the lowest monthly cost.
3. Go over the insights. Based on what you see at first glance, can you support Dana's assumption of a cost increase?

   <details>
   <summary>Answer</summary>

   **Yes.** Last month's total cost is the highest in the 12-month window, and the current month's forecast is projected even higher — confirming the upward trend Dana is reacting to.

   </details>

---

## Cloud Platform Enterprise Agreement

Analyzing costs is only half of FinOps. The other half is managing the contract. APEX Holdings runs on a **CPEA (Cloud Platform Enterprise Agreement)** — a cloud credit pool that covers all consumption-based spending. Staying within that pool matters: charges beyond the cloud credit pool or limit are billed at list price, which is higher than the contracted rate — cloud credits are purchased at a discount, so consumption beyond the limit costs more.

1. Locate the **Cloud Platform Enterprise Agreement** card and review the current cloud credit balance.
2. Toggle on **"Show Forecast"** to project consumption through the end of the contract.
3. Click the **expand icon** to see the detailed monthly trend graph.

**Is there an expected overage?**

<details>
<summary>Answer</summary>

**Yes.** At the current consumption rate, APEX Holdings is projected to exceed its cloud credit balance before the current contract period ends.

</details>

**When does the overage start, and how long is it expected to remain in overage state until a new period starts?**

<details>
<summary>Answer</summary>

- **Overage starts:** mid-January 2027 — approximately 3 months from now
- **Duration:** approximately 2 months, through end of March 2027

Unless additional credits are purchased or consumption is reduced, APEX Holdings will be billed at list price for that entire period.

</details>

4. Close the expanded view.

> [!TIP]
> Spotting the overage 3 months ahead — here, from the CPEA forecast — gives enough lead time to negotiate additional credits at contracted rates. Waiting until January means paying list price.

---

## Last Month's Prepaid Quota Consumption

APEX Holdings runs on a **combined commercial model** — licensed for both a consumption-based model (the CPEA cloud credits from the previous card) and a **subscription-based model** that provides prepaid quotas for specific services at a fixed cost.

For subscription-based services, usage within the prepaid quota is already paid for. Only usage that **exceeds** the quota is charged — at your consumption-based rates, against the cloud credit pool. Consumption well below quota means the subscription isn't being used optimally — you're paying for quota you don't consume.

> [!TIP]
> In the UI, the **Combined commercial model** info link explains how billing works across both models.

This card helps identify both problems at a glance.

1. Locate the **Last Month's Prepaid Quota Consumption** card. The pie chart groups the 7 subscription service plans used last month by utilization level: exceeded quota, 81–100% utilized, and 1–80% utilized.

**How many service plans exceeded the prepaid quota last month, and how many are significantly under-utilized (below 80%)?**

<details>
<summary>Answer</summary>

- **Exceeded quota:** 1 service plan
- **Under-utilized (<80%):** 6 service plans

</details>

2. Click **"View in Billing tab"** to see the breakdown by service plan.

**In the table, add the Prepaid Quota Used column via table settings if not visible. Which service plan exceeded its quota, and which are under-utilized?**

<details>
<summary>Answer</summary>

**Exceeded:**

- Cloud Foundry Runtime - Standard — **133%** (80 GB used, 60 GB quota, 20 GB overage charged)

**Under-utilized:**

- SAP Build Apps - Standard — 40%
- Cloud Transport Management - Standard — 20%
- Integration Suite - Edge Integration Cell — 13%
- Alert Notification - standard — 4%
- SAP Build Work Zone, standard edition - Standard — 1%
- Integration Suite - Messages — 1%

</details>

3. Return to the **Overview** tab.

> [!NOTE]
> We will investigate the Cloud Foundry Runtime overage in Exercise 1.6 (Optimization).

---

## Cost and Usage Recommendations

The **Cost and Usage Recommendations** section surfaces insights that help you monitor costs, identify anomalies, control spending, and optimize your contract. Each recommendation includes a link to navigate directly to the relevant data.

1. Locate the **Cost and Usage Recommendations** section.
2. Go through the recommendations. You will notice:

   - A **budgets** recommendation — no budgets are configured yet for this account. We will set one up in Exercise 1.5.
   - A **cloud credit overage** forecast — you already identified this proactively in Card 2.
   - Two **cost spike** recommendations — one for unusual service plan costs, one for a subaccount anomaly.
3. Find the **4th recommendation** (a cost spike recommendation). Click **"View subaccount costs in Billing tab"**.
4. In the Billing tab, click on **"Budgeting Hub – TEST"** to select it.
5. Scroll down to the **cost graph** below the table.

**What is the significant spike in the last month for this subaccount?**

<details>
<summary>Answer</summary>

A cost increase of over 60% in the last month compared to the previous month.

</details>

> [!NOTE]
> Budgeting Hub – TEST belongs to the **Crestline Retail** subsidiary (Finance department, EMEA region, contact: alex.yamamoto@apex.com) — you can see these details yourself by clicking the **labels** link on the subaccount. In Exercise 1.4 you will explore how to use labels to track ownership and cross-charge this cost.

6. Return to the **Overview** tab.

---

## Cost Breakdown and Cost Distribution

1. Locate the **Cost Breakdown** section. It shows the top service plans and top subaccounts ranked by cost, each with a monthly bar chart covering the last 12 months.
2. Click the **expand icon** on a chart to view its full 12-month trend.

**Can you see the overall cost increase trend Dana mentioned?**

<details>
<summary>Answer</summary>

Yes — even without calculating quarterly totals, the bar charts make it visible: the highest month in Q2 is less costly than the lowest month in Q3, confirming a clear upward shift between the two quarters.

</details>

2. Locate the **Cost Distribution** section. It shows pie charts for service plans and subaccounts based on cumulative costs over the last 12 months.

**Which service plan is the top cost driver over the last 12 months?**

<details>
<summary>Answer</summary>

**SAP HANA Cloud - HANA** is the top cost driver for the last 12 months, responsible for **22.2%** of APEX Holdings' overall BTP costs.

</details>

---

## Summary

### 🎯 Key Takeaways

- ✅ The Overview tab consolidates the full APEX Holdings cost picture in one page
- ✅ Monthly Cost Summary shows the current month's estimate, full-month forecast with trend, last month's finalized cost, and 12-month benchmarks
- ✅ The CPEA card with forecast tells you when cloud credits will be exhausted — early warning for contract management
- ✅ Prepaid Quota Consumption shows subscription utilization — services over quota generate additional charges against cloud credits
- ✅ Automated recommendations surface budget breaches, overage forecasts, and cost spikes proactively
- ✅ Cost Breakdown and Distribution give a ranked and proportional view of the top cost drivers

---

[← Getting Started](../../ex0/) | [Continue to: Exercise 1.2 — Billing Verification →](../ex1.2/)
