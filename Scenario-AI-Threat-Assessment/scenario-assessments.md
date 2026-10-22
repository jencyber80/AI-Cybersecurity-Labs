# Scenario Assessments

> Educational exercise, not a penetration test or assessment of a real bank/company. Rankings are the learner's qualitative priorities, not validated likelihood scores.

## Scenario 1 — Retail Banking Chatbot

**Environment:** A public-facing, text-only GenAI chatbot answers questions using a bank product knowledge base. Marketing proposes personalized loan, credit-card and investment guidance with no pre-publication human review.

### Learner's prioritized threats
1. **Hallucination** — Incorrect claims about investment returns or unsuitable personalized recommendations could mislead customers, cause losses and damage trust.
2. **Jailbreaks** — A user could impersonate an executive or authority to try to bypass safety restrictions.
3. **Direct prompt injection** — Untrusted public prompts could contain instructions to disregard the chatbot's rules.

**Other threats considered:** Indirect prompt injection could be introduced through compromised retrieved knowledge-base content; deepfake media is lower priority for the stated text-only interface. Adversarial examples were considered but prompt injection/jailbreak are more direct classifications for the example attacks.

**Impact qualification:** The scenario confirms access to product information, *not* confidential account systems. A jailbreak cannot expose confidential records the chatbot cannot access. Hallucination likelihood was not measured, but the potential business impact of inaccurate financial guidance is material.

### Controls and deployment decision
- **HITL:** Keep routine product questions automated; route personalized, high-stakes financial advice to qualified staff *before* providing individualized recommendations.
- **Least privilege:** Limit chatbot retrieval to the information necessary for approved customer-service tasks.
- **Input sanitization/trust boundaries:** Keep public prompts and retrieved content from being treated as authoritative system instructions.
- **AI-BOM:** Document the model, components and dependencies.

**Learner's decision:** Launch with restrictions. General information can remain available; hold personalized financial recommendations until human oversight is in place.

**Tutor-identified gap:** Early human review triggers focused on passwords and executive impersonation rather than ordinary high-stakes investment questions. The learner revised the design to escalate personalized financial guidance.

---

## Scenario 2 — Autonomous Inbox Agent

**Environment:** Forty sales representatives use MCP-connected AI agents that read external email, send responses, update CRM, schedule meetings and issue refunds up to $500 without prior approval.

### Learner's prioritized threats
1. **Agentic risks** — Autonomous access to business systems creates authorization/control hijacking, critical-system interaction and impact/blast-radius risks.
2. **Indirect prompt injection** — Malicious directions in external emails or attachments could be mistaken for legitimate work instructions.
3. **Hallucinations** — The agent could autonomously send false customer information.

**Other threats considered:** Deepfakes were judged lower priority because the scenario does not establish video/audio processing. Jailbreaks are relevant but the salient entry point is untrusted inbox material.

**Impact qualification:** If each of 40 agents were misused for one $500 refund, the hypothetical exposure is $20,000; the scenario gives no cumulative refund cap, so this is illustrative rather than a maximum.

### Controls and deployment decision
- **Least privilege:** Make sensitive CRM fields read-only by default, limit tool scopes and restrict refund authority.
- **HITL:** Let agents draft proposed CRM changes and refund requests, but require authorized human approval before execution.
- **Input sanitization/trust boundaries:** Treat external email as untrusted data, not as instructions that override agent rules or permissions.
- **AI-BOM:** Record agents and their connected components and integrations.
- **Refund guardrails discussed:** Validate eligibility against a real purchase, refund only the original payment method, prevent duplicate/excess refunds and escalate exceptions. Enforce restrictions in the transaction system, not merely in text prompts.

**Learner's decision:** Continue lower-risk automation with restrictions; prioritize human review for CRM modifications and refunds.

**Tutor-identified gap:** Outgoing email can also cause broad harm if a manipulated agent sends unauthorized or misleading messages. The learner's focus had been on CRM and refunds.

---

## Scenario 3 — Shadow AI and Synthetic-Media Wire Transfer

**Environment:** Marketing uses unapproved AI image/video tools; finance puts customer spreadsheets into a public chatbot; an unapproved coding agent is wired into a production code repository; and a convincing CEO video impersonation nearly led to a $4 million wire transfer.

### Learner's prioritized threats
1. **Deepfakes / synthetic media** — A near-miss involving executive impersonation presents an immediate financial-fraud risk.
2. **Agentic risks** — An unapproved coding agent connected to production may put critical code and systems at risk, dependent on its permissions.
3. **Shadow AI** — AI use without oversight may expose customer data and obscure organizational risk.

**Other threats considered:** The learner initially misclassified unauthorized AI use as AI-BOM and indirect prompt injection, then correctly identified shadow AI after tutoring. The actual coding agent permissions and whether any code was modified were not established.

### Controls and deployment decision
- **HITL:** Require independent, trusted-channel verification and human approval of high-value transfer requests. Do not rely solely on a convincing video call.
- **Least privilege:** Restrict the coding agent's access, require human approval before production merges, and keep employee access aligned to job functions.
- **AI-BOM:** Inventory AI models, components, dependencies and integrations to improve visibility; maintain separate authorization/enforcement processes for approved AI tools.
- **Input sanitization/trust boundaries:** Keep confidential customer information within authorized processing destinations rather than allowing uploads to unapproved public chatbots.

**Learner's decision:** Prioritize the deepfake wire-transfer near-miss, then assess/restrict production coding-agent access, then address unapproved AI data sharing.

**Tutor-identified gap:** The learner originally ranked coding-agent and spreadsheet risks ahead of the already attempted financial fraud, then updated the ordering in light of the stronger evidence.
