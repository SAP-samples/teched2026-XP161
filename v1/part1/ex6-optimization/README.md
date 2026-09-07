# Exercise 6 - Optimization (approx. 7 minutes)

> [!NOTE]
> **[DRAFT — CONTENT TBD]**
>
> This exercise adapts Exercise 7 from TechEd 2025 (XP263). Core content covers cloud credit forecasting and prepaid quota vs. consumption optimization. Open question: are there new optimization features in 2026 (e.g., new recommendations types, new optimization views) that should be showcased here instead of or alongside the 2025 content?

## Exercise 6.1 - Introduction

In this section you will identify cost and utilization optimizations for the Apex Holdings global account, focusing on two areas: cloud credit forecasting and prepaid quota management.

## Exercise 6.2 - Optimizing Cloud Credit Costs

**Scenario:** Use cloud credit forecasting to anticipate potential overages and plan purchasing strategy.

![Cloud Credit Forecast](images/cloud-credit-forecast.jpg)

1. On the **Costs and Usage** page, locate the **Cloud Platform Enterprise Agreement** card in the header.
2. Review the current cloud credits to see whether Apex Holdings has exceeded or is approaching its limit.
3. Switch on **"Show Forecast"** to enable predictive analysis.

> [!TIP]
> The forecast uses historical consumption patterns and current trends to predict future cloud credit usage throughout the contract period.

4. Click the expand icon to view the detailed monthly trend graph.
5. Review the forecasted trend. Identify when costs are projected to exceed the cloud credit allocation.
   - **Forecasted Cost** (white) = projected costs within the credit limit
   - **Forecasted Cost Overage** (red) = projected costs beyond the limit

   **When does the forecast predict overage?**

   <details>
   <summary>Answer</summary>

   **In approximately 3–4 months**

   *This early warning provides lead time to purchase additional credits at discounted rates or implement cost reduction measures before overage charges at list price begin.*
   </details>

6. Close the expanded card.

## Exercise 6.3 - Optimizing Prepaid Quota Utilization

**Scenario:** Identify where Apex Holdings is paying consumption-based overage charges that could be eliminated by purchasing additional subscription quota.

![Prepaid Quota Overview](images/prepaid-quota-overview.jpg)

1. Set the **Month** filter to **Previous Month**.
2. Navigate to **Billing → View by Service** and confirm **"Show only services with charged usage"** is **unchecked**.
3. Sort the **Prepaid Quota** column **descending** to show services with the highest quotas first.
4. Review services with prepaid quota. Most have zero Charged Usage and zero List Price — they are consuming within their subscription entitlement.
5. Identify the one service that has both a prepaid quota **and** a non-zero List Price (indicating overage).

   <details>
   <summary>Answer</summary>

   **Cloud Foundry Runtime - Standard**

   *This service has exceeded its prepaid quota and is incurring consumption-based charges for the overage.*
   </details>

6. Select **Cloud Foundry Runtime - Standard**. Scroll down to the graph and choose **View by: Total Usage**.
7. Analyze the 12-month trend:
   - Prepaid quota started at **40 GB**; usage was initially 30 GB, then grew to 40 GB
   - Apex purchased an additional 20 GB subscription, raising the quota to **60 GB**
   - Usage continued to grow to **80 GB**, creating a **20 GB overage** charged at consumption rates

> [!TIP]
> The dotted line in the graph represents the prepaid quota. When the solid usage line exceeds it, you pay consumption-based overage charges.

8. **How can Apex optimize Cloud Foundry Runtime costs?**

   <details>
   <summary>Answer</summary>

   **Purchase an additional 20 GB of prepaid quota subscription**

   *Subscription pricing is lower than consumption-based overage rates. When usage is consistent and predictable, buying quota upfront reduces the total cost.*
   </details>

## Summary

### 🎯 Key Takeaways

- ✅ Use cloud credit forecasting to anticipate overages and act before list-price charges begin
- ✅ Identify services where usage exceeds prepaid quota and overage is being charged
- ✅ Use 12-month usage trends to make data-driven subscription purchasing decisions

> [!TIP]
> Review cloud credits and prepaid quota utilization monthly to catch trends early and make timely purchasing adjustments.

---

[← Previous: Exercise 5 - Controlling Costs Using Budgets](../ex5/) | [Continue to: Exercise 7 - Export to Excel (Optional) →](../ex7/)
