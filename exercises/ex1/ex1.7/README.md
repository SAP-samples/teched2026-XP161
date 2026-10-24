# Exercise 1.7 — Export to Excel — Optional (approx. 10 minutes)

> [!TIP]
> **This exercise is optional.** Complete it if time allows, or revisit it later using your own SAP BTP account. Ensure labels are assigned to your subaccounts beforehand to maximize the exercise value.

## Introduction

Dana needs the cost center breakdown as a workbook she can pivot herself — export it here.

The **Export to Excel** feature lets you download BTP cost data for the past 12, 24, or 36 months. You can customize the export by applying filters (subaccounts, labels, services) and adding label columns. The exported file integrates with third-party reporting tools.

![1789985877830](images/export-excel-custom-menu.jpg)

## Scenario 1: Share Costs with a Contact Person

**Scenario:** Export cost data filtered by a specific contact person to share relevant costs with a stakeholder.

1. Make sure you're in the **Billing** tab, with all filters cleared and the **Month** set to **Previous Month**.
2. In the search box, type `ContactPerson` and use auto-complete to select `ContactPerson alex.yamamoto@apex.com`.
3. Click the small arrow next to the **Export** button and select **"Custom..."**.
4. Verify: time period = the previous month (shown as the month name in the UI); search filter shows `ContactPerson:alex.yamamoto@apex.com`.
5. Keep default settings and click **Export**.
6. Open the exported Excel file from your Downloads folder.
   - The **Global Account Costs** and **Subaccount Costs by Service** sheets are filtered to the selected contact person.
7. In the **Global Account Costs** sheet, select column I (Cost) to see the total cost for this contact in the footer.
8. Use this file to share costs with the contact person and prompt action if needed.

> You can apply the same approach with any label (service, subaccount, department, cost center) to generate stakeholder-specific cost reports.

## Scenario 2: Aggregate Costs by Cost Center

**Scenario:** Export all costs with a cost center label column, then use Excel's AI analytics to aggregate and compare cost centers.

1. Click **"Clear Filters"** to reset all filters.
2. Set **Month** to **Previous Month**.
3. Click the small arrow next to **Export** and select **"Custom..."**.
4. Confirm all **Active Filters** show **(no filter)**.
5. In the **"Labels as Columns"** field, enter: `CostCenter`

> [!TIP]
> Adding labels as columns lets you pivot and analyze data by those dimensions in Excel — useful for aggregating costs by business unit, department, or project.

6. Click **Export** and open the downloaded file.
7. Navigate to the **"Subaccount Costs by Service"** sheet.
8. Find the column **"Label Values for Key: CostCenter"** — this contains the cost center labels (e.g. CC-100, CC-200). Note: there is also an adjacent **"Entity ID of Label Source: CostCenter"** column showing a GUID — ignore that one. Use Excel's filter on the label column to isolate any cost center and sum its total. This column also works as a dimension in a pivot table, giving you a data cube where cost center is one axis of your cost analysis.

### Using Excel's Analyze Data Feature

1. In Excel, click the **Data** tab in the ribbon, then click **"Analyze Data"**.
2. In the text box, enter: `Cost by Label Values for Key: CostCenter`
3. Review the generated analysis and click **"Insert PivotChart"** to add it to your worksheet.

   **Which cost center has the highest costs?**

   <details>
   <summary>Answer</summary>

   **CC-400**

   *Cost center CC-400 has the highest aggregated costs. This insight helps focus budget adjustments and optimization efforts.*

   </details>

## Summary

### 🎯 Key Takeaways

- ✅ Export customized cost data (12–36 months) with filters and label columns for tailored reporting
- ✅ Share filtered cost reports by contact person for transparent, data-driven cost discussions
- ✅ Use Excel's AI-powered Analyze Data to aggregate and compare cost centers with natural language
- ✅ Integrate SAP BTP cost data into third-party reporting tools

*For Dana:* Dana now has a board-ready export she can share with each cost owner — the deliverable behind her question.

---

[← Exercise 1.6 — Optimization](../ex1.6/) | [Continue to: Exercise 2 — Advanced Cost Allocation →](../../ex2/)
