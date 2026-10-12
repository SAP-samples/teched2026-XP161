[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2026-XP161)](https://api.reuse.software/info/github.com/SAP-samples/teched2026-XP161)

# SAP TechEd 2026 — XP161: SAP BTP FinOps Hands-On

## The Story

Dana Mercer, APEX Holdings CFO, walks in before the board meeting:

> *"BTP spend is up 25% this quarter. Before the board meeting I need five things: verify the numbers match our billing statement, find what's driving the increase, identify which subsidiary owns it, tell me whether we have any cost controls in place, and get me a cost center breakdown I can put in a slide."*

You are the APEX Holdings FinOps controller. Over the next 120 minutes, you work through three escalating responses to Dana's demand.

---

## APEX Holdings

Apex Holdings is a sample global enterprise created to simulate SAP BTP FinOps practices. The company operates across diverse industries - such as health, retail, energy, etc. - each represented as Subsidiary with its own BTP directory.

Within each Subsidiary, you'll find departments such as finance, sales, HR, IT, and operations with subaccounts spanning regions like EMEA, North America, APAC, LATAM, and the Middle East (represented as labels). Each Subsidiary manages its own dedicated applications, ranging from payroll and performance reviews in HR to revenue forecasting, logistics, and customer insights.

The overall account structure mirrors a real-world organization with production, test, and development environments (represented as directories) aligned to cost centers and contact persons (represented as labels).

---

## Session Structure

### [Exercise 1 — Cost Visibility and Control](exercises/ex1/) (~55 min)

*Investigate the Q3 bill using today's tools.*

You find the cost spike (SAP HANA Cloud in Sales App 1 – PROD), the budget breach (HR App 4 – TEST over 40,000 USD), and the optimization opportunity (Cloud Foundry Runtime overage). You have the investigation covered — but Dana's next question is "which business line owns these costs?" and that's where the current tools hit their limits.

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 1.1](exercises/ex1/ex1.1/) | Cost and Usage Overview | ~10 min | **Core** |
| [Exercise 1.2](exercises/ex1/ex1.2/) | Billing Verification | ~10 min | **Core** |
| [Exercise 1.3](exercises/ex1/ex1.3/) | Monitoring Costs — Finding the Spike | ~7 min | **Core** |
| [Exercise 1.4](exercises/ex1/ex1.4/) | Cross Charge / Cost Allocation | ~10 min | Optional |
| [Exercise 1.5](exercises/ex1/ex1.5/) | Controlling Costs Using Budgets | ~10 min | **Core** |
| [Exercise 1.6](exercises/ex1/ex1.6/) | Optimization | ~7 min | **Core** |
| [Exercise 1.7](exercises/ex1/ex1.7/) | Export to Excel | ~10 min | Optional |

### [Exercise 2 — Advanced Cost Allocation](exercises/ex2/) (~35 min)

*Break the three ceilings Part 1 couldn't cross.*

The new Billing Preview answers Dana's business-line question: drill to the SAP HANA Cloud instance inside Sales App 1 – PROD, label all 5 subsidiaries in 3 clicks (200+ subaccounts inherit), and split the shared Cloud Foundry Runtime cost 60/25/15 across Sales, Finance, and HR Operations.

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 2.1](exercises/ex2/ex2.1/) | Basic View — Same Data, New Interface | ~4 min | **Core** |
| [Exercise 2.2](exercises/ex2/ex2.2/) | Granular Breakdown & Business Line Assignment | ~8 min | **Core** |
| [Exercise 2.3](exercises/ex2/ex2.3/) | Fixed Cost Allocation for Shared Resources | ~5 min | **Core** |
| [Exercise 2.4](exercises/ex2/ex2.4/) | Multi-Dimensional Cost Ownership | ~5 min | Optional |
| [Exercise 2.5](exercises/ex2/ex2.5/) | Export to Excel | ~3 min | Optional |

### [Exercise 3 — Ask Joule](exercises/ex3/) (~30 min)

*Dana's 6 follow-up questions, answered in natural language.*

Dana has the allocation report. Now she has questions. Each one would take 10–15 minutes of cockpit navigation — or 30 seconds of Joule. Six prompts, six answers, all grounded in APEX Holdings data.

| Exercise | Title | Joule Scenario | Duration |
|----------|-------|----------------|----------|
| [Exercise 3.1](exercises/ex3/ex3.1/) | Q3 Cost Summary — The Big Picture | `quarterly_cost_summary` | ~5 min |
| [Exercise 3.2](exercises/ex3/ex3.2/) | Which Subaccounts Spiked? | `subaccounts_cost_spikes` | ~5 min |
| [Exercise 3.3](exercises/ex3/ex3.3/) | What's Driving the Spend? | `top_expensive_services` | ~5 min |
| [Exercise 3.4](exercises/ex3/ex3.4/) | Service Plan Spike Detection | `service_plans_cost_spikes` | ~5 min |
| [Exercise 3.5](exercises/ex3/ex3.5/) | Prepaid Quota — Are We Wasting Money? | `service_plans_utilization` | ~5 min |
| [Exercise 3.6](exercises/ex3/ex3.6/) | The Top 5 Cost Offenders | `top_costly_subaccounts` | ~5 min |

---

## Getting Started

→ [Getting Started](exercises/ex0/)

---

*Session code: XP161 | TechEd 2026*

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support
Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (2026) SAP SE or an SAP affiliate company and teched2026-XP161 contributors. Please see our [LICENSE](LICENSE) for copyright and license information. Detailed information including third-party components and their licensing/copyright information is available [via the REUSE tool](https://api.reuse.software/info/github.com/SAP-samples/teched2026-XP161).
