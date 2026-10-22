# Lessons Learned and Reflection

## What improved during the exercise

- **Separate threat, capability and impact.** In Scenario 1, I initially treated jailbreaks as likely to expose confidential bank data. I learned to ask what the chatbot can actually access before estimating harm.
- **Focus HITL on consequential decisions.** I first suggested flagging sensitive phrases and executive impersonation. Later I recognized that ordinary requests for personalized investment advice also need qualified review.
- **Distinguish model instructions from enforced permissions.** In Scenario 2, I suggested written rules for refunds, but learned that permissions and refund restrictions need enforcement by connected systems so an injected prompt cannot simply override them.
- **Consider the whole blast radius.** The scale of forty agents makes misuse more consequential; outgoing communications are also an important exposure, not just refunds and CRM changes.
- **Reprioritize when the evidence changes.** In Scenario 3, the already attempted $4 million deepfake fraud warranted greater urgency than unverified harm from the coding-agent connection.
- **Differentiate threat categories from controls.** Shadow AI is the risk of unapproved AI use; an AI-BOM is a visibility tool that helps inventory AI components, but is not by itself an approved-use policy.

## Remaining questions for a real-world assessment

- Which banking data sources can the chatbot really query, and what safeguards prevent confidential access?
- What are the inbox agents' exact MCP tool permissions, refund limits and approval rules?
- Can the coding agent write or merge production code, and is there evidence of changes?
- What customer data was uploaded to the public AI service, and under what retention terms?
- What is the independent authorization workflow for executive wire-transfer requests?

## Evidence notes

This lab is a discussion-based simulation. There are no screenshots of real infrastructure, code test artifacts, or verified incidents. The complete tutoring discussion remains in the original ChatGPT conversation; this repository provides a structured account of the learner's conclusions and feedback.
