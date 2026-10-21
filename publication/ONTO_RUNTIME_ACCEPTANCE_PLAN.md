# TCM v1.5 — Onto runtime acceptance plan

**Status:** BLOCKED / NOT RUN.  
**Source case:** [StroyPack document walkthrough](../examples/STROYPACK_END_TO_END_TEST.md).  
**Method reference:** [TCM v1.5](../docs/ru/method-reference.md).  
**Last attempted connection:** Onto `list_available_realms` returned `Onto API request failed.`; root cause not established.

## Preconditions

- Confirm working Onto API connection and exact realm identifier; never assume an older realm is the intended target.
- Obtain explicit authorization to create/update test entities and relations in an isolated test realm.
- Obtain S0–S4 source documents and locators, or mark the test **technical-only** (no substantive contract authority conclusion).
- Record reviewer, owner, date and approved plan ID.
- Ensure no production or unrelated project objects are changed.

## Acceptance sequence

| Step | Action | Evidence required | Status |
| --- | --- | --- | --- |
| A0 | List realms; identify approved test realm | Realm ID and successful read | BLOCKED |
| A1 / FRAME | Approve VBQ for contract and date | VBQ, owner approval, G1 | NOT RUN |
| A2 / MODEL | Approve MVTC and unknowns | Entity/relation model, evidence needs, G2 | NOT RUN |
| A3 / READ | Capture existing realm state | Baseline objects, relations, fields | NOT RUN |
| A4 / PLAN | Define exact intended changes and non-targets | Plan ID, entity/relation counts, field values | NOT RUN |
| A5 / APPROVE | Obtain explicit human authorization for writes | Approval record tied to plan ID | NOT RUN |
| A6 / WRITE | Apply approved changes only | API operation log, IDs, errors | NOT RUN |
| A7 / READ BACK | Re-read all created/updated objects and relations | Complete post-write snapshot | NOT RUN |
| A8 / COMPARE | Compare plan to actual; detect duplicates and side effects | Field-level and relation-level diffs, G3 | NOT RUN |
| A9 / GROUND | Link S0–S4 to claims with precise locators | Evidence IDs, versions, scope, G4 | NOT RUN |
| A10 / CONNECT | Query the realm through the intended access interface | Permissions, request log, retrieved IDs, G5 | NOT RUN |
| A11 / VERIFY | Validate warrants, temporal applicability and authority | VRP, unknowns/conflicts, G6 | NOT RUN |
| A12 / DECIDE | Prepare and approve permissible decision | DSP, human authority, G7 | NOT RUN |

## Safety and negative tests

1. Missing delegation evidence must not produce `ACT`; expected draft decision: `REQUEST EVIDENCE`.
2. `UNKNOWN` must not be silently coerced to `FALSE` or `STOP`.
3. Appointment must not be interpreted as delegation.
4. If READ BACK finds duplicate or stale values, G3 is FAIL; do not auto-repair without a new approved plan.
5. Successful authentication without retrieved objects is not G5 PASS.
6. Changes outside approved realm or scope are FAIL.
7. No raw confidential S0–S4 text is exported without an explicit storage and access policy.

## Current verdict

- API connectivity: **FAILED / cause unknown**
- Write authorization: **NOT OBTAINED**
- BUILD / CONNECT / VERIFY runtime evidence: **NOT RUN**
- End-to-end acceptance: **BLOCKED**
- Release readiness: **NOT ESTABLISHED**

This document is an execution plan, not an execution receipt.
