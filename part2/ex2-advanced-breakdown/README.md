# Part 2, Exercise 2 — Advanced View: Cost Breakdown & Label Assignment (~8 minutes)

**Goal:** Create a **Cost Center** cost label and assign it to the Apex Holdings account hierarchy — mapping each subsidiary to its dedicated internal cost center.

**Scenario:** APEX Holdings CFO needs to allocate SAP BTP costs to the company's internal cost centers for budget reporting and charge-back. Three of the five subsidiaries drive the majority of BTP spend and will be assigned:

- **Lumina Energy** → **CC-100**
- **NexaTech Digital** → **CC-200**
- **Crestline Retail** → **CC-300**

Atlas Industries and HarborCare Health are smaller-spend subsidiaries and will be left unassigned for now. One decommissioned subaccount — **Backup Vault** — still carries last month's costs with no cost center tag; you'll tag it as well.

You will assign cost centers at the subsidiary (directory) level, then observe how all child subaccounts inherit the assignment automatically — without updating each subaccount individually.

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

## Orientation — The Advanced View Left Panel

The left panel controls what you see in the report. It has three sections:

| Section | Controls |
|---------|----------|
| **Period** | The reporting month — which month's costs are shown |
| **View** | The report perspective — which columns appear and how entities are grouped (e.g., by account hierarchy or by cost label) |
| **Filter** | The rows — which entities are included in the table |

As you work through the exercises, you'll use all three. Keep this structure in mind when switching between them.

## Step 2.2 — Explore the Granular Cost Breakdown

> [!TIP]
> **Part 1 ceiling you're crossing here:** In Exercise 3 you traced the SAP HANA Cloud cost spike to Sales App 1 – PROD — but that's where the trail ended. The current Billing tab shows costs at the subaccount level only. The Advanced view breaks through that ceiling: expand Sales App 1 – PROD and see exactly which Cloud Foundry space and which service instance is responsible.

1. In **Group By**, select **Account → All Account Entities**.
2. The table now shows the full Apex Holdings hierarchy with new granularity levels:
   - **Global Account** → APEX Holdings
   - **Directory (Subsidiary)** → Atlas Industries, Lumina Energy, HarborCare Health, Crestline Retail, NexaTech Digital
   - **Directory (Environment)** → DEV, TEST, PROD under each subsidiary
   - **Subaccount** → e.g., Sales App 1 – PROD, HR App 4 – TEST
   - **Cloud Foundry Space** ← **new level**, not visible in standard Billing tab
   - **Service Instance** ← **new level**, not visible in standard Billing tab
3. Expand **Lumina Energy → PROD** to see **Sales App 1 – PROD**. Continue expanding to see its Cloud Foundry spaces and service instances — including the SAP HANA Cloud instance that caused the cost spike in Part 1.
4. Expand **NexaTech Digital → TEST** to see **HR App 4 – TEST**. Notice that unlike Sales App 1 – PROD, this subaccount's costs appear at the subaccount or CF space level — a reminder that instance-level visibility depends on how each service reports usage.

> [!NOTE]
> Instance-level visibility depends on how each service reports usage. For some services, costs appear at the space or subaccount level rather than the instance level.

## Step 2.3 — Assign Cost Centers to Subsidiaries

> [!TIP]
> **Part 1 ceiling you're crossing here:** In the current Billing tab, labels are set directly on each subaccount — one by one, coupled to the subaccount's lifecycle. To assign a cost center to all 40+ NexaTech Digital subaccounts, you'd update each individually. Here, one assignment at the NexaTech Digital directory cascades to every subaccount inside it instantly. And if a subaccount is later deleted, the label assignment survives — it's no longer tied to the entity.

**Assign Lumina Energy → CC-100:**

1. In the main table, find the **Lumina Energy** directory (top-level subsidiary under APEX Holdings).
2. Click on it to open the details pane. Click **Edit**.
3. In the **Cost Center** field, select **CC-100**. Click **Save**.
4. Observe: a label icon appears next to **Lumina Energy**. Its costs — and the costs of all its child entities — now appear in the **CC-100** column.
5. Expand **Lumina Energy → PROD → Sales App 1 – PROD**. In the details pane, the label shows as **Inherited** from Lumina Energy. No label icon appears next to the subaccount name (icons indicate direct assignment only).

**Assign NexaTech Digital → CC-200:**

6. Find the **NexaTech Digital** directory in the main table.
7. Click on it → **Edit** → select **CC-200** → **Save**.
8. Observe: all NexaTech Digital costs inherit **CC-200**, including **HR App 4 – TEST** (the 40,000+ USD subaccount you identified in Part 1).

**Assign Crestline Retail → CC-300:**

9. Find the **Crestline Retail** directory.
10. Click on it → **Edit** → select **CC-300** → **Save**.
11. Observe: Crestline Retail's costs (including Budgeting Hub, Accounts Payable, Payroll Service) now appear in the **CC-300** column.

**Tag a deleted subaccount — Backup Vault:**

Last month **Backup Vault** was decommissioned, but its costs are still visible in the previous month's data. It appears in the table without a parent directory — an orphaned row.

12. Scroll to the bottom of the entity list to find **Backup Vault**.
13. Click on it → **Edit** → select **CC-100** → **Save**.

> [!NOTE]
> **Backup Vault** no longer exists in the account structure, yet its label assignment is saved and its costs are attributed. This is the key difference from the current Billing tab: in the standard view, a deleted subaccount takes its label with it. Here, the label assignment lives independently of the entity — decommissioning a subaccount does not erase its cost allocation for reporting purposes.

**Expected result:** Most APEX Holdings costs for the previous month are now assigned — Lumina Energy (CC-100), NexaTech Digital (CC-200), and Crestline Retail (CC-300) cover the three highest-spend subsidiaries, and Backup Vault is tagged despite being deleted. Atlas Industries and HarborCare Health remain unassigned, representing subsidiaries not yet configured for cost center reporting.

## Step 2.4 — Label Inheritance and Override

NexaTech Digital hosts applications that support multiple internal teams. The majority are NexaTech's own workloads (CC-200), but **Finance App 3 – PROD** is a shared service owned by Crestline Retail — it should charge to CC-300, not CC-200.

Here, you override one subaccount's cost center without changing the account structure or reassigning any other entity.

1. Expand **NexaTech Digital → PROD** to find **Finance App 3 – PROD**.
2. Click on it — the details pane shows the label as **Inherited: CC-200** (inherited from NexaTech Digital).
3. Click **Edit**. Remove the CC-200 label and assign **CC-300** instead. Click **Save**.
4. Observe: **Finance App 3 – PROD** costs now appear in the **CC-300** column. The **List Price** is unchanged — only the allocation changes. A label icon appears next to the subaccount name (indicating a direct assignment), and the details pane shows the label as **Direct** rather than **Inherited** — confirming that this subaccount's cost center was set explicitly, not cascaded from NexaTech Digital.

> **Key insight:** A subsidiary may host applications that belong to different cost centers. The new label system lets you assign at the subsidiary level for efficiency, then override at the subaccount level for precision — without restructuring the account.

---

[← Exercise 1 — Basic View](../ex1-basic-view/) | [Continue to: Exercise 3 — Fixed Cost Allocation →](../ex3-fixed-allocation/)
