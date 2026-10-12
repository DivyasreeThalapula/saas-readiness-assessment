# Functional and Role-Based Testing

## 1. Purpose

This document defines a reusable process for assessing the functional correctness, usability, and role-based behavior of a SaaS product.

The assessment should verify that features behave as expected, user workflows are consistent, and users can access only the functionality permitted by their roles.

The checklist must be adapted to the product's actual features and requirements. Features that do not exist should not automatically be treated as failures.

## 2. Preconditions

Before testing:

- Identify the product's intended users and user roles.
- Understand the main features and expected workflows.
- Obtain authorized test accounts for relevant roles.
- Use staging environments and synthetic data where possible.
- Record the environment, browser, test account role, and test date.
- Identify any known limitations or features that are not implemented.
- Confirm the expected behavior before classifying an outcome as a defect.

## 3. Authentication and Account Management

Check the following where applicable:

- Users can register when registration is supported.
- Users can log in with valid credentials.
- Invalid credentials produce an appropriate error message.
- Empty or malformed inputs are handled appropriately.
- Logout ends the authenticated session.
- Password reset or recovery follows the expected workflow.
- Session expiration behaves as expected.
- Account changes are reflected consistently across relevant pages.
- Restricted pages cannot be accessed after logout.
- Authentication errors do not expose sensitive information.

Record whether each check passes, fails, requires investigation, was not tested, or is not applicable.

## 4. Role-Based Access and Permissions

Identify each role and its intended permissions before testing.

For each role, verify:

- The correct dashboard or landing page is displayed.
- Only permitted pages, features, and actions are available.
- Restricted actions are blocked.
- Direct navigation to restricted pages does not bypass permissions.
- Changes made by one role appear correctly to other authorized roles.
- Role changes are reflected in the user's permissions.
- Users cannot access another user's private information without authorization.
- Tenant-specific data remains isolated in multi-tenant products.
- Administrative actions are available only to authorized users.

Do not assume that hiding a button is sufficient access control. Where authorized testing tools are available, verify that the underlying request is also protected.

## 5. Navigation and User Experience

Verify that:

- Navigation links lead to the correct destinations.
- Back and forward navigation behave consistently.
- Browser refresh does not produce unexpected states.
- Opening a page directly produces the expected result.
- Closing and reopening a tab does not unexpectedly change the user's state.
- Breadcrumbs and back buttons lead to the expected locations.
- Loading, empty, success, and error states are understandable.
- Error messages help users understand what went wrong.
- Forms preserve or clear entered data according to the expected behavior.
- The interface remains usable at supported screen sizes.

Pay special attention to inconsistent dashboards, unexpected redirects, broken links, and navigation that changes the user's context.

## 6. Feature and Workflow Testing

Create a feature inventory based on the product's actual functionality.

For every relevant feature, verify:

- The feature can be opened by an authorized user.
- Required inputs are accepted.
- Invalid inputs are handled correctly.
- The primary action completes successfully.
- The displayed result matches the expected result.
- Changes are saved when persistence is expected.
- Data remains consistent after refresh or re-login.
- Cancel and back actions behave as expected.
- Duplicate submissions do not cause unintended results.
- Failures are communicated clearly.
- Related features continue to work after the action.

For workflows involving multiple steps, test the entire journey from beginning to end rather than checking each screen in isolation.

## 7. Data Management

Where the product supports creating, viewing, updating, or deleting data, verify:

- Authorized users can create records.
- Required fields are enforced.
- Records can be viewed by the appropriate users.
- Updates persist correctly.
- Deletion follows the intended behavior.
- Confirmation is requested for destructive actions when appropriate.
- Deleted or updated records are reflected consistently across the application.
- Duplicate records are handled according to the requirements.
- Search, filtering, sorting, and pagination return appropriate results.
- Users cannot modify records they are not authorized to change.

Use synthetic test data and avoid deleting real customer data.

## 8. Forms, Validation, and File Handling

Check applicable forms and upload/download features:

