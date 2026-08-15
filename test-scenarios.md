# Test Scenarios

| ID | Module | Scenario | Priority |
| --- | --- | --- | --- |
| TS-001 | Authentication | Log in with valid credentials | Critical |
| TS-002 | Authentication | Reject invalid credentials with a clear message | High |
| TS-003 | Authentication | Restrict access after logout or session expiry | High |
| TS-004 | Client | Create an individual client with valid data | High |
| TS-005 | Client | Create a corporate client with valid data | High |
| TS-006 | Client | Validate duplicate email and phone number | Medium |
| TS-007 | Client | Edit and persist client information | High |
| TS-008 | Client | Assign a client to a marketer | High |
| TS-009 | Quote | Create a quote for a configured product | Critical |
| TS-010 | Quote | Prevent preview until required fields are valid | High |
| TS-011 | Quote | Display correct currency and premium values | Critical |
| TS-012 | Quote | Preserve quote preview after refresh | High |
| TS-013 | Quote | Accept or reject a quote according to role | High |
| TS-014 | Policy | Convert an accepted quote into a policy | Critical |
| TS-015 | Policy | Display quote and assigned marketer information | High |
| TS-016 | Invoice | Generate an invoice from a valid policy | Critical |
| TS-017 | Invoice | Show currency loading and exchange-rate states correctly | High |
| TS-018 | Invoice | Restrict invoice actions by permission | High |
| TS-019 | Claims | Submit a valid claim against an active policy | Critical |
| TS-020 | Claims | Validate claim amount and supporting documents | High |
| TS-021 | Claims | Settle a claim using a valid method and amount | Critical |
| TS-022 | Remittance | Create and update a remittance schedule | High |
| TS-023 | Remittance | Require a start and end date before download | Medium |
| TS-024 | Permissions | Hide restricted actions from unauthorized users | High |
| TS-025 | Compatibility | Complete a smoke test in supported browsers | Medium |

