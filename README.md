# SaaS Readiness Assessment

A reusable, structured assessment framework for evaluating SaaS products before market launch.

The framework supports evidence-based assessments of product functionality, security, privacy, potentially applicable compliance requirements, and operational readiness.

It is designed to work across different SaaS products rather than being limited to a specific technology stack or industry.

## Objectives

- Establish a repeatable pre-launch assessment process.
- Identify functional defects and potential security weaknesses.
- Evaluate behavior across user roles, permissions, and tenant boundaries.
- Review privacy practices and potentially applicable compliance requirements.
- Classify findings by severity, impact, and verification status.
- Produce structured test records, finding reports, and readiness assessments.
- Document untested areas, evidence gaps, limitations, and unresolved risks.
- Provide clear, evidence-based launch-readiness recommendations.

## Assessment Areas

| Area | Purpose |
|---|---|
| Product Discovery | Understand the product, its users, architecture, and assessment scope. |
| Security Assessment | Review authentication, authorization, data protection, configuration, and other applicable security controls. |
| Penetration Testing | Guide authorized security testing within an explicitly approved scope. |
| Functional Testing | Assess workflows, navigation, data consistency, permissions, and expected behavior. |
| Privacy Assessment | Review personal-data collection, use, retention, access, and disclosure. |
| Compliance Review | Identify potentially applicable obligations and assess available evidence without assuming compliance. |
| Operational Readiness | Review monitoring, logging, backup and recovery, deployment, and incident response. |
| Launch Readiness | Summarize findings, evidence gaps, unresolved risks, and conditions for launch consideration. |

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
│   ├── severity-classification.md
│   └── operational-readiness.md
├── assets/
│   ├── test-case-template.md
│   ├── vulnerability-report-template.md
│   └── final-assessment-template.md
└── tests/
    └── test-scenarios.md