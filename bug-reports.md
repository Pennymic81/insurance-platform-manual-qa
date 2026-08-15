# Sample Bug Reports

These reports use fictional records and evidence placeholders. Replace each placeholder with your own sanitized screenshot or short recording when presenting the portfolio.

## BUG-001 — Quote Preview Does Not Reappear After Page Refresh

| Field | Details |
| --- | --- |
| Module | Quote Management |
| Environment | QA; Chrome latest; Windows 11 |
| Severity / Priority | High / High |
| Status | Open |
| Related test | TC-QTE-005 |

**Precondition:** A saved quote preview is open.

**Steps to reproduce:**

1. Log in as a Broker.
2. Open Quotes and select a saved quote.
3. Open the quote preview.
4. Refresh the browser page.

**Expected result:** The same quote preview should reload with its saved details.

**Actual result:** The quote preview does not appear after the refresh, preventing the user from reviewing the quote.

**Evidence:** `evidence/BUG-001-quote-preview-refresh.png`

---

## BUG-002 — Updated Corporate Client Information Is Not Saved

| Field | Details |
| --- | --- |
| Module | Client Management |
| Environment | QA; Chrome latest; Windows 11 |
| Severity / Priority | High / High |
| Status | Open |
| Related test | TC-CLT-004 |

**Precondition:** A corporate client record exists.

**Steps to reproduce:**

1. Log in as a Broker.
2. Open Clients and select a corporate client.
3. Click **Edit** and change the phone number.
4. Save the update.
5. Reopen the corporate client record.

**Expected result:** The updated phone number should be saved and displayed.

**Actual result:** The previous phone number is displayed after the record is reopened.

**Evidence:** `evidence/BUG-002-corporate-client-update.mp4`

---

## BUG-003 — Assigned Marketer Is Missing from Policy Details and Invoice

| Field | Details |
| --- | --- |
| Module | Policy / Invoice |
| Environment | QA; Chrome latest; Windows 11 |
| Severity / Priority | Medium / High |
| Status | Open |
| Related test | TC-POL-003 |

**Precondition:** A client is assigned to a marketer and has a saved policy and invoice.

**Steps to reproduce:**

1. Open the assigned client's policy.
2. Review Policy Details.
3. Open the invoice generated for that policy.

**Expected result:** The assigned marketer should be displayed consistently on both records.

**Actual result:** Assigned marketer information is not displayed on Policy Details or the invoice.

**Evidence:** `evidence/BUG-003-marketer-missing.png`

---

## BUG-004 — Exchange Rate Displays a Value While Currency Options Are Loading

| Field | Details |
| --- | --- |
| Module | Invoice |
| Environment | QA; throttled network; Chrome latest |
| Severity / Priority | Medium / Medium |
| Status | Open |
| Related test | TC-INV-002 |

**Precondition:** The Create Invoice page is open.

**Steps to reproduce:**

1. Enable network throttling in browser developer tools.
2. Open the Currency dropdown.
3. Observe the dropdown and Exchange Rate field while currency options are being fetched.

**Expected result:** A loading indicator should appear, and Exchange Rate should remain empty until a valid currency is loaded and selected.

**Actual result:** No loader is shown, and Exchange Rate displays a value before the currency options finish loading.

**Evidence:** `evidence/BUG-004-currency-loading.mp4`

---

## BUG-005 — Error Occurs When Settling an Approved Claim

| Field | Details |
| --- | --- |
| Module | Claims |
| Environment | QA; Chrome latest; Windows 11 |
| Severity / Priority | Critical / High |
| Status | Open |
| Related test | TC-CLM-004 |

**Precondition:** An approved claim is available for settlement.

**Steps to reproduce:**

1. Log in as a Claims Officer.
2. Open an approved claim.
3. Click **Settle Claim**.
4. Enter a valid settlement amount and payment method.
5. Confirm the settlement.

**Expected result:** The claim should be settled, the status and audit history should update, and a success message should appear.

**Actual result:** An error occurs and the claim remains unsettled.

**Evidence:** `evidence/BUG-005-claim-settlement.png`

