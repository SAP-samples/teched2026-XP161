# Part 3, Exercise 5 — Prepaid Quota: Are We Wasting Money? (~5 minutes)

**Dana's question:** *"We pay a subscription fee that includes prepaid quota for several services. Are we actually using it? Or are we paying for quota we don't touch — while simultaneously paying overage charges on something else?"*

**Joule scenario:** `service_plans_utilization`

---

## What You'll Ask Joule

> **"Show me prepaid quota consumption for the last 3 months"**

---

## What Joule Returns

Joule returns a monthly breakdown of prepaid quota consumption — for each service plan with a prepaid quota, how much of that quota APEX Holdings consumed each month (as a percentage of the entitlement).

**What to look for:**

**Cloud Foundry Runtime - Standard** should show **over 100% consumption** — it has been exceeding its prepaid quota, generating overage charges at list price. You identified this in Part 1, Exercise 6, and traced it to a 20 GB overage. Joule now shows the monthly progression of that overage.

**Most other services** will show consumption well below 100% — meaning APEX Holdings is paying for quota it doesn't fully use. This is the subscription vs. consumption optimization story from Part 1 Exercise 6: the answer is not always "buy more quota" — sometimes it's "use what you have."

Each entry includes: service plan name, prepaid quota amount, monthly consumption %, and a utilization trend.

---

## The Optimization Angle

Joule gives Dana two actionable signals in one response:

1. **Over-utilized** (>100%): Cloud Foundry Runtime — buy additional quota at subscription rates to avoid overage charges
2. **Under-utilized** (<50%): services with unused quota — potential contract renegotiation candidates

In Part 1 Exercise 6, you worked through the Cloud Foundry Runtime case manually. Joule surfaces the full picture across all services simultaneously.

> **For Dana:** "Cloud Foundry Runtime is running 133% of quota and generating overage charges. 8 other services are below 60% utilization — those quotas may be renegotiable."

---

[← Exercise 4 — Service Spikes](../ex3.4/) | [Continue to: Exercise 6 — Top 5 Cost Offenders →](../ex3.6/)
