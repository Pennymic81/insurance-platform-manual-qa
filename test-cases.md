# Detailed Test Cases

## Authentication

| ID | Test Case | Preconditions | Steps | Expected Result | Priority | Status |
| --- | --- | --- | --- | --- | --- | --- |
| TC-AUTH-001 | Login with valid credentials | Active Broker account exists | 1. Open Login. 2. Enter valid email and password. 3. Click **Login**. | User is authenticated and taken to the permitted dashboard. | Critical | Pass |
| TC-AUTH-002 | Login with an incorrect password | Active account exists | 1. Open Login. 2. Enter valid email and wrong password. 3. Click **Login**. | Login is rejected and a clear error appears without revealing sensitive details. | High | Pass |
| TC-AUTH-003 | Submit empty login form | None | 1. Open Login. 2. Leave both fields empty. 3. Click **Login**. | Required-field messages appear below both fields and login is not submitted. | High | Pass |
| TC-AUTH-004 | Access protected page after logout | User was logged in | 1. Log out. 2. Use browser Back. 3. Open a protected URL. | User is redirected to Login and protected information is not shown. | High | Pass |

## Client Management

| ID | Test Case | Preconditions | Steps | Expected Result | Priority | Status |
| --- | --- | --- | --- | --- | --- | --- |
| TC-CLT-001 | Create an individual client | Broker is logged in | 1. Open Clients. 2. Click **New Client**. 3. Select Individual. 4. Complete required fields. 5. Save. | Client is saved once and appears in the client list with correct details. | High | Pass |
| TC-CLT-002 | Create a corporate client | Broker is logged in | 1. Open New Client. 2. Select Corporate. 3. Enter valid company data. 4. Save. | Corporate client is saved and a success message appears. | High | Pass |
| TC-CLT-003 | Prevent duplicate client email | A client already uses the test email | 1. Create another client. 2. Enter the existing email. 3. Save. | Save is prevented and the duplicate-email message identifies the affected field. | Medium | Pass |
| TC-CLT-004 | Persist corporate client edits | Corporate client exists | 1. Open client details. 2. Click Edit. 3. Change phone number. 4. Save. 5. Reopen record. | Updated phone number remains saved and is visible everywhere the client appears. | High | Pass — BUG-002 fixed and retested |
| TC-CLT-005 | Assign a client to a marketer | Client and Marketer account exist | 1. Open Assign Client. 2. Select client type. 3. Select client. 4. Select marketer. 5. Save. | Selected values remain visible and assignment is saved. | High | Pass |

## Quote Management

| ID | Test Case | Preconditions | Steps | Expected Result | Priority | Status |
| --- | --- | --- | --- | --- | --- | --- |
| TC-QTE-001 | Create a valid motor quote | Motor product and client exist | 1. Open Create Quote. 2. Select client and Motor product. 3. Complete risk and premium fields. 4. Preview. 5. Save. | Preview displays correct information and quote is saved with a unique number. | Critical | Pass |
| TC-QTE-002 | Keep Preview disabled for missing required fields | Create Quote is open | 1. Select a product. 2. Leave Nature of Work and Sum Insured empty. | Preview remains disabled and clear required-field guidance is shown. | High | Pass |
| TC-QTE-003 | Reject zero Sum Insured | Create Quote is open | 1. Complete other fields. 2. Enter 0 for Sum Insured. 3. Attempt preview. | Preview is prevented and a valid positive amount is requested. | High | Pass |
| TC-QTE-004 | Display local currency correctly | Base currency is NGN | 1. Create NGN quote. 2. Open Preview. | Naira symbol precedes financial values; foreign exchange fields are hidden. | Critical | Pass |
| TC-QTE-005 | Refresh quote preview | Saved quote preview is open | 1. Note quote number. 2. Refresh browser. | Same quote preview reloads without blank or missing content. | High | Fail — BUG-001 |
| TC-QTE-006 | Accept quote as authorized user | Pending quote and authorized account exist | 1. Open quote. 2. Click Accept. 3. Confirm. | Status changes to Accepted; acceptance controls are no longer shown. | High | Pass |

