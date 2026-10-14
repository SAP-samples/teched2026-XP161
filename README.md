[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/teched2026-XP161)](https://api.reuse.software/info/github.com/SAP-samples/teched2026-XP161)

![XP161 Banner](images/banner.jpg)

# SAP TechEd 2026 — XP161: SAP BTP FinOps Hands-On

## The Story

Dana, APEX Holdings CFO, walks in before the board meeting:

> *"BTP spend is up 25% this quarter. Before the board meeting I need five things: verify the numbers match our billing statement, find what's driving the increase, identify which subsidiary owns it, tell me whether we have any cost controls in place, and get me a cost center breakdown I can put in a slide."*

Over the next 100 minutes, you investigate the cost increase, allocate it to business lines, and get answers fast using Joule — each exercise building on the last.

---

## APEX Holdings

Apex Holdings is a sample global enterprise created to simulate SAP BTP FinOps practices. The company operates across diverse industries - such as health, retail, energy, etc. - each represented as Subsidiary with its own BTP directory.

Within each Subsidiary, you'll find departments such as finance, sales, HR, IT, and operations with subaccounts spanning regions like EMEA, North America, APAC, LATAM, and the Middle East (represented as labels). Each Subsidiary manages its own dedicated applications, ranging from payroll and performance reviews in HR to revenue forecasting, logistics, and customer insights.

The overall account structure mirrors a real-world organization with production, test, and development environments (represented as directories) aligned to cost centers and contact persons (represented as labels).

---

## Getting Started

→ [Getting Started](exercises/ex0/)

---

## Session Structure

> [!NOTE]
> **Recommended** exercises cover the complete session. **Optional** exercises go beyond the session scope — complete them if time allows or revisit them on your own account after TechEd.

### [Exercise 1 — Cost Visibility and Control](exercises/ex1/) (~40 min)

*Investigate the Q3 cost increase using today's BTP Cockpit tools.*

You find the cost spike, the budget breach, and the optimization opportunity, You have the investigation covered — but Dana's next question is "which business line owns these costs?" and that's where the current tools hit their limits.

| Exercise                            | Title                                 | Type           |
| ----------------------------------- | ------------------------------------- | -------------- |
| [Exercise 1.1](exercises/ex1/ex1.1/) | Cost and Usage Overview               | **Recommended** |
| [Exercise 1.2](exercises/ex1/ex1.2/) | Billing Verification                  | **Recommended** |
| [Exercise 1.3](exercises/ex1/ex1.3/) | Monitoring Costs — Finding the Spike | **Recommended** |
| [Exercise 1.4](exercises/ex1/ex1.4/) | Cross Charge / Cost Allocation        | Optional       |
| [Exercise 1.5](exercises/ex1/ex1.5/) | Controlling Costs Using Budgets       | **Recommended** |
| [Exercise 1.6](exercises/ex1/ex1.6/) | Optimization                          | **Recommended** |
| [Exercise 1.7](exercises/ex1/ex1.7/) | Export to Excel                       | Optional       |

### [Exercise 2 — Advanced Cost Allocation](exercises/ex2/) (~30 min)

*Break the three ceilings Part 1 couldn't cross.*

The new Billing Preview answers Dana's business-line question: drill to the SAP HANA Cloud instance inside Sales App 1 – PROD, label all 5 subsidiaries in 3 clicks (200+ subaccounts inherit), and split the shared Cloud Foundry Runtime cost 60/25/15 across Sales, Finance, and HR Operations.

| Exercise                            | Title                                         | Type           |
| ----------------------------------- | --------------------------------------------- | -------------- |
| [Exercise 2.1](exercises/ex2/ex2.1/) | Basic View — Same Data, New Interface        | **Recommended** |
| [Exercise 2.2](exercises/ex2/ex2.2/) | Granular Breakdown & Business Line Assignment | **Recommended** |
| [Exercise 2.3](exercises/ex2/ex2.3/) | Fixed Cost Allocation for Shared Resources    | **Recommended** |
| [Exercise 2.4](exercises/ex2/ex2.4/) | Multi-Dimensional Cost Ownership              | Optional       |
| [Exercise 2.5](exercises/ex2/ex2.5/) | Export to Excel                               | Optional       |

### [Exercise 3 — Ask Joule](exercises/ex3/) (~10 min)

*Dana's board-prep email, answered in natural language.*

Dana sends one urgent question before the board meeting. It would take 10–15 minutes of cockpit navigation — or a few sentences to Joule. You answer it, then have Joule draft your reply.

| Exercise                            | Title                                  |
| ----------------------------------- | -------------------------------------- |
| [Exercise 3.1](exercises/ex3/ex3.1/) | Q2 vs Q3 Service Plan Comparison       |
| [Exercise 3.2](exercises/ex3/ex3.2/) | Draft the Reply to Dana                |

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
