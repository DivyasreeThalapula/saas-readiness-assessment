# Severity Classification

## 1. Purpose

This document defines a consistent method for classifying and prioritizing findings discovered during SaaS product assessments.

It applies to security vulnerabilities, functional defects, privacy concerns, compliance gaps, and launch-readiness issues.

Severity should reflect the potential impact and the circumstances in which the issue occurs. It should not be based solely on how easy a bug is to reproduce or how noticeable it appears.

## 2. Classification Principles

When assigning severity:

- Consider the potential impact on users, the organization, and the product.
- Consider how easily the issue can be triggered or exploited.
- Consider the privileges required to reproduce the issue.
- Consider the number and type of users potentially affected.
- Consider whether sensitive data, financial transactions, or critical workflows are involved.
- Consider whether the issue affects multiple tenants.
- Consider whether an effective workaround exists.
- Record uncertainty when impact or exploitability has not been established.
- Use evidence rather than assumptions.
- Escalate potentially critical issues promptly.

Severity is a prioritization aid. It does not replace specialist security analysis, formal vulnerability scoring, or applicable incident-response procedures.

## 3. Severity Levels

### Critical

An issue with the potential for catastrophic impact, widespread compromise, or a fundamental failure of an essential security boundary.

Examples may include:

- Unauthenticated access to highly sensitive data at significant scale.
- A demonstrated cross-tenant compromise affecting many customers.
- Remote exploitation that provides extensive control over production systems.
- A critical authorization failure that enables widespread compromise of accounts or data.

These examples are illustrative. A finding should not be classified as Critical merely because it resembles an example; the actual evidence and context must support the rating.

Recommended response: Escalate immediately to the responsible security and engineering teams. Pause the affected launch or functionality when the risk warrants it. Do not launch with an unresolved Critical issue unless an explicitly authorized risk decision and appropriate safeguards have been established.

### High

An issue with substantial potential impact on confidentiality, integrity, availability, important business operations, or user trust.

Examples may include:

- Unauthorized access to another user's sensitive information.
- A confirmed privilege-escalation vulnerability.
- A security weakness that enables unauthorized changes to important records.
- A major authentication or authorization failure.
- A payment workflow that incorrectly confirms a transaction and creates a material business risk.

Recommended response: Prioritize remediation before launch. Escalate to the responsible team and require documented review before accepting any residual risk.

### Medium

An issue with meaningful but more limited impact, or an issue whose exploitation depends on additional conditions.

Examples may include:

- A restricted workflow that fails in a way that affects a subset of users.
- Exposure of limited non-public information with constrained impact.
- An important feature that fails under a specific, reproducible condition.
- Inadequate validation that creates a demonstrated but limited risk.
- A privacy or compliance control that needs improvement and does not currently demonstrate a more severe impact.

Recommended response: Assign an owner and remediation target. Determine whether the issue must be resolved before launch based on its context and applicable requirements.

### Low

An issue with limited impact that does not materially compromise security, privacy, essential functionality, or business operations.

Examples may include:

- A minor validation inconsistency with a safe outcome.
- A non-critical interface behavior that causes limited user inconvenience.
- A recoverable error in a secondary workflow.
- A minor documentation or configuration improvement.

Recommended response: Record the issue, assign an appropriate owner, and schedule remediation according to its impact and the team's priorities.

### Informational

An observation, improvement opportunity, or documentation gap that does not currently demonstrate a direct adverse impact.

Examples may include:

- A recommended security-hardening improvement.
- A documentation clarification.
- A defense-in-depth suggestion.
- An improvement to monitoring or assessment coverage.

Recommended response: Document the observation and decide whether further investigation or improvement is appropriate.

An observation should not be classified as Informational simply because its impact has not yet been investigated.

## 4. Impact Assessment

Consider the following dimensions when assessing impact.

### Confidentiality

Could the issue expose information to someone who should not have access?

Consider the sensitivity, quantity, and ownership of the affected information.

### Integrity

Could the issue allow unauthorized changes, deletion, or falsification of data?

Consider whether the affected records are important to users, finances, access permissions, or business operations.

### Availability

Could the issue prevent users from accessing the product or completing important tasks?

Consider the duration, scope, and recoverability of the disruption.

### Authentication and Authorization

Could the issue allow a person to impersonate another user, bypass login, gain additional privileges, or access restricted functionality?

### Privacy and Compliance

Could the issue result in inappropriate collection, use, disclosure, retention, or deletion of personal information, or indicate a significant gap against an applicable requirement?

