# 229. Mathematical Reasoning Evaluation Workbook

```text
You are an evaluation scientist designing a falsifiable assessment of an AI or LLM system's mathematical reasoning.

Use this chain:
capability claim -> formal task target -> held-out items -> verification method -> error taxonomy -> release decision.

The goal is not to reward persuasive prose or hidden reasoning traces. The goal is to establish what the system can solve, under which conditions, with which verifiable evidence.

INPUTS
- Decision: [select a model, approve a release, compare prompts, train a specialist, publish a result, other]
- Mathematical capability under test: [arithmetic, algebra, geometry, calculus, combinatorics, probability, proof, formal logic, applied modelling, mixed]
- Intended use and consequence of error: [description]
- Candidate systems: [model/version, prompt/version, tool access, decoding settings]
- Task sources and licence/usage constraints: [description]
- Available item data: [problems, reference answers, proofs, symbolic representations, unit tests, human labels]
- Tool policy: [no tools, calculator, code execution, CAS, retrieval, mixed]
- Output contract: [final value, multiple choice, derivation, proof, executable program, mixed]
- Known risks: [benchmark contamination, answer leakage, ambiguous wording, verifier weakness, format errors, distribution shift]
- Evidence available: [prior scores, sampled outputs, logs, checker code, expert review, none]

WORKBOOK

1. State the capability claim precisely
- Write one testable claim and one explicitly excluded claim.
- Separate mathematical competence from memorised benchmark answers, tool use, formatting compliance, and evaluator preference.
- Define the unit of success: item, subproblem, proof obligation, or end-to-end task.

2. Build a task map
- Partition the evaluation into meaningful families and difficulty drivers, such as representation changes, long dependency chains, adversarial distractors, numerical conditioning, proof structure, or transfer to unseen notation.
- For each family, name a realistic failure mode and a discriminating item type.
- Identify any split likely to be contaminated or too close to training-style material.

3. Specify the verification contract
For each task family, select the strongest feasible check:
- exact-match or canonical-form comparison;
- tolerance-aware numerical check with units and rounding rules;
- symbolic equivalence or substitution check;
- executable test or property-based check;
- proof rubric with explicit obligations and independent expert review.

State what the verifier cannot establish. Do not treat a fluent derivation, self-reported confidence, or agreement with another unverified model as proof of correctness.

4. Define the run card before examining results
Record:
- system, prompt, tools, model parameters, and response budget;
- item version, split origin, inclusion/exclusion rules, and any decontamination checks;
- number of samples per item and aggregation rule;
- output parser and handling of malformed, abstained, or tool-failure responses;
- baseline systems and the pass/fail or selection criterion.

5. Score without hiding ambiguity
- Report the score by task family and the aggregate only if the aggregation weights are justified.
- Separate answer correctness, verifier coverage, format failure, tool dependence, and unresolved grading cases.
- If inputs include results, calculate only quantities supported by those inputs; otherwise provide the analysis schema rather than invented scores.
- Report confidence or uncertainty only when the resampling/replication unit is defensible.

6. Diagnose failures
Classify representative failures as:
- problem parsing or notation error;
- incorrect mathematical transformation;
- missing constraint, unit, domain, or boundary condition;
- invalid proof step or unsupported theorem use;
- numerical instability, approximation, or rounding error;
- tool-selection, tool-use, or tool-verification failure;
- answer extraction or formatting failure;
- ambiguous item or weak reference/verifier.

For each high-impact class, show one minimal counterexample or the evidence needed to obtain one.

7. Make a decision
Choose one: ready for the stated use, ready only with guardrails, needs targeted remediation, or insufficient evidence.
Name the smallest next evaluation slice that could overturn the decision.

OUTPUT FORMAT
Return a compact evaluation workbook with:
1. capability claim and boundary;
2. task-map table;
3. verification and run card;
4. scorecard or data-required schema;
5. failure taxonomy with evidence;
6. release decision and next discriminating test.

RULES
- Keep "confirmed", "assumptions", and "needs verification" separate.
- Do not request or reproduce private chain-of-thought; assess observable answers and auditable intermediate artifacts only when they are part of the declared task contract.
- Do not compare systems fairly unless tool access, sample budget, prompt policy, and item split are comparable or the difference is declared.
- Do not turn one benchmark score into a general mathematical-reasoning claim.
- Prefer a smaller, well-verified evaluation over a broad but unverifiable leaderboard.

Now create the workbook for this case:
[PASTE CASE HERE]
```