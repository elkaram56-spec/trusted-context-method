# TCM v1.5 — Editorial acceptance review for seven schema-aligned templates

**Status:** REVIEW / decision pending. **Scope:** templates/ru/schema-aligned/{VBQ,MVTC,TCBS,GCP,TCAC,VRP,DSP}.md. **Normative baseline:** docs/ru/method-reference.md §§6–7. This review does not amend the approved normative reference or declare any Gate passed.

## Confirmed
- All seven draft templates are present and distinguish common metadata from artifact-specific fields.
- Each draft names its stage, Gate, reviewer, evidence and an explicit PASS/FAIL/NOT RUN review control.
- The drafts themselves state they are not approved replacements.

## Issues for authorial/editorial resolution
1. **Rights and licenses (blocking):** Original templates are marked CC BY-NC-SA 4.0; intended open methodology is CC BY-SA 4.0. Author must confirm ownership and permission to relicense each included original element. Do not silently remove notices.
2. **Gate outcome vs form completion:** A structurally complete template is not a Gate PASS. Preserve separate structural and semantic/evidence review results; NOT RUN must not be represented as PASS.
3. **TCBS/G3:** Document all READ → PLAN → APPROVE → WRITE → READ BACK → COMPARE steps and approved plan reference, not just a final comparison result. Clarify what approval authorizes.
4. **GCP/G4:** Current scalar source_id/evidence_id/claim_id fields can be read as a single triple. Specify repeatable evidence-to-claim records and locators without changing normative required field names; confirm whether the normative schema permits this representation.
5. **DSP/G7:** authority is mandatory but may be UNKNOWN. Explicitly allow an unresolved authority claim/status without fabricating a person or granting ACT; confirm representation against normative schema.
6. **Types and machine validation:** Tables are human-readable; no executable JSON Schema or validators have been approved. Do not claim machine conformance.

## Acceptance criteria
- [ ] Authorial licensing decision recorded
- [ ] Seven artifact field/type/requiredness comparisons signed off against §§6–7
- [ ] G1–G7 Gate outcomes represented independently of template completeness
- [ ] TCBS write protocol and re-approval on failure documented
- [ ] GCP repeatability and DSP UNKNOWN authority resolved
- [ ] Reviewer, date and disposition recorded
- [ ] Only then promote drafts to approved release templates

## Non-goals
No Onto runtime test, no claim that S0–S4 original locators are verified, no release/tag/DOI, no change to docs/ru/method-reference.md.

**Editorial proposal:** Publish original educational templates only within their authorized licensing scope; adopt separate explicitly authorized public-method templates under CC BY-SA 4.0 after review. This is a proposal, not a rights determination.
