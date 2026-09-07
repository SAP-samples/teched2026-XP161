# Part 2, Exercise 2 — Advanced View: Cost Breakdown & Label Assignment (~8 minutes)

**Goal:** Create a **Line of Business** cost label and assign it to the Apex Holdings account hierarchy — connecting the cost insights from Part 1 to Apex's internal business lines.

**Scenario:** Apex Holdings CFO wants to understand SAP BTP costs by business line: **Sales**, **Finance**, and **HR Operations**. You know from Part 1 exactly which entities are the cost drivers:
- **Lumina Energy** subsidiary is home to **Sales App 1 – PROD** (SAP HANA Cloud spike) → assign to **Sales**
- **NexaTech Digital** subsidiary is home to **HR App 4 – TEST** (40K budget breach) → assign to **HR Operations**
- **Crestline Retail** subsidiary runs Finance apps (Budgeting Hub, Accounts Payable) → assign to **Finance**

You will assign labels at the subsidiary level, then observe how child subaccounts inherit them automatically.

## Step 2.1 — Switch to Advanced View and Create the Line of Business Label

1. In the left sidebar, click **"Advanced"**.
2. In the **Group By** dropdown, confirm **Cost Labels → All Cost Labels** is selected.
3. The system shows default **Sample** labels — these are placeholders. The new label system is separate from the Apex labels you used in Part 1 (Contact Person, Cost Center, Department, Region).
4. Click **Manage Cost Labels** and update the sample label:
   - Rename the label key to **"Line of Business"** (remove *(Sample)*)
   - Rename the three values to **"Sales"**, **"Finance"**, and **"HR Operations"** (remove *(Sample)* from each)
   - Delete the 4th sample value
   - Click **Save**. When prompted, click **Close**.

**Expected result:** Your "Line of Business" label with values Sales, Finance, and HR Operations is ready.

## Step 2.2 — Explore the Granular Cost Breakdown

> [!TIP]
> **Part 1 ceiling you're crossing here:** In Exercise 3 you traced the SAP HANA Cloud spike to Sales App 1 – PROD — but that's where the trail ended. The current Billing tab shows costs at the subaccount level only. The Advanced view breaks through that ceiling: expand Sales App 1 – PROD and see exactly which Cloud Foundry space and which service instance is responsible.

1. In **Group By**, select **Account → All Account Entities**.
2. The table now shows the full Apex Holdings hierarchy with new granularity levels:
   - **Global Account** → APEX Holdings
   - **Directory (Subsidiary)** → Atlas Industries, Lumina Energy, HarborCare Health, Crestline Retail, NexaTech Digital
   - **Directory (Environment)** → DEV, TEST, PROD under each subsidiary
   - **Subaccount** → e.g., Sales App 1 – PROD, HR App 4 – TEST
   - **Cloud Foundry Space** ← **new level**, not visible in standard Billing tab
   - **Service Instance** ← **new level**, not visible in standard Billing tab
3. Expand **Lumina Energy → PROD** to see **Sales App 1 – PROD**. Continue expanding to see its Cloud Foundry spaces and service instances inside — including the SAP HANA Cloud instance that caused the cost spike in Part 1.
4. Expand **NexaTech Digital → TEST** to see **HR App 4 – TEST** and drill down to its SAP Integration Suite instances.

> [!NOTE]
> Instance-level visibility depends on how each service reports usage. For some services, costs appear at the space or subaccount level rather than the instance level.

## Step 2.3 — Assign Line of Business to Subsidiaries

> [!TIP]
> **Part 1 ceiling you're crossing here:** In the current Billing tab, cost labels (Department, Region, etc.) are set directly on each subaccount — one by one, coupled to the subaccount's lifecycle. To tag all 40+ NexaTech Digital subaccounts as "HR Operations" in the current tab, you'd update each individually. Here, one assignment at the NexaTech Digital directory cascades to every subaccount inside it instantly. And if a subaccount is later deleted, the label assignment survives — it's no longer tied to the entity.

**Assign Lumina Energy → Sales:**

1. In the main table, find the **Lumina Energy** directory (top-level subsidiary under APEX Holdings).
2. Click on it to open the details pane. Click **Edit**.
3. In the **Line of Business** field, select **Sales**. Click **Save**.
4. Observe: a label icon appears next to **Lumina Energy**. Its costs — and the costs of all its child entities — now appear in the **Sales** column.
5. Expand **Lumina Energy → PROD → Sales App 1 – PROD**. In the details pane, the label shows as **Inherited** from Lumina Energy. No label icon appears next to the subaccount name (icons indicate direct assignment only).

**Assign NexaTech Digital → HR Operations:**

6. Find the **NexaTech Digital** directory in the main table.
7. Click on it → **Edit** → select **HR Operations** → **Save**.
8. Observe: all NexaTech Digital costs inherit **HR Operations**, including **HR App 4 – TEST** (the 40,000+ USD subaccount you identified in Part 1).

**Assign Crestline Retail → Finance:**

9. Find the **Crestline Retail** directory.
10. Click on it → **Edit** → select **Finance** → **Save**.
11. Observe: Crestline Retail's costs (including Budgeting Hub, Accounts Payable, Payroll Service) now appear in the **Finance** column.

**Expected result:** In **Group By → Cost Labels → All Cost Labels**, you can see how APEX Holdings total cost is distributed across Sales, Finance, and HR Operations.

## Step 2.4 — Label Inheritance and Override

NexaTech Digital runs mixed workloads — HR apps, Finance apps, IT apps, and Sales apps all co-exist under one subsidiary. The current Billing tab has no way to express this: each subaccount has its own Department label, but there's no cost-allocation layer on top that lets you re-cut those costs by business line without changing the account structure.

Here, you assign at the subsidiary level for efficiency and override at the subaccount level for precision — no account restructuring needed.

NexaTech Digital also runs Finance App 2, Finance App 3, Finance App 4. Let's reassign one of them to Finance instead of inheriting HR Operations.

1. Expand **NexaTech Digital → PROD** to find **Finance App 3 – PROD**.
2. Click on it — the details pane shows the label as **Inherited: HR Operations** (inherited from NexaTech Digital).
3. Click **Edit**. Remove the HR Operations label and assign **Finance** instead. Click **Save**.
4. Observe: **Finance App 3 – PROD** costs now appear in the **Finance** column. The **List Price** is unchanged — only the allocation changes.

> **Key insight:** Subsidiaries often run mixed workloads across business lines. The new label system lets you assign at the subsidiary level for efficiency, then override at the subaccount level for precision — without restructuring the account.

---

[← Exercise 1 — Basic View](../ex1-basic-view/) | [Continue to: Exercise 3 — Fixed Cost Allocation →](../ex3-fixed-allocation/)
