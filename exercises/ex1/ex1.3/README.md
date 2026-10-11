# Exercise 1.3 — Monitoring Costs (approx. 5-7 minutes)

## Exercise 1.3.1 - Introduction

In this section you will monitor costs and resource consumption by comparing services and subaccounts, analyzing trends, and drilling into detailed data. The objective is to identify the reasons behind the cost increase in the previous month — identified in Exercise 1.2 as the highest-cost month over the past 12 months.

## Exercise 1.3.2 - Investigate the Cost Increase

1. In the **Costs and Usage** header, ensure the **Month** filter is set to **Previous Month**.
2. The default view displays **Billing → View by Service**.
3. Which service plan has the highest cost?

   <details>
   <summary><b>Hint</b></summary>

   Sort the **List Price** column in descending order.

   </details>

   <details>
   <summary><b>Answer</b></summary>

   **SAP HANA Cloud - HANA**

   *This service plan has the highest cost and is a key focus area for investigating the cost increase.*

   </details>
4. With no service selected, scroll down to the **Global Account — Cost Summary** graph and choose **View By: Cost Breakdown by Service Plan**.

   1. **Expand** the graph.
   2. Find the highest-cost service plan from the previous step. Has its cost increased compared to the month before?

      <details>
      <summary><b>Answer</b></summary>

      **Yes**

      *SAP HANA Cloud - HANA costs increased from $134K to $180K USD (~$44K delta, over 30%). This upward trend contributes to the overall cost increase and requires investigation to identify which subaccounts are driving the growth.*

      </details>
   3. **Close** the expanded graph.
5. Select the highest-cost service plan in the table.
6. In the right-side panel, review the subaccounts using this service plan.
7. Which subaccount has the highest cost for this service plan in the previous month?

   <details>
   <summary><b>Hint</b></summary>

   Check **"Show subaccounts only"** and sort **List Price** descending.

   </details>

   <details>
   <summary><b>Answer</b></summary>

   **Sales App 1 – PROD**

   *This production subaccount is the primary driver of SAP HANA Cloud costs. Identifying the specific subaccount enables targeted investigation.*

   </details>

   ![Service Plan Details](images/service-plan-subaccount-view.jpg)
8. For this subaccount, click the switch button (highlighted in the screenshot). This navigates to **View by Account**, showing the subaccount within the account hierarchy.
9. Scroll down to the graph and select **Cost Breakdown by Service Plans**. Can you identify the reason for the cost increase?

   <details>
   <summary><b>Answer</b></summary>

   *Sales App 1 – PROD began incurring SAP HANA Cloud – HANA costs last month for the first time — rising from $0 to ~$26K USD. This single subaccount accounts for the majority of the overall $44K HANA cost increase.*

   </details>
10. Close the subaccount detail panel.

## Summary

### 🎯 Key Takeaways

- ✅ Drill down from service-level costs to specific subaccounts
- ✅ Identify highest-cost service plans and trace spending increases
- ✅ Interpret Cost Breakdown graphs for data-driven decisions

---

[← Exercise 1.2 — Billing Verification](../ex1.2/) | [Continue to: Exercise 1.4 — Cross Charge / Cost Allocation →](../ex1.4/)
