# 174. Supply Chain Planning and Resilience Optimizer

## Current prompt — Supply-chain disruption tabletop

```text
Run a realistic supply-chain disruption tabletop exercise for the business situation below.

You are the operations control tower at the moment a disruption begins. Do not produce a generic assessment or a fixed consulting report. Simulate how the situation develops and show the decisions that matter while there is still time to act.

First, choose the single disruption most capable of exposing the chain's real weakness. It may be a supplier failure, a port or transport disruption, a demand spike, a quality hold, a capacity loss, a systems outage, or a combination only if the case genuinely supports it.

If important data is missing, state up to three bounded operating assumptions and continue. Do not ask the user follow-up questions.

Write the exercise as a chronological control-tower log:

T+0: The signal
- State what the team sees first and why it could be misleading.
- Identify the product, customer, inventory, supplier, transport lane, or planning dependency most immediately exposed.
- Name the first fact that must be checked before escalating.

T+4 hours: Contain or amplify
- Show the two most credible immediate moves.
- For each, state what it protects and what it sacrifices: service, margin, cash, quality, customer trust, or future capacity.
- Choose the move you would make and explain the trigger that justifies it.

T+24 hours: The hidden dependency
- Reveal the second-order constraint that makes the first response insufficient.
- Explain how planning data, inventory allocation, supplier information, warehouse capacity, transport, customer promises, or decision rights change the situation.
- Name one seemingly sensible action that would make the system worse.

T+72 hours: Commit under uncertainty
- Present a decision fork with two realistic paths, such as allocation versus expedites, alternate sourcing versus quality risk, production prioritization versus customer fairness, or buffer protection versus working-capital pressure.
- Select a path using the facts available at that point, not hindsight.
- State the threshold that would make you reverse the decision.

T+14 days: What the incident taught the operator
- Give the operational outcome: recovered, contained with loss, or escalating.
- Separate the immediate cause from the design weakness that allowed it to spread.
- Identify the one control, data signal, operating rule, or network change that would have reduced the impact most.

End with a compact operator card:
- first owner to act;
- first metric to watch;
- first customer or supplier conversation to have;
- decision that must not wait for the next planning cycle;
- resilience investment that should be rejected unless the scenario repeats or evidence improves.

Use concrete tradeoffs and plausible operational consequences. Do not invent supplier names, demand data, inventory quantities, contracts, regulations, or service commitments. Make uncertainty visible, but do not hide behind it.

Supply-chain situation:
[PASTE CASE HERE]
```

## Original version — preserved

```text
You are a senior supply chain strategist advising a COO, CSCO, operations lead, or transformation team.

Your task is to analyze a supply chain situation and produce a decision grade review covering planning, inventory, supplier risk, logistics, and resilience.

INPUTS
- Company and product context: [industry, product or service, business model, customer promise]
- Supply chain footprint: [suppliers, plants, co-manufacturers, warehouses, channels, regions]
- Demand profile: [stable, seasonal, promotional, highly volatile, project based, or other]
- Current operating model: [make to stock, make to order, assemble to order, hybrid, or other]
- Planning cadence: [forecasting, S&OP, replenishment, review rhythm]
- Constraints: [capacity, lead time, supplier dependency, service level commitments, budget, working capital, systems]
- Known issues: [stockouts, excess inventory, late deliveries, forecast misses, supplier instability, manual planning, poor visibility, or other]
- Known assumptions: [optional]

DELIVERABLE
Create a structured report with the following sections.

1. Executive summary
- State whether the supply chain appears stable, stressed, or fragile.
- Summarize the main operational problem in one sentence.
- Identify the top 3 drivers of cost, service, or resilience risk.

2. End to end supply chain diagnosis
- Review the flow from sourcing and procurement through production, inventory, warehousing, logistics, and customer fulfillment.
- Identify the most important bottlenecks, handoff failures, and coordination gaps.
- Distinguish structural weaknesses from temporary disruptions.

3. Planning and demand supply alignment
- Assess forecast reliability, planning discipline, and how well supply is synchronized with demand.
- Evaluate the planning process for demand sensing, replenishment logic, and cross functional alignment.
- Explicitly note whether the operation appears demand driven or buffer driven.
- Identify where scenario planning or what if analysis is missing.

4. Inventory and working capital review
- Assess whether inventory is positioned intelligently or mainly used as a substitute for visibility and control.
- Identify risks of stockouts, overstocks, obsolescence, poor allocation, or excess safety stock.
- Explain the likely working capital and service level tradeoffs.
- Separate healthy buffers from wasteful buffers.

5. Supplier and network resilience assessment
Classify risks using at least these categories:
- supply risk
- demand risk
- process risk
- environmental or ecosystem risk

Then evaluate:
- single source exposure
- lead time concentration
- supplier reliability and quality risk
- transport and logistics disruption risk
- geopolitical, regulatory, weather, or labor risk
- dependency on manual escalation or heroics

6. Operations and fulfillment review
- Assess production or service capacity, warehouse flow, transportation reliability, order fulfillment, and reverse logistics if relevant.
- Identify where service failure is most likely to appear first.
- Note whether network design and execution are aligned with the actual customer promise.

7. Data visibility and decision support
- Evaluate whether the team has end to end visibility across supply, inventory, orders, and fulfillment.
- Identify fragmented systems, manual reconciliation, stale data, or KPI blind spots.
- Explain how poor visibility may be driving bad planning or unnecessary inventory.

8. Risk register
Build a risk table with columns:
- risk
- category
- likelihood low, medium, or high
- impact low, medium, or high
- early warning signal
- mitigation

Include at least:
- forecast error risk
- supplier disruption risk
- inventory imbalance risk
- logistics delay risk
- process breakdown risk
- environmental or geopolitical risk

9. Recommended interventions
Provide:
- 3 immediate actions for the next 30 days
- 3 structural improvements for the next 90 to 180 days
- 3 metrics that should be monitored weekly

For each action, explain:
- why it matters
- expected effect on cost, service, or resilience
- what dependency or blocker must be handled first

10. Final recommendation
End with:
- overall operating verdict
- the single most important correction
- the biggest hidden supply chain risk
- what must be verified before larger investment or redesign

RESPONSE RULES
- Be operational, concrete, and commercially realistic.
- Do not use generic textbook filler.
- Explicitly separate:
  - Confirmed
  - Assumptions
  - Needs verification
- If the evidence is weak, say so directly.
- Prefer practical planning and execution logic over abstract theory.
- If inventory buffers appear to be compensating for poor visibility or planning, say so clearly.
- If resilience is overstated and depends on one supplier, one lane, or one planner, flag it directly.

OUTPUT FORMAT
Use Markdown with:
- clear headings
- one compact diagnosis table
- one risk table
- concise bullet points
- a short final recommendation block

Now analyze this case:
[PASTE CASE HERE]
```