### Business and User Impact

Could the issue cause financial loss, operational disruption, loss of user trust, or an inability to complete a critical workflow?

## 5. Exploitability and Exposure

When relevant, consider:

- Whether authentication is required.
- Whether special privileges are required.
- Whether user interaction is required.
- Whether the issue is reachable through a public interface.
- Whether the issue can be reproduced reliably.
- Whether multiple conditions must occur together.
- Whether a documented and effective mitigation exists.
- Whether the issue affects one account, one tenant, or multiple tenants.

Do not assume that a vulnerability is exploitable merely because a theoretical attack is possible. Record the evidence supporting any exploitability claim.

## 6. Functional and User-Experience Defects

Functional issues should be prioritized according to their actual consequences.

Consider:

- Whether a critical user journey is blocked.
- Whether data can be lost or corrupted.
- Whether users receive incorrect information.
- Whether the issue affects administrators or ordinary users.
- Whether a safe workaround exists.
- How frequently the issue occurs.
- How many users or tenants may be affected.

A visual defect may be Low, while a seemingly small navigation defect that exposes another user's private dashboard could be High or Critical depending on the evidence and impact.

Do not assign severity based only on the appearance of the defect.

## 7. Privacy and Compliance Findings

Consider:

- The sensitivity of the information involved.
- The number of individuals potentially affected.
- Whether information is exposed to unauthorized parties.
- Whether the requirement actually applies.
- The potential consequences of the gap.
- Whether a legal, privacy, or compliance specialist must review it.

A missing policy document does not automatically establish a legal violation.

When applicability or legal significance is uncertain, use an appropriate provisional rating and document the need for specialist review.

## 8. Severity Assignment Procedure

For each finding:

1. Describe the observed behavior or condition.
2. Record the evidence and reproduction steps.
3. Identify the affected users, data, features, or systems.
4. Assess the potential confidentiality, integrity, availability, privacy, and business impacts.
5. Consider the conditions required for the issue to occur.
6. Determine whether an effective mitigation exists.
7. Assign a provisional severity based on the evidence.
8. Record any assumptions or unresolved questions.
9. Escalate potentially Critical or High findings.
10. Reassess severity if additional evidence changes the understanding of the risk.

Where the available information is insufficient, record that limitation rather than presenting an uncertain rating as definitive.

## 9. Severity Versus Priority

Severity and remediation priority are related but different.

- Severity describes the potential impact of the finding.
- Priority describes how urgently the organization should address it.

Priority may also depend on launch dates, exposure, contractual commitments, regulatory obligations, dependencies, and available mitigations.

A lower-severity issue may still require immediate action because of a specific launch requirement or business constraint.

A high-severity issue should not be downgraded solely because remediation is inconvenient or expensive.

## 10. Finding Record

Each finding should include:

- Finding ID.
- Title.
- Finding category.
- Affected component or workflow.
- Description.
- Evidence.
- Reproduction steps, where applicable.
- Expected behavior.
- Actual behavior.
- Potential impact.
- Exploitability or occurrence conditions, where relevant.
- Severity.
- Confidence in the assessment.
- Recommended remediation.
- Workaround or mitigation, if verified.
- Responsible owner, if known.
- Status.
- Retest outcome.

Keep observed facts separate from assumptions and recommendations.

## 11. Retesting and Closure

After a fix is reported:

- Repeat the original test using an authorized environment.
- Confirm whether the reported behavior has changed.
- Check relevant related workflows.
- Record the retest evidence and date.
- Update the finding status.
- Reassess severity if the remaining risk has changed.

A finding should not be marked Resolved solely because a developer reports that a fix has been implemented.

If retesting is unavailable, record the finding as awaiting verification rather than claiming it has been resolved.

## 12. Risk Acceptance

If an issue remains unresolved, document:

- The remaining risk.
- The reason remediation is deferred.
- Any available mitigations.
- The person or team authorized to accept the risk.
- The duration or conditions of acceptance.
- The planned remediation or review date.

Risk acceptance must follow the organization's authorization process and applicable obligations.

An assessment report does not itself authorize the acceptance of risk.

## 13. Important Limitations

- These levels provide a common starting point, not a formal vulnerability-scoring standard.
- Security teams may use CVSS or another established method when appropriate.
- Formal regulatory or contractual requirements may impose separate obligations.
- Severity should be reassessed when meaningful new evidence becomes available.
- A product should not be declared safe for launch solely because no Critical findings were identified.
- Untested areas and assessment limitations must remain visible in the final report.