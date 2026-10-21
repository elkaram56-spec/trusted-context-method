# TCM v1.5 — Editorial acceptance review for seven schema-aligned templates

**Status:** REVIEW / authorial licensing decision recorded 2026-10-21; normative acceptance pending. **Scope:** templates/ru/schema-aligned/{VBQ,MVTC,TCBS,GCP,TCAC,VRP,DSP}.md. **Normative baseline:** docs/ru/method-reference.md §§6–7. This review does not amend the approved normative reference or declare any Gate passed.

## Confirmed
- All seven draft templates are present and distinguish common metadata from artifact-specific fields.
- Each draft names its stage, Gate, reviewer, evidence and an explicit PASS/FAIL/NOT RUN review control.
- The drafts themselves state they are not approved replacements.

## Issues for authorial/editorial resolution
1. **Rights and licenses (authorial decision recorded):** On 2026-10-21 the author confirmed CC BY-SA 4.0 for author-owned public TCM method and schema-aligned templates; separate educational materials remain CC BY-NC-SA 4.0 where marked. Third-party rights audit remains open. Original educational notices are preserved.
2. **Gate outcome vs form completion:** A structurally complete template is not a Gate PASS. Preserve separate structural and semantic/evidence review results; NOT RUN must not be represented as PASS.
3. **TCBS/G3:** Document all READ → PLAN → APPROVE → WRITE → READ BACK → COMPARE steps and approved plan reference, not just a final comparison result. Clarify what approval authorizes.
4. **GCP/G4:** Current scalar source_id/evidence_id/claim_id fields can be read as a single triple. Specify repeatable evidence-to-claim records and locators without changing normative required field names; confirm whether the normative schema permits this representation.
5. **DSP/G7:** authority is mandatory but may be UNKNOWN. Explicitly allow an unresolved authority claim/status without fabricating a person or granting ACT; confirm representation against normative schema.
6. **Types and machine validation:** Tables are human-readable; no executable JSON Schema or validators have been approved. Do not claim machine conformance.

## Acceptance criteria
- [x] Authorial licensing decision recorded (2026-10-21; third-party rights audit remains open)
- [ ] Seven artifact field/type/requiredness comparisons signed off against §§6–7
- [ ] G1–G7 Gate outcomes represented independently of template completeness
- [ ] TCBS write protocol and re-approval on failure documented
- [ ] GCP repeatability and DSP UNKNOWN authority resolved
- [ ] Reviewer, date and disposition recorded
- [ ] Only then promote drafts to approved release templates

## Non-goals
No Onto runtime test, no claim that S0–S4 original locators are verified, no release/tag/DOI, no change to docs/ru/method-reference.md.

**Editorial proposal:** Publish original educational templates only within their authorized licensing scope; adopt separate explicitly authorized public-method templates under CC BY-SA 4.0 after review. This is a proposal, not a rights determination.

## Normative field/type review — 2026-10-21

Compared each schema-aligned draft against the field names, types, and requiredness stated in normative §§6.1–6.7, including common metadata in §6. Result: **7/7 editorial field/type matches**; this is not executable JSON Schema validation, a semantic Gate PASS, or runtime acceptance. Corrected all seven relative links to `../../../docs/ru/method-reference.md`.

Added explanatory sections for G1–G7 without modifying normative required fields. G3 specifies READ → PLAN → APPROVE → WRITE → READ BACK → COMPARE; G4 uses repeatable normative scalar records (container convention still requires approval); G7 preserves `authority` as string and proposes literal `UNKNOWN` with no ACT (convention still requires approval).

**Pending authorial decision:** accept GCP repeatable-record convention and DSP authority=`UNKNOWN` convention; then decide whether to mark the templates approved for editorial publication. Third-party rights review and real-case Gate tests remain open.

## Author decision — 2026-10-21

Accepted: GCP repeatable Source–Evidence–Claim records retaining normative scalar field types; DSP authority string may explicitly be UNKNOWN, which never permits ACT. Editorial template acceptance is distinct from actual Gate execution and third-party rights clearance.
