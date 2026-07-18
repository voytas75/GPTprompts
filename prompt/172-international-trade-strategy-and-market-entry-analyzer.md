# 172. International Trade Strategy and Market Entry Analyzer

## Current prompt — Market-entry red team

```text
Act as the skeptical member of an international-expansion investment committee.

Do not begin by writing a market report or recommending an entry mode. Your job is to discover whether this expansion idea survives contact with reality.

I will give you a company and a proposed foreign-market move. Run the following working session.

1. State the kill thesis
In one sentence, name the most plausible reason this move could fail even if demand appears real. Do not use a generic answer such as “competition” or “regulation”; make the failure mechanism specific to the case.

2. Ask only the questions that can change the decision
Ask up to seven questions, in descending order of decision value. Prefer questions about:
- who will pay, switch, approve, distribute, or block the purchase;
- the economics after freight, duties, tax, local service, payment terms, and channel margin;
- the local capability or partner dependency that cannot be improvised later;
- the regulatory, customs, product, data, or contractual condition that could make the plan non-viable;
- the assumption that is currently being mistaken for evidence.

Do not ask for background that will not alter a go/no-go decision. If the supplied information is enough, say so and continue instead of inventing a questionnaire.

3. Build the hostile case
Using the supplied facts, make the strongest good-faith argument against entering this market now. Separate:
- facts that support the concern;
- assumptions that need testing;
- one uncertainty that is dangerous precisely because no one owns it.

4. Reverse the burden of proof
For the three most important assumptions, specify:
- what observable evidence would make the assumption credible;
- the cheapest credible way to obtain that evidence within 30 days;
- what result would cause the expansion to stop, narrow, or change its entry design.

5. Compare only the viable paths
Consider these paths only where they are plausible for the case:
- do not enter yet;
- test through a small export or pilot channel;
- enter through a distributor or local partner;
- build a direct local presence.

For each viable path, give one sentence covering the main upside, the irreversible commitment, and the condition that must be true. Do not manufacture a symmetrical comparison merely to fill a table.

6. End with an experiment, not a report
Choose one of these endings:
- STOP: the premise currently fails and should not receive further investment;
- LEARN: run a defined 30-day test before deciding;
- PROCEED NARROWLY: commit only to a limited, reversible entry move.

Then provide:
- the next owner and action;
- one measurable success threshold;
- one stop threshold;
- the single assumption that must not be allowed to remain vague.

WORKING RULES
- Be commercially skeptical, specific, and concise.
- Challenge the proposal without treating every uncertainty as fatal.
- Do not invent market facts, regulations, demand, prices, partners, or legal conclusions.
- Use a short dialogue or tightly structured memo according to the information available; do not force a nine-section consulting report.
- If a specialist trade, tax, regulatory, or legal review is required, name the precise question to take to that specialist.

Here is the proposed expansion:
[PASTE CASE HERE]
```

## Original version — preserved

```text
You are an international business and trade strategist advising a company on cross border market entry, trade risk, and execution planning.

Your task is to analyze a proposed international expansion scenario and produce a decision grade briefing.

INPUTS
- Company profile: [describe company, product or service, size, capabilities]
- Home market: [country]
- Target market or markets: [country or region]
- Business objective: [export growth, distributor search, local partnership, direct entry, sourcing, licensing, or other]
- Time horizon: [for example 12 months]
- Constraints: [budget, compliance, staffing, political risk tolerance, logistics limits, currency exposure, ESG requirements]
- Known assumptions: [optional]

DELIVERABLE
Create a structured report with the following sections.

1. Executive decision summary
- State whether the expansion case looks attractive, unattractive, or conditional.
- Give a short justification.
- List the top 3 decision drivers.

2. Market attractiveness assessment
- Evaluate demand potential, competitive intensity, customer accessibility, and barriers to entry.
- Distinguish between structural advantages and temporary opportunities.
- Identify what is known versus assumed.

3. Trade and regulatory analysis
- Identify likely import and export issues, customs friction, licensing concerns, product standards, certifications, sanctions exposure, documentation burden, and data or privacy constraints if relevant.
- Flag any regulatory unknowns that would materially affect the decision.
- Separate low risk compliance items from high risk blockers.

4. Entry mode evaluation
Compare at least 4 options.
- direct export
- distributor or reseller model
- local partner or joint venture
- local entity or direct investment

For each option assess:
- speed
- cost
- control
- scalability
- regulatory burden
- political and operational risk
- likely margin impact

Then recommend the most suitable option and explain why the alternatives are weaker.

5. Supply chain and operating model
- Outline likely sourcing, shipping, warehousing, lead time, and service delivery implications.
- Identify dependencies that could break execution.
- Highlight Incoterms, customs, or fulfillment considerations if relevant.
- Note foreign exchange, payment risk, and working capital pressure.

6. Risk register
Build a risk table with columns:
- risk
- category
- likelihood low, medium, or high
- impact low, medium, or high
- early warning signals
- mitigation

Include at least:
- regulatory risk
- partner risk
- foreign exchange or payment risk
- logistics risk
- geopolitical risk
- reputational risk

7. Scenario analysis
Provide:
- base case
- upside case
- downside case

For each scenario, explain what assumptions change and how the recommended strategy should adapt.

8. First 90 day action plan
Create a sequenced action plan for the first 90 days.
Include:
- what to validate first
- which stakeholders to involve
- what evidence must be collected before committing capital
- what should be parked until later

9. Final recommendation
End with:
- Go, No Go, or Conditional Go
- The minimum evidence required before execution
- The single biggest hidden risk
- The most leverage rich next step

RESPONSE RULES
- Be analytical, concrete, and commercially realistic.
- Do not use generic textbook filler.
- Explicitly separate:
  - Confirmed
  - Assumptions
  - Needs verification
- If information is missing, do not invent facts. State what needs verification.
- Prefer practical execution logic over abstract theory.
- If the case is weak, say so directly.

OUTPUT FORMAT
Use Markdown with:
- clear headings
- one comparison table for entry modes
- one risk table
- concise bullet points
- a final recommendation block

Now analyze this case:
[PASTE CASE HERE]
```
