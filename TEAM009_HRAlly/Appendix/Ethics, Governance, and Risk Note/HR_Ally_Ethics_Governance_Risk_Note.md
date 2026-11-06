# HR Ally: Ethics, Governance, and Risk Note

**Team:** TEAM009 · **Date:** 6 November 2026 · **Standards:** IAPP AIGP body of knowledge; India's Digital Personal Data Protection Act, 2023 (DPDP Act) and DPDP Rules, 2025

## 1. Summary

HR Ally gives employees guidance, never decisions, and every employee can reach a person at any point. It is governed as a **medium-risk AI system** under the AIGP framework and processes employee data as a **legitimate use for employment under DPDP Section 7(i)**. The two zero-tolerance risks are a sensitive matter answered by the AI and personal data exposed; either one triggers rollback.

| Standard | Governs | HR Ally's position |
| --- | --- | --- |
| AIGP Domain I: Foundations | Principles, roles, accountability | Organisation uses AI to support HR guidance |
| AIGP Domain II: Laws and frameworks | DPDP Act, NIST AI RMF, ISO/IEC 42001, OECD AI Principles | DPDP is the governing law; NIST AI RMF structures risk work |
| AIGP Domain III: Governing development | Data, design, testing, documentation | Team builds the retrieval pipeline, prompts and checks |
| AIGP Domain IV: Governing deployment | Vendor due diligence, monitoring, incidents | Deployer of a vendor's hosted language model |
| DPDP Act and Rules | Lawful processing, security, breach, retention, rights | Employer = Data Fiduciary; AI vendor = Data Processor; employees = Data Principals |

## 2. Ethical principles

These seven commitments follow from the HR Ally proposal and the OECD AI Principles.

| # | Principle | In practice |
| --- | --- | --- |
| P1 | Human authority | Leave, pay, benefits, hiring, performance and exceptions are decided only by authorised staff (H1, H7) |
| P2 | Grounded truthfulness | Answers only from approved sources, with a citation; no source means escalation (FR-03 to FR-08) |
| P3 | Care for sensitive matters | Grievances, discipline, employee relations, compensation and exceptions go straight to HR (H3, FR-09) |
| P4 | Privacy by design | Personal data only after SSO and authorisation, only for the question asked, never for training (H5) |
| P5 | Fairness | Same answer for the same question, whatever the channel, role, language skill or phrasing (G2, G8) |
| P6 | Transparency | Employees know they are talking to an AI, see the source, and see that it is guidance |
| P7 | Accountability | Every answer logged and traceable to its source and a named owner (H6, FR-15) |

## 3. Ethical issues and safeguards

| Issue | Concern | Safeguard | Check |
| --- | --- | --- | --- |
| Fairness | Weaker understanding of non-native or informal writers; policies differ by location and grade | Retrieval filtered to the employee's policies; diverse phrasing in the test set; no ranking or profiling of employees | Quality and escalation rates compared across groups and channels |
| Privacy | Employees volunteer health, family or complaint details | Minimisation; masked logs; restricted access to sensitive conversations; no vendor training | Quarterly log-access review; red-team leakage tests |
| Transparency | AI answer mistaken for an HR decision | First-use notice; source link and "guidance only" on every answer | HR reviewers check every sampled answer |
| Over-trust | Fluent answers taken as final | No decision wording; employee reviews details before submission; "talk to HR" always one click away | Red-team requests for approvals must be refused |
| Wellbeing | Distress (bereavement, harassment, health) met by automation | Distress cues route to a person, with Employee Assistance Programme details where available | Monthly HR review of these conversations |

## 4. Governance

An **HR Ally Steering Group** (HR head, IT security, DPO, legal, product owner) owns risk appetite and decides go or no-go for each release. Named owners run the system day to day.

| Role | Responsible for |
| --- | --- |
| Product owner | Requirements, evaluation results, risk register |
| HR content owners | Accuracy and currency of each policy source; approving content changes |
| HR escalation team | Routed sensitive matters and escalations; every HR outcome |
| Platform and IT security | SSO, access control, logging, vendor management, uptime |
| Data protection officer | DPDP compliance: impact assessment, retention, breach reporting, employee rights |
| HR reviewers | Scoring answer quality; judging critical policy errors |

**Change control.** Policy updates are approved by the content owner and the old version withdrawn the same day. Any model, prompt or threshold change re-runs the full evaluation set. A vendor or model swap is a new release needing security review, a data protection check and Steering Group approval.

**Review cadence.** Weekly live-answer spot checks; monthly metrics and risk register review; quarterly content, log-access and fairness reviews; a full governance review every six months and before each release stage.

### AI lifecycle governance (AIGP Domains III and IV)

| Stage | Key controls | Evidence |
| --- | --- | --- |
| 1. Plan | Use case and prohibited uses; risk tier; AI impact assessment combined with data protection assessment | Use-case statement; impact assessment |
| 2. Data | Source inventory, provenance, owner, purpose and legal ground; no personal data in the index | Data inventory; record of processing |
| 3. Vendor due diligence | Security review; data processing agreement; no training; data residency | Vendor assessment; signed agreement |
| 4. Build and test | HR-reviewed test set; fairness checks; red-team testing | System card; evaluation report |
| 5. Deploy | Release gate; employee notice and AI disclosure; escalation staffed | Go/no-go record |
| 6. Monitor | Metric thresholds; incident handling; periodic audit | Dashboards; incident log |
| 7. Change and retire | Re-assessment on triggers; deletion of logs and indexes on retirement | Change records; deletion certificate |

**Risk classification.** HR Ally is **medium risk** because it makes no employment decisions. It becomes **high risk**, needing a new impact assessment and Steering Group approval, if it starts to recommend HR outcomes, writes to HR records, has its logs used to monitor employees, or is extended to applicants or EU staff.

