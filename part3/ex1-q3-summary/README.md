# Part 3, Exercise 1 — Q3 Cost Summary: The Big Picture (~5 minutes)

**Dana's question:** *"Before I walk into the board meeting, give me the Q3 numbers. Total spend, what drove it, how does it compare to Q2."*

**Joule scenario:** `quarterly_cost_summary`

---

## What You'll Ask Joule

Open Joule in the BTP Cockpit and type:

> **"Show me the cost summary for Q3"**

Joule may ask you to confirm the year if it's ambiguous. Confirm the current year.

---

## What Joule Returns

Joule returns a structured Q3 summary for APEX Holdings with four sections:

**1. Total Q3 Cost**
The total list-price spend for the quarter. You will see this is significantly higher than Q2 — confirming the 40% increase Dana mentioned.

**2. Top Service Plans**
The highest-cost service plans in Q3, ranked by spend. You will recognize:
- **SAP HANA Cloud - HANA** at the top — the service you traced to Sales App 1 – PROD in Part 1, Exercise 3
- **SAP Integration Suite, advanced event mesh** — the service driving HR App 4 – TEST's costs

**3. Top Subaccounts**
The highest-cost subaccounts in Q3. You will see:
- **HR App 4 – TEST** (NexaTech Digital) — the subaccount that exceeded its 40,000 USD budget in Part 1, Exercise 5
- **Sales App 1 – PROD** (Lumina Energy) — the subaccount with the HANA spike from Part 1, Exercise 3

**4. Quarter-over-Quarter Comparison**
Q3 vs. Q2 delta, confirming the acceleration Dana is concerned about.

---

## The Value

In Part 1, building this picture required four separate exercises. Joule assembles it in one prompt — same data, zero navigation.

> **For Dana's board deck:** the Q3 summary Joule just produced is the opening slide.

---

[← Part 3 Overview](../README.md) | [Continue to: Exercise 2 — Which Subaccounts Spiked? →](../ex2-subaccount-spikes/)
