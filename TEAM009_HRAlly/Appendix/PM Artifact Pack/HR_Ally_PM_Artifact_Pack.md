# PM Artifact Pack

## Problem Statement

Employees often struggle to obtain timely and reliable answers to routine HR questions because information is distributed across policy documents, employee portals, emails, service desks, and HR systems. They may not know which policy is current, which procedure applies to their location or employment context, or whom to contact when the available information is unclear.

As a result, employees experience delays and uncertainty, while HR teams spend significant time responding to repetitive, low-complexity questions instead of focusing on higher-value workforce activities. HR Ally addresses this problem through a conversational assistant in Microsoft Teams and the intranet portal that retrieves approved HR information, explains it in clear language, guides employees to the appropriate next step, and escalates sensitive or uncertain cases to authorized HR representatives.

### How AI Changes the Problem

A conventional HR portal requires employees to know what to search for and where to find it. An AI-powered product must go further by:

- Interpreting natural-language questions and employee intent.

- Retrieving information from approved HR sources.

- Combining relevant policy content into a concise response.

- Recognizing ambiguity, missing information, or sensitive topics.

- Communicating uncertainty rather than presenting assumptions as facts.

- Escalating cases where human judgment or authorization is required.

Therefore, the product problem is not simply access to information. It is the delivery of **relevant, explainable, source-grounded, and appropriately governed HR guidance**.

## Product Vision

To make employee-HR interactions simple, trusted, personalized, and accessible through an intelligent HR companion embedded in the digital workplace.

HR Ally will become the trusted first point of contact for routine HR support. It will help employees obtain approved information, understand applicable processes, identify required documents, and initiate supported requests through a single conversational experience. Over time, it can evolve from an information assistant into a governed HR service platform supporting personalized guidance and approved transactional workflows.

### AI-Powered Future State

The future product will not behave like a generic chatbot. It will combine:

- **Generative AI** for natural, context-aware conversations.

- **Retrieval-Augmented Generation, or RAG,** for answers grounded in approved HR content.

- **Deterministic rules** for eligibility, approvals, calculations, and regulated processes.

- **Workflow orchestration** for creating or tracking supported HR requests.

- **Human oversight** for exceptions, sensitive matters, and final decisions.

- **Continuous evaluation** to monitor accuracy, trust, safety, and content gaps.

## PRD Summary

### User Problem

Employees need fast and reliable guidance on HR policies, benefits, leave, payroll documents, expenses, attendance, onboarding, training, and related procedures. Existing channels require employees to search across multiple systems or wait for help-desk and HR responses.

HR teams need to reduce repetitive inquiries without compromising accuracy, confidentiality, compliance, or employee trust.

### Target Users

#### Primary users

- Employees seeking HR information or procedural guidance.

- New employees navigating onboarding and benefits.

- Managers seeking standard HR process information.

#### Secondary users

- HR service-desk representatives.

- HR business partners.

- Policy and knowledge-content owners.

- Product administrators and AI-governance teams.

### Core Workflow

1.  The employee opens HR Ally in Microsoft Teams or the intranet portal.

2.  The employee asks a question in natural language.

3.  The system identifies the employee’s intent and requires context.

4.  The retrieval layer searches approved HR policies and knowledge sources.

5.  The AI generates a concise, source-linked response.

6.  HR Ally presents applicable steps, required documents, and official links.

7.  If the answer is uncertain, sensitive, or outside scope, the system offers clarification or escalation.

8.  The employee confirms whether the response resolved the issue.

9.  Anonymous usage signals and unresolved-query patterns are recorded for product improvement.

### AI Role

AI will:

- Classify the employee’s intent.

- Understand conversational and follow-up questions.

- Retrieve relevant passages from approved HR sources.

- Summarize complex policies in employee-friendly language.

- Maintain context during a conversation.

- identify potential ambiguity or conflicting information.

- Recommend the appropriate next step.

- Route unresolved cases to the correct HR channel.

AI will **not**:

- Make employment, compensation, disciplinary, promotion, or eligibility decisions.

- Invent policy information when no approved source is available.

- Override official HR systems or approval workflows.

- expose information that the user is not authorized to access.

- present low-confidence content as definitive guidance.

### Risks

| **Risk**                              | **Product Response**                                                                                 |
|---------------------------------------|------------------------------------------------------------------------------------------------------|
| Hallucinated or inaccurate guidance   | Use RAG, approved data sources, source citations, answer validation, and confidence-based fallback   |
| Outdated policy information           | Assign document owners, effective dates, review dates, and automated expiry alerts                   |
| Exposure of sensitive employee data   | Apply role-based access, data minimization, encryption, audit logging, and retention controls        |
| Incorrect personalization             | Require authenticated context and use deterministic rules for eligibility-sensitive responses        |
| User overreliance on AI               | Clearly distinguish guidance from official decisions and show source links                           |
| Bias or inconsistent treatment        | Conduct evaluation across employee groups, locations, languages, and question types                  |
| Prompt injection or malicious content | Restrict retrieval sources, filter inputs, isolate instructions, and test adversarial scenarios      |
| Poor employee adoption                | Embed the solution in Teams and the intranet portal and provide concise answers with visible sources |

### Fallback Logic

HR Ally will use the following response hierarchy:

1.  **High confidence:** Provide a direct answer with the applicable source and next step.

2.  **Medium confidence:** Provide the likely answer, state the limitation, and ask a focused clarification question.

3.  **Low confidence:** Do not generate a definitive answer. Present relevant official resources or create an HR inquiry.

4.  **Conflicting sources:** Inform the employee that the available policies appear inconsistent and escalate to the designated content owner.

5.  **Sensitive subject:** Route the employee to an authorized HR representative without unnecessary conversational probing.

6.  **System or model failure:** Display official HR links and escalation options so the employee is never left without a path forward.

A recommended launch rule is that HR Ally should provide a definitive policy answer only when it retrieves an approved source, confirms access permissions, and meets the agreed confidence threshold. Thresholds should be calibrated during pilot evaluation rather than selected arbitrarily.

## Feature Prioritization

The prioritization logic balances **user value, delivery effort, confidence in the use case, operational risk, and learning value**. Features that offer frequent value with manageable AI risk are prioritized before sensitive or transactional capabilities.

| **Feature**                                               | **User Value** | **Effort** | **Confidence** | **Priority** |
|-----------------------------------------------------------|----------------|------------|----------------|--------------|
| Natural-language HR policy Q&A                            | High           | Medium     | High           | P0           |
| Source citations and policy links                         | High           | Medium     | High           | P0           |
| Clarification questions for ambiguous requests            | High           | Medium     | High           | P0           |
| Confidence-based human escalation                         | High           | Medium     | High           | P0           |
| Employee feedback on answer usefulness                    | Medium         | Low        | High           | P0           |
| Search across approved HR knowledge sources               | High           | Medium     | High           | P0           |
| Guided navigation for leave, benefits and payroll queries | High           | Medium     | High           | P1           |
| HR inquiry creation with conversation summary             | High           | Medium     | Medium         | P1           |
| Multilingual interaction                                  | Medium         | Medium     | Medium         | P1           |
| Personalized answers based on authorized profile data     | High           | High       | Medium         | P2           |
| HR request status tracking                                | High           | High       | Medium         | P2           |
| Transactional leave or document requests                  | High           | High       | Medium         | P2           |
| Proactive reminders and recommendations                   | Medium         | High       | Low            | P3           |
| Predictive workforce insights                             | Medium         | Very High  | Low            | P3           |

### Prioritization Logic

- **P0 features** are required to prove that HR Ally can answer routine HR questions accurately, safely, and transparently.

- **P1 features** improve resolution and accessibility after response quality has been established.

- **P2 features** require HR-system integration, identity validation, authorization controls, and stronger governance.

- **P3 features** have higher privacy, bias, and explainability risks and should be considered only after the core product demonstrates sustained trust and value.

The AI-specific priority is not maximum automation. It is **maximum reliable resolution within an explicitly controlled risk boundary**.

## MVP Definition

The MVP is an HR assistant in Microsoft Teams and the intranet portal that answers a limited set of high-volume, low-risk HR policy and benefits questions using approved organizational content.

### MVP Scope

The MVP will include:

- Microsoft Teams and intranet portal conversational interfaces.

- Natural-language question handling.

- RAG-based retrieval from approved HR policies and FAQs.

- Coverage of three initial domains:

  - Leave and time-off policies.

  - Employee benefits.

  - Payroll and standard HR document guidance.

- Source-linked responses.

- Clarification questions for ambiguous requests.

- Confidence-based fallback.

- Escalation to the existing HR support channel.

- Basic feedback collection.

- Administrative reporting on usage, unresolved questions, and content gaps.

### Out of Scope

The MVP will not include:

- Employment or eligibility decisions.

- Compensation recommendations.

- Performance-management decisions.

- Direct modification of employee records.

- Autonomous approval of leave, expense, or recruitment requests.

- Predictive employee-behaviour analysis.

- Open-ended answers produced without approved source material.

### MVP Hypothesis

If employees can ask routine HR questions through Microsoft Teams or the intranet portal and receive concise, source-grounded answers with a clear escalation path, then they will resolve more queries independently, experience faster support, and reduce repetitive demand on HR teams without decreasing trust or policy compliance.

### What the MVP Must Prove

The MVP must demonstrate that:

1.  Employees are willing to use a conversational HR channel.

2.  The AI can provide grounded and useful answers within selected domains.

3.  Source visibility and fallback logic create sufficient user trust.

4.  Routine inquiry volumes can be deflected without increasing errors or escalations.

5.  Unresolved questions reveal actionable gaps in HR content and processes.

## Roadmap

