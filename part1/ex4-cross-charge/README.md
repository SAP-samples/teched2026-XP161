# Exercise 4 - Cross Charge / Cost Allocation — Optional for newcomers (approx. 10 minutes)

> [!TIP]
> **This exercise is optional.** Complete it if you are new to cost allocation in SAP BTP. Otherwise, proceed directly to [Exercise 5 - Controlling Costs Using Budgets](../ex5-budgets/).

## Exercise 4.1 - Introduction

**Cross charging** is an internal cost allocation practice where one part of an organization charges another for shared services or resources. It ensures fair cost distribution and helps each business unit reflect the true cost of what it consumes.

In this section you will track costs within the Apex Holdings account hierarchy and distribute expenses across the organization using the account structure and **labels** (Contact Person, Cost Center, Department, Environment, Region).

> [!NOTE]
> In this exercise we focus on cross charging using **today's capabilities** — cost breakdown at the subaccount level combined with account labels. In **Part 2** of this session you will get a preview of the upcoming release, which introduces a fundamentally more powerful cross-charging model: cost allocation at the service instance level, label inheritance across the hierarchy, and fixed percentage distribution for shared resources.

![Account Hierarchy Overview](images/account-hierarchy.jpg)

## Exercise 4.2 - Track Costs Using the Account Hierarchy

1. Ensure the **Month** filter is set to **Previous Month**.
2. Navigate to **Billing → View by Account** and click **Collapse All** to view the account hierarchy. This is the same structure explored in Exercise 0.
3. You will see 5 **subsidiaries** and a list of subaccounts that had cost or usage during the last 12 months and were subsequently deleted.
4. Select subsidiary **NexaTech Digital**. What is the cumulative list price for the last 12 months?

   <details>
   <summary><b>Hint</b></summary>

   Scroll down to the graph and choose **View by: Cumulative List Price**.

   </details>

   <details>
   <summary><b>Answer</b></summary>

   **1,887,337.35 USD**

   *This represents the total cost for NexaTech Digital over 12 months — useful for tracking cost distribution across subsidiaries.*

   </details>
5. Deselect NexaTech Digital.
6. Which subaccount had the highest costs in the previous month?

   <details>
   <summary><b>Hint</b></summary>

   Select **"Show only subaccounts"** and sort **List Price** descending.

   </details>

   <details>
   <summary><b>Answer</b></summary>

   **HR App 4 – TEST**

   *This subaccount has the highest costs, indicating a potential optimization or investigation opportunity.*

   </details>
7. Which service plan is responsible for most of its cost?

   <details>
   <summary><b>Hint</b></summary>

   Select HR App 4 – TEST and scroll down to the graph, choose **View by: Cost Breakdown by Service Plans**.

   </details>

   <details>
   <summary><b>Answer</b></summary>

   **SAP Integration Suite, advanced event mesh - Default**

   *Investigate whether this usage level is expected or if optimization opportunities exist.*

   </details>
8. View the labels assigned to HR App 4 – TEST. Who is the contact person to notify about the cost?

   <details>
   <summary><b>Answer</b></summary>

   **logan.ibrahim@apex.com**

   *Logan Ibrahim is the designated contact and should be notified about the cost exceeding 40,000 USD.*

   </details>
9. Check the **Environment** label. Note that it is labeled **"Test"** — a testing environment with costs higher than most production subaccounts. This warrants investigation.
10. Deselect the subaccount and uncheck **"Show only subaccounts"**.

## Exercise 4.3 - Cross Charge Using Labels

1. Ensure the **Month** filter is set to **Previous Month**.
2. HR App 4 – TEST is in EMEA. What are the total costs for the EMEA region?

   <details>
   <summary><b>Hint</b></summary>

   Type **Region** in the search box and choose **Region: EMEA**, or search for **EMEA** directly.

   </details>

   <details>
   <summary><b>Answer</b></summary>

   **362,710.05 USD**

   *Total cost for the Apex EMEA region in the previous month — useful for regional cross-charging.*

   </details>
3. Bookmark the EMEA filter by clicking the **Bookmark** button. This copies a link you can save or share with the EMEA region owner for ongoing tracking.

## Summary

### 🎯 Key Takeaways

- ✅ Navigate the account hierarchy to compare cost distribution across subsidiaries
- ✅ Use labels (Region, Department, Cost Center, Contact Person, Environment) to filter and aggregate costs
- ✅ Calculate accurate costs for cross-charging using both hierarchy and labels
- ✅ Bookmark and share key views for ongoing tracking

---

[← Previous: Exercise 3 - Monitoring Costs](../ex3-monitoring-costs/) | [Continue to: Exercise 5 - Controlling Costs Using Budgets →](../ex5-budgets/)
