# Part 3 — FinOps with Joule (~30 minutes)

## Where the Story Stands

In Part 1 you investigated APEX Holdings' Q3 bill — found the HANA spike, the budget breach, the CF Runtime overage. In Part 2 you allocated costs by business line using the new Billing Preview.

Dana Mercer has the allocation report. Now she has questions. Not navigation — questions.

> *"Before I walk into the board meeting, I need six things. Give them to me."*

Six questions. Each one would normally require 10–15 minutes of cockpit navigation. With Joule, each takes one sentence.

---

## How Joule Works Here

Joule's FinOps capability is a closed set of six analytical scenarios. You trigger each one with a natural-language prompt. Joule resolves your global account automatically (you're already logged into APEX Holdings) and returns a structured answer.

The six scenarios Joule supports:

| What you want to know | Say something like |
|---|---|
| Quarter-level summary | "Cost summary for Q3" |
| Which subaccounts spiked | "Subaccount cost spikes last 6 months" |
| Top cost drivers by service | "Top 5 most expensive services this year" |
| Unusual service cost increases | "Service plan cost spikes" |
| Prepaid quota vs. actual usage | "Show prepaid quota consumption last 3 months" |
| Top cost drivers by subaccount | "Top 5 most expensive subaccounts" |

> [!NOTE]
> Joule does not manage budgets, set alerts, or configure allocations — those are done in the Cockpit views you used in Parts 1 and 2. Joule answers analytical questions, fast.

---

## Exercises

| Exercise | Title | Duration |
|----------|-------|----------|
| [Exercise 1](ex1-q3-summary/) | Q3 Cost Summary — The Big Picture | ~5 min |
| [Exercise 2](ex2-subaccount-spikes/) | Which Subaccounts Spiked? | ~5 min |
| [Exercise 3](ex3-top-services/) | What's Driving the Spend? | ~5 min |
| [Exercise 4](ex4-service-spikes/) | Service Plan Spike Detection | ~5 min |
| [Exercise 5](ex5-quota-utilization/) | Prepaid Quota — Are We Wasting Money? | ~5 min |
| [Exercise 6](ex6-top-subaccounts/) | The Top 5 Cost Offenders | ~5 min |

---

[← Back to Session Overview](../README.md) | [Start with Exercise 1 →](ex1-q3-summary/)
