---
name: saas-readiness-assessment
description: Assess SaaS products before launch through authorized security testing, functional and role-based testing, privacy and compliance reviews, operational readiness checks, and evidence-based reporting. Use when planning or conducting a pre-launch SaaS assessment, evaluating product readiness, documenting defects or vulnerabilities, or preparing a launch-readiness report.
---

# SaaS Readiness Assessment

## 1. Purpose

Guide a structured, repeatable assessment of a SaaS product before market launch.

The assessment should identify functional defects, security weaknesses, privacy concerns, potentially applicable compliance gaps, and operational risks.

Produce evidence-based findings and a final readiness report that helps responsible stakeholders make informed decisions.

The methodology must be adaptable to different SaaS products, industries, architectures, and technology stacks.

Do not assume that the product is an LMS or that any particular feature, role, integration, or compliance obligation exists.

## 2. Core Principles

Follow these principles throughout every assessment:

- Evidence first: Distinguish observed facts, assumptions, hypotheses, and recommendations.
- Authorization first: Do not perform testing outside the explicitly approved scope.
- Product independence: Adapt the methodology to the product rather than assuming a particular architecture.
- Risk-based assessment: Prioritize checks according to potential impact and exposure.
- Honest reporting: Never claim a test was performed if it was not.
- Explicit uncertainty: Record missing evidence and unverified areas.
- Data protection: Avoid unnecessary access to personal, sensitive, or confidential information.
- Actionable findings: Provide clear reproduction steps and recommendations when supported by evidence.
- Human accountability: Leave launch approval, formal risk acceptance, and legal determinations to authorized stakeholders.

## 3. Required Workflow

Follow the stages below in order. Adapt the depth of each stage to the product, scope, and available evidence.

### Stage 1: Understand the Product

Collect or ask for the information needed to plan the assessment.

Identify:

- Product name and purpose.
- Product version or release, if known.
- Intended users and user roles.
- Main features and critical user journeys.
- Technology stack and architecture, if available.
- Authentication and authorization mechanisms, if known.
- Data categories processed.
- Third-party integrations.
- Deployment environment.
- Intended launch date, if relevant.
- Applicable organizational requirements.

Do not invent missing information.

If information is unavailable, record the gap and continue only where it is safe and reasonable to do so.

### Stage 2: Establish Authorization and Scope

Before testing, establish:

- The system and environment being assessed.
- The person or organization authorizing the work.
- The permitted accounts and roles.
- The allowed testing methods.
- Any excluded components or activities.
- The permitted testing window, if applicable.
- Restrictions on data access and handling.
- Whether automated tools are permitted.
- Whether destructive or state-changing tests are permitted.
- The escalation contact for serious findings, if known.

Prefer staging environments, test accounts, and synthetic data.

If authorization or scope is unclear, do not begin intrusive testing. Ask for clarification and offer safe planning or documentation work in the meantime.

### Stage 3: Create the Assessment Plan

Use the product information and approved scope to build a tailored checklist.

Select applicable checks from:

- Security assessment.
- Authorized penetration testing.
- Functional testing.
- Role-based access testing.
- Privacy assessment.
- Compliance review.
- Operational readiness.
- Launch readiness.

For each planned check, specify:

- Check ID.
- Assessment area.
- Objective.
- Preconditions.
- Required role or permissions.
- Procedure.
- Expected outcome.
- Evidence to collect.
- Risk addressed.
- Status.

Use the test case template in `assets/test-case-template.md`.

Exclude irrelevant checks or mark them Not Applicable with a reason.

Identify critical workflows and high-impact risks first.

### Stage 4: Conduct or Guide the Assessment

Use the appropriate reference documents:

- `references/security-testing.md`
- `references/functional-testing.md`
- `references/compliance-assessment.md`
- `references/assessment-methodology.md`

Use `references/severity-classification.md` to prioritize findings.

When available tools and permissions support it, perform suitable checks and record their actual results.

When execution is not possible, provide a proposed procedure and label it as Not Tested until evidence confirms the outcome.

Do not imply that reviewing a checklist is equivalent to executing its tests.

#### Security Assessment

Evaluate applicable areas such as:

- Authentication and session management.
- Authorization and privilege boundaries.
- Tenant isolation.
- API access controls.
- Input validation.
- Data exposure.
- File handling.
- Security configuration.
- Dependency and secret management.
- Logging and monitoring.

#### Authorized Penetration Testing

Only guide or perform penetration testing within the approved scope.

Start with low-impact verification and increase testing depth only when permitted and justified.

Do not perform destructive tests, denial-of-service testing, uncontrolled exploitation, persistence, or real data extraction without explicit authorization for the specific activity.

Use non-destructive proof where possible.

Stop and escalate if testing reveals a potentially serious vulnerability that could expose sensitive data, compromise accounts, or disrupt service.

#### Functional and Role-Based Testing

Verify applicable user journeys, forms, navigation, data persistence, error handling, and feature behavior.

Test each relevant role against its intended permissions.

For multi-tenant products, assess tenant isolation only within the approved scope.

Record the expected and actual behavior rather than guessing the root cause.

#### Privacy and Compliance

Identify potentially applicable requirements and examine the available evidence.

Record missing documentation, questionable practices, and controls that require further verification.

Do not declare legal compliance, certification, or regulatory violations without adequate evidence and appropriate expertise.

#### Operational Readiness

Where relevant, review monitoring, error handling, backups, recovery, deployment, rollback, incident response, support, and external dependencies.

Distinguish documented procedures from procedures that have actually been tested.

### Stage 5: Record Findings

For every failed check or concerning observation:

1. Assign a unique finding ID.
2. Write a concise, factual title.
3. Describe the observed behavior.
4. Record the environment and affected component.
5. Include reproducible steps where applicable.
6. State the expected and actual results.
7. Attach or reference relevant evidence.
8. Explain demonstrated and potential impact separately.
9. Assign a provisional severity with justification.
10. Recommend a corrective action.
11. Record limitations and unresolved questions.

Use `assets/vulnerability-report-template.md` for security findings.

Use `assets/test-case-template.md` for test execution records.

Do not report speculative vulnerabilities as confirmed findings.

If evidence is insufficient, use Needs Investigation.

### Stage 6: Classify and Prioritize Findings

Apply the severity levels in `references/severity-classification.md`.

Use:

- Critical
- High
- Medium
- Low
- Informational
- Pending Assessment

Base severity on evidence, potential impact, exposure, and relevant circumstances.

Keep severity separate from remediation priority.

Escalate potentially Critical or High findings promptly to the appropriate responsible team.

Do not lower a finding's severity merely because it is inconvenient to fix.

### Stage 7: Evaluate Launch Readiness

Review the complete assessment record.

Consider:

- Critical and High findings.
- Important unresolved functional defects.
- Authentication and authorization weaknesses.
- Privacy and compliance concerns.
- Operational preparedness.
- Unverified high-risk areas.
- Applicable launch requirements.
- Residual risks and documented mitigations.

Identify which issues should be resolved before launch and which require stakeholder review.

Do not use a simple count of passing tests as proof that a product is ready.

Do not independently authorize a launch or accept organizational risk.

### Stage 8: Generate the Final Report

Use `assets/final-assessment-template.md`.

Include:

- Executive summary.
- Assessment scope and environment.
- Assessment coverage.
- Findings summary.
- Critical and High-priority findings.
- Functional testing results.
- Security assessment results.
- Privacy and compliance results.
- Operational readiness.
- Launch blockers and required actions.
- Recommended next steps.
- Limitations and unverified areas.
- Overall assessment status and rationale.

Choose an overall status based on the evidence:

- Ready for Review.
- Ready for Launch Consideration.
- Conditionally Ready.
- Not Ready.
- Insufficient Evidence.

Explain the selected status and any outstanding conditions.

A report marked Ready for Review is not a launch approval.

## 4. Test Statuses

Use consistent test statuses:

- Pass: The observed result matches the expected result.
- Fail: The observed result differs from the expected result.
- Needs Investigation: Evidence is insufficient to determine the outcome.
- Not Tested: The check has not been executed.
- Not Applicable: The check does not apply, with a documented reason.

Never convert a proposed test into a passing result without executing it and evaluating the evidence.

## 5. Reference Loading Rules

Use progressive disclosure. Read only the supporting material required for the current task.

- For overall workflow planning, consult `references/assessment-methodology.md`.
- For security checks, consult `references/security-testing.md`.
- For feature and permission checks, consult `references/functional-testing.md`.
- For privacy and regulatory considerations, consult `references/compliance-assessment.md`.
- For severity decisions, consult `references/severity-classification.md`.
- For individual test records, use `assets/test-case-template.md`.
- For security finding reports, use `assets/vulnerability-report-template.md`.
- For the final readiness report, use `assets/final-assessment-template.md`.

Do not reproduce every reference document in every response.

Summarize the relevant instructions and use the templates where appropriate.

## 6. Tool and Automation Rules

Use only tools that are actually available in the current environment.

Before running a tool:

- Confirm that the action is within the authorized scope.
- Understand whether it can modify data or affect service availability.
- Check the tool's permissions and configuration.
- Avoid exposing secrets in commands, output, or reports.
- Prefer read-only checks when they can answer the question.

If a scanner, browser, terminal, API client, or other testing tool is unavailable, do not pretend to have used it.

Instead, provide an appropriate manual procedure or state that the check could not be performed.

Automation output must be reviewed for relevance, false positives, and limitations.

## 7. Output Expectations

Adapt the output to the user's immediate request.

For a planning request, provide:

- Scope questions.
- Proposed assessment areas.
- Test plan.
- Required access and tools.
- Safety constraints.

For a testing request, provide:

- Test objective.
- Preconditions.
- Steps performed or proposed.
- Expected and actual outcomes.
- Evidence.
- Status.
- Limitations.

For a finding, provide:

- Finding ID and title.
- Category.
- Evidence.
- Impact.
- Severity and justification.
- Recommended remediation.
- Retest status.

For a final assessment, use the final assessment template.

Keep findings concise, factual, and actionable. Clearly distinguish completed work from suggested next steps.

## 8. Final Safety and Quality Checks

Before presenting an assessment:

- Confirm that the scope and limitations are documented.
- Check that test statuses match the available evidence.
- Check that finding severity has a justification.
- Verify that recommendations address the described issue.
- Remove credentials, access tokens, and unnecessary personal information.
- Identify untested areas and unresolved uncertainties.
- Confirm that compliance claims are appropriately qualified.
- Ensure the overall readiness status follows from the findings and limitations.

The goal is to produce a repeatable, useful, and defensible assessment—not an unsupported guarantee of security or launch readiness.