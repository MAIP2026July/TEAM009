# Executive Summary

## HR Ally – An AI-Powered Assistant for Employee HR Support

### Problem

Employees often need to search across employee handbooks, HR policy documents, internal portals, emails, and different HR systems to find answers to routine Human Resources (HR) questions. They may struggle to identify the latest applicable policy, understand the correct procedure, determine which documents are required, or find the appropriate HR contact.

This fragmented process creates unnecessary effort for employees and increases the workload of HR teams, which spend considerable time answering repetitive questions and redirecting employees to the correct resources. Inconsistent guidance and delayed responses can also reduce employee confidence in HR support.

HR Ally aims to address this problem by providing a single, accessible starting point for routine HR information and guidance.

### Target User / Customer

The primary users are employees who need assistance with common HR-related questions and procedures, including:

- Leave policies and attendance procedures.
- Employee benefits and expense claims.
- Salary documents and payslip access.
- Onboarding and training procedures.
- HR forms, internal portals, and support contacts.

The secondary users and beneficiaries are HR operations teams that handle recurring employee inquiries. By helping employees resolve routine information needs independently, HR teams can devote more time to complex cases, sensitive employee concerns, and activities requiring professional judgment.

The proposed product is intended for an organizational environment where employees already use Microsoft Teams and where approved HR policies and support resources can be made accessible to the assistant.

### Product Concept

HR Ally is an AI-powered employee HR assistant designed to operate through Microsoft Teams. Employees can ask questions in everyday language and receive concise, relevant guidance based on approved HR information.

The proposed minimum viable product (MVP) will focus on five core capabilities:

1. **Conversational HR support:** Employees can ask questions without knowing the exact policy name or search terminology.
2. **Source-backed answers:** The assistant retrieves relevant information from approved HR documents and provides a reference or link to the applicable policy.
3. **Guided next steps:** Responses direct employees to the appropriate form, portal, procedure, or HR support channel.
4. **Clarification and safe escalation:** When a question is incomplete, unclear, or outside the assistant's reliable scope, it asks for clarification or directs the employee to authorized HR staff.
5. **User feedback:** Employees can indicate whether a response was helpful, supporting future product evaluation and improvement.

The initial MVP will focus on information retrieval and guidance rather than completing every HR transaction within Teams. It will not independently make decisions about leave approvals, compensation, benefit eligibility, recruitment, disciplinary matters, or policy exceptions. These decisions will remain with authorized HR professionals.

### Why AI?

A conventional FAQ page, keyword-based search, or fixed decision tree can help with predictable questions but often requires employees to know the right terminology, navigate categories, and interpret policy documents themselves. The same HR question may be expressed in many different ways, using informal language, spelling variations, or incomplete details.

AI can interpret natural-language questions and connect different expressions of the same question to relevant information in approved HR sources. A retrieval-augmented generation (RAG) approach is a suitable candidate for the MVP: it retrieves relevant policy content and uses a language model to formulate a concise response grounded in that content.

This approach can improve accessibility and reduce search effort while providing policy references that employees can verify. However, AI does not guarantee correctness. The product must be evaluated for answer accuracy, source relevance, unsupported responses, and appropriate escalation. If reliable supporting information cannot be found, HR Ally should avoid guessing and direct the employee to a human support channel.

An API-first approach using an approved AI platform is preferable for the initial version to reduce the need to develop and train a model from scratch. The product's value will depend not only on the language model but also on the quality and currency of HR content, access controls, user experience, and safe handling of uncertain or sensitive questions.

### Recommendation

**Recommendation: Prototype, then evaluate before piloting.**

The team should proceed with a narrow, Microsoft Teams-based prototype that demonstrates the end-to-end experience for a selected set of routine HR questions. The prototype should include source-backed answers, links to approved policies, guided next steps, clarification, user feedback, and safe escalation to HR.

Before considering a pilot, the team should test the prototype against representative employee questions and HR-reviewed expected answers. Evaluation should measure answer correctness, the proportion of responses supported by approved sources, source relevance, helpfulness, successful routing, and the handling of sensitive or unanswerable questions. The team should also compare the time needed to find answers using HR Ally with the existing manual process.

Progress to a limited pilot should depend on evidence that the assistant provides useful and appropriately grounded guidance, protects employee information, and escalates cases safely. HR content owners should be responsible for maintaining approved knowledge sources, and authorized HR professionals should retain decision-making authority.

HR Ally should therefore be treated as a promising employee-support product that warrants a controlled prototype and evidence-based evaluation—not as a fully autonomous HR decision system. This staged approach allows the organization to validate employee value and operational feasibility before committing to broader deployment or integration with additional HR systems.