- Required fields are validated.
- Input formats and length limits are enforced.
- Invalid values produce useful feedback.
- Valid submissions are processed correctly.
- File uploads enforce expected file types and size limits.
- Failed uploads produce understandable errors.
- Uploaded files are associated with the correct records.
- Downloads return the expected file.
- Exported documents contain the expected information.
- Canceling an operation does not accidentally submit it.
- Repeated actions do not create unintended duplicates.

Test only file types and inputs that are permitted by the approved test scope.

## 9. Notifications and Communication

Where applicable, verify:

- Notifications are triggered by the expected events.
- Notifications reach the correct users.
- Notification content is accurate.
- Links in notifications lead to the correct pages.
- Read and unread states behave as expected.
- Email or in-app notifications do not disclose information to unauthorized recipients.
- Disabled or unavailable notification channels are handled clearly.

Use test accounts and controlled recipients.

## 10. Payments and Other External Integrations

For features involving payments or external services:

- Verify that the feature's current implementation status is understood.
- Confirm that the displayed status reflects the actual operation.
- Check success, failure, cancellation, and pending states where supported.
- Verify that retrying an operation does not unintentionally duplicate it.
- Confirm that external-service failures are handled appropriately.
- Check that the application does not report success when the operation has not succeeded.

Use sandbox or test integrations when available.

Never initiate real payments or other consequential transactions without explicit authorization.

If a feature is only a UI placeholder or has not been implemented, document that limitation rather than assuming the full workflow works.

## 11. Cross-Browser and Responsive Testing

Where supported by the product's requirements, check:

- Primary workflows in supported browsers.
- Layout and controls at supported screen sizes.
- Forms and dialogs on smaller screens.
- Tables, navigation menus, and content overflow.
- Keyboard navigation for important workflows.
- Visible focus indicators and understandable labels.
- Basic accessibility concerns that interfere with completing tasks.

Prioritize critical user journeys and supported environments.

## 12. Regression and State Consistency

After identifying a defect or applying a fix, retest the affected workflow.

Also verify relevant related behavior:

- The original issue no longer occurs.
- Existing functionality still works.
- Data remains consistent across pages.
- State remains correct after refresh or re-login.
- Different roles see the correct information.
- Navigation does not unexpectedly change context.
- Related integrations still behave as expected.

Record the environment and steps needed to reproduce any regression.

## 13. Test Case Record

Each test case should contain:

- Test case ID
- Feature or workflow
- User role
- Preconditions
- Test steps
- Expected result
- Actual result
- Status
- Evidence
- Notes or limitations

Use consistent status values:

- Pass: Actual behavior matches the expected behavior.
- Fail: Actual behavior differs from the expected behavior.
- Needs Investigation: Available evidence is insufficient to determine the outcome.
- Not Tested: The check has not been performed.
- Not Applicable: The check does not apply to this product or feature.

Do not mark a check as passed merely because the page loads.

## 14. Defect Reporting

For each confirmed defect, record:

- Defect ID
- Short title
- Affected feature
- Environment
- User role
- Preconditions
- Reproduction steps
- Expected behavior
- Actual behavior
- Reproducibility
- Evidence
- User or business impact
- Severity, using the shared severity classification
- Suggested next action

Separate observed facts from assumptions. If the root cause is unknown, report the observed behavior without claiming a cause.

## 15. Completion Criteria

Functional testing is ready for review when:

- Important user roles have been identified.
- Critical workflows have been exercised.
- Applicable checks have recorded outcomes.
- Confirmed defects have reproducible steps and evidence where possible.
- Unavailable or unimplemented features are documented.
- Important untested areas and limitations are disclosed.
- Findings are prioritized using the shared severity classification.

Passing this checklist does not prove that the entire product is defect-free. Report the scope and coverage of the assessment.

## 16. Safe Testing Principles

- Test only systems for which explicit authorization has been provided.
- Follow the approved scope and testing constraints.
- Prefer staging environments and synthetic data.
- Do not access, expose, or modify real customer data unnecessarily.
- Do not perform destructive actions without explicit approval.
- Do not claim that a test was performed unless it was actually performed.
- Preserve evidence while minimizing sensitive information.