SaaS Assessment Methodology

1. Purpose

This document defines a standardized methodology for assessing Software as a Service (SaaS) products before market launch.

It provides a reusable process for evaluating product functionality, security, privacy, compliance requirements, operational readiness, and overall launch readiness.

The methodology is designed to work across different SaaS products. Assessment activities should be adapted to each product's architecture, features, users, data sensitivity, and applicable requirements.

2. Scope

The assessment may cover the following areas:

- Product discovery and assessment planning
- Security assessment
- Authorized penetration testing
- Functional testing
- Role-based access control testing
- Privacy and compliance assessment
- Operational readiness
- Market launch readiness

Not every assessment will require the same tests. The assessment scope must be determined based on the product's risks, requirements, and intended use.

3. Objectives

The objectives of this methodology are to:

- Establish a consistent process for assessing SaaS products.
- Identify and document functional defects and potential security vulnerabilities.
- Evaluate access controls and protection of sensitive data.
- Identify applicable privacy, regulatory, and security requirements.
- Record findings with supporting evidence and remediation recommendations.
- Provide an evidence-based assessment of launch readiness.
- Support manual testing and suitable automation where authorized and technically feasible.

4. Guiding Principles

All assessments should follow these principles:

1. Authorization first: Security testing must remain within an explicitly authorized scope.
2. Risk-based assessment: Prioritize checks according to potential impact and likelihood.
3. Evidence-based findings: Record evidence and distinguish verified findings from suspected issues.
4. Data protection: Prefer staging environments and synthetic data wherever practical.
5. Repeatability: Use documented procedures so assessments can be reproduced.
6. Appropriate automation: Automate suitable checks without assuming that every requirement can be validated automatically.
7. Continuous improvement: Update the methodology based on assessment results and lessons learned.
8. Transparent reporting: Clearly identify untested areas, limitations, unresolved risks, and assumptions.

5. Standard Assessment Process

Every SaaS assessment should follow the stages below. The depth of each stage should depend on the product's features, architecture, risks, and intended use.

Stage 1: Product Discovery

Objective: Understand the product before planning any assessment activities.

Activities:
- Identify the product's purpose, target users, and business requirements.
- Identify user roles and their permissions.
- Review available architecture diagrams, technical documentation, and API documentation.
- Identify frontend, backend, databases, external integrations, and hosting infrastructure.
- Determine what types of data the product collects, processes, and stores.
- Identify critical features and business workflows.

Expected output:
- Product overview
- Initial architecture and data-flow understanding
- User-role inventory
- Preliminary risk areas

Stage 2: Assessment Planning

Objective: Define the assessment scope, approach, and acceptance criteria.

Activities:
- Establish the authorized testing scope and exclusions.
- Identify the environments, accounts, tools, and documentation available.
- Determine which assessment activities are applicable.
- Identify dependencies, assumptions, and limitations.
- Define test priorities based on risk.
- Establish evidence collection and reporting requirements.

Expected output:
- Assessment plan
- Scope and exclusions
- Applicable testing activities
- Defined acceptance criteria

Stage 3: Security Assessment

Objective: Evaluate the product's security controls and identify potential weaknesses.

Activities:
- Review authentication and session management.
- Examine authorization and role-based access controls.
- Assess API security and input validation.
- Review sensitive-data handling and exposure risks.
- Examine security configurations and relevant code, where authorized.
- Review dependency risks, secrets management, and error handling.
- Evaluate logging and security monitoring capabilities.

Expected output:
- Security findings
- Supporting evidence
- Risk and severity assessments
- Recommended remediation actions

Stage 4: Penetration Testing

Objective: Validate whether security weaknesses can be exploited within the authorized scope.

Activities:
- Confirm written authorization and testing boundaries.
- Review the application and identify potential attack surfaces.
- Select relevant test cases based on the product's technology and risks.
- Conduct approved tests using suitable manual methods and tools.
- Validate potential vulnerabilities without unnecessarily accessing, modifying, or exposing data.
- Document verified findings and distinguish them from unconfirmed suspicions.
- Retest resolved findings when appropriate.

Potential testing areas include:
- Broken access control
- Authentication weaknesses
- Injection vulnerabilities
- Cross-site scripting
- Session-management weaknesses
- Security misconfigurations
- Sensitive-data exposure

Expected output:
- Penetration-testing report
- Validated vulnerabilities and supporting evidence
- Severity assessments
- Remediation recommendations
- Retest results, where applicable

Stage 5: Functional and Role-Based Testing

Objective: Verify that features work correctly and that users can access only the functionality and data permitted by their roles.

Activities:
- Identify key features and user workflows.
- Create positive, negative, boundary, and error-handling test cases.
- Test registration, login, logout, and account-management workflows where applicable.
- Verify feature behavior against documented requirements.
- Test permissions across different user roles.
- Verify that users cannot access another user's data without authorization.
- Check navigation, validation messages, and recovery from errors.
- Record reproducible defects and expected versus actual results.

Expected output:
- Functional test cases and results
- Role-based access test results
- Defect reports
- Regression-testing recommendations

Stage 6: Privacy and Compliance Assessment

Objective: Identify applicable privacy obligations, regulatory requirements, and security standards.

Activities:
- Determine the jurisdictions and industries relevant to the product.
- Identify applicable privacy laws, contractual obligations, and industry requirements.
- Review data collection, processing, storage, retention, and deletion practices.
- Examine consent, transparency, and user-rights mechanisms where applicable.
- Review access to personal data and relevant third-party data sharing.
- Map applicable requirements to available evidence.
- Record gaps requiring further investigation or specialist review.

Expected output:
- Applicable-requirements inventory
- Compliance assessment checklist
- Evidence and identified gaps
- Recommended remediation actions

The assessment must not claim formal certification or legal compliance solely because a checklist has been completed.

Stage 7: Operational Readiness

Objective: Evaluate whether the product's operational controls support a reliable and secure launch.

Activities:
- Review logging, monitoring, and alerting.
- Assess backup and recovery arrangements.
- Review incident-response procedures.
- Examine deployment and environment-management practices.
- Assess dependency and vulnerability-management processes.
- Review availability, scalability, and performance evidence where relevant.
- Identify operational risks and recovery limitations.

Expected output:
- Operational-readiness findings
- Identified gaps and risks
- Recommended improvements

Stage 8: Market Launch Readiness

Objective: Consolidate assessment results and determine whether the product meets its defined launch criteria.

Activities:
- Review findings from all applicable assessment stages.
- Prioritize unresolved issues according to severity and business impact.
- Identify critical defects, significant vulnerabilities, and unresolved compliance obligations.
- Verify whether required remediation and retesting have been completed.
- Document assessment limitations and untested areas.
- Compare the results against agreed launch acceptance criteria.
- Provide a recommendation supported by the available evidence.

Possible outcomes:
- Ready: Required acceptance criteria have been met, with no unresolved blocking issues identified within the assessment scope.
- Ready with Conditions: Launch may proceed only if explicitly defined conditions and risk-acceptance requirements are satisfied.
- Not Ready: One or more blocking issues or unmet mandatory requirements prevent launch.
- Inconclusive: Insufficient evidence or incomplete assessment prevents a reliable readiness decision.

The final launch decision belongs to the authorized product owner or responsible decision-makers, not to the assessment tool alone.

Expected output:
- Consolidated assessment report
- Prioritized risk register
- Remediation and retesting status
- Launch-readiness recommendation
- Outstanding risks, limitations, and required follow-up actions

6. Evidence Collection

Objective: Ensure that assessment findings are supported by sufficient, relevant, and reproducible evidence.

For each finding, collect the following information where applicable:

- Finding ID
- Date identified
- Assessment area
- Affected feature, component, endpoint, or workflow
- Environment in which the issue was observed
- Preconditions and steps to reproduce
- Expected behavior
- Actual behavior
- Supporting evidence, such as screenshots, sanitized logs, test results, or relevant code references
- Potential impact
- Recommended remediation
- Verification or retest status

Evidence Handling Principles

1. Collect only the evidence necessary to demonstrate the finding.
2. Remove or mask passwords, access tokens, personal information, and other secrets.
3. Avoid copying production customer data into reports.
4. Store evidence in an access-controlled location.
5. Record relevant limitations when evidence is incomplete.
6. Never claim a vulnerability has been verified if the available evidence does not support that conclusion.

7. Finding Classification and Severity

Objective: Apply a consistent approach to prioritizing findings across assessments.

Classify each finding by its nature:

- Security vulnerability
- Functional defect
- Access-control issue
- Privacy or compliance gap
- Operational weakness
- Performance or reliability issue
- Documentation or process gap

Severity Levels

| Severity | Description | Typical Response |
|---|---|---|
| Critical | Catastrophic potential impact, such as a major compromise of sensitive data or critical systems. | Escalate immediately. Block launch until resolved or formally addressed. |
| High | Significant security, privacy, or business impact. | Prioritize remediation before launch unless an authorized risk decision permits otherwise. |
| Medium | Meaningful but more limited impact. | Schedule remediation according to risk and launch requirements. |
| Low | Minor weakness with limited impact. | Address through planned improvements. |
| Informational | Observation or recommendation without demonstrated direct adverse impact. | Document and consider for future improvement. |

Severity must be assigned using evidence, potential impact, exploitability, and the product's context. Security findings may use an appropriate version of the Common Vulnerability Scoring System (CVSS) as supporting guidance.

A severity label alone does not determine launch readiness. Applicable legal obligations, business requirements, and the product's risk-acceptance policy must also be considered.

8. Reporting Requirements

Objective: Present assessment results clearly so technical teams and decision-makers can take appropriate action.

Assessment Report Structure

A consolidated report should include:

1. Executive summary
2. Product overview and assessment scope
3. Assessment approach and standards used
4. Areas tested and results
5. Findings grouped by severity and category
6. Evidence and reproduction steps for relevant findings
7. Remediation recommendations
8. Retesting and remediation status
9. Untested areas, assumptions, and limitations
10. Compliance gaps and unresolved requirements, where applicable
11. Launch-readiness recommendation
12. Outstanding risks and required follow-up actions

Reporting Rules

- Distinguish verified findings from suspected issues.
- Clearly identify checks that were not performed.
- Avoid presenting missing evidence as proof that a control is absent.
- Use language appropriate for both technical teams and management.
- Prioritize actionable recommendations over vague statements.
- Do not claim that a product is completely secure or universally compliant.
- Ensure the final recommendation is traceable to documented evidence and agreed acceptance criteria.

9. Using the Methodology with Claude

Objective: Ensure that Claude follows a consistent, evidence-based process when assisting with SaaS assessments.

### 9.1 Understand the Product

Before recommending tests, Claude should:

- Understand the product's purpose, features, and architecture.
- Identify user roles, permissions, and sensitive data.
- Review the available documentation and authorized testing scope.
- Ask for missing information when it materially affects the assessment.

### 9.2 Create an Assessment Plan

Claude should:

- Identify the assessment areas relevant to the product.
- Select appropriate testing procedures and checklists.
- Prioritize tests according to risk.
- Identify required tools, access, permissions, and prerequisites.
- Clearly state assumptions, exclusions, and limitations.

### 9.3 Guide and Automate Testing

Claude should:

- Provide clear steps for manual testing.
- Recommend suitable automated checks where practical.
- Use available tools and scripts only when authorized and supported.
- Explain the purpose and expected result of each test.
- Avoid destructive or disruptive activities unless explicitly authorized and appropriately controlled.

Claude must distinguish between planning a test, executing a test, and verifying its result.

### 9.4 Record and Analyze Findings

For each finding, Claude should:

- Document the observed behavior and supporting evidence.
- Explain the potential impact.
- Assign a justified severity.
- Recommend practical remediation steps.
- Identify whether the finding is verified, suspected, resolved, or awaiting verification.

Claude must not invent test results, evidence, or successful remediation.

### 9.5 Produce the Final Assessment

Claude should generate a structured report containing:

- Assessment scope and methodology
- Completed and incomplete checks
- Findings and severity classifications
- Evidence and remediation recommendations
- Compliance gaps, where applicable
- Assessment limitations
- Outstanding risks
- Launch-readiness recommendation

The recommendation must be based on documented evidence and predefined acceptance criteria.

### 9.6 Continuous Improvement

After each assessment, Claude should help identify:

- Missing or unclear test procedures
- Repeated findings that need better coverage
- Opportunities for safe automation
- Improvements to checklists and report templates

Updates to the methodology should be reviewed and validated before being adopted.