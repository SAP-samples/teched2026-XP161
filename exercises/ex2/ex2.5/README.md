# Exercise 2.5 — Export to Excel (~3 minutes)

> [!TIP]
> **This exercise is optional.** Complete it to share the APEX Holdings cost breakdown with the finance team.

**Goal:** Export the Advanced View cost data to Excel — with cost label assignments included — ready for cross-charge reporting and further analysis.

**Scenario:** APEX Holdings finance team needs the monthly BTP cost breakdown in Excel. The Advanced View export generates a structured workbook that includes both the instance-level cost report (with cost center columns) and all label assignments across every dimension.

## Configure Export Settings

Click **Export** in the top-right toolbar and select **Advanced View** from the dropdown menu.

In the export dialog:

1. **Time Period** — keep the selected month: **September 2026**.
2. **Export only filtered data** — leave this checked.
3. **Label as column** — select **"Cost Center"**.

   > **Why Cost Center?** All labels — Cost Center and Region — are exported as metadata in a dedicated **Cost Labels** sheet. The **"Label as column"** selection applies only to the predefined **Instance Cost by Service** report sheet, where it determines which label values appear as column headers. Since Cost Center is the leading dimension for internal cross-charging in APEX Holdings, we use it here.

4. Click **Export** and open the downloaded file.

## Explore the Exported Workbook

**Instance Cost by Service sheet:**

1. Navigate to the **Instance Cost by Service** sheet.
2. Each row is a service instance; cost is distributed across columns **CC-100**, **CC-200**, and **CC-300** based on the label assignments from Exercises 2–3.

   > **Observe:** Unlike a standard billing export — where cost stops at the subaccount level — each row here represents an individual service instance. This is the same drill-down depth you explored in Exercise 2.2: Cloud Foundry spaces and service instances are fully visible.

3. Click the **CC-100** column to select it — the sum appears in the Excel status bar at the bottom. Repeat for **CC-200** and **CC-300**.

   **Observe:** Which cost center carries the highest total? Does the CC-100 share reflect the fixed percentage allocation from Exercise 2.3?

**Cost Labels sheet:**

4. Navigate to the **Cost Labels** sheet.
5. This sheet lists every entity in the account that has at least one label assignment — across all label keys. Both **Cost Center** and **Region** assignments appear here as separate rows.

   > **Tip:** The Cost Labels sheet is raw data — use it to build additional pivot tables or custom reports in Excel beyond the predefined Instance Cost by Service layout.

---

[← Exercise 2.4 — Additional Label](../ex2.4/) | [Continue to: Exercise 3 — Ask Joule →](../ex3/)
