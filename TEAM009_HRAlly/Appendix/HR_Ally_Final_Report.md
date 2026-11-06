# Final Report — HR Ally

## An AI-Powered Assistant for Employee HR Support

**Team:** TEAM009 · **Industry / Function:** Human Resources – Employee Services and HR Operations
**Team members:** Rashmi K G, Senthil Kumar P, Sharadhi Jain, Pitchai Muthu M, Rajat

## 1. Recommendation

We recommend building a narrow HR Ally prototype, evaluating it against HR-reviewed questions, and moving to a limited pilot only when the evidence supports it. HR Ally gives employees a single conversational entry point for routine HR questions, in **Microsoft Teams** and on an **online portal in the organisation's intranet**, from one shared back end. It answers from approved HR sources with a reference and next step, and escalates unclear, sensitive or exceptional cases to authorised HR staff. It provides guidance; it does not make HR decisions.

## 2. The problem

Employees search handbooks, policy documents, internal portals, emails and several HR systems to answer routine questions. They may not know which information is current, which process applies, what documents are required, or whom to contact, and they may use the wrong form because there is no single conversational entry point for HR support.

HR teams spend considerable time answering similar questions, and answers vary by who responds. HR Ally aims to make the associate journey smoother by giving employees an accessible first point of contact, so qualified HR staff can focus on complex cases and matters requiring judgment.

## 3. Users and channels

**Primary users** are employees needing help with HR policies, benefits, leave, expenses, attendance, salary documents, onboarding, training, recruitment and other routine services. **Secondary users** are HR teams handling repetitive inquiries, and HR content owners who maintain the approved sources.

| Channel | Who uses it | Notes |
| --- | --- | --- |
| Microsoft Teams integration | Employees who work in Teams | Conversational entry point inside the everyday workplace tool |
| Intranet web portal | Employees without Teams access, or anyone when Teams is unavailable | Same answers, sources and safeguards as Teams |

## 4. Strategy and opportunity

Our strategy is **feature first, platform later**: start with trusted HR policy and benefits Q&A, prove value and trust, then expand to personalised guidance, transactions and finally a reusable HR AI platform. The durable advantage is not the language model, which is bought through an approved platform, but the curated HR knowledge, workflow integration, access controls and safe escalation design.

**Why AI:** a portal, FAQ page or decision tree requires employees to know the right terminology. The same need is expressed in many ways, with spelling errors, incomplete context or several requests at once. AI connects differently worded questions to the right approved information while keeping employees and HR staff in control.

## 5. The product

The smallest credible MVP gives an employee, in Teams or on the intranet portal:

1. A concise answer based on an approved HR source.
2. A reference or link to the relevant policy or handbook section.
3. A suggested next step, such as a form, portal or HR support channel.
4. A clarification question when essential information is missing.
5. A safe escalation option when no reliable answer is available.
6. A simple feedback option on whether the answer helped.

The first version does not complete every HR transaction; it provides verified information and routes employees to the approved system.

### Human-in-the-loop rules

HR Ally provides guidance but makes no final HR decisions. Unclear questions are clarified or sent to HR. Grievances, disciplinary concerns, employee relations, compensation decisions and policy exceptions go directly to qualified HR staff. Employees review request details before anything is submitted. Personal information is accessed only after identity and authorisation checks. Approved HR content owners maintain the knowledge sources. Final decisions on recruitment, leave approval, compensation, benefits eligibility, performance and policy exceptions remain with authorised staff.

## 6. UX and trust design

The user journey runs **Ask → Understand → Retrieve → Respond → Clarify or escalate → Feedback**, and is the same in both channels. Four screens carry it: home and question entry, answer with source, clarification, and escalation and support.

Trust is designed in:

- **Visible:** the policy name or source link, a clear line between guidance and a final HR decision, clarification questions, a contact-HR option, and feedback.
- **Protected:** internal instructions, other employees' information, confidential data the user is not authorised to see, and unsupported statements presented as policy.
- **Uncertainty:** high confidence gives a sourced answer; low confidence triggers a focused clarification; failure or conflicting sources lead to a stated limitation and an HR route. Confidence rests on source relevance, approval status and support for the answer, not on a model score alone.

## 7. Data, model and evaluation

HR Ally uses **retrieval-augmented generation (RAG)** on an approved AI platform or API, rather than building or training a model. Answers draw only on approved HR sources, each with a named content owner and review date. The prototype is evaluated against representative employee questions with HR-reviewed expected answers, including ambiguous, sensitive and unanswerable cases, and the time to answer is compared with the existing manual process. Results are reported separately for Teams and the portal.

## 8. Roadmap

| Phase | Timing (indicative) | Focus | Gate to proceed |
| --- | --- | --- | --- |
| 1a. Prototype and evaluate | Months 0–3 | Six MVP elements in both channels; HR-reviewed test questions | Gate A: success evidence met on test questions in both channels |
| 1b. Limited pilot | Months 0–3 | Policy, benefits and handbook Q&A for a representative employee group | Gate B: grounded, useful guidance; data protected; safe escalation |
| 2. Personalised assistant | Months 4–6 | Authorised employee context, more HR domains, inquiry summaries | Gate C: identity and authorisation checks proven |
| 3. Transactional assistant | Months 7–12 | Leave, expense and document requests through HR system APIs, reviewed by the employee | Gate D: proven use cases need shared services |
| 4. HR AI platform | After month 12 | Onboarding, learning, recruitment support and analytics as shared services | — |

Accuracy and safety outweigh volume at every gate.

## 9. Success measures

**North Star:** routine HR questions resolved correctly and safely through HR Ally each month, across both channels.

| Success evidence (from the proposal) | Proposed pilot target |
| --- | --- |
| Faster answers than the manual process | Faster than baseline; aim for 50% reduction |
| Answers supported by approved HR sources | ≥ 98% |
| Responses rated helpful and understandable | ≥ 4.0 / 5 |
| Fewer repetitive HR questions on covered topics | 20% reduction |
| Correct form, portal or channel reached | Higher than baseline |
| Fewer clarification exchanges | Lower than baseline |
| Unclear and sensitive questions safely escalated | ≥ 90% safe fallback; ≥ 95% sensitive routed; zero answered by AI |
| Responses consistent with approved content | ≥ 95% HR-validated; critical errors < 1% |

Targets are proposed and confirmed after baselining; each is reported for Teams, the portal and combined.

## 10. Risks and mitigations

| Risk | Mitigation |
| --- | --- |
| Incorrect or outdated policy information | Approved sources only; content owners and review dates; source shown with every answer |
| Answers not supported by approved content | Answers grounded in retrieved sources; escalation instead of guessing |
| Exposure of personal or confidential data | Identity and authorisation checks; role-based access in both channels |
| Sensitive matters handled inappropriately | Direct routing to qualified HR staff with no AI answer |
| Over-trust in guidance | Clear guidance-versus-decision messaging; decisions stay with authorised staff |
| Different quality between Teams and portal | One shared back end; metrics reported per channel |

## 11. Business view

Value comes from faster answers, fewer repetitive inquiries, consistent guidance and HR time redirected to judgment work; the main costs are the AI platform, Teams and intranet integration, and content upkeep. Detail is in the Business, Economics and Scaling View.

## 12. Reflection

The hardest part of an AI product is often the content and process around the model. Defining success evidence and gates before building keeps the team honest, and deciding early what HR Ally must never do made it simpler and safer.
