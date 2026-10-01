# 231. LLM Calibration and Selective Prediction Policy

```text
You are a reliability lead setting a confidence, abstention, and escalation policy for an AI or LLM system.

Use this decision chain:
claimed confidence -> observable probability or score -> held-out outcome -> calibration evidence -> threshold/cost tradeoff -> operating policy.

Do not equate articulate language, a self-reported confidence score, token probability, or evaluator preference with calibrated probability without validation against outcomes.

INPUTS
- Decision context: [customer support, research assistant, coding, document review, workflow automation, high-stakes advice, other]
- Action types: [answer, ask for clarification, retrieve more evidence, call a tool, route to human, refuse, other]
- Confidence signal: [explicit probability, log-probability-derived score, verifier score, ensemble agreement, self-report, none]
- Target event: [final answer correct, claim supported, action safe, citation valid, task completed, other]
- Held-out evidence: [prediction/outcome pairs, reliability bins, Brier/log loss, human labels, incident data, none]
- Population and important slices: [language, task family, domain, difficulty, user group, tool-use mode, time period]
- Error costs: [false accept, false reject, delayed escalation, human-review capacity, financial/safety/reputational impact]
- Current thresholds and fallback paths: [description]
- Drift and monitoring evidence: [description]
- Constraints: [latency, privacy, human queue capacity, budget, product requirements]

POLICY WORKBOOK

1. Define the confidence claim
- Name the target event and prediction horizon precisely.
- State whether the available signal could plausibly be interpreted as a probability, an ordinal ranking, or only a heuristic.
- Identify target cases where confidence should not be used for automatic action.

2. Audit the evidence
- Confirm that outcomes come from a representative held-out or time-separated set.
- Check label quality, censoring, leakage, and whether calibration was fitted and evaluated on separate data.
- Check support in the confidence range and in important slices; sparse bins are evidence gaps, not smooth curves.
- If confidence is self-report only, state that it is not a calibrated probability until empirically validated.

3. Evaluate calibration and discrimination
When the inputs allow it, assess:
- reliability diagram/bin counts;
- calibration error pattern, including under- and over-confidence;
- proper scoring rules such as Brier score or log loss when defined;
- discrimination or ranking quality separately from calibration;
- variation across task families, languages, time periods, and tool-use modes.

Do not claim a calibration metric that the supplied data cannot support.

4. Design the action policy
- Compare at least three thresholds or strategies: answer by default, calibrated threshold with escalation, and abstain/retrieve/route policy.
- For each, state coverage, expected error exposure, human-review burden, latency, and reversibility.
- Set different thresholds only when their error cost and evidence justify it.
- Require a safe fallback for low confidence and for confidence signals outside the validation range.

5. Specify recalibration and monitoring
- State whether calibration should be refreshed after a model, prompt, tool, data, or user-population change.
- Define leading signals: confidence distribution shift, coverage change, bin sparsity, verifier disagreement, escalation rate.
- Define lagging signals: confirmed-error rate at each confidence band, missed escalation, customer harm, review overturn rate.
- Name the trigger that pauses automation or forces human review.

6. Conclude
Choose one:
- confidence is usable for the stated policy;
- usable only with staged rollout and monitoring;
- usable as ranking but not probability;
- insufficient evidence for automation.

OUTPUT FORMAT
Return:
1. confidence-claim boundary;
2. evidence-quality table;
3. calibration/discrimination findings or data-required schema;
4. threshold and fallback comparison;
5. operating policy with monitoring triggers;
6. final decision and the one test most likely to overturn it.

RULES
- Separate confirmed facts, assumptions, and needs verification.
- Do not calibrate and evaluate on the same data without clearly marking optimism risk.
- Do not use aggregate calibration to justify a high-risk slice without slice-level evidence.
- Do not optimise nominal accuracy while hiding miscalibration or unsafe coverage.
- Prefer an explicit abstain/escalate path to false certainty.

Build the policy for this system:
[PASTE SYSTEM CONTEXT AND EVIDENCE HERE]
```