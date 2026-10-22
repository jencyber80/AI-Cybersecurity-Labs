# Methodology

## Format

A structured, scenario-based discussion with ChatGPT acting as a tutor. The tutor asked **one question at a time**, requested the learner's reasoning, challenged assumptions and withheld complete answers until each scenario was finished.

## Steps

1. Review the provided GenAI/agentic threat catalog and four allowed controls.
2. Identify possible threats in each scenario using the facts supplied.
3. Examine user inputs, external/untrusted data, tool permissions, potential impacts and human oversight.
4. Compare realistic consequences and rank the top three threats.
5. Match risk-reduction recommendations to the allowed controls.
6. Revise priorities when new information changes the evaluation.
7. Summarize the proposed controls and one key learning gap per scenario.

## Threat catalog used

- Hallucination
- Deepfakes / synthetic media
- Adversarial examples (model evasion)
- Jailbreaks
- Direct prompt injection
- Indirect prompt injection
- Shadow AI
- OWASP agentic risks: authorization/control hijacking, critical-systems interaction, goal/instruction manipulation, impact chain & blast radius, memory/context manipulation, multi-agent exploitation, supply-chain/dependency attacks, untraceability, checker out-of-the-loop, alignment faking

## Control catalog used

- Human-in-the-Loop (HITL)
- AI Bill of Materials (AI-BOM)
- Least privilege
- Input sanitization / trust boundaries

## Assessment limitations

This is a **qualitative educational threat assessment** based solely on fictional scenarios. No live systems, configurations, logs, exploits or evidence were examined. Specific likelihoods, regulatory violations, actual breaches, and successful attacks have not been verified. Scenario-based priorities are not numerical risk scores.

## AI assistance disclosure

ChatGPT supplied the case-based questions, feedback and final summaries. Threat selections, original justifications and deployment recommendations were supplied by the learner during the interactive exercise. The repository documents a reconstructed summary, not a verbatim or independently validated audit log.
