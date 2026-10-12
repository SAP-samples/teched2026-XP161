# Exercise 2.2 — Advanced View: Cost Breakdown & Label Assignment (~8 minutes)

**Goal:** Create a **Cost Center** cost label and assign it to the Apex Holdings account hierarchy — mapping each subsidiary to its dedicated internal cost center.

**Scenario:** Assign cost centers to three of APEX Holdings' five subsidiaries for budget reporting and charge-back:

- **Lumina Energy** → **CC-100**
- **NexaTech Digital** → **CC-200**
- **Crestline Retail** → **CC-300**

Atlas Industries and HarborCare Health are left unassigned — the same assignment flow applies and is omitted here for brevity. One decommissioned subaccount — **Backup Vault** — still carries last month's costs with no cost center tag; you'll tag it to demonstrate that advanced cost labels are decoupled from the entity lifecycle.

Assignments are made at the subsidiary (directory) level, and all child subaccounts inherit automatically.

## Step 2.1 — Switch to Advanced View and Create the Cost Center Label

1. In the left sidebar, click **"Advanced"**.
2. In the **Group By** dropdown, confirm **Cost Labels → All Cost Labels** is selected.
   1. The system shows default **Sample** labels — these are placeholders. You'll rename them to create a **Cost Center** dimension for internal allocation.
3. Click **Manage Cost Labels** and update the sample label:
   - Rename the label key to **"Cost Center"** (remove *(Sample)*)
   - Rename the three values to **"CC-100"**, **"CC-200"**, and **"CC-300"** (remove *(Sample)* from each)
   - Delete the 4th sample value
   - Click **Save**. When prompted, click **Close**.

**Expected result:** Your "Cost Center" label with values CC-100, CC-200, and CC-300 is ready.

## Step 2.2 — Explore the Granular Cost Breakdown

1. In **Group By**, select **Account → All Account Entities**.
2. The table now shows the full hierarchy down to **Cloud Foundry Space** and **Service Instance**.

**Can you view the costs of the HANA instances contributing to the Sales App 1 – PROD cost spike?**

<details>
<summary>Hint</summary>

Drill down: **Lumina Energy → PROD → Sales App 1 – PROD → sales_app_1_prod_space_1**

</details>

<details>
<summary>Answer</summary>

Yes — SAP HANA Cloud costs are visible at the instance level. In this case, a single instance in the subaccount is responsible for the spike, with a cost of **26,371.50 USD**.

</details>

> [!NOTE]
> Cost breakdown to space or instance level is optional and may not be supported for all services.

## Step 2.3 — Assign Cost Centers to Subsidiaries

> [!TIP]
> **Exercise 1 ceiling you're crossing here:** One directory-level assignment cascades to all 40+ child subaccounts instantly — no individual updates. And if a subaccount is later deleted, the label assignment survives.

**Assign Lumina Energy → CC-100:**

1. In the main table, find the **Lumina Energy** directory (top-level subsidiary under APEX Holdings).
2. Click on it to open the details pane. Click **Edit**.
3. In the **Cost Center** field, select **CC-100**. Click **Save**.
4. Close the details pane to see the updated table.
5. Observe: a label icon appears next to **Lumina Energy**. Its costs — and the costs of all its child entities — now appear in the **CC-100** column.
6. Expand **Lumina Energy → PROD → Sales App 1 – PROD**. In the details pane, the label shows as **Inherited** from Lumina Energy. No label icon appears next to the subaccount name (icons indicate direct assignment only).

**Repeat the same flow for the remaining subsidiaries:**

7. **NexaTech Digital → CC-200** — close the pane and verify that **HR App 4 – TEST** (40,000+ USD) now appears in the CC-200 column.
8. **Crestline Retail → CC-300** — close the pane and verify its costs appear in CC-300.

**Tag a deleted subaccount — Backup Vault:**

Last month **Backup Vault** was decommissioned, but its costs are still visible in the previous month's data. It appears in the table without a parent directory — an orphaned row.

9. Scroll to the bottom of the entity list to find **Backup Vault**.
10. Click on it → **Edit** → select **CC-100** → **Save**.
11. Close the details pane to see the updated table.

> [!NOTE]
> **Backup Vault** no longer exists in the account structure, yet its label assignment and costs are still attributed. Unlike the standard Billing tab — where a deleted subaccount takes its labels with it — cost label assignments here are independent of the entity lifecycle.

**Expected result:** Lumina Energy (CC-100), NexaTech Digital (CC-200), Crestline Retail (CC-300), and Backup Vault (CC-100) are assigned. Atlas Industries and HarborCare Health remain unassigned.

## Step 2.4 — Label Inheritance and Override at Instance Level

Sales App 1 – PROD inherits **CC-100** from Lumina Energy. Inside it, three SAP HANA Cloud instances share the same space — but each is used by a different team. Two of them should be attributed to different cost centers.

1. Expand **Lumina Energy → PROD → Sales App 1 – PROD → sales_app_1_prod_space_1**.
2. You will see three SAP HANA Cloud – HANA instances, all currently showing costs in the **CC-100** column (inherited from Lumina Energy).

3. Click on instance `cce2dd07-0931-4355-95c8-aa037a88f83c` → **Edit** → deselect **CC-100**, select **CC-200** → **Save**.
4. Override instance `30eeba60-2008-4dc9-bf2b-9db1f358e8a4` with **CC-300** the same way.
5. View the result in the main table.

**How are Lumina Energy's costs now distributed across cost centers?**

<details>
<summary>Answer</summary>

The costs are split across three cost centers:
- **CC-100** — $X (all Lumina Energy entities except the two overridden instances)
- **CC-200** — $Y (instance `cce2dd07-0931-4355-95c8-aa037a88f83c`)
- **CC-300** — $Z (instance `30eeba60-2008-4dc9-bf2b-9db1f358e8a4`)

</details>

> **Key insight:** Overrides work at any level of the hierarchy — from subsidiary down to individual service instance. The details pane always shows whether a label is **Inherited** or **Direct**, so you can audit every assignment at a glance.

---

[← Exercise 2.1 — Basic View](../ex2.1/) | [Continue to: Exercise 2.3 — Fixed Cost Allocation →](../ex2.3/)
