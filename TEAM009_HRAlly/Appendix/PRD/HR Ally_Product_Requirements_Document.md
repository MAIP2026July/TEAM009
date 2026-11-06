# HR Ally — Product Requirements Document

## 1. Document control and summary

HR Ally is an AI-powered assistant that gives employees a single conversational entry point for routine HR questions and requests. It answers from approved HR sources with a reference and next step, and escalates unclear, sensitive or exceptional cases to authorised HR staff. It runs integrated with Microsoft Teams and as an online portal on the organisation's intranet.

| Field | Value |
| --- | --- |
| Product | HR Ally – An AI-Powered Assistant for Employee HR Support |
| Team | TEAM009 |
| Team members | Rashmi K G (2025MB26047), Senthil Kumar P (2025MB26180), Sharadhi Jain (2025MB26051), Pitchai Muthu M (2025MB26187), Rajat (2025MB26031)|
| Industry / function | Human Resources – Employee Services and HR Operations |
| Master document | HR Ally Product Proposal (this PRD follows it; anything beyond it is marked as an extension) |
| Release | MVP prototype, then evaluation before pilot |
| Channels | Microsoft Teams integration and intranet web portal, on one shared back end |
| Status | Draft for team review |

**Product principle:** HR Ally reduces repetitive work; it does not replace HR professionals. It provides guidance, never final HR decisions.

## 2. Problem and why it matters

### Current workflow problem

Employees often need to search through employee handbooks, policy documents, internal portals, emails and different HR systems to find answers to routine questions. They may not know which information is current, which process applies, what documents are required, or whom they should contact.

HR teams therefore spend considerable time answering similar questions, redirecting employees and explaining standard procedures. Responses may vary depending on who handles the inquiry, which leads to inconsistent guidance and delays. Employees may also use the wrong form or process because there is no single conversational entry point for HR support.

### Why this matters

HR support directly affects employee experience. When employees cannot find accurate information quickly, simple requests become frustrating and time-consuming. Delayed or inconsistent guidance reduces employee confidence and creates avoidable work for HR teams.

HR Ally aims to make the associate journey smoother and more efficient by giving employees an accessible first point of contact for common HR questions and routine requests, wherever they work: in Teams or on the intranet.

## 3. Goals and non-goals

### Goals

| # | Goal | Linked success evidence (section 11) |
| --- | --- | --- |
| G1 | Employees get answers faster than through the existing manual process | SE-1 |
| G2 | Answers are supported by approved HR sources and consistent with them | SE-2, SE-8 |
| G3 | Employees find responses helpful and understandable | SE-3 |
| G4 | HR teams receive fewer repetitive questions on covered topics | SE-4 |
| G5 | Employees reach the correct form, portal or support channel first time | SE-5 |
| G6 | Routine requests need fewer clarification exchanges | SE-6 |
| G7 | Unclear and sensitive questions are safely escalated, never given unsupported answers | SE-7 |
| G8 | The same quality of help is available in Teams and on the intranet portal | All, measured per channel |

### Non-goals

- Final decisions on recruitment, leave approval, compensation, benefits eligibility, performance or policy exceptions; these always remain with authorised staff.
- Handling grievances, disciplinary concerns, employee relations, compensation decisions or policy exceptions; these go directly to qualified HR staff.
- Completing every HR transaction inside either channel in the first version.
- Building or training an AI model from the beginning.
- Replacing HR professionals.

## 4. Users and deployment channels

### Target users

**Primary:** employees who need information or assistance related to HR policies, benefits, procedures, leave, expenses, attendance, salary documents, onboarding, training, recruitment and other routine HR services.

**Secondary:** HR teams that handle repetitive employee inquiries and standard service requests, plus the approved HR content owners who maintain the knowledge sources the assistant uses.

### Deployment channels

HR Ally is deployed in two channels from one shared back end, so knowledge sources, AI behaviour, escalation rules, access controls and logging are identical in both.

| Channel | Who uses it | How it is reached | Notes |
| --- | --- | --- | --- |
| Microsoft Teams integration | Employees who work in Teams | HR Ally app or chat in Teams | Conversational entry point inside the everyday workplace tool |
| Intranet web portal | Employees without Teams access, and anyone when Teams is unavailable | Link from the intranet home page and HR pages | Same answers, sources and safeguards as Teams; works in standard web browsers |

Both channels authenticate users through the organisation's identity and authorisation checks before any personal information is accessed.

