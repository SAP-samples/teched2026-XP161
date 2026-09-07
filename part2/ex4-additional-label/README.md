# Part 2, Exercise 4 — Add a Second Cost Label Dimension — Optional (~5 minutes)

> [!TIP]
> **This exercise is optional.** Complete it if time allows.

**Goal:** Add a second independent cost label dimension for regional cost reporting — enabling the CFO to slice BTP costs by geography alongside the Cost Center dimension from Exercise 2.

**Scenario:** APEX Holdings subsidiaries are multinational companies with operations distributed across regions. Cost center reporting answers *"which business unit is responsible?"* — but the CFO also needs to answer *"which region drove this spend?"* for regional cross-charge reporting and geographic budget allocation.

The two dimensions are fully independent: a workload in CC-200 might serve EMEA, AMER, or APJ. Regional reporting cuts across cost centers without restructuring the account.

APEX Holdings uses four regions: **EMEA**, **AMER**, **APJ**, and **Global** (for shared services with no single regional owner). You already know where two key workloads operate from Part 1:

- **Sales App 1 – PROD** (Lumina Energy) serves the **AMER** market
- **HR App 4 – TEST** (NexaTech Digital) serves the **APJ** region

## Step 4.1 — Create the Region Label

1. In **Group By**, confirm **Cost Labels → All Cost Labels** is selected.
2. Click **Manage Cost Labels → Add Cost Label Key**.
3. Name the key: **"Region"**
4. Add 4 values: **"EMEA"**, **"AMER"**, **"APJ"**, **"Global"**
5. Click **Save**.

**Expected result:** Your second label "Region" with 4 values is ready alongside "Cost Center".

## Step 4.2 — Assign Regions to Known Workloads

1. Switch to **Account → All Account Entities** in **Group By**.
2. In the left sidebar under **View**, set **Cost Label** to **"Region"**.
3. Assign the regions you know from Part 1:
   - Navigate to **Sales App 1 – PROD** (Lumina Energy → PROD) → Edit → assign **AMER** → Save
   - Navigate to **HR App 4 – TEST** (NexaTech Digital → TEST) → Edit → assign **APJ** → Save

## Step 4.2.1 — Observe the Two Dimensions Side by Side

With both assignments saved, the main table now supports two independent label perspectives. Take a moment to switch between them and observe that they are entirely separate.

1. Confirm **Group By** is set to **Account → All Account Entities** and **View → Cost Label** is set to **"Region"**.
   - The table shows each entity's Region assignment. Most entities show no region (unassigned). **Sales App 1 – PROD** shows **AMER**; **HR App 4 – TEST** shows **APJ**.
   - Notice that the region column says nothing about which cost center these workloads belong to.

2. In the left sidebar under **View**, switch **Cost Label** to **"Cost Center"**.
   - The same entities now show their Cost Center assignments from Exercise 2. Sales App 1 – PROD shows **CC-100** (inherited from Lumina Energy); HR App 4 – TEST shows **CC-200** (inherited from NexaTech Digital).

3. Switch **Cost Label** back to **"Region"**.

> **Key observation:** Changing the View dimension does not change any assignment — it only changes which label column is displayed. The two dimensions coexist independently on every entity. A workload tagged CC-100 and AMER holds both labels at the same time; neither overwrites the other.

## Step 4.3 — Cross-Dimensional Reporting

1. In the left sidebar under **Filter**, expand **Cost Labels** and select **Cost Center → CC-100**.
2. The table now shows only CC-100-labeled entities (Lumina Energy and its workloads). With **Region** visible alongside Cost Center, you can see the regional breakdown of Lumina Energy's BTP spend.

   **Question:** What is the total BTP cost for **AMER** workloads within **CC-100**?

   <details>
   <summary>Answer</summary>

   The AMER cost within CC-100 is **27,702.73 USD** — the cost attributed to **Sales App 1 – PROD**, most of which comes from the SAP HANA Cloud instance you identified in Part 1.
   </details>

3. Clear the filter. In **Group By**, select **Cost Labels → All Cost Labels**. Switch the **View Cost Label** to **Region** to see total BTP cost per region across all of APEX Holdings — regardless of which cost center each workload belongs to.

> [!TIP]
> The two label dimensions answer different questions from the same data. Cost Center answers: *"Which business unit do we charge?"* Region answers: *"Which geography drove the spend?"* Filtering by one while viewing the other makes cross-dimensional reporting possible without modifying the account structure or duplicating any data.

---

[← Exercise 3 — Fixed Allocation](../ex3-fixed-allocation/) | [Continue to: Exercise 5 — Export to Excel (Optional) →](../ex5-export/)
