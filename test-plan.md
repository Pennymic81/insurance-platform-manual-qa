# Test Plan

## 1. Project Overview

The system under test is a fictional insurance brokerage web application used to manage the lifecycle of clients, quotes, policies, invoices, claims, and premium remittance.

## 2. Test Objectives

- Confirm that critical insurance workflows operate correctly from start to finish.
- Confirm that required fields and business rules are enforced.
- Confirm that users see only actions allowed by their roles.
- Confirm that saved information remains accurate across related modules.
- Identify issues that could cause financial, compliance, or customer-service risk.

## 3. In Scope

- Login, logout, invalid credentials, and session handling
- Individual and corporate client creation and editing
- Quote creation, validation, preview, acceptance, and rejection
- Policy creation from accepted quotes
- Invoice generation and currency display
- Claim submission and settlement
- Premium remittance and report download
- Role-based access to sensitive actions
- Cross-browser smoke testing

## 4. Out of Scope

- Payment-gateway processing
- Email delivery infrastructure
- Performance and load testing
- Security penetration testing
- Mobile-native applications
- Third-party insurer integrations

## 5. Test Approach

Testing is risk based. Quote, policy, invoice, claim, and remittance workflows receive the highest priority because failures can affect financial records and customer service.

The following techniques are used:

- Positive testing for expected user journeys
- Negative testing for missing or invalid inputs
- Boundary testing for dates, amounts, and text limits
- Exploratory testing around state changes and navigation
- Role-based testing for restricted actions
- Regression testing after defect fixes

## 6. Test Environment

| Item | Configuration |
| --- | --- |
| Environment | QA/Staging |
| Browser | Chrome latest; Firefox latest |
| Operating system | Windows 10/11 |
| User roles | Super Admin, Broker, Marketer, Claims Officer |
| Test data | Fictional clients, products, quotes, policies, and claims |

## 7. Entry Criteria

- QA environment is accessible.
- Test build is deployed and stable enough to test.
- Requirements or acceptance criteria are available.
- Required user accounts and product configurations exist.
- Critical third-party dependencies are available or mocked.

## 8. Exit Criteria

- All critical and high-priority cases are executed.
- No open Critical defects remain.
- High-severity defects have an agreed resolution or workaround.
- At least 90% of planned cases pass for release approval.
- Regression testing is completed on fixed areas.
- A test summary report is shared with stakeholders.

## 9. Risks and Mitigation

| Risk | Impact | Mitigation |
| --- | --- | --- |
| Unstable QA environment | Testing delays or false failures | Record environment incidents separately and retest |
| Incomplete requirements | Incorrect expectations | Confirm assumptions with the product owner |
| Limited role accounts | Permission gaps | Prepare accounts for every supported role |
| Test-data dependency | Blocked end-to-end flow | Seed reusable fictional records before execution |
| Late fixes | Regression risk | Prioritize critical-path regression checks |

## 10. Defect Severity

| Severity | Definition |
| --- | --- |
| Critical | System unavailable, data loss, or core workflow completely blocked |
| High | Major feature fails and no reasonable workaround exists |
| Medium | Feature partly fails, but a workaround exists |
| Low | Minor usability, visual, or content issue |

## 11. Deliverables

- Test plan
- Test scenarios and detailed test cases
- Bug reports with supporting evidence placeholders
- Requirements traceability matrix
- Regression checklist
- Test summary report

