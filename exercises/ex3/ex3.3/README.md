# Exercise 3.3 — What's Driving the Spend? (~5 minutes)

**Dana's question:** *"Which specific services are we paying the most for? I want the top 5 — ranked."*

**Joule scenario:** `top_expensive_services`

---

## What You'll Ask Joule

> **"What are the top 5 most expensive service plans this year?"**

---

## What Joule Returns

Joule returns the 5 highest-cost service plans across APEX Holdings for the current year, ranked by total list-price spend.

**Expected ranking for APEX Holdings:**

| Rank | Service Plan | Why you recognize it |
|---|---|---|
| #1 | **SAP HANA Cloud - HANA** | The spike you traced in Exercise 1.3; Sales App 1 – PROD is the main driver |
| #2 | **SAP Integration Suite, advanced event mesh - Default** | The costliest service in HR App 4 – TEST (Exercise 1.4) |
| #3 | **Cloud Foundry Runtime - Standard** | The service with 20 GB overage from Exercise 1.6; you split its cost 60/25/15 in Exercise 2.3 |

Each entry includes: service plan name, total cost for the period, and a breakdown by month showing the trend.

---

## Follow-Up in Context

Joule retains conversation context. After seeing the top 5, you can follow up:

> **"Show me the monthly cost trend for SAP HANA Cloud - HANA"**

Joule will return the month-by-month breakdown for that service — confirming the upward trend you saw manually in Exercise 1.3, but now in seconds.

---

## What This Adds to the Story

In Exercise 1, ranking services required sorting the Billing view by List Price. Joule returns this ranked list with trend context in one prompt, across the full year — not just the selected month.

> **For Dana:** "SAP HANA Cloud is our biggest spend, and it's been accelerating since [month]. Here's the trend."

---

[← Exercise 3.2 — Subaccount Spikes](../ex3.2/) | [Continue to: Exercise 3.4 — Service Plan Spike Detection →](../ex3.4/)