## Policies and Invoices

| ID | Test Case | Preconditions | Steps | Expected Result | Priority | Status |
| --- | --- | --- | --- | --- | --- | --- |
| TC-POL-001 | Create policy from accepted quote | Accepted quote exists | 1. Open quote. 2. Click Create Policy. 3. Enter dates. 4. Save. | Policy is created once with correct quote, client, product, dates, and premium. | Critical | Pass |
| TC-POL-002 | Prevent end date before start date | Policy form is open | 1. Choose a start date. 2. Choose an earlier end date. 3. Save. | Save is prevented and the date relationship is explained. | High | Pass |
| TC-POL-003 | Display assigned marketer downstream | Client has assigned marketer; policy exists | 1. Open policy details. 2. Open its invoice. | Assigned marketer is displayed consistently on policy and invoice. | High | Fail — BUG-003 |
| TC-INV-001 | Generate invoice from policy | Active policy exists | 1. Open policy. 2. Click Generate Invoice. 3. Review values. 4. Save. | Unique invoice is created with correct client, premium, commission, and currency. | Critical | Pass |
| TC-INV-002 | Show correct currency loading state | Create Invoice is open | 1. Open currency selector on a slow connection. 2. Observe exchange rate. | Loader appears while currencies load; exchange rate remains empty until selection completes. | High | Fail — BUG-004 |

## Claims

| ID | Test Case | Preconditions | Steps | Expected Result | Priority | Status |
| --- | --- | --- | --- | --- | --- | --- |
| TC-CLM-001 | Submit claim for active policy | Active policy exists | 1. Open Claims. 2. Click New Claim. 3. Select policy. 4. Enter incident data. 5. Submit. | Claim is created with a unique reference and Submitted status. | Critical | Pass |
| TC-CLM-002 | Prevent claim amount above Sum Insured | Active policy exists | 1. Start claim. 2. Enter amount greater than Sum Insured. 3. Submit. | Submission is prevented and the allowed maximum is explained. | High | Pass |
| TC-CLM-003 | Reject unsupported document type | Claim form is open | 1. Upload an executable file. | File is rejected and supported formats and size limit are shown. | High | Pass |
| TC-CLM-004 | Start settlement for an eligible claim | Registered claim is eligible for settlement | 1. Open claim details. 2. Scroll to claim actions. 3. Inspect the Settle Claim button. 4. Attempt to begin settlement. | Settle Claim is enabled for the authorized user and opens the settlement workflow. | Critical | Fail — BUG-005 |

## Remittance and Permissions

| ID | Test Case | Preconditions | Steps | Expected Result | Priority | Status |
| --- | --- | --- | --- | --- | --- | --- |
| TC-REM-001 | Create premium remittance | Eligible invoice exists | 1. Open Remittance. 2. Select invoice. 3. Enter amount and date. 4. Save. | Remittance is saved and outstanding balance is recalculated correctly. | High | Pass |
| TC-REM-002 | Require dates before summary download | Remittance report page is open | 1. Leave Start and End Date empty. 2. Click Download Summary. | Download does not start and prompts identify both required dates. | Medium | Pass |
| TC-REM-003 | Reject start date after end date | Report page is open | 1. Enter a start date after end date. 2. Download. | Download is prevented and a clear date-range error appears. | Medium | Pass |
| TC-PER-001 | Hide user deletion from unauthorized role | Broker account is logged in | 1. Open Users. 2. Open Action menu. | Delete User is absent and direct delete requests are denied. | High | Pass |
| TC-PER-002 | Restrict quote acceptance by role | Marketer lacks approval permission | 1. Open pending quote. 2. Inspect actions. 3. Attempt direct approval URL. | Accept/Reject controls are hidden and server rejects unauthorized action. | High | Pass |
| TC-COMP-001 | Run critical smoke flow in Firefox | Firefox is supported | 1. Login. 2. Create client. 3. Create quote. 4. Logout. | Critical flow completes without browser-specific functional failure. | Medium | Blocked — environment unavailable |
