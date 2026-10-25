# Exercise 3 — Ask Joule (~10 minutes)

## The Email

In Exercise 1 you investigated APEX Holdings' Q3 bill. In Exercise 2 you allocated costs by business line. The analysis is done — but Dana still has a question.

You're back at your desk when an email from Dana lands, flagged urgent:

> **From:** Dana, CFO
> **Subject:** Need this before the board meeting — EOD
>
> *"I'm finalizing the board deck and one thing is still open. I need it today:*
>
> *How did our most expensive service plans change from Q2 to Q3?*
>
> *You know the cockpit inside out, but I need this fast. — Dana"*

You could answer this by navigating the cockpit — around 15 minutes. Instead, you'll use **Joule** to answer in natural language, then have Joule draft your reply to Dana.

> [!WARNING]
> **The features in this exercise are a TechEd Preview — not yet generally available.** They represent the planned direction and may change before release.

## Why Joule for FinOps

The cockpit's cost views give you predefined perspectives — breakdowns by subaccount, service, and month. They work well for routine monitoring, but they can't easily answer the specific, ad-hoc questions that come up during a cost review. **Joule** adds a natural-language interface: instead of navigating to the right view and setting filters, you ask your question in your own words and get a structured answer back.

Generative AI has a catch, though. These models are probabilistic — the same question can return slightly different answers, and a model asked to reason over numbers can get them wrong. For FinOps that's unacceptable: cost figures must be exact and repeatable, matching the cockpit to the cent.

Joule in the cockpit solves this with a **defined set of cost-analysis scenarios**. Each question you ask maps to a fixed analytical function that runs against your account's actual billing data. The AI understands your question and fills in the details — the time period, how many results — while the numbers come from deterministic computation, not from the model. You get the flexibility of natural language with the reliability of a database query.

<details>
<summary><b>The cost-analysis scenarios Joule supports</b></summary>

- **Quarterly cost summary** — total cost for a quarter, its top service plans and subaccounts, and how it compares to the previous quarter and the same quarter a year earlier.
- **Most expensive subaccounts** — the top subaccounts ranked by cost over a period.
- **Most expensive service plans** — the top service plans ranked by cost over a period.
- **Service plan cost spikes** — the service plans with the largest month-over-month cost increases.
- **Subaccount cost spikes** — the subaccounts with the largest month-over-month cost increases.
- **Prepaid quota consumption** — how much of each service plan's prepaid quota was used, month by month.

For a quarterly summary, give the quarter and year. For the others, give a start month and year (an end month is optional).

</details>

> [!NOTE]
> Joule answers analytical cost questions in natural language — no dashboard navigation. Its cost analysis covers consumption-based usage — the same data behind the Cockpit's **Costs and Usage** views.

---

## Exercises

| Exercise | Title | Duration |
|----------|-------|----------|
| [Exercise 3.1](ex3.1/) | Q2 vs Q3 Service Plan Comparison | ~5 min |
| [Exercise 3.2](ex3.2/) | Draft the Reply to Dana | ~5 min |

---

[← Back to Session Overview](../../README.md) | [Start with Exercise 3.1 →](ex3.1/)
