[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2026-XP161)](https://api.reuse.software/info/github.com/SAP-samples/teched2026-XP161)

# SAP TechEd 2026 — XP161: SAP BTP FinOps Hands-On

## The Story

Dana Mercer, APEX Holdings CFO, walks in before the board meeting:

> *"BTP spend is up 25% this quarter. Before the board meeting I need five things: verify the numbers match our billing statement, find what's driving the increase, identify which subsidiary owns it, tell me whether we have any cost controls in place, and get me a cost center breakdown I can put in a slide."*

You are the APEX Holdings FinOps controller. Over the next 120 minutes, you work through three escalating responses to Dana's demand.

---

## Session Structure

### [Part 1 — Cost Visibility and Control](2_cost-visibility-and-control/) (~55 min)

*Investigate the Q3 bill using today's tools.*

You find the cost spike (SAP HANA Cloud in Sales App 1 – PROD), the budget breach (HR App 4 – TEST over 40,000 USD), and the optimization opportunity (Cloud Foundry Runtime overage). You have the investigation covered — but Dana's next question is "which business line owns these costs?" and that's where the current tools hit their limits.

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 1](2_cost-visibility-and-control/ex1-cost-overview/) | Cost and Usage Overview | ~10 min | **Core** |
| [Exercise 2](2_cost-visibility-and-control/ex2-billing-verification/) | Billing Verification | ~10 min | **Core** |
| [Exercise 3](2_cost-visibility-and-control/ex3-monitoring-costs/) | Monitoring Costs — Finding the Spike | ~7 min | **Core** |
| [Exercise 4](2_cost-visibility-and-control/ex4-cross-charge/) | Cross Charge / Cost Allocation | ~10 min | Optional |
| [Exercise 5](2_cost-visibility-and-control/ex5-budgets/) | Controlling Costs Using Budgets | ~10 min | **Core** |
| [Exercise 6](2_cost-visibility-and-control/ex6-optimization/) | Optimization | ~7 min | **Core** |
| [Exercise 7](2_cost-visibility-and-control/ex7-export-excel/) | Export to Excel | ~10 min | Optional |

### [Part 2 — Advanced Cost Allocation](3_advanced-cost-allocation/) (~35 min)

*Break the three ceilings Part 1 couldn't cross.*

The new Billing Preview answers Dana's business-line question: drill to the SAP HANA Cloud instance inside Sales App 1 – PROD, label all 5 subsidiaries in 3 clicks (200+ subaccounts inherit), and split the shared Cloud Foundry Runtime cost 60/25/15 across Sales, Finance, and HR Operations.

| Exercise | Title | Duration | Type |
|----------|-------|----------|------|
| [Exercise 1](3_advanced-cost-allocation/ex1-basic-view/) | Basic View — Same Data, New Interface | ~4 min | **Core** |
| [Exercise 2](3_advanced-cost-allocation/ex2-advanced-breakdown/) | Granular Breakdown & Business Line Assignment | ~8 min | **Core** |
| [Exercise 3](3_advanced-cost-allocation/ex3-fixed-allocation/) | Fixed Cost Allocation for Shared Resources | ~5 min | **Core** |
| [Exercise 4](3_advanced-cost-allocation/ex4-additional-label/) | Multi-Dimensional Cost Ownership | ~5 min | Optional |
| [Exercise 5](3_advanced-cost-allocation/ex5-export/) | Export to Excel | ~3 min | Optional |
| [Exercise 6](3_advanced-cost-allocation/ex6-cleanup/) | Clean Up | ~3 min | Optional |

### [Part 3 — Ask Joule](4_ask-joule/) (~30 min)

*Dana's 6 follow-up questions, answered in natural language.*

Dana has the allocation report. Now she has questions. Each one would take 10–15 minutes of cockpit navigation — or 30 seconds of Joule. Six prompts, six answers, all grounded in APEX Holdings data.

| Exercise | Title | Joule Scenario | Duration |
|----------|-------|----------------|----------|
| [Exercise 1](4_ask-joule/ex1-q3-summary/) | Q3 Cost Summary — The Big Picture | `quarterly_cost_summary` | ~5 min |
| [Exercise 2](4_ask-joule/ex2-subaccount-spikes/) | Which Subaccounts Spiked? | `subaccounts_cost_spikes` | ~5 min |
| [Exercise 3](4_ask-joule/ex3-top-services/) | What's Driving the Spend? | `top_expensive_services` | ~5 min |
| [Exercise 4](4_ask-joule/ex4-service-spikes/) | Service Plan Spike Detection | `service_plans_cost_spikes` | ~5 min |
| [Exercise 5](4_ask-joule/ex5-quota-utilization/) | Prepaid Quota — Are We Wasting Money? | `service_plans_utilization` | ~5 min |
| [Exercise 6](4_ask-joule/ex6-top-subaccounts/) | The Top 5 Cost Offenders | `top_costly_subaccounts` | ~5 min |

---

## Getting Started

→ [Getting Started](1_setup/)

---

*Session code: XP161 | TechEd 2026 | Previous draft: [v1/](v1/)*

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support
Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (2026) SAP SE or an SAP affiliate company and teched2026-XP161 contributors. Please see our [LICENSE](LICENSE) for copyright and license information. Detailed information including third-party components and their licensing/copyright information is available [via the REUSE tool](https://api.reuse.software/info/github.com/SAP-samples/teched2026-XP161).
