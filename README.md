# Insurance Brokerage Platform — Manual QA Portfolio

This repository demonstrates my manual testing approach for a fictional web-based insurance brokerage platform. The platform allows brokers to manage clients, create insurance quotes, convert accepted quotes into policies, issue invoices, process claims, and track premium remittance.

All company names, users, policy numbers, screenshots, and test data in this project are fictional. No confidential employer or customer information is included.

## Project Objectives

- Validate the platform's critical business workflows.
- Identify functional, validation, usability, and permission defects.
- Document clear and reproducible test evidence.
- Demonstrate risk-based testing and regression planning.

## Scope

The portfolio covers:

1. Authentication and role-based access
2. Client management
3. Quote creation and approval
4. Policy creation
5. Invoice generation
6. Claims processing
7. Premium remittance

## Repository Contents

| File | Purpose |
| --- | --- |
| [Test Plan](test-plan.md) | Scope, strategy, risks, environments, and exit criteria |
| [Test Scenarios](test-scenarios.md) | High-level coverage across platform modules |
| [Test Cases](test-cases.md) | Detailed positive, negative, boundary, and permission tests |
| [Bug Reports](bug-reports.md) | Five sample defects written in a professional format |
| [Traceability Matrix](traceability-matrix.md) | Mapping between requirements, test cases, and defects |
| [Regression Checklist](regression-checklist.md) | Critical checks before a release |
| [Test Summary](test-summary-report.md) | Sample execution results and release recommendation |
| [Test Data](test-data.csv) | Fictional reusable test inputs |

## Test Execution Summary

| Metric | Result |
| --- | ---: |
| Test cases designed | 30 |
| Test cases executed | 30 |
| Passed | 25 |
| Failed | 4 |
| Blocked | 1 |
| Pass rate | 83.3% |

Formula: `Pass Rate = Passed / Executed × 100`

## Key Findings

- Quote preview can become unavailable after a page refresh.
- Corporate client edit persistence was fixed and passed retesting.
- Assigned marketer information may be missing from downstream documents.
- Currency-dependent values can appear before currency data finishes loading.
- The Settle Claim button may remain disabled for an eligible claim.

## Tools and Techniques

- Manual functional testing
- Exploratory testing
- Positive and negative testing
- Boundary-value analysis
- Role and permission testing
- Regression and smoke testing
- Jira-style defect reporting
- Browser developer tools for evidence gathering

## How to Use This Portfolio

Open the documents in the order shown above. During an interview, explain how requirements were converted into test scenarios and cases, how failed cases became bug reports, and how release risk was evaluated in the summary report.

## Author

Paul Michael Adekunle  
Junior QA Engineer | Manual Testing | Functional Testing | Regression Testing
