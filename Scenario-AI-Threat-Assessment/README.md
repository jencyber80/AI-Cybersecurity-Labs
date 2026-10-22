# Scenario-AI Threat Assessment

**Status:** Completed — guided educational exercise  
**Date:** October 22, 2026  
**Topics:** GenAI Security · Agentic AI · Threat Modeling · Risk Prioritization · Security Controls

## Overview

This project documents my completion of a three-scenario AI threat assessment through a guided Socratic exercise with ChatGPT. For each fictional deployment I identified risks, justified my priorities, analyzed business impact and proposed security controls. The AI tutor asked one question at a time and challenged gaps in my reasoning.

This is a **scenario-based learning exercise**, not a penetration test, live product evaluation, or verified compliance assessment.

## Scenarios and results

| Scenario | My top three priorities | Main recommendation |
|---|---|---|
| 1. Retail banking chatbot | Hallucination; jailbreaks; direct prompt injection | Launch only with restrictions; human review before personalized financial recommendations |
| 2. Autonomous inbox agent | Agentic risks; indirect prompt injection; hallucination | Limit CRM/refund permissions and require approval for sensitive actions |
| 3. Shadow AI & synthetic-media fraud | Deepfakes; agentic risks; shadow AI | Independently verify high-value transfers; restrict unapproved AI and production access |

## Documentation

- [Detailed scenario assessments](scenario-assessments.md) — threat rankings, rationale, controls and recommendations
- [Methodology](methodology.md) — catalog, evaluation process and exercise limitations
- [Lessons learned](lessons-learned.md) — revised judgments, gaps and open questions

## Security controls evaluated

1. **Human-in-the-Loop (HITL):** Human approval for consequential decisions.
2. **AI Bill of Materials (AI-BOM):** Inventory AI components and dependencies.
3. **Least privilege:** Limit the permissions and data available to users and agents.
4. **Input sanitization / trust boundaries:** Avoid treating untrusted user or external content as authoritative instructions.

## Skills practiced

AI threat identification, prioritization based on scenario evidence, agentic permissions analysis, prompt-injection recognition, deployment decision-making, and cybersecurity reporting.

## Tools

- **ChatGPT:** Interactive AI tutor and documentation assistance
- **GitHub:** Portfolio hosting and version control
- **Markdown:** Project documentation

## Authorship and transparency

Threat rankings and the underlying decisions come from my responses during the lab. ChatGPT facilitated the discussion, challenged assumptions and helped organize the final documentation. No real customer records, production code, sensitive credentials, or live security test results are included.
