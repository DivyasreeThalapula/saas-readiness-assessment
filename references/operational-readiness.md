# Operational Readiness Assessment

## 1. Purpose

This document defines a repeatable process for evaluating the operational
readiness of SaaS products before launch.

Adapt the assessment to the product's architecture, hosting environment,
critical workflows, business requirements, and operational risks.

Do not assume that every product uses the same infrastructure or services.

## 2. Assessment Principles

- Obtain authorization before performing operational tests.
- Prefer staging environments and synthetic data.
- Distinguish documented procedures from verified capabilities.
- Record evidence for each assessed control.
- Do not claim that a control works merely because documentation exists.
- Avoid disruptive testing unless specifically authorized.
- Identify untested areas and operational dependencies.
- Leave formal risk acceptance and launch approval to authorized stakeholders.

## 3. Operational Assessment Areas

### 3.1 Monitoring and Alerting

Check whether applicable monitoring covers:

- Application availability.
- Application errors and failures.
- Resource utilization.
- Critical background jobs.
- External service dependencies.
- Security-relevant events.

Record whether monitoring is documented, configured, and verified.

Do not trigger production incidents merely to test alerting without authorization.

### 3.2 Logging and Error Handling

Evaluate whether:

- Important application events are logged.
- Errors provide sufficient diagnostic information.
- Logs avoid unnecessary personal information and secrets.
- Access to logs is appropriately restricted.
- Log retention and access procedures are documented.
- Unexpected errors are handled without exposing sensitive details.

Record the evidence reviewed and any limitations.

### 3.3 Backup and Recovery

Assess whether:

- Backup requirements are documented.
- Backup schedules and retention are defined where applicable.
- Backup access is appropriately restricted.
- Backup completion is monitored where applicable.
- Recovery procedures are documented.
- Recovery objectives are defined where required.
- Restoration has been tested in an authorized environment.

Distinguish carefully between these states:

- Documented: A procedure or configuration is described in available evidence.
- Configured: Evidence indicates the relevant configuration exists.
- Tested: The procedure was executed and its result was recorded.
- Verified: Sufficient evidence supports the expected outcome.

A documented backup process does not prove that data can be restored.
A successful backup does not prove that recovery works.

### 3.4 Deployment and Rollback

Review applicable controls for:

- Deployment procedures.
- Environment configuration.
- Secrets management.
- Release verification.
- Rollback or recovery procedures.
- Database migration safety.
- Separation between development, staging, and production.

Do not execute deployments, migrations, or rollback procedures without explicit
authorization for the target environment and activity.

### 3.5 Incident Response

Determine whether the organization has applicable procedures for:

- Detecting and reporting incidents.
- Escalating serious issues.
- Assigning incident responsibilities.
- Containing and investigating incidents.
- Communicating with affected stakeholders.
- Recovering services.
- Recording lessons learned.

Distinguish between a documented response plan and a response process that
has been exercised.

Do not claim that incident response is effective solely because a policy exists.

### 3.6 Availability and Performance

Where relevant, review:

- Availability requirements.
- Performance expectations.
- Existing load or performance test results.
- Known capacity limits.
- Rate limits and resource controls.
- Dependencies that could affect service availability.
- Documented scaling and recovery strategies.

Do not conduct load, stress, or denial-of-service testing without explicit
authorization covering the specific activity, environment, and limits.

If performance testing has not been performed, record it as Not Tested.

### 3.7 External Dependencies

Identify relevant dependencies, such as:

- Authentication providers.
- Payment services.
- Email or messaging providers.
- File storage.
- Databases.
- Monitoring services.
- Third-party APIs.

Review applicable failure handling, configuration, access controls, and
documented recovery arrangements.

Do not claim that an external service has been assessed when only its
documentation has been reviewed.

### 3.8 Support and Escalation

Where applicable, determine whether:

- Users have a documented support channel.
- Serious issues have an escalation path.
- Responsibilities are assigned.
- Support procedures cover critical workflows.
- Operational ownership is known.

Do not invent owners, response times, or service-level commitments.

## 4. Evidence and Status Recording

For each applicable check, record:

- Check ID.
- Assessment area.
- Objective.
- Evidence source.
- Procedure performed or proposed.
- Expected outcome.
- Actual outcome.
- Test status.
- Verification status.
- Limitations.
- Recommended actions.
- Responsible owner, if known.

Use these test statuses:

- Pass: Sufficient evidence demonstrates that the expected outcome was met.
- Fail: Sufficient evidence demonstrates that the expected outcome was not met.
- Needs Investigation: Evidence is insufficient to determine the outcome.
- Not Tested: The check has not been executed.
- Not Applicable: The check does not apply, with a documented reason.

Do not mark a check Pass solely because a procedure is documented.

For example, if backup instructions exist but restoration has not been tested,
record the documentation as reviewed and restoration as Not Tested.

## 5. Operational Findings

For each operational weakness, document:

- Finding ID and title.
- Affected service or process.
- Observed condition.
- Evidence and evidence source.
- Potential impact.
- Severity and justification.
- Recommended remediation.
- Responsible owner, if known.
- Verification status.
- Retest requirements.

Distinguish confirmed failures from missing evidence and suspected weaknesses.

## 6. Launch Readiness Considerations

Evaluate operational findings alongside security, functional, privacy, and
compliance results.

Consider:

- Whether critical operational controls have been verified.
- Whether recovery requirements are met.
- Whether serious single points of failure remain.
- Whether required monitoring and escalation are available.
- Whether important dependencies have appropriate failure handling.
- Whether operational acceptance criteria have been met.
- Whether significant operational risks remain unverified.

Do not declare a product operationally ready based only on documentation.

Untested high-risk controls must remain visible in the overall assessment.

Apply the readiness decision rules in `SKILL.md` and
`assessment-methodology.md`.

## 7. Limitations

- The absence of evidence does not prove that a control is absent.
- Documentation review is not equivalent to operational testing.
- A limited assessment cannot guarantee availability or recoverability.
- Third-party services may remain outside the authorized scope.
- Formal launch approval and risk acceptance belong to authorized stakeholders.