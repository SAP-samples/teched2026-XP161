# Part 3, Exercise 2 — Which Subaccounts Spiked? (~5 minutes)

**Dana's question:** *"I don't just want to know who costs the most. I want to know who suddenly costs more than they used to. Who changed?"*

This is a different question from "top spenders." A subaccount can consistently be expensive without being a problem. A spike — a sudden month-over-month jump — is the signal that something changed and needs attention.

**Joule scenario:** `subaccounts_cost_spikes`

---

## What You'll Ask Joule

> **"Which subaccounts had the biggest cost spikes in the last 6 months?"**

---

## What Joule Returns

Joule returns the top subaccount cost spikes — ranked by the size of the month-over-month increase, not by total spend.

**What to look for:**

- **Sales App 1 – PROD** (Lumina Energy) should appear near the top. In Part 1, Exercise 3, you traced this subaccount's cost jump to SAP HANA Cloud - HANA beginning to incur charges. Joule quantifies exactly how large that month-over-month jump was.
- The spike result includes: subaccount name, the month when the spike occurred, the cost before and after, and the absolute increase.

**Key distinction Joule makes explicit:**
> HR App 4 – TEST may have higher total costs than Sales App 1 – PROD — but if its costs have been consistently high for months, it does not appear as a spike. A spike requires a *change*, not just a high level.

---

## What This Adds to the Story

In Part 1, Exercise 3, you manually drilled down from service → subaccount to find Sales App 1 – PROD. Joule surfaces it automatically across ALL subaccounts — including ones you never examined — and ranks them by the steepness of the increase. You might find a spike you didn't know to look for.

> **For Dana:** "The biggest sudden increase was in Sales App 1 – PROD. Here's the month it started and how much it jumped."

---

[← Exercise 1 — Q3 Summary](../ex1-q3-summary/) | [Continue to: Exercise 3 — What's Driving the Spend? →](../ex3-top-services/)
