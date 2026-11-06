# UX, Workflow, and Trust Design — HR Ally

## Main Workflow

HR Ally is designed as a Microsoft Teams-based HR support assistant. The user journey begins when an employee asks a question in natural language. Since AI responses are probabilistic, the system must not assume that every generated answer is correct. It should use approved HR information, communicate uncertainty where necessary, and provide a safe alternative when it cannot answer reliably.

**Main user journey:**

1. **Ask:** The employee opens HR Ally in Teams and enters a question about leave, attendance, benefits, expenses, salary documents, onboarding, or another routine HR topic.
2. **Understand:** The assistant identifies the likely intent and checks whether essential details are missing.
3. **Retrieve:** It searches approved HR documents or policy sources for relevant information.
4. **Respond:** If sufficient supporting information is available, it provides a concise answer with the relevant policy reference, link, and suggested next step.
5. **Clarify or escalate:** If the question is ambiguous, HR Ally asks a follow-up question. If it is sensitive, exceptional, unsupported, or unresolved, it directs the employee to an authorized HR representative.
6. **Feedback:** The employee can mark the answer as helpful or not helpful. Feedback can help the team identify issues for review.

### Workflow diagram

![HR Ally support workflow](ux_images/workflow_diagram.png)

Sensitive matters, such as grievances, disciplinary concerns, employee relations, compensation decisions, and policy exceptions, should be routed to qualified HR staff rather than handled as routine questions. HR Ally provides guidance but does not make final HR decisions.

## Wireframes / Screens

The prototype will contain four main screens:

### Screen 1 — Home and question entry

- HR Ally welcome message.
- Suggested topics such as Leave, Benefits, Attendance, and Salary Documents.
- A text input for natural-language questions.
- A brief notice that answers are based on available approved HR information.

![Screen 1 — Home and question entry (Teams chat)](ux_images/screen1_home_teams_chat.png)

![Screen 1 — Home and question entry (Teams channel)](ux_images/screen1_home_teams_channel.png)

### Screen 2 — Answer with source

- The employee's question and the assistant's response.
- The name of the supporting HR policy or document and a link to it.
- A suggested next step, such as opening a form or portal.
- Helpful / Not helpful feedback options.

![Screen 2 — Answer with source (Teams chat)](ux_images/screen2_answer_teams_chat.png)

![Screen 2 — Answer with source (Teams channel)](ux_images/screen2_answer_teams_channel.png)

### Screen 3 — Clarification

- A short explanation of what information is missing or unclear.
- One focused follow-up question.
- Options to provide the missing detail or contact HR if the issue remains unresolved.

![Screen 3 — Clarification (Teams channel)](ux_images/screen3_clarification_teams_channel.png)

![Screen 3 — Clarification (Teams chat)](ux_images/screen3_clarification_teams_chat.png)

### Screen 4 — Escalation and support

- A clear explanation that the assistant cannot reliably resolve the issue or that the matter needs human review.
- A link or route to the appropriate authorized HR support channel.
- A privacy-conscious notice advising the employee not to share unnecessary sensitive information in the chat.

![Screen 4 — Escalation and support (Teams chat)](ux_images/screen4_escalation_teams_chat.png)

![Screen 4 — Escalation and support (Teams channel)](ux_images/screen4_escalation_teams_channel.png)

## Trust and Explainability

### What does the user need to know?

- Whether the answer is based on approved HR information.
- Which policy or document supports the response.
- What action to take next and when to contact HR.
- When the assistant cannot provide a reliable answer.

### What must be visible?

- A relevant policy name or source link for substantive policy answers.
- A clear distinction between general guidance and a final HR decision.
- Clarification questions when required information is missing.
- A visible option to contact HR or escalate an issue.
- A feedback mechanism for reporting an unhelpful answer.

### What should be hidden or protected?

- Internal model instructions, technical implementation details, and irrelevant system information.
- Confidential employee information that the user is not authorized to access.
- Information about other employees.
- Unsupported statements presented as confirmed policy.

The assistant should not expose private information in a shared conversation. Personal information should only be accessed after appropriate identity and authorization checks. Its tone should be helpful and respectful, especially when directing employees to a human representative.

## Uncertainty Handling

**High-confidence behavior:**

When a question matches relevant, current, approved HR information and the retrieved content supports the answer, HR Ally provides a concise response with the source and next step. This is still guidance, not a guarantee that the response is correct.

**Low-confidence behavior:**

When multiple policies may apply, the question is ambiguous, or essential details are missing, HR Ally should ask a focused clarification question or explain that it needs more information. It should not select a policy or invent a rule merely to provide an answer.

**Failure or fallback behavior:**

If no suitable approved source is found, the source is outdated or conflicting, retrieval fails, or the assistant cannot support a reliable answer, it should state the limitation and direct the employee to the appropriate HR channel. Sensitive or exceptional matters should be escalated without attempting to make a final decision.

Confidence should be assessed using evidence such as the relevance of retrieved sources, source approval status, and whether the response is supported by those sources. A model-generated confidence score alone should not be treated as proof of correctness.

## Human-in-the-Loop

Human review is required wherever the assistant lacks reliable information or where a decision requires HR judgment.

- **Sensitive cases:** Route grievances, disciplinary concerns, employee relations issues, compensation decisions, and policy exceptions to qualified HR staff.
- **Unresolved questions:** Provide an HR contact or support route when clarification does not resolve the issue.
- **Final decisions:** Leave approvals, recruitment decisions, benefits eligibility, performance decisions, compensation decisions, and policy exceptions remain with authorized staff.
- **Knowledge maintenance:** Approved HR content owners review and update the policies and documents used by the assistant.
- **Employee control:** Employees review their details before any information is submitted to another system.

This design positions HR Ally as an AI-assisted first point of contact rather than an autonomous HR decision-maker. It aims to reduce repetitive inquiries while preserving privacy, accountability, and human judgment.
