# Part 2, Exercise 4 — Add a Second Cost Label Dimension — Optional (~5 minutes)

> [!TIP]
> **This exercise is optional.** Complete it if time allows.

**Goal:** Add a second independent cost label dimension to track cost ownership by contact person, alongside the Line of Business label from Exercise 2.

**Scenario:** APEX Holdings has five designated cost owners who are responsible for BTP spending. You already know two of them from Part 1:
- **logan.ibrahim@apex.com** — contact person for HR App 4 – TEST (the subaccount that exceeded 40,000 USD)
- **elliot.kowalski@apex.com** — contact person for Sales App 1 – PROD (the SAP HANA Cloud spike driver)

The other three cost owners are: **alex.yamamoto@apex.com**, **parker.reyes@apex.com**, and **casey.carter@apex.com**.

With two label dimensions, you can answer questions like: *"What are Sales business line costs owned by logan.ibrahim?"*

## Step 4.1 — Create the Cost Owner Label

1. In **Group By**, confirm **Cost Labels → All Cost Labels** is selected.
2. Click **Manage Cost Labels → Add Cost Label Key**.
3. Name the key: **"Cost Owner"**
4. Add 5 values: **"logan.ibrahim@apex.com"**, **"elliot.kowalski@apex.com"**, **"alex.yamamoto@apex.com"**, **"parker.reyes@apex.com"**, **"casey.carter@apex.com"**
5. Click **Save**.

**Expected result:** Your second label "Cost Owner" with 5 values is ready alongside "Line of Business".

## Step 4.2 — Assign Cost Owner Labels to Known Entities

1. Switch to **Account → All Account Entities** in Group By.
2. In the left sidebar under **View**, set **Cost Label** to **"Cost Owner"**.
3. Assign Cost Owner to the entities you know from Part 1:
   - Navigate to **HR App 4 – TEST** (NexaTech Digital → TEST) → Edit → assign **logan.ibrahim@apex.com** → Save
   - Navigate to **Sales App 1 – PROD** (Lumina Energy → PROD) → Edit → assign **elliot.kowalski@apex.com** → Save

## Step 4.3 — Cross-Dimensional Analysis

1. In the left sidebar under **Filter**, expand **Cost Labels** and select **Line of Business → HR Operations**.
2. The table now shows only HR Operations-labeled entities. With **Cost Owner** visible, you can see cost ownership within the HR Operations business line.

   **Question:** Who is the cost owner for **HR App 4 – TEST**, and what is their total allocated cost within HR Operations?

   <details>
   <summary>Answer</summary>

   **logan.ibrahim@apex.com** — assigned directly to HR App 4 – TEST, which is the highest-cost entity within the HR Operations business line (the subaccount that exceeded 40,000 USD in Part 1).
   </details>

3. Clear the filter. In **Group By**, select **Cost Labels → All Cost Labels**. Switch the **View Cost Label** to **Cost Owner** to see the total cost distribution by owner across all of APEX Holdings.

> [!TIP]
> Multi-dimensional labeling lets APEX Holdings answer questions like "What are logan.ibrahim's HR Operations costs?" without modifying the account structure — just filter by one dimension, view the other.

---

[← Exercise 3 — Fixed Allocation](../ex3-fixed-allocation/) | [Continue to: Exercise 5 — Clean Up (Optional) →](../ex5-cleanup/)