### Phase 1a: Prototype and Evaluate

**Indicative timeline: 0 to 3 months**

- Prototype in Teams and the intranet portal on one shared back end.

- Cover selected leave, benefits, payroll, and document-request FAQs.

- Use RAG on approved HR sources, with source links and effective dates.

- Test accuracy, groundedness, safety, latency, and access controls offline.

- Compare time to answer with the manual process.

**Primary goal:** Prove the six MVP elements work in both channels (Gate A).

### Phase 1b: Limited Pilot – Trusted Knowledge Assistant

**Indicative timeline: 0 to 3 months**

- Pilot with a representative employee group in both channels.

- Run confidence-based fallback and human escalation live.

- Measure feedback, routing, and inquiries by channel.

**Primary goal:** Prove HR Ally answers high-volume, low-risk questions accurately and consistently (Gate B).

### Phase 2: Personalized Assistant

**Indicative timeline: 4 to 6 months**

- Add more HR policy domains.

- Introduce multilingual support.

- Create HR inquiries with structured conversation summaries.

- Introduce authorized, limited personalization.

- Provide HR administrators with content-gap and resolution dashboards.

- Conduct bias, privacy, security, and accessibility testing.

- Establish formal content-owner review and service-level agreements.

**Primary goal:** Improve end-to-end resolution while maintaining human oversight (Gate C).

### Phase 3: Transactional Assistant

**Indicative timeline: 7 to 12 months**

- Integrate approved HR transactional workflows.

- Support leave, expense, document, and certificate requests, reviewed by the employee first.

- Add request tracking where supported.

- Implement continuous model and retrieval monitoring.

- Create formal incident-response and model-change processes.

**Primary goal:** Complete routine requests while approvals stay in HR systems (Gate D).

### Phase 4: HR AI Platform

**Indicative timeline: after 12 months**

- Expand to onboarding and training journeys.

- Provide proactive reminders where consent and policy permit.

- Introduce controlled analytics on aggregate inquiry trends.

- Scale the platform across relevant geographies and business units.

**Primary goal:** Evolve from an information assistant into a governed employee-service platform.

### AI Roadmap Principle

Each phase should advance only when the preceding phase meets defined **quality, trust, privacy, and safety thresholds**. Feature expansion must depend on evidence from evaluation and production monitoring, not only delivery readiness. Gates A to D apply to both channels.

## Success Metrics

The following are proposed pilot targets and should be baselined against current HR service performance before final approval.

### Product Metric

### Self-Service Resolution Rate

Percentage of eligible employee questions resolved through HR Ally without a subsequent HR inquiry within 24 hours.

- **Pilot target:** 50% or higher.

- **Post-pilot target:** 65% to 70% within approved use cases.

- **Supporting measures:** Weekly active users, repeat usage, task completion, median response time, and clarification rate.

### Business Metric

### Reduction in Repetitive HR Inquiry Volume

Change in HR help-desk inquiries for the policy areas covered by HR Ally.

- **Pilot target:** 20% reduction in covered inquiry categories.

- **Scale target:** 30% to 40% reduction after content and workflow expansion.

- **Supporting measures:** Cost per resolved inquiry, average handling time, first-response time, and HR hours redirected to higher-value activities.

### Trust and Guardrail Metrics

| **Metric**                      | **Proposed Target**                                                           |
|---------------------------------|-------------------------------------------------------------------------------|
| Grounded-answer rate            | At least 98% of definitive answers supported by an approved source            |
| Critical policy-error rate      | Below 1%, with zero tolerance for severe employee-impacting errors            |
| Citation accuracy               | At least 95%                                                                  |
| Appropriate fallback rate       | At least 90% on unsupported or ambiguous test questions                       |
| Unauthorized data exposure      | Zero confirmed incidents                                                      |
| User trust or helpfulness score | At least 4.0 out of 5                                                         |
| Escalation completion rate      | At least 95% of escalated cases provide a valid next step                     |
| P95 response time               | Under 8 seconds during the pilot                                              |
| Coverage parity                 | No material quality gap across tested employee groups, locations, or channels |

### AI Evaluation Approach

Success cannot be measured only through adoption or inquiry reduction. HR Ally should be evaluated across four levels:

1.  **Offline evaluation:** Test against a curated set of representative, ambiguous, sensitive, and adversarial questions.

2.  **Human review:** HR subject-matter experts assess answer accuracy, completeness, tone, and source alignment.

3.  **Pilot monitoring:** Compare AI answers, escalations, and employee feedback with existing support outcomes.

4.  **Production monitoring:** Track quality drift, source freshness, fallback behaviour, incidents, and differences across user segments.

## Final Product Principle

HR Ally should automate access to HR information, not HR accountability. The product creates value when it resolves routine questions quickly while remaining transparent about its sources, limitations, and confidence. Human HR professionals must retain responsibility for sensitive interpretation, exceptions, formal approvals, and employment decisions.
