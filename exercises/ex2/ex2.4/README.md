# Exercise 2.4 — Add a Second Cost Label Dimension — Optional (~5 minutes)

> [!TIP]
> **This exercise is optional.** Complete it if time allows.

**Goal:** Add a second independent cost label dimension for regional cost reporting — enabling the CFO to slice BTP costs by geography alongside the Cost Center dimension from Exercise 2.

**Scenario:** APEX Holdings subsidiaries are multinational companies with operations distributed across regions. Cost center reporting answers *"which business unit is responsible?"* — but the CFO also needs to answer *"which region drove this spend?"* for regional cross-charge reporting and geographic budget allocation.

The two dimensions are fully independent: a workload in CC-200 might serve EMEA, AMER, or APJ. Regional reporting cuts across cost centers without restructuring the account.

APEX Holdings uses four regions: **EMEA**, **AMER**, **APJ**, and **Global** (for shared services with no single regional owner). You already know where two key workloads operate from Exercise 1:

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
3. Assign the regions you know from Exercise 1:
   - Navigate to **Sales App 1 – PROD** (Lumina Energy → PROD) → Edit → assign **AMER** → Save
   - Navigate to **HR App 4 – TEST** (NexaTech Digital → TEST) → Edit → assign **APJ** → Save

## Step 4.2.1 — Observe the Two Dimensions Side by Side

1. Confirm **Group By → Account → All Account Entities** and **Cost Label → Region**. Sales App 1 – PROD shows **AMER**; HR App 4 – TEST shows **APJ**. Cost center is not visible here.
2. Switch **Cost Label** to **"Cost Center"** — the same entities now show CC-100 and CC-200. Neither dimension overwrites the other.
3. Switch **Cost Label** back to **"Region"**.

## Step 4.3 — Cross-Dimensional Reporting

1. Filter by **Cost Center → CC-100**. The table shows only Lumina Energy's workloads.

   **What is the total cost for AMER workloads within CC-100?**

   <details>
   <summary>Answer</summary>

   **27,702.73 USD** — attributed to **Sales App 1 – PROD**, driven by the SAP HANA Cloud instance from Exercise 1.

   > [!WARNING]
   > **TODO (author):** Verify this figure after the HANA instance data is finalized in APEX.

   </details>

2. Clear the filter. Switch **Group By → Cost Labels → All Cost Labels** and **Cost Label → Region** to see total BTP cost per region across all of APEX Holdings.

> [!TIP]
> The two label dimensions answer different questions from the same data. Cost Center answers: *"Which business unit do we charge?"* Region answers: *"Which geography drove the spend?"* Filtering by one while viewing the other makes cross-dimensional reporting possible without modifying the account structure or duplicating any data.

---

[← Exercise 2.3 — Fixed Allocation](../ex2.3/) | [Continue to: Exercise 2.5 — Export to Excel (Optional) →](../ex2.5/)
