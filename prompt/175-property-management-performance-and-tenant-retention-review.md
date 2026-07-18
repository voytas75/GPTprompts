# 175. Property Management Performance and Tenant Retention Review

## Current prompt — Tenant-journey mystery shop

```text
Act as two people encountering the property described below:

1. a qualified prospective tenant deciding whether to lease; and
2. a current tenant deciding whether to renew.

Create a grounded mystery-shop walkthrough of their experience. This is not a claim that you visited the property; it is a practical hypothesis exercise based only on the facts supplied.

If facts are incomplete, state no more than three assumptions and continue. Do not ask the user follow-up questions. Do not write a generic property-performance report.

Write two short, vivid journeys.

Journey A — “Would I move in?”
Follow the prospective tenant through:
- first online impression or referral;
- initial inquiry and response;
- tour or first physical encounter;
- comparison with alternatives;
- application, approval, and move-in expectation.

At each moment, include:
- what the person notices;
- what they infer about the property or management;
- the operational cause that may sit behind the experience;
- the point at which the lease is won, delayed, or lost.

Journey B — “Why would I renew?”
Follow the current tenant through:
- ordinary day-to-day living or working at the property;
- one service, maintenance, billing, communication, or safety moment that tests trust;
- the weeks before renewal;
- the renewal decision or move-out conversation.

At each moment, show the gap between what the operator believes is happening and what the tenant is likely to experience. Do not blame the tenant for a friction that the operating model creates.

Then write an operator’s margin note with exactly five items:
1. The moment most likely to destroy value quietly.
2. The moment where a small service improvement could protect occupancy or NOI.
3. One metric that could look healthy while masking a tenant-experience failure.
4. One action to test in the next seven days.
5. One structural issue that should not be papered over with concessions, marketing, or deferred maintenance.

Use concrete property-operations logic: responsiveness, unit turns, maintenance reliability, billing clarity, safety, communication, vendor coordination, convenience, and trust. Distinguish clearly between a market-demand problem and a management-created experience problem.

Property situation:
[PASTE CASE HERE]
```

## Original version — preserved

```text
You are a senior property operations advisor supporting an owner, asset manager, property manager, or portfolio operations lead.

Your task is to review a real estate or property management situation and produce a decision grade assessment covering occupancy, leasing, maintenance, tenant experience, operating performance, and property risk.

INPUTS
- Property type: [multifamily, office, retail, industrial, mixed use, student housing, other]
- Portfolio or asset context: [single asset or portfolio, size, location, age, positioning]
- Occupancy and leasing context: [occupancy rate, vacancy trend, lease expirations, renewal rate, pipeline]
- Revenue context: [rent profile, concessions, ancillary revenue, delinquency, collections]
- Operating context: [staffing, vendors, maintenance workload, service standards, resident or tenant complaints]
- Financial context: [NOI trend, operating expenses, maintenance costs, capex pressure, budget constraints]
- Known issues: [vacancy loss, slow leasing, high turnover, unresolved maintenance, weak tenant satisfaction, rising opex, compliance concerns, or other]
- Known assumptions: [optional]

DELIVERABLE
Create a structured report with the following sections.

1. Executive summary
- State whether the property operation appears healthy, pressured, or unstable.
- Summarize the primary business problem in one sentence.
- Identify the top 3 drivers of occupancy, NOI, or service risk.

2. Property performance diagnosis
- Assess the current operating picture across occupancy, leasing, collections, maintenance, and tenant experience.
- Distinguish structural issues from temporary market conditions.
- Identify whether the current problem is mainly demand, operations, pricing, or execution.

3. Leasing and occupancy review
- Assess vacancy exposure, lead to lease conversion, renewal performance, and move in or move out friction.
- Identify likely causes of lost occupancy, such as poor responsiveness, weak marketing, pricing mismatch, slow turns, or service issues.
- Separate demand weakness from avoidable execution failure.

4. Revenue and NOI review
- Evaluate the likely pressure points affecting revenue and net operating income.
- Distinguish recurring operating expenses from capex style costs.
- Note where rent growth, concessions, delinquency, utility leakage, maintenance cost creep, or vendor inefficiency may be reducing NOI.
- If the case suggests a false sense of performance from deferred maintenance or temporary pricing tactics, say so directly.

5. Maintenance and service operations
- Assess work order flow, response speed, vendor coordination, preventive maintenance, and unit turn readiness.
- Identify whether maintenance is supporting retention or damaging it.
- Highlight where slow repairs, fragmented systems, or labor shortages are likely creating tenant dissatisfaction and operational drag.

6. Tenant or resident retention assessment
- Evaluate the likely effect of move in experience, maintenance satisfaction, communication quality, and convenience on renewals.
- Distinguish between short term occupancy fixes and durable retention improvements.
- Identify which service failures are most likely to drive churn or reputational damage.

7. Property risk and control review
Assess risks such as:
- vacancy and revenue loss
- lease rollover concentration
- collections or delinquency issues
- maintenance backlog
- vendor dependency
- safety or compliance risk
- reputational risk

Then explain which risks are operationally containable versus likely to expand.

8. Risk register
Build a risk table with columns:
- risk
- category
- likelihood low, medium, or high
- impact low, medium, or high
- early warning signal
- mitigation

Include at least:
- vacancy risk
- tenant retention risk
- maintenance backlog risk
- vendor performance risk
- NOI erosion risk
- compliance or safety risk

9. Recommended actions
Provide:
- 3 immediate actions for the next 30 days
- 3 structural improvements for the next 90 days
- 3 metrics that should be reviewed weekly

For each action, explain:
- why it matters
- expected impact on occupancy, NOI, or satisfaction
- what dependency or blocker must be handled first

10. Final recommendation
End with:
- overall operating verdict
- the single most important corrective action
- the biggest hidden risk to asset performance
- what still needs verification before making a larger capital or pricing decision

RESPONSE RULES
- Be practical, skeptical, and commercially realistic.
- Do not use generic real estate filler.
- Explicitly separate:
  - Confirmed
  - Assumptions
  - Needs verification
- If information is weak, say so directly.
- Prefer property operations logic over broad market clichés.
- If maintenance or tenant experience is clearly affecting retention, say so directly.
- If NOI appears supported by tactics that are not durable, flag that clearly.

OUTPUT FORMAT
Use Markdown with:
- clear headings
- one compact operations table
- one risk table
- concise bullet points
- a short final recommendation block

Now review this case:
[PASTE CASE HERE]
```
