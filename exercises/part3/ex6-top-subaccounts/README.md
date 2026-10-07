# Part 3, Exercise 6 — The Top 5 Cost Offenders (~5 minutes)

**Dana's question:** *"Give me the five subaccounts that spent the most this year. I want names — the ones I should be asking questions about at the board meeting."*

**Joule scenario:** `top_costly_subaccounts`

---

## What You'll Ask Joule

> **"Show me the top 5 most expensive subaccounts this year"**

---

## What Joule Returns

Joule returns the 5 highest-cost subaccounts across APEX Holdings for the current year, ranked by total spend.

**Expected for APEX Holdings:**

| Rank | Subaccount | Subsidiary | Why you recognize it |
|---|---|---|---|
| Top 5 | **HR App 4 – TEST** | NexaTech Digital | Exceeded the 40,000 USD monthly budget (Part 1 Ex5); labeled HR Operations in Part 2 |
| Top 5 | **Sales App 1 – PROD** | Lumina Energy | SAP HANA Cloud spike (Part 1 Ex3); labeled Sales in Part 2 |

Each entry includes: subaccount name, parent directory, total cost for the year, and the primary service plan driving the spend.

---

## Closing the Loop

This is the final answer in the investigation that started in Part 1.

| Part 1 finding | Part 2 allocation | Part 3 confirmation |
|---|---|---|
| Sales App 1 – PROD is the HANA spike driver | Labeled as **Sales** (Lumina Energy) | Appears in top 5 by total spend |
| HR App 4 – TEST breached the 40K budget | Labeled as **HR Operations** (NexaTech Digital) | Appears in top 5 by total spend |
| CF Runtime has 20 GB overage | Split 60/25/15 across business lines | Visible in quota utilization (Ex5) |

Dana now has everything she needs:
- **What happened:** Q3 summary (Ex1)
- **Who changed:** Spike detection by subaccount and service (Ex2, Ex4)
- **What costs most:** Top services and subaccounts (Ex3, Ex6)
- **Where we're over-spending on quota:** Prepaid utilization (Ex5)
- **Who owns it:** Business line allocation from Part 2

> *"Board meeting ready."*

---

## Part 3 Summary

### 🎯 Key Takeaways

- ✅ Joule answers cost analysis questions in natural language — no dashboard navigation needed
- ✅ Six scenarios cover: quarterly summary, spike detection (by service and subaccount), top rankings (by service and subaccount), and prepaid quota utilization
- ✅ Joule's spike detection finds anomalies that manual ranking misses — services not in the top 5 that are accelerating fast
- ✅ Every Joule answer connects back to what you found in Parts 1 and 2 — it's the same data, faster

---

[← Exercise 5 — Prepaid Quota](../ex5-quota-utilization/) | [← Back to Session Overview](../../README.md)

---

**This concludes the SAP TechEd 2026 XP161 FinOps Hands-On session. Thank you for participating!**
