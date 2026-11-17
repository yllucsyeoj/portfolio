---
title: A membership programme worth NT$16.7M, or NT$1.7M?
description: A pet-services chain's enrolment opportunity looked like a 10x bigger prize than it was. Finding the honest number was the whole job.
---

*A customer analysis for a Taiwan pet-services chain: 2,212 customers, 27,027 transactions, February 2023 to February 2026. Client anonymised; data held privately under confidentiality.*

[&larr; Back to portfolio](../)

## The finding in one line

Customers on the chain's membership platform were worth **3.7x more** over their lifetime than those who had never joined (NT$22,517 vs NT$6,058). The obvious read was a **NT$16.7M prize**: enrol the 1,014 customers who had not joined, lift them to member value, bank the difference. That number was a mirage. The honest, reachable prize was closer to **NT$1.7M**, and saying so was the point of the engagement.

## What this piece demonstrates

- **It started from the decision, not the dashboard.** The question on the table was whether to run a large enrolment campaign. So the job was to size that prize properly before anyone spent money chasing it.
- **It killed its own best headline.** The NT$16.7M figure assumes every non-member can become an average member. When I split the non-members by value, 73% of them were below NT$5K lifetime, mostly one-time visitors: people boarding a pet once while travelling, or trying the service and not needing it again. They are structurally low-engagement, not un-asked. Only about 75 of the 1,014 were high-value customers genuinely worth converting. That is where the NT$1.7M lives.
- **It kept correlation and causation apart.** Members engage more, but it is not established that enrolment *causes* the engagement rather than engaged customers *choosing* to enrol. I flagged this as something a controlled pilot has to settle, instead of asserting a causal NT$16.7M and letting someone budget against it.

That is the job. Anyone can multiply a 3.7x gap by 1,014 customers and present a big number. The value is being the person who says the big number is wrong, shows why, and hands back the smaller one you can actually hit.

## What the customer base actually looked like

- **Revenue is heavily concentrated.** The top 1% of customers (22 people) drove 19% of revenue; the top 10% drove 59%. Losing one of the biggest customers is equivalent to losing around 150 average ones.
- **Non-members have a retention problem, not just an enrolment gap.** Half of non-members (50%) never came back after their first visit, against 22% for members. The one-time rate, not the enrolment rate, is the thing bleeding value.
- **So the priority inverts.** The biggest customers are already enrolled, so there is little enrolment upside there; they need a retention and early-warning programme instead. The enrolment effort belongs narrowly on the ~75 high-value non-members, and the broad retention effort belongs on recent one-time visitors.

## Method

Three years of transaction history aggregated to the customer: lifetime value, visit frequency, recency, service mix, and value tier. Members and non-members compared as cohorts across every engagement metric. Non-members then broken down by value tier to test the "convert everyone" assumption directly, which is where the headline opportunity fell apart. Pareto concentration computed to locate revenue risk. Python and pandas throughout.

## Honest limits

This is lagging transactional data only: no demographics, no satisfaction, no reason-for-leaving, so it describes what happened and cannot predict churn on its own. The 3.7x gap is a strong correlation whose causal share is unproven, which is exactly why the recommendation is a measured pilot rather than a full campaign. Ninety-day inactivity cannot be cleanly separated from a pet that has passed or a simple data lag. The honest NT$1.7M is a floor you can act on, not a ceiling.

---

*Built by Joey Scully. Product and Commercial Analytics consultant. Available for remote interim and contract work.*