## 5. Risk register

Ratings are likelihood × impact before controls (inherent) and after them (residual), reviewed monthly. R1 to R7 come from the proposal; R8 to R12 were added in this review.

| # | Risk | Inherent | Key controls | Residual | NIST AI RMF | DPDP link |
| --- | --- | --- | --- | --- | --- | --- |
| R1 | Outdated or incorrect policy given | High | Approved sources; review dates; citations | Low | Manage | None |
| R2 | Unsupported (hallucinated) answer | High | Grounding; answerability check; escalate when unsure | Low | Measure | None |
| R3 | Personal data exposed | High | SSO; no personal data in index; masked logs | Low | Manage | Sec 8(5), 8(6) |
| R4 | Dates or details misunderstood | Medium | Clarification; employee review before submission | Low | Measure | Sec 8(3) |
| R5 | Sensitive matter answered by AI | High | Sensitivity check first; rules backstop; zero-tolerance test | Low | Map, Manage | Internal policy |
| R6 | Guidance treated as a decision | High | "Guidance only"; no decision wording | Medium | Map | Sec 5 notice |
| R7 | Loss of human touch | Medium | Human escalation always available | Low | Govern | None |
| R8 | Unequal quality across groups | Medium | Policy filtering; per-group metrics | Low | Measure | None |
| R9 | Prompt injection or misuse | Medium | Input filtering; red-team tests; read-only access | Low | Measure | Sec 8(5) |
| R10 | Vendor change or data retention | Medium | Contract terms; regression before model change | Low | Govern | Sec 8(2), 16 |
| R11 | Logs used to monitor employees | Medium | Purpose limitation; audited access | Low | Govern | Sec 7(i), 8(7) |
| R12 | Escalation queue overloaded | Medium | Weekly volume monitoring; staffing review | Low | Manage | Sec 8(10) |

R6 stays medium because over-trust depends on employee behaviour, which design can reduce but not remove.

## 6. DPDP Act compliance

HR Ally relies on Section 7(i), legitimate use for employment, rather than consent. All other Data Fiduciary duties still apply. This is a planning aid, not legal advice.

| Provision | Requirement | HR Ally control |
| --- | --- | --- |
| Sec 4, 7(i), 7(a) | Lawful purpose; volunteered data used only for its purpose | Purpose limited to answering and routing HR questions |
| Sec 5 (good practice) | Notice of data and purpose | First-use notice in Teams and on the portal |
| Sec 8(1), 8(2) | Fiduciary accountable for processors; processors under contract | Data processing agreements with AI and hosting vendors |
| Sec 8(3) | Accurate data where it affects the employee | Employee reviews details; live reads from HR systems |
| Sec 8(4), 8(5) | Reasonable security safeguards | SSO, role-based access, encryption, masked logs |
| Sec 8(6) | Breach notice to the Board and affected employees | Breach process in section 7 |
| Sec 8(7) | Erase once purpose is served | Retention schedule; vendor deletion terms |
| Sec 8(9), 8(10), 11–14 | Published contact; grievance redressal; access, correction, erasure, nomination | DPO contact published; HR can export or delete an employee's history |
| Sec 10 | Extra duties if notified as a Significant Data Fiduciary | DPIA and audit done anyway as AIGP practice |
| Sec 16 | Cross-border transfer except to restricted countries | Vendor regions checked at contract and each review |

**DPDP Rules, 2025.** Notified in November 2025, with most obligations in force after an 18-month transition (around May 2027). HR Ally should meet them from the pilot:

- affected employees are told of a breach without delay
- the Board gets a detailed report within 72 hours
- security logs are kept for at least one year
- grievances are answered within 90 days

Penalties reach ₹250 crore for inadequate security safeguards and ₹200 crore for failing to report a breach. Conversation text is deleted sooner than the one-year security logs, on a schedule legal confirms.

**Before the pilot:**

- [ ] DPIA and record of processing signed off by the DPO
- [ ] Employee notice published
- [ ] Vendor agreements signed, including no-training and deletion terms
- [ ] Data regions checked against Section 16
- [ ] Retention schedule agreed
- [ ] Breach response rehearsed against the 72-hour deadline
- [ ] Rights request process ready

## 7. Incident response and accountability

| Severity | Examples | Action | Notify |
| --- | --- | --- | --- |
| Critical | Sensitive matter answered; data shown to the wrong person; wrong HR outcome | Disable topic or service; preserve logs; HR contacts employee | Steering Group and DPO at once; for a data breach, affected employees without delay and the Board within 72 hours (Sec 8(6)) |
| Major | Critical policy error; wrong form on a high-impact process | Withdraw faulty source; fix and re-test | Product and content owners same day |
| Minor | Unclear wording; broken link | Fix in next release | Weekly review |

**Steps:**

1. Detect.
2. Contain, routing employees to HR.
3. Assess: if personal data is involved, the DPO starts the DPDP clock.
4. Remediate the employee's situation, then the root cause.
5. Verify by adding the case to the test set and re-running it.
6. Record in the risk register and report to the Steering Group.

**Accountability.** Responsibility never sits with the AI. Content owners answer for source accuracy, the product owner for system behaviour, the platform team for security, and HR staff for every HR decision. Employees who act on wrong guidance in good faith are not penalised; HR corrects the outcome.

**Open questions:**

- Is the employer, or might it be notified as, a Significant Data Fiduciary?
- Are any employees outside India in scope?
- Is there an Employee Assistance Programme to route to?
- What HR response times apply to escalations?
- What is the retention period for conversation text?

*DPDP section numbers, Rules details and the AIGP domain structure should be confirmed against the official texts and the current IAPP body of knowledge.*
