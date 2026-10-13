# SaaS Product Readiness Assessment Report

## 1. Executive Summary

- Product Name:
- Product Version or Release:
- Assessment Date:
- Assessment Environment:
- Assessment Period:
- Assessment Scope:
- Overall Assessment Status:

### Summary

Provide a concise summary of the assessment, major findings, important limitations, and recommended next steps.

## 2. Assessment Scope

### Included

List the features, components, workflows, user roles, and controls assessed.

### Excluded

List areas that were outside the authorized scope.

### Environments and Access

Describe the environment and the access available during testing.

Do not include credentials or secrets.

## 3. Assessment Coverage

| Assessment Area | Status | Coverage Notes |
|---|---|---|
| Product Discovery | Not Assessed | |
| Authentication | Not Assessed | |
| Authorization and Roles | Not Assessed | |
| Security Testing | Not Assessed | |
| Functional Testing | Not Assessed | |
| Privacy Assessment | Not Assessed | |
| Compliance Review | Not Assessed | |
| Operational Readiness | Not Assessed | |
| Launch Readiness | Not Assessed | |

Use accurate statuses such as Assessed, Partially Assessed, Not Assessed, or Not Applicable.

Do not infer coverage from the existence of documentation alone.

## 4. Findings Summary

| Severity | Confirmed Findings | Unverified Findings |
|---|---:|---:|
| Critical | 0 | 0 |
| High | 0 | 0 |
| Medium | 0 | 0 |
| Low | 0 | 0 |
| Informational | 0 | 0 |

Update the counts from the assessment records. Keep provisional severity
separate from verification status.

Count each finding once per applicable reporting category. Do not count
unverified findings as confirmed vulnerabilities.

## 5. Critical and High-Priority Findings

For each relevant finding, include:

- Finding ID and title.
- Affected component.
- Observed behavior.
- Evidence.
- Potential impact.
- Severity and justification.
- Recommended remediation.
- Current status.

If no such findings were identified, state that explicitly while clarifying the assessment scope and limitations.

## 6. Functional Testing Results

Summarize:

- Important workflows tested.
- Roles tested.
- Confirmed functional defects.
- Data consistency issues.
- Navigation or usability issues affecting important workflows.
- Unimplemented or unavailable features.
- Important tests that remain incomplete.

## 7. Security Assessment Results

Summarize:

- Security areas assessed.
- Confirmed vulnerabilities and potential weaknesses.
- Authentication and authorization results.
- Tenant isolation results, where applicable.
- Data exposure and input-validation findings.
- Configuration and dependency review results.
- Areas not tested or requiring specialist review.

Clearly distinguish tested controls from controls that were not verified.

## 8. Privacy and Compliance Results

Summarize:

- Relevant data categories and processing activities.
- Potentially applicable requirements.
- Evidence reviewed.
- Privacy and data protection findings.
- Missing documentation or controls.
- Questions requiring legal or compliance review.

Do not claim legal compliance or certification without appropriate evidence and review.

## 9. Operational Readiness

Assess applicable areas such as:

- Monitoring and alerting.
- Error handling and logging.
- Backup and recovery.
- Performance and scalability.
- Deployment and rollback.
- Incident response.
- Support and escalation procedures.
- External service dependencies.

Record whether each area was verified, partially assessed, or not assessed.

## 10. Launch Blockers and Required Actions

| ID | Issue or Action | Severity | Required Action | Owner | Status |
|---|---|---|---|---|---|
| | | | | | |

List issues that should be resolved before launch and explain the reason.

Distinguish mandatory requirements from recommendations.

## 11. Recommended Next Steps

Prioritize remediation and verification activities.

For each action, include:

- Recommended action.
- Reason.
- Priority.
- Suggested responsible team, if known.
- Required verification.

Do not invent owners or completion dates.

## 12. Limitations and Unverified Areas

Document:

- Features that were unavailable.
- Tests that could not be performed.
- Missing access or evidence.
- Environmental constraints.
- Third-party systems not assessed.
- Compliance questions requiring specialist review.
- Any other limitation that affects confidence in the assessment.

## 13. Overall Assessment

### Report Status

Choose one:

- Draft: The report is still being prepared.
- Ready for Review: The report is ready for stakeholder review.

### Overall Readiness Outcome

Choose exactly one:

- Ready for Launch Consideration: Sufficient evidence supports the agreed
  assessment scope, mandatory criteria are met, and no unresolved blocking
  issues have been identified. This is not launch approval.
- Conditionally Ready: Outstanding issues or residual risks remain, and
  documented conditions have been identified for stakeholder review.
- Not Ready: A confirmed blocking issue or unmet mandatory requirement
  prevents a positive readiness outcome.
- Insufficient Evidence: Available evidence is insufficient to determine
  readiness reliably.

### Decision Rationale

Explain the selected readiness outcome using assessment evidence,
unresolved findings, agreed launch criteria, and limitations.

A confirmed unresolved Critical finding results in Not Ready. Evaluate
unresolved High findings against their impact, exposure, and agreed criteria.

Untested high-risk areas prevent an unqualified positive readiness outcome.
Missing mandatory evidence normally results in Insufficient Evidence,
unless a confirmed blocking issue independently requires Not Ready.

A developer's statement that an issue is fixed does not establish resolution.
Retesting and sufficient evidence are required before marking it Resolved.

### Required Conditions

List outstanding actions, verification activities, and stakeholder decisions
required before launch consideration.

### Risk Acceptance

Document formally accepted residual risks, including the authorized
decision-maker and applicable conditions, if known.

An assessment recommendation does not itself authorize a launch or accept
organizational risk.

## 14. Final Disclaimer

This report reflects the evidence available within the documented assessment scope and period.

It does not guarantee that all defects or vulnerabilities have been identified, that the product is completely secure, or that every legal and regulatory obligation has been satisfied.