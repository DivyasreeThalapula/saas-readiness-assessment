# Compliance and Privacy Assessment

## 1. Purpose

This document defines a reusable process for reviewing privacy, data protection, and compliance considerations before a SaaS product is launched.

The assessment identifies applicable obligations, checks available evidence, and records potential gaps requiring further investigation.

It is not a legal opinion, a formal certification, or proof of regulatory compliance.

## 2. Identify Applicable Requirements

Before performing the assessment, determine:

- The type of product and services provided.
- The countries or regions in which the product will operate.
- The locations of its intended customers and users.
- The categories of personal and sensitive data processed.
- The purpose for collecting and processing each category of data.
- Whether children or other potentially vulnerable groups use the product.
- Whether the product processes financial, health, educational, or other regulated information.
- Whether third-party services process data on the product's behalf.
- Any contractual, industry-specific, or organizational requirements.

Use these details to identify potentially applicable laws, regulations, contractual commitments, and industry standards.

Do not assume that a regulation applies solely because a product belongs to a particular industry or uses a particular technology.

Record requirements whose applicability needs confirmation by a qualified legal or compliance professional.

## 3. Privacy Notice and Transparency

Review the available privacy notice and related disclosures.

Check whether they clearly explain, where applicable:

- What personal information is collected.
- Why the information is collected.
- How the information is used.
- Whether information is shared with third parties.
- How long information is retained.
- Whether information is transferred across borders.
- What rights users may have over their information.
- How users can contact the organization about privacy concerns.
- How material changes to privacy practices are communicated.

Compare the stated practices with the product's observed behavior and available technical documentation.

Record inconsistencies or missing information for further investigation.

Do not conclude that a privacy notice is legally sufficient without the appropriate legal review.

## 4. Data Collection and Minimization

Assess whether the product appears to collect only the information necessary for its stated purposes.

Check:

- Whether forms request unnecessary personal information.
- Whether optional fields are clearly distinguished from required fields.
- Whether sensitive information is collected only when justified.
- Whether information collection aligns with the stated purpose.
- Whether unnecessary data is included in URLs, logs, exports, or notifications.
- Whether test environments contain production personal data.
- Whether development and debugging processes expose personal information unnecessarily.

Document questionable collection practices and identify the relevant evidence.

## 5. Consent and User Choices

Where consent or user permission is required, review:

- Whether the user receives a clear explanation before the relevant action.
- Whether the choice is appropriately recorded.
- Whether users can change their choices when required.
- Whether optional processing is distinguished from essential processing.
- Whether marketing or non-essential tracking preferences are respected.
- Whether the interface avoids misleading or coercive consent choices.
- Whether the recorded preference is reflected in the product's behavior.

The exact requirements depend on the applicable law and processing activity.

Do not treat a checkbox or consent banner as sufficient evidence of compliance by itself.

## 6. Access, Correction, and Deletion Requests

Where applicable, determine whether users can exercise relevant rights concerning their information.

Review support for:

- Accessing personal information.
- Correcting inaccurate information.
- Requesting deletion.
- Exporting or receiving a copy of information.
- Withdrawing consent.
- Restricting or objecting to processing.
- Understanding how to submit a request.
- Tracking and responding to requests within applicable time limits.

Verify which capabilities are implemented and which require a documented manual process.

Do not delete real user data during testing without explicit authorization.

## 7. Data Retention and Deletion

Assess whether the organization has defined retention and deletion practices.

Check:

- Whether retention periods or retention criteria are documented.
- Whether data is retained only as long as justified.
- Whether deletion workflows behave as intended.
- Whether deleted data remains accessible through ordinary application interfaces.
- Whether relevant backups, logs, and exports are addressed by the retention policy.
- Whether legal or contractual retention obligations are considered.
- Whether deletion is recorded when appropriate.
- Whether data retention behavior is consistent across relevant services.

Distinguish between deletion from the active application and eventual deletion from backups or other systems.

Do not claim that all copies of data have been permanently deleted unless this has been verified.

## 8. Data Security and Confidentiality

Review the evidence available for protecting information against unauthorized access, disclosure, modification, and loss.

Where applicable, assess:

- Authentication and authorization controls.
- Access restrictions for sensitive records.
- Tenant isolation in multi-tenant environments.
- Encryption during transmission.
- Encryption at rest and its documented scope.
- Protection of credentials and secrets.
- Secure handling of backups and exports.
- Restrictions on access by employees and service providers.
- Security logging and incident investigation capabilities.
- Procedures for reporting and responding to suspected data breaches.

Use the separate security-testing checklist for detailed technical verification.

Do not infer that a control exists merely because it is described in a product interface or marketing document.

## 9. Data Sharing and Third-Party Processors

Identify relevant third-party services, such as:

- Cloud hosting providers.
- Authentication providers.
- Payment processors.
- Analytics services.
- Email and messaging providers.
- AI or machine-learning APIs.
- File storage services.
- Monitoring and error-reporting tools.

Where applicable, assess:

- What information each service receives.
- Why the information is shared.
- Whether the sharing is disclosed appropriately.
- Whether appropriate contractual arrangements are documented.
- Whether the third party's security and privacy practices have been reviewed.
- Whether international data transfers require additional safeguards.
- Whether data sharing can be configured or disabled where appropriate.

Do not send real personal or confidential information to external services during testing unless explicitly authorized.

## 10. User Roles and Confidential Information

Assess whether personal and confidential information is available only to appropriate users.

Check:

- Whether users can access only permitted records.
- Whether administrators have appropriately controlled access.
- Whether support personnel access is governed by documented procedures.
- Whether sensitive information appears in notifications or emails sent to unintended recipients.
- Whether downloadable reports contain only authorized information.
- Whether one tenant can access another tenant's information.
- Whether account closure and role changes affect access as expected.

Refer to the security and functional testing checklists for detailed testing procedures.

## 11. Cookies, Tracking, and Analytics

Where the product uses cookies, tracking technologies, or analytics, review:

- Which technologies are used and for what purposes.
- Whether non-essential tracking is activated only when permitted.
- Whether user preferences are respected.
- Whether tracking disclosures are available.
- Whether analytics events unnecessarily include personal or sensitive information.
- Whether third-party scripts receive information beyond what is necessary.
- Whether tracking behavior is consistent with the stated privacy practices.

The applicable requirements depend on the product's users, operating regions, and technologies.

## 12. Records and Organizational Policies

Identify relevant policies and records, where applicable:

- Privacy policy.
- Information security policy.
- Data retention and deletion policy.
- Access control policy.
- Incident response procedure.
- Business continuity and disaster recovery plans.
- Vendor and processor agreements.
- Data processing agreements.
- Records of relevant processing activities.
- Employee confidentiality and security training records.

Record whether each document exists, has been reviewed, and is supported by appropriate evidence.

The absence of a document should be evaluated against applicable requirements rather than automatically classified as a legal violation.

## 13. Incident Response and Breach Management

Review whether documented procedures exist for:

- Detecting and reporting suspected data breaches.
- Investigating security incidents.
- Containing and remediating incidents.
- Preserving relevant evidence.
- Assessing potential effects on affected individuals.
- Escalating incidents to appropriate personnel.
- Meeting applicable notification obligations.
- Recording lessons learned and corrective actions.

Do not trigger a real incident or send external notifications as part of an assessment without explicit authorization.

## 14. Accessibility and Other Applicable Obligations

Determine whether accessibility, consumer protection, education-sector requirements, financial regulations, or other industry-specific obligations may apply.

Where relevant, assess:

- Whether applicable requirements have been identified.
- Whether accessibility expectations are documented.
- Whether key workflows are usable with supported assistive technologies.
- Whether pricing, cancellation, and subscription terms are communicated clearly.
- Whether product claims are consistent with available evidence.
- Whether industry-specific requirements have been assigned to an appropriate reviewer.

Use specialized assessments when a requirement cannot be evaluated adequately through this general checklist.

## 15. Compliance Evidence Register

For each applicable requirement, record:

- Requirement ID.
- Requirement or control description.
- Source of the requirement.
- Reason it applies to the product.
- Evidence reviewed.
- Assessment result.
- Identified gap or uncertainty.
- Risk or potential impact.
- Responsible person or team, if known.
- Recommended next action.
- Review date.

Use the following statuses:

- Supported: Available evidence supports the stated control or practice.
- Gap Identified: Evidence indicates that a relevant requirement or control may not be met.
- Needs Review: Applicability or sufficiency requires additional investigation.
- Not Verified: There is insufficient evidence to assess the requirement.
- Not Applicable: The requirement does not apply, with the reason documented.

Supported does not mean that overall legal compliance has been established.

## 16. Reporting and Escalation

The assessment report should distinguish between:

- Confirmed observations.
- Potential compliance gaps.
- Missing documentation.
- Unverified technical or organizational controls.
- Requirements whose applicability is uncertain.
- Matters requiring legal or specialist review.

Prioritize issues according to potential impact, applicable obligations, likelihood, and available evidence.

Escalate potentially serious privacy or regulatory concerns to the appropriate security, privacy, legal, or compliance personnel.

Do not make definitive legal conclusions when the assessment lacks the required expertise or evidence.

## 17. Safe Assessment Principles

- Use only authorized systems and information.
- Prefer staging environments and synthetic data.
- Minimize access to personal and confidential information.
- Do not perform unauthorized data exports or deletions.
- Do not disclose sensitive evidence in reports.
- Record uncertainty rather than inventing evidence.
- Do not claim that a regulation, certification, or standard has been satisfied without adequate verification.
- Obtain qualified review when legal interpretation or formal certification is required.

## 18. Completion Criteria

The compliance and privacy review is ready for review when:

- Relevant data categories and processing activities have been identified.
- Potentially applicable requirements have been documented.
- Available evidence has been reviewed.
- Gaps and uncertainties have been recorded.
- Important third-party data flows have been considered.
- Items requiring specialist review have been identified.
- Recommendations and next actions have been documented.
- The assessment's limitations are clearly stated.

A completed checklist is an assessment record, not a guarantee of legal compliance.