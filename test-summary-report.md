# Test Summary Report

## Executive Summary

Manual testing was completed on the fictional Insurance Brokerage Platform across seven core modules. Thirty test cases were executed: 24 passed, five failed, and one was blocked. The observed pass rate is 80%, which is below the 90% exit target.

## Execution Results

| Result | Count | Percentage |
| --- | ---: | ---: |
| Passed | 24 | 80.0% |
| Failed | 5 | 16.7% |
| Blocked | 1 | 3.3% |
| Total | 30 | 100% |

## Defect Summary

| Severity | Open Defects |
| --- | ---: |
| Critical | 1 |
| High | 2 |
| Medium | 2 |
| Low | 0 |
| Total | 5 |

## Major Risks

- Claim settlement is blocked by a Critical defect, creating financial and operational risk.
- Corporate client changes may be lost, creating incorrect customer records.
- Quote preview may become inaccessible after refresh.
- Missing assigned marketer information reduces record traceability.
- Incorrect currency-loading state could confuse users during invoice creation.

## Blocked Testing

Firefox compatibility testing was blocked because the browser environment was unavailable. It should be completed before final release approval.

## Release Recommendation

**Not recommended for production release in the current state.** BUG-005 should be fixed and retested first. BUG-001 and BUG-002 should also be resolved or explicitly accepted by the product owner. After fixes, targeted retesting and a full critical-path regression should be completed.

## Sign-off

Prepared by: Paul Michael Adekunle  
Role: Junior QA Engineer  
Test type: Manual functional and regression testing

