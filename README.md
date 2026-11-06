# HR Ally – An AI-Powered Assistant for Employee HR Support

**Team:** TEAM009 · **Course:** MBA ZG583 · **Industry / function:** Human Resources – Employee Services and HR Operations

## Team Members

| # | Name | Student ID |
| --- | --- | --- |
| 1 | Rashmi K G | 2025MB26047 |
| 2 | Senthil Kumar P | 2025MB26180 |
| 3 | Sharadhi Jain | 2025MB26051 |
| 4 | Pitchai Muthu M | 2025MB26187 |
| 5 | Rajat Ranjan Verma | 2025MB26031 |

## Summary

HR Ally is an AI-powered assistant that gives employees a single conversational entry point for routine HR questions and requests. It runs in **Microsoft Teams** and on the **intranet web portal**, both on one shared back end.

**The problem.** Employees search through handbooks, policy documents, portals and emails to find answers to routine HR questions. They often don't know which information is current, which process applies or whom to contact. HR teams spend considerable time answering the same questions, and answers can vary depending on who handles them.

**The solution.** An employee types a question in everyday language. HR Ally identifies the intent, retrieves information from approved HR sources and replies with:

1. A concise answer based on an approved HR source
2. A reference or link to the relevant policy or handbook section
3. A suggested next step (form, portal or HR support channel)
4. A clarification question when essential details are missing
5. A safe escalation option when no reliable answer is available
6. A feedback option to say whether the answer helped

**Product principle.** HR Ally reduces repetitive work; it does not replace HR professionals. It gives guidance, never final HR decisions.

## Human-in-the-Loop Safeguards

- Sensitive matters (grievances, disciplinary concerns, employee relations, compensation decisions, policy exceptions) go directly to qualified HR staff, with no AI answer.
- Unclear or incomplete questions are clarified or escalated to HR.
- Employees review request details before anything is submitted to another system.
- Personal information is accessed only after identity and authorization checks.
- Approved HR content owners review and maintain the knowledge sources.
- Final decisions on recruitment, leave, compensation, benefits eligibility, performance and policy exceptions stay with authorized staff.

## Approach

- **Build vs buy:** uses an approved AI platform or API with retrieval over approved HR content (retrieval-augmented generation), not a custom-trained model.
- **Value focus:** authoritative content, guided workflows, access control, safe escalation and rigorous evaluation.
- **Release approach:** Prototype → Evaluate → Limited pilot → Later releases, each stage gated by success evidence.

## Success Evidence (proposed targets)

| # | Measure | Target |
| --- | --- | --- |
| SE-1 | Faster answers than the manual process | Faster than baseline |
| SE-2 | Answers backed by approved HR sources | ≥ 95% |
| SE-3 | Helpful and understandable rating | ≥ 4.0 / 5 |
| SE-4 | Fewer repetitive HR inquiries (pilot) | 20% reduction |
| SE-5 | Correct form, portal or channel reached | Higher than baseline |
| SE-6 | Fewer clarification exchanges | Lower than baseline |
| SE-7 | Unclear and sensitive questions safely escalated | ≥ 90%; zero sensitive answered by AI |
| SE-8 | Critical policy errors (HR review) | < 1% |

Targets are proposed and will be confirmed after baselining. All measures are reported separately for Teams and the intranet portal.
