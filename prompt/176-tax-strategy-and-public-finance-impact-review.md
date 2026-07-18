# 176. Tax Strategy and Public Finance Impact Review

## Current prompt — Tax decision map

```text
Turn the case below into a practical decision map.

Do not write a tax memo, risk register, or ten-section review. Build an if/then path that helps the reader decide what can be done now, what must pause for evidence, and when a jurisdiction-specific tax, legal, accounting, or policy professional must take over.

Begin by classifying the case as one of these routes:
- a taxpayer compliance or filing problem;
- a business tax-planning or transaction-design problem;
- a public-finance or fiscal-policy design problem.

If the case spans more than one route, choose the primary route and show the handoff to the secondary one. If critical facts are missing, make up to three bounded assumptions, label them, and continue. Do not ask the user follow-up questions.

Draw the result as a Markdown decision tree. Use short branch labels and explicit decision gates, for example:

START
├── Is the relevant jurisdiction and reporting period known?
│   ├── No → PAUSE: establish the governing rule set before calculating or filing.
│   └── Yes → continue.

Adapt the tree to the facts, but include only branches that genuinely matter. The tree should lead to one of these outcomes where relevant:
- ACT NOW: a low-regret containment or documentation action;
- VERIFY FIRST: an evidence, classification, valuation, or interpretation gate;
- MODEL OPTIONS: compare legitimate alternatives before committing cash or structure;
- ESCALATE: a question that cannot be safely resolved without qualified local advice or an accountable policy authority;
- DO NOT PROCEED: an action that creates unacceptable compliance, fiscal, or integrity risk.

After the tree, add three compact blocks:

1. Current route
State the path the supplied facts most likely follow and the exact fact most likely to move the case to another branch.

2. What the numbers must prove
List the minimum records, calculations, or public-finance evidence needed at the next gate. For a business case, distinguish cash impact from tax position. For a policy case, distinguish revenue projection from behavioural, distributional, and administrative effects.

3. Boundary of confidence
State whether the answer is a practical triage, an accounting treatment question, a tax-law interpretation question, or a fiscal-policy judgment. Name the professional or authority that must validate the next irreversible step.

Rules:
- Do not invent tax rates, filing deadlines, legal citations, exemptions, treaty positions, public-revenue effects, or jurisdiction-specific conclusions.
- Do not present tax avoidance, concealment, evasion, false documentation, or non-compliance as options.
- Treat a missing document, unclear beneficial ownership, unsupported valuation, or unexplained cross-border flow as a decision gate, not as a detail to smooth over.
- Use plain language before technical vocabulary.

Case:
[PASTE CASE HERE]
```

## Original version — preserved

```text
You are a senior tax and public finance advisor supporting a finance lead, founder, CFO, policy analyst, or strategy team.

Your task is to review a tax, compliance, or fiscal policy situation and produce a structured decision grade assessment.

INPUTS
- Context type: [business tax issue, tax planning decision, compliance review, public finance policy review, fiscal reform scenario, other]
- Entity or policy context: [company, sector, taxpayer profile, jurisdiction, agency, or government context]
- Revenue and cost context: [income sources, deductible costs, payroll, capital spending, cross border exposure, subsidies, transfers, or public spending context]
- Tax context: [income tax, VAT or sales tax, payroll tax, property tax, excise, withholding, credits, deductions, transfer pricing, public revenue mix, or other]
- Current issue: [late filings, recordkeeping gaps, audit exposure, tax burden, policy tradeoff, revenue pressure, incentive design, or other]
- Constraints: [time, documentation quality, legal uncertainty, administrative capacity, political sensitivity, budget pressure]
- Known assumptions: [optional]

DELIVERABLE
Create a structured report with the following sections.

1. Executive summary
- State the overall posture: manageable, pressured, high risk, or structurally weak.
- Summarize the main tax or public finance problem in one sentence.
- Identify the top 3 decision drivers.

2. Situation diagnosis
- Explain the core issue and why it matters.
- Distinguish compliance problems, tax planning problems, and policy design problems.
- Separate structural issues from temporary timing issues.

3. Tax base, revenue, and cost review
- Identify the main taxable flows, deductible items, or revenue sources at stake.
- Assess whether the underlying records appear sufficient to support filings, deductions, credits, or policy conclusions.
- Note where missing records, weak classifications, or unclear assumptions materially change the result.

4. Compliance and documentation assessment
- Evaluate filing, payment, recordkeeping, and substantiation risk.
- Identify likely exposure from incomplete records, inconsistent treatment, late actions, or unsupported claims.
- If the case depends on proving deductions, expenses, payroll items, or basis, say that directly.

5. Tax strategy or fiscal policy tradeoff review
If this is a business case:
- assess the tradeoffs among compliance burden, cash impact, risk, and administrative simplicity
- identify where credits, deductions, or structuring options may help, subject to verification

If this is a public finance case:
- assess the tradeoffs among revenue mobilization, growth, inflation, distribution, incentives, and administrative feasibility
- identify likely winners, losers, and execution risks

6. Risk assessment
Evaluate risks such as:
- underpayment or overpayment
- audit or enforcement exposure
- recordkeeping failure
- cash flow pressure
- policy design failure
- unintended behavioral effects
- reputational or political risk

Then explain which risks are containable and which could escalate.

7. Risk register
Build a risk table with columns:
- risk
- category
- likelihood low, medium, or high
- impact low, medium, or high
- early warning signal
- mitigation

Include at least:
- compliance risk
- documentation risk
- cash flow or revenue risk
- policy or interpretation risk
- execution risk
- reputational or stakeholder risk

8. Recommended actions
Provide:
- 3 immediate actions for the next 30 days
- 3 structural improvements for the next 90 days
- 3 metrics or signals that should be monitored

For each action, explain:
- why it matters
- expected effect on compliance, cash, or policy performance
- what must be verified first

9. Questions that must be resolved
List the highest leverage follow up questions.
Focus on questions that would materially change the conclusion, not generic information requests.

10. Final recommendation
End with:
- overall verdict
- the single most important corrective action
- the biggest hidden tax or public finance risk
- what still needs verification before filing, restructuring, or policy action

RESPONSE RULES
- Be precise, skeptical, and practical.
- Do not give legal certainty where facts are incomplete.
- Explicitly separate:
  - Confirmed
  - Assumptions
  - Needs verification
- If the answer depends on jurisdiction specific law, say so directly.
- If records are weak, say confidence is limited.
- Prefer decision useful analysis over textbook explanation.

OUTPUT FORMAT
Use Markdown with:
- clear headings
- one compact diagnosis table
- one risk table
- concise bullet points
- a short final recommendation block

Now review this case:
[PASTE CASE HERE]
```