## 5. Core workflow

The same workflow runs in Teams and on the intranet portal.

1. The employee opens HR Ally in Microsoft Teams or on the intranet portal and is signed in through the organisation's identity checks.
2. The employee types an HR-related question in everyday language, including informal wording, spelling errors or several requests at once.
3. HR Ally identifies the likely intent.
4. If the matter is sensitive (grievance, disciplinary concern, employee relations, compensation decision or policy exception), HR Ally routes it directly to qualified HR staff without attempting an answer.
5. If essential details are missing, HR Ally asks a clarification question.
6. HR Ally retrieves relevant information from approved HR sources.
7. If a reliable answer is found, HR Ally replies with a concise answer, a reference or link to the policy or handbook section, and a suggested next step (form, portal or HR support channel).
8. If no reliable answer is found, HR Ally offers safe escalation to HR rather than guessing.
9. Where a next step involves submitting a request to another system, the employee reviews the details before anything is submitted.
10. The employee indicates whether the answer was helpful.

## 6. MVP scope and user stories

### Smallest credible MVP

A simple tool, available in Microsoft Teams and on the intranet portal, where an employee types an HR-related question and gets:

1. A concise answer based on an approved HR source.
2. A reference or link to the relevant policy or employee handbook section.
3. A suggested next step, such as a form, portal or HR support channel.
4. A clarification question when essential information is missing.
5. A safe escalation option when the assistant cannot provide a reliable answer.
6. A simple feedback option indicating whether the answer was helpful.

The first version does not need to complete every HR transaction in either channel. It provides verified information and routes employees to the approved system. Deeper workflow integrations come later.

### Out of scope for the MVP

Final HR decisions of any kind; completing transactions inside Teams or the portal; handling sensitive matters beyond routing them to HR; building a custom AI model.

### User stories

| ID | As a… | I want to… | So that… | Acceptance criteria |
| --- | --- | --- | --- | --- |
| US-01 | Employee | ask an HR question in everyday language in Teams or on the intranet portal | I don't need the right terminology or search category | Intent identified for differently worded questions, including spelling errors and incomplete context |
| US-02 | Employee | get a concise answer from an approved HR source | I can rely on it | Every answer is based on an approved source |
| US-03 | Employee | see a reference or link to the policy or handbook section | I can verify the answer | Each answer shows the source with a working link |
| US-04 | Employee | be told the next step | I use the correct form, portal or channel | Process answers include the right form, portal or support channel |
| US-05 | Employee | be asked for missing details | the answer fits my situation | A clarification question is asked when essential information is missing |
| US-06 | Employee | escalate safely when HR Ally can't answer reliably | I'm never given a guess | Escalation offered whenever no reliable answer is found |
| US-07 | Employee raising a sensitive matter | reach qualified HR staff directly | it is handled with care | Grievances, disciplinary concerns, employee relations, compensation decisions and policy exceptions go straight to HR |
| US-08 | Employee | review request details before submission | nothing is sent on my behalf by mistake | Explicit confirmation before anything is submitted to another system |
| US-09 | Employee | say whether the answer helped | the service improves | Feedback option on every answer |
| US-10 | Employee without Teams access | use HR Ally on the intranet portal | I get the same help | Same answers, sources, next steps and escalation as in Teams |
| US-11 | HR content owner | review and maintain the knowledge sources | answers stay current and approved | Only content approved by owners is used |

## 7. Functional requirements

All MVP requirements apply equally to the Teams integration and the intranet portal.

