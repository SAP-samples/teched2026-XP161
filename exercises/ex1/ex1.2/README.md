# Exercise 1.2 — Billing Verification (approx. 8 minutes)

## Introduction

Before Dana takes the Q3 numbers to her board, she needs to know they match the actual billing statement.

Billing verification is done on a monthly basis, verifying the charges in the balance statement. It confirms all charges are accurate, establishing confidence in the data before further cost analysis.

1. You are on the **Overview** tab. Scroll to the **footer** of the page and click the **"Billing Statement Information"** link. This links to SAP for Me where you can download the Balance Statement. For this exercise, screenshots are provided — no SAP for Me login is needed.
2. Click the hamburger icon ![hamburger menu icon](images/hamburger.png) in the top-left corner to collapse the left pane and expand the viewing area.
3. Make sure you're in the **Billing** tab, **View by Service**, with all filters cleared and the **Month** set to **Previous Month**.

> [!NOTE]
> The **Billing** tab displays and analyzes monthly charges for all billable services consumed over the last 12 months. Two perspectives are available:
>
> - **View by Service** — suited for billing verification; ordered as in the balance statement.
> - **View by Account** — suited for cross-charging; shows account hierarchy with costs per entity.

**Screenshot: Billing Views by Service**
![Billing View by Service](images/billing-view-by-service-with-cost-summary.jpg)

## Compare the Balance Statement with BTP Cockpit

> [!NOTE]
> The Balance Statement is the starting point for monthly cost verification. Screenshots from the previous month's balance statement are provided below for comparison.

**Screenshot #1: Balance Statement — Total Consumption Section**
![Balance Statement — Total Consumption Section](images/balance_statement_total_consumption.png)

1. The default view is **Billing → View by Service**, sorted automatically by Product (SKU) — matching the balance statement order.
2. Select **"Show only services with charged usage"** to filter out services with zero cost. Compare what disappears with what the balance statement shows.
3. Compare the **Usage**, **Prepaid Quota**, and **Charged Usage** columns for the first three services against screenshot #1. If unsure what a column means, click its ⓘ icon.

**Screenshot #2: Balance Statement — Cloud Platform Enterprise Agreement Section**
![Balance Statement — CPEA Section](images/balance_statement_cpea_section.png)

4. Compare the **List Price** column for the first three services against screenshot #2.
5. Notice that the BTP Cockpit combines both balance statement sections — **Total Consumption** (screenshot #1) and **Cloud Platform Enterprise Agreement** (screenshot #2) — into a single view, enabling drill-down per service.

**Screenshot #3: Balance Statement — Cloud Credits and Payment Summary**
![Balance Statement — Cloud Credits and Payment Summary](images/balance_statement_cloud_credits_payment_summary.png)

6. Cloud credit details are available in the **Overview tab** — refer to the **Cloud Platform Enterprise Agreement** card you explored in Exercise 1.1 to verify consumed and remaining cloud credits against the balance statement.
7. In screenshot #3 (section 3.B), the balance statement shows **remaining cloud credits**. Confirm this matches what you saw in the CPEA card on the Overview tab.
8. Remaining cloud credits mean no Net Overage Amount — the Payment Summary shows no additional costs to pay.

## Summary

### 🎯 Key Takeaways

- ✅ Find the Billing Statement Information link in the Overview tab footer
- ✅ Verify balance statement data systematically against the BTP Cockpit Billing view
- ✅ Validate cloud credit balances using the CPEA card on the Overview tab

*For Dana:* With the bill verified against the cockpit, Dana can quote these Q3 figures to her board with confidence.

---

[← Exercise 1.1 — Cost and Usage Overview](../ex1.1/) | [Continue to: Exercise 1.3 — Monitoring Costs →](../ex1.3/)
