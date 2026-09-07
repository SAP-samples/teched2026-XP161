# SAP TechEd 2026 — XP161: SAP BTP FinOps Hands-On

## The Story

Dana Mercer, APEX Holdings CFO, walks in before the board meeting:

> *"BTP spend is up 40% this quarter. I need to know what's driving it, who owns it, and what we're doing about it — by tomorrow."*

You are the APEX Holdings FinOps controller. Over the next 120 minutes, you work through three escalating responses to Dana's demand.

---

## Session Structure

### [Part 1 — Existing Cost and Usage FinOps Capabilities](part1/) (~55 min)

*Investigate the Q3 bill using today's tools.*

You find the cost spike (SAP HANA Cloud in Sales App 1 – PROD), the budget breach (HR App 4 – TEST over 40,000 USD), and the optimization opportunity (Cloud Foundry Runtime overage). You have the investigation covered — but Dana's next question is "which business line owns these costs?" and that's where the current tools hit their limits.

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 1](part1/ex1-cost-overview/) | Cost and Usage Overview | ~10 min | **Core** |
| [Exercise 2](part1/ex2-billing-verification/) | Billing Verification | ~10 min | Optional |
| [Exercise 3](part1/ex3-monitoring-costs/) | Monitoring Costs — Finding the Spike | ~7 min | **Core** |
| [Exercise 4](part1/ex4-cross-charge/) | Cross Charge / Cost Allocation | ~10 min | Optional |
| [Exercise 5](part1/ex5-budgets/) | Controlling Costs Using Budgets | ~10 min | **Core** |
| [Exercise 6](part1/ex6-optimization/) | Optimization | ~7 min | **Core** |
| [Exercise 7](part1/ex7-export-excel/) | Export to Excel | ~10 min | Optional |

### [Part 2 — Preview: Upcoming Cost and Usage FinOps Capabilities](part2/) (~35 min)

*Break the three ceilings Part 1 couldn't cross.*

The new Billing Preview answers Dana's business-line question: drill to the SAP HANA Cloud instance inside Sales App 1 – PROD, label all 5 subsidiaries in 3 clicks (200+ subaccounts inherit), and split the shared Cloud Foundry Runtime cost 60/25/15 across Sales, Finance, and HR Operations.

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 1](part2/ex1-basic-view/) | Basic View — Same Data, New Interface | ~4 min | **Core** |
| [Exercise 2](part2/ex2-advanced-breakdown/) | Granular Breakdown & Business Line Assignment | ~8 min | **Core** |
| [Exercise 3](part2/ex3-fixed-allocation/) | Fixed Cost Allocation for Shared Resources | ~5 min | **Core** |
| [Exercise 4](part2/ex4-additional-label/) | Multi-Dimensional Cost Ownership | ~5 min | Optional |
| [Exercise 5](part2/ex5-export/) | Export to Excel | ~3 min | Optional |
| [Exercise 6](part2/ex6-cleanup/) | Clean Up | ~3 min | Optional |

### [Part 3 — FinOps with Joule](part3/) (~30 min)

*Dana's 6 follow-up questions, answered in natural language.*

Dana has the allocation report. Now she has questions. Each one would take 10–15 minutes of cockpit navigation — or 30 seconds of Joule. Six prompts, six answers, all grounded in APEX Holdings data.

| Exercise | Title | Joule Scenario | Duration |
|----------|-------|----------------|----------|
| [Exercise 1](part3/ex1-q3-summary/) | Q3 Cost Summary — The Big Picture | `quarterly_cost_summary` | ~5 min |
| [Exercise 2](part3/ex2-subaccount-spikes/) | Which Subaccounts Spiked? | `subaccounts_cost_spikes` | ~5 min |
| [Exercise 3](part3/ex3-top-services/) | What's Driving the Spend? | `top_expensive_services` | ~5 min |
| [Exercise 4](part3/ex4-service-spikes/) | Service Plan Spike Detection | `service_plans_cost_spikes` | ~5 min |
| [Exercise 5](part3/ex5-quota-utilization/) | Prepaid Quota — Are We Wasting Money? | `service_plans_utilization` | ~5 min |
| [Exercise 6](part3/ex6-top-subaccounts/) | The Top 5 Cost Offenders | `top_costly_subaccounts` | ~5 min |

---

## Getting Started

→ [Exercise 0 — Getting Started](ex0/)

---

*Session code: XP161 | TechEd 2026 | Previous draft: [v1/](v1/)*
