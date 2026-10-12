# SaaS Security Assessment Checklist

## 1. Purpose

This document defines a reusable checklist for assessing the security of SaaS applications.

It helps identify potential security weaknesses in application functionality, access controls, APIs, data handling, configurations, and supporting infrastructure.

The checklist should be adapted to the product's architecture, technology stack, features, and risk profile.

## 2. Prerequisites

Before beginning the assessment:

- Confirm authorization to assess the application.
- Identify the approved application URLs, APIs, repositories, and environments.
- Understand the application's architecture and user roles.
- Obtain test accounts with appropriate permissions.
- Prefer a staging environment and synthetic data.
- Identify prohibited tests and activities that could disrupt services.
- Determine how findings and supporting evidence should be stored.

Do not proceed with testing that falls outside the authorized scope.

## 3. Authentication and Session Management

### What to Check

- Login and logout behavior.
- Password requirements and password-reset workflows.
- Multi-factor authentication, where supported.
- Session creation, expiration, and invalidation.
- Protection against unauthorized account access.
- Authentication error messages and account-recovery behavior.

### How to Check

- Test valid and invalid login scenarios using authorized test accounts.
- Verify that logging out invalidates the relevant session.
- Check whether expired sessions can still access protected resources.
- Review password-reset tokens for appropriate expiration and single-use behavior.
- Verify that MFA is enforced where required by the product's security policy.
- Review authentication implementation in the code, where authorized.

### Evidence to Record

- Affected authentication workflow.
- Steps to reproduce the issue.
- Expected and actual behavior.
- Relevant sanitized screenshots, responses, or code references.

## 4. Authorization and Access Control

### What to Check

- Role-based permissions.
- Access to administrative functionality.
- Access to other users' records.
- Access to tenant-specific resources in multi-tenant applications.
- Server-side enforcement of permissions.
- Restrictions on unauthorized actions.

### How to Check

- Identify the roles and permissions defined by the application.
- Test each role against its permitted and prohibited actions.
- Attempt to access authorized test resources belonging to another test user.
- Verify that protected API endpoints enforce permissions independently of the frontend.
- Check whether users can perform restricted actions by modifying requests.
- For multi-tenant applications, verify that tenant boundaries are enforced server-side.

### Evidence to Record

- The affected roles, users, or tenants.
- The resource or action involved.
- Expected and actual authorization behavior.
- Sanitized evidence demonstrating the issue.

## 5. API Security

### What to Check

- Authentication requirements for protected endpoints.
- Authorization at the endpoint and resource levels.
- Input validation.
- Sensitive information in responses.
- Rate limiting where appropriate.
- Error handling and response consistency.
- CORS and other relevant browser security configurations.

### How to Check

- Review available API documentation and endpoint definitions.
- Test protected endpoints with authorized and unauthorized test accounts.
- Submit valid, invalid, missing, and unexpected input values.
- Check whether responses expose secrets or unnecessary personal information.
- Review rate limits and abuse protections where applicable.
- Inspect API middleware and authorization logic in the code, where authorized.

### Evidence to Record

- Endpoint and HTTP method.
- Relevant request and response details, with secrets removed.
- Expected and actual behavior.
- Reproduction steps and potential impact.

## 6. Data Protection and Privacy

### What to Check

- Exposure of sensitive information.
- Protection of data in transit.
- Secure handling of stored sensitive data.
- Access restrictions for personal and confidential information.
- Data retention and deletion behavior.
- Sensitive information in logs, URLs, and error messages.

### How to Check

- Review the types of data collected, processed, and stored.
- Verify that protected information is accessible only to authorized users.
- Review transport security and relevant storage protections.
- Examine logs and error responses for exposed secrets or personal information.
- Review data deletion and retention controls where applicable.
- Inspect relevant configuration and code, where authorized.

### Evidence to Record

- Data type and affected component.
- Observed exposure or protection weakness.
- Potential impact.
- Sanitized evidence and remediation recommendations.

## 7. Input Validation and Injection Risks

### What to Check

- Validation of user-supplied input.
- Protection against SQL and NoSQL injection.
- Cross-site scripting (XSS) risks.
- Unsafe file uploads.
- Path traversal and other relevant input-handling weaknesses.
- Safe handling of unexpected input.

### How to Check

- Identify input fields, query parameters, request bodies, and file-upload features.
- Review input validation and output encoding.
- Inspect database queries for unsafe construction.
- Use safe, non-destructive test inputs within the authorized scope.
- Verify that uploaded files are subject to appropriate validation and access restrictions.
- Review relevant framework protections and code.

### Evidence to Record

- Input location and affected functionality.
- Test conditions and observed behavior.
- Evidence supporting the finding.
- Potential impact and recommended remediation.

## 8. Security Configuration

### What to Check

- Security-related HTTP headers.
- HTTPS configuration.
- Cookie security attributes.
- CORS configuration.
- Debug mode and exposed development interfaces.
- Default credentials and unnecessary exposed services.
- Error messages that reveal internal implementation details.

### How to Check

- Inspect HTTP responses and browser security settings.
- Review cookie attributes, including Secure, HttpOnly, and SameSite where appropriate.
- Check whether production configuration exposes debugging information.
- Review deployment configuration and exposed services within the authorized scope.
- Compare relevant settings against documented security requirements.

### Evidence to Record

- Affected setting or component.
- Observed configuration.
- Expected configuration.
- Potential impact and recommended correction.

## 9. Dependencies and Secrets Management

### What to Check

- Known vulnerabilities in dependencies.
- Outdated packages and unsupported software.
- Hardcoded credentials, tokens, and API keys.
- Accidental exposure of secrets in source control.
- Dependency update and patching practices.
- Security of environment-variable handling.

### How to Check

- Review dependency manifests and lockfiles.
- Use appropriate dependency-scanning tools where available.
- Inspect authorized source code for accidentally committed secrets.
- Review secret-management practices and environment configuration.
- Verify findings before treating them as confirmed vulnerabilities.

### Evidence to Record

- Affected dependency, file, or component.
- Relevant advisory or detection result.
- Whether the issue was verified.
- Recommended remediation.

Never copy discovered credentials or secret values into assessment reports.

## 10. Logging and Monitoring

### What to Check

- Recording of important security events.
- Protection of logs from unauthorized access.
- Detection and alerting for relevant suspicious activity.
- Avoidance of sensitive information in logs.
- Availability of audit trails for critical administrative actions.

### How to Check

- Review logging requirements and available audit records.
- Verify that relevant events are recorded.
- Check access controls for logging systems.
- Inspect sample logs for unnecessary sensitive information.
- Review alerting and incident-response procedures where available.

### Evidence to Record

- Event or control being assessed.
- Expected and observed behavior.
- Relevant sanitized log entries or configuration references.
- Identified gaps and recommendations.

## 11. Assessment Results

Record each check using one of the following statuses:

- Pass: The check was performed and the expected control was verified.
- Fail: Evidence demonstrates that the control does not meet the defined requirement.
- Needs Investigation: An observation requires additional evidence or validation.
- Not Tested: The check was not performed.
- Not Applicable: The check does not apply to the product, with a documented reason.

A lack of evidence must not automatically be treated as a failure or as proof that a control is secure.

## 12. Security Finding Record

For each identified issue, record:

- Finding ID.
- Finding title.
- Affected component.
- Assessment date.
- Severity and justification.
- Status.
- Description and potential impact.
- Reproduction steps.
- Supporting evidence.
- Recommended remediation.
- Retest result, where applicable.

Refer to `severity-classification.md` for the project's severity definitions.

## 13. Assessment Limitations

- Perform only authorized security testing.
- Use non-destructive techniques wherever possible.
- Do not expose or retain unnecessary sensitive data.
- Do not perform denial-of-service or other disruptive tests without explicit authorization and appropriate safeguards.
- Distinguish verified vulnerabilities from suspected issues.
- Document unavailable tools, inaccessible components, and untested areas.
- Do not claim that completing this checklist proves the application is completely secure.