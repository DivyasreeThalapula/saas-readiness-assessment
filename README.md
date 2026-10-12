# SaaS Readiness Assessment

A reusable, structured assessment framework for evaluating SaaS products before market launch.

The framework helps assess product functionality, security, privacy, compliance considerations, and operational readiness through a consistent, evidence-based process.

It is designed to work across different SaaS products rather than being limited to a specific technology stack or industry.

## Objectives

- Establish a repeatable pre-launch assessment process.
- Identify functional defects and security weaknesses.
- Evaluate behavior across different user roles and permissions.
- Review privacy and potentially applicable compliance requirements.
- Classify findings by severity and potential impact.
- Produce structured findings and launch-readiness reports.
- Document untested areas, limitations, and unresolved risks.

## Assessment Areas

| Area | Purpose |
|---|---|
| Product Discovery | Understand the product, its users, architecture, and scope. |
| Security Assessment | Review authentication, authorization, data protection, configuration, and other security controls. |
| Penetration Testing | Guide authorized testing of potential vulnerabilities within an explicitly approved scope. |
| Functional Testing | Verify features, workflows, navigation, data consistency, and role-based behavior. |
| Privacy Assessment | Review personal-data collection, use, retention, and disclosure. |
| Compliance Review | Identify potentially applicable obligations and assess available evidence. |
| Operational Readiness | Review monitoring, recovery, deployment, and incident-response preparations. |
| Launch Readiness | Summarize findings, outstanding risks, and conditions for launch consideration. |

## Repository Structure

```text
saas-readiness-assessment/
├── SKILL.md
├── README.md
├── references/
│   ├── assessment-methodology.md
│   ├── security-testing.md
│   ├── functional-testing.md
│   ├── compliance-assessment.md
│   └── severity-classification.md
└── assets/
    ├── test-case-template.md
    ├── vulnerability-report-template.md
    └── final-assessment-template.md