# Exercise 3.4 — Service Plan Spike Detection (~5 minutes)

**Dana's question:** *"Are there any services that aren't in our top 5 but suddenly started costing us money? I don't want to miss a quiet cost that's about to become a big problem."*

This is the service-plan equivalent of Exercise 2's subaccount spikes. Top-N rankings miss anomalies in lower-spend services. Spike detection finds them.

**Joule scenario:** `service_plans_cost_spikes`

---

## What You'll Ask Joule

> **"Show me the biggest service plan cost spikes in the last 6 months"**

---

## What Joule Returns

Joule returns the top service plan cost spikes — ranked by the size of the month-over-month increase, not by total spend.

**What to look for:**

- **SAP HANA Cloud - HANA** should confirm the spike you already know about (Sales App 1 – PROD began incurring HANA charges). This cross-validates what you found manually in Exercise 1.
- Look for any **additional services** that spiked which weren't visible in your Exercise 1 investigation — services that don't appear in the top 5 by total spend but had a sudden increase.

Each spike entry includes: service plan name, the month of the spike, cost before and after, and the absolute and percentage increase.

---

## The Difference from Exercise 3

| Exercise 3 (top_expensive_services) | Exercise 4 (service_plans_cost_spikes) |
|---|---|
| "Who costs the most overall?" | "Who suddenly costs more than before?" |
| Ranks by total spend | Ranks by month-over-month delta |
| Finds the biggest services | Finds the fastest-changing services |
| SAP HANA Cloud is always #1 | A small service with a 500% spike would rank high |

Running both gives a complete picture: the established cost drivers AND the emerging ones.

---

> **For Dana:** "Here are services that had sudden cost increases — including some that don't appear in our top 5 rankings but are accelerating."

---

[← Exercise 3.3 — Top Services](../ex3.3/) | [Continue to: Exercise 3.5 — Prepaid Quota →](../ex3.5/)
