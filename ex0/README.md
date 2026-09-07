# Getting Started (approx. 5 minutes)

Welcome to **SAP TechEd 2026 XP161 — SAP BTP FinOps Hands-On**.

## The Story

Dana Mercer, APEX Holdings CFO, walks in before the board meeting:

> *"BTP spend is up 40% this quarter. I need to know what's driving it, who owns it, and what we're doing about it — by tomorrow."*

You are the APEX Holdings FinOps controller. Over the next 120 minutes you will investigate, allocate, and answer Dana's questions using SAP BTP's FinOps capabilities.

---

## The APEX Holdings Account

All exercises run on the **APEX Holdings** demo account — a fictional multinational company built into the BTP Cockpit as static mock data. No real cloud costs are incurred.

APEX Holdings structure:
- **5 subsidiaries:** Atlas Industries, Lumina Energy, HarborCare Health, Crestline Retail, NexaTech Digital
- **200+ subaccounts** across DEV / TEST / PROD environments under each subsidiary
- **Labels** on every subaccount: Region, Department, Cost Center, Contact Person, Environment
- A **hybrid commercial model:** subscription-based prepaid quotas for specific services + CPEA cloud credits for consumption

---

## Accessing the Session

1. **Open the following link** in a browser. It contains a special parameter that provides access to the APEX Holdings SAP BTP account with mock data:

   <https://emea.cockpit.btp.cloud.sap/cockpit/?idp=ainfvn15r.accounts.ondemand.com&teched-finops-2026=true#>

2. Enter the user name `XP161-XXX@education.cloud.sap`, where `XXX` is the number of your workshop place.  
   For example: `XP161-042@education.cloud.sap`

3. Enter the password for your user as provided to you at the beginning of the workshop.

This will open the **BTP Cockpit** with the APEX Holdings mock data.

4. In the BTP Cockpit left pane, scroll to the bottom and click **Costs and Usage**.

5. You will land on the **Overview** tab. You are ready to begin.

> [!NOTE]
> The data used in this exercise is **mock data created specifically for TechEd**. All costs and names shown are for demonstration purposes only.

---

## Session Structure

| Part | Topic | Duration |
|------|-------|----------|
| [**Part 1**](../part1/) | Existing Cost and Usage FinOps Capabilities | ~55 min |
| [**Part 2**](../part2/) | Preview: Upcoming FinOps Capabilities | ~35 min |
| [**Part 3**](../part3/) | FinOps with Joule | ~30 min |

Optional exercises are marked clearly — complete them if time allows, or revisit them later on your own account.

---

[Continue to: Part 1 — Exercise 1, Cost and Usage Overview →](../part1/ex1-cost-overview/)
