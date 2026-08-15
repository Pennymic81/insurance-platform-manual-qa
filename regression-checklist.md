# Regression Checklist

Use this checklist after every major fix or before a release candidate.

## Smoke Checks

- [ ] Login succeeds for every supported role.
- [ ] Dashboard loads without a blank page or server error.
- [ ] Main navigation opens each permitted module.
- [ ] Logout ends the session and blocks protected pages.

## Client and Assignment

- [ ] Individual and corporate clients can be created.
- [ ] Required-field errors remain visible until corrected.
- [ ] Client edits persist after refresh and re-login.
- [ ] Duplicate email and phone values are handled correctly.
- [ ] Client-to-marketer assignment saves and appears downstream.

## Quotes

- [ ] Quote can be created for every enabled product category.
- [ ] Preview is disabled until required data is valid.
- [ ] Sum Insured, premium, commission, and tax calculations are correct.
- [ ] Local and foreign currency fields appear only when relevant.
- [ ] Quote preview survives refresh and direct navigation.
- [ ] Quote acceptance changes the status and available actions.

## Policies and Invoices

- [ ] Accepted quote converts to one policy only.
- [ ] Policy dates and premium match the accepted quote.
- [ ] Invoice uses the correct client, policy, currency, and exchange rate.
- [ ] Loading indicators appear while remote options are fetched.
- [ ] Assigned account or sales manager is displayed consistently.

## Claims and Remittance

- [ ] Claim can be created only for an eligible policy.
- [ ] Claim amount and file validations work.
- [ ] Approved claim can be settled and is recorded in audit history.
- [ ] Premium remittance updates the outstanding balance.
- [ ] Report download requires a valid start and end date.

## Permissions and Quality

- [ ] Restricted buttons are hidden for unauthorized users.
- [ ] Direct requests to restricted actions are rejected.
- [ ] Success and error messages are clear and persistent enough to read.
- [ ] No action menus, modals, or fields overflow their containers.
- [ ] Critical flow passes in Chrome and Firefox.