| ID | Requirement | MVP element | Priority |
| --- | --- | --- | --- |
| FR-01 | Accept HR questions in everyday language, including spelling errors, incomplete context and multiple requests | Conversational entry point | Must |
| FR-02 | Identify the likely intent of each question | Conversational entry point | Must |
| FR-03 | Retrieve information only from approved HR sources maintained by content owners | 1. Concise answer | Must |
| FR-04 | Provide a concise answer grounded in the retrieved source | 1. Concise answer | Must |
| FR-05 | Show a reference or link to the relevant policy or handbook section | 2. Reference or link | Must |
| FR-06 | Suggest the next step: the correct form, portal, policy or HR support channel | 3. Next step | Must |
| FR-07 | Ask a clarification question when essential details are missing | 4. Clarification | Must |
| FR-08 | Offer safe escalation to authorised HR staff when no reliable answer is available | 5. Safe escalation | Must |
| FR-09 | Route sensitive matters (grievances, disciplinary concerns, employee relations, compensation decisions, policy exceptions) directly to qualified HR staff | 5. Safe escalation | Must |
| FR-10 | Collect feedback on whether each answer was helpful | 6. Feedback | Must |
| FR-11 | Require the employee to review request details before anything is submitted to another system | Human-in-the-loop | Must |
| FR-12 | Access personal information only after identity and authorisation checks | Human-in-the-loop | Must |
| FR-13 | Run Teams and the intranet portal on one shared back end with identical behaviour | Channels | Must |
| FR-14 | Make the intranet portal reachable from the intranet home page and HR pages | Channels | Must |
| FR-15 | Record usage, escalations and feedback by channel for evaluation | Evaluation | Should |
| FR-16 | Deeper workflow integration with approved HR systems | Later release | Could |

## 8. AI role, human-in-the-loop rules and build vs buy

### Proposed AI role

The assistant reads an employee's question in everyday language, identifies the likely intent, retrieves relevant information from approved HR sources, and provides a concise response with a source or next step. It may guide employees to the correct form, portal, policy or support channel, and asks follow-up questions when essential details are missing. Unclear, sensitive or exceptional cases are escalated to authorised HR staff.

### Why AI instead of a simpler alternative

A traditional portal, FAQ page or fixed decision tree requires employees to know the correct terminology and search category. The same requirement may be expressed in many ways, and questions may contain spelling errors, incomplete context or multiple requests. A dashboard without language understanding would still require employees or HR staff to search for and interpret content manually. AI understands conversational language and connects differently worded questions to relevant approved HR information, reducing search effort while keeping employees and HR staff in control.

### Human-in-the-loop rules

| # | Rule |
| --- | --- |
| H1 | HR Ally provides guidance but does not make final HR decisions. |
| H2 | Unclear or incomplete questions are flagged for clarification or direct HR attention. |
| H3 | Sensitive matters, including grievances, disciplinary concerns, employee relations, compensation decisions and policy exceptions, go directly to qualified HR staff. |
| H4 | Employees review request details before anything is submitted to another system. |
| H5 | Personal information is accessed only after appropriate identity and authorisation checks. |
| H6 | Approved HR content owners review and maintain the knowledge sources used by the assistant. |
| H7 | Final decisions on recruitment, leave approval, compensation, benefits eligibility, performance or policy exceptions always remain with authorised staff. |

These rules apply identically in Teams and on the intranet portal.

### Build vs buy vs API

Use an approved existing AI platform or API for language understanding, information retrieval and response drafting instead of building a model from the beginning. The real value lies in selecting authoritative HR content, designing guided workflows, applying access controls, creating safe escalation paths, integrating approved systems (including Teams and the intranet), and ensuring that employees or HR staff review actions before completion.

## 9. Non-functional requirements

| Area | Requirement |
| --- | --- |
| Access control | Organisation single sign-on in both channels; personal information only after identity and authorisation checks; role-based access |
| Privacy and confidentiality | Collect only the data needed; protect personal and confidential employee information; defined retention for logs |
| Content governance | Only approved sources used; each source has a content owner who reviews and maintains it |
| Channel parity | Teams and portal give the same answers, sources, next steps and escalation; quality measured per channel |
| Availability | The intranet portal remains available as an alternative when Teams is unavailable; on any system failure, employees see HR contact details |
| Responsiveness | Answers fast enough to beat the existing manual process (target to be set after baselining) |
| Auditability | Questions, sources used, answers, escalations and feedback logged for review |
| Accessibility | Usable on Teams desktop and mobile, and in standard web browsers on desktop and mobile for the portal |
| Tone | Plain, polite and concise; guidance clearly presented as guidance, not a decision |

## 10. Risks and mitigations

The seven risks are those named in the product proposal; mitigations draw on the human-in-the-loop rules and MVP design.

| # | Risk | Mitigation | Linked rule or requirement |
| --- | --- | --- | --- |
| R1 | Incorrect or outdated policy information may be presented to employees | Approved sources only; content owners review and maintain them; source reference on every answer so employees can verify | H6, FR-03, FR-05 |
| R2 | The AI may generate an answer not supported by approved HR content | Answers grounded in retrieved sources; safe escalation instead of guessing when no reliable answer exists | FR-04, FR-08 |
| R3 | Personal or confidential employee information may be exposed without proper access control | Identity and authorisation checks before personal data; role-based access in both channels | H5, FR-12 |
| R4 | The assistant may misunderstand dates, request types or employee-provided details | Clarification questions; employee reviews details before submission | H2, H4, FR-07, FR-11 |
| R5 | Sensitive HR matters may be handled inappropriately instead of being escalated | Sensitive matters routed directly to qualified HR staff without an AI answer | H3, FR-09 |
| R6 | Employees may over-trust the assistant and treat guidance as a final HR decision | Clear statement that HR Ally gives guidance only; final decisions remain with authorised staff | H1, H7 |
| R7 | Excessive automation may reduce the personal element of HR support | Escalation to a person always available; HR time redirected to complex cases | FR-08, product principle |
| R8 (extension) | Quality or behaviour differs between Teams and the portal | One shared back end; quality measured separately per channel | FR-13, FR-15 |

## 11. Success evidence and measures

The eight items of success evidence come from the product proposal. Measures and proposed targets make them testable; targets marked *proposed* come from the team's PM Artifact Pack and are confirmed after baselining. Every measure is reported separately for Teams and the intranet portal.

| # | Success evidence | How it is measured | Proposed target |
| --- | --- | --- | --- |
| SE-1 | Employees obtain answers faster with HR Ally than through the existing manual process | Time to answer with HR Ally vs the current process, on the same set of questions | Faster than baseline |
| SE-2 | Eligible answers are supported by approved HR sources | Share of definitive answers backed by an approved source | ≥ 95% *(proposed)* |
| SE-3 | Employees rate responses as helpful and understandable | Average feedback rating | ≥ 4.0 / 5 *(proposed)* |
| SE-4 | HR teams receive fewer repetitive questions for covered topics | Change in HR inquiries in covered categories (pilot stage) | 20% reduction *(proposed)* |
| SE-5 | Employees reach the correct form, portal or support channel more consistently | Share of process questions routed to the right next step | Higher than baseline |
| SE-6 | Routine requests require fewer clarification exchanges | Average clarification exchanges per resolved routine request | Lower than baseline |
| SE-7 | Unclear and sensitive questions are safely escalated instead of receiving unsupported answers | Share of unclear or sensitive test questions escalated correctly | ≥ 90% *(proposed)*; zero sensitive questions answered by AI |
| SE-8 | HR reviewers find responses consistent with the applicable approved content | HR reviewer assessment of answers against approved content | Critical policy errors < 1% *(proposed)* |

### How evidence is gathered

1. **Prototype evaluation:** representative employee questions with HR-reviewed expected answers, run in both channels.
2. **Human review:** HR reviewers assess correctness, source alignment and consistency.
3. **Time comparison:** the same questions answered through HR Ally and through the existing manual process.
4. **Limited pilot (if evaluation passes):** live feedback, routing and inquiry-volume data by channel.

## 12. Release approach, dependencies and open questions

### Release approach: prototype, then evaluate before piloting

| Stage | What happens | Move on when |
| --- | --- | --- |
| 1. Prototype | Narrow prototype in Teams and on the intranet portal demonstrating all six MVP elements for a selected set of routine HR questions | All six elements work end to end in both channels |
| 2. Evaluate | Test against representative questions and HR-reviewed expected answers; compare time to answer with the manual process | Success evidence SE-1 to SE-3 and SE-5 to SE-8 met in both channels |
| 3. Limited pilot | Controlled use by a representative employee group in both channels | Useful, grounded guidance; employee information protected; cases escalated safely; SE-4 measured |
| 4. Later releases | Deeper workflow integrations with approved HR systems | Pilot evidence and governance approval |

### Dependencies

- An approved AI platform or API for language understanding, retrieval and response drafting.
- Microsoft Teams app approval and intranet portal hosting.
- Organisation single sign-on and authorisation checks for both channels.
- Approved HR sources with named content owners.
- An HR support channel to receive escalations.

### Assumptions

- Approved HR policies and support resources can be made accessible to the assistant.
- Employees will use a conversational entry point in Teams or on the portal before contacting HR.
- Current time-to-answer and routing performance can be baselined.

### Open questions

- Which routine HR topics form the selected set for the prototype?
- Which HR support channel receives escalations?
- Which employees lack Teams access, and must the portal work outside the corporate network?
- Which proposed targets in section 11 does the team adopt after baselining?
