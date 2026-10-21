# Trusted Context Method (TCM) — Method Reference v1.5

> Open Edition 1.0 · English reference translated from the approved Russian authorial specification.
> Method source: TCM Method Reference v1.5 EXAMPLES (39 slides); formal artifact schemas and Gates approved for v1.5.
> Licensing notice: Public release under CC BY-SA 4.0 for author-owned method content; third-party rights and source review remain subject to PUBLICATION_CHECKLIST.md.

Complete methodological and operational specification · English edition corresponding to TCM Method Reference v1.5

Educational and methodological publication · 15 October 2026

7 stages · 7 artifacts · 3 control dimensions

## Document status and reading rules

**Provenance:** TCM Method Reference v1.5 EXAMPLES (39 slides). Original source tags in the internal specification were removed; slide-level citations must be checked before public release.

Version 1.5 was approved by the method owner on 15 October 2026. Formal schemas and Gate criteria, initially proposed as draft norms, were approved for this edition. This is an original authorial method, not an external standard.

## 1. Purpose and scope

TCM is a seven-stage method for constructing and verifying evidence-grounded context, transforming a persuasive AI answer into a verifiable conclusion and an authorized action. It addresses three questions: WHY (purpose and boundaries), ON WHAT GROUNDS (evidence and inference rules), and WHO (authority). “Can answer” ≠ “can prove” ≠ “is authorized to act”.

TCM is not a NIST, W3C, or ISO standard; it uses selected concepts and practices from them. Onto and MCP are implementation options, not mandatory components of the method.

## 2. Conceptual model

- **Source** — an identifiable source with a version, date, scope of applicability, and status.
- **Evidence** — a specific verifiable fragment of a Source with a locator.
- **Claim** — a statement requiring justification.
- **Rule / Warrant** — an explicit admissible rule for moving from Evidence to Claim.
- **Provenance** — origin and history of a claim; **Data Lineage** — movement and transformation of data. Neither alone guarantees truth.
- **Authority** — a subject's authority to authorize an action; a substantiated answer does not itself confer authority.

Critical sequence: Source → Evidence → Claim + Rule/Warrant → Verification → Authority → Decision. Grounded Context ≠ Grounded Reasoning; Retrieved ≠ Grounded ≠ Verified.

## 3. Method map

| Stage | Artifact | Contents | Gate |
| --- | --- | --- | --- |
| 1 FRAME | VBQ | Question, objective, date, scope, stakeholders, answer criterion | The question has not been substituted |
| 2 MODEL | MVTC | Types, entities, relations, Rule, Claim, Evidence Needs, statuses | Model is sufficient for VBQ |
| 3 BUILD | TCBS | Realm, version, schema, entities, relations, WRITE/READ BACK/COMPARE | Actual model matches the plan |
| 4 GROUND | GCP | Source–Evidence–Claim, locator, provenance, scope, conflicts | Grounds are traceable; UNKNOWN is preserved |
| 5 CONNECT | TCAC | Connection, permissions, requests, retrieved IDs, scope | Actual retrieval is confirmed |
| 6 VERIFY | VRP | Claims, Evidence, warrants, assumptions, conflicts, limits | Evidence and its limits are explicit |
| 7 DECIDE | DSP | Decision Status, rationale, authority, WHO→DOES WHAT→NEXT | Action does not exceed authority |

Route and Gates: slides 5, 9–16, 26–32.

## 4. Three independent control dimensions

| Dimension | Values | Meaning |
| --- | --- | --- |
| Epistemic | KNOWN / DERIVED / INFERRED / UNKNOWN / CONFLICTED | What is justified and by which means |
| Delegation | AUTO / REVIEW / HUMAN | Who prepares, reviews, and approves |
| Decision | ACT / REQUEST EVIDENCE / ESCALATE / STOP | What action is permitted |

- KNOWN — directly supported; DERIVED — derived through an admissible rule; INFERRED — hypothesis/interpretation; UNKNOWN — insufficient grounds; CONFLICTED — contradiction.
- AUTO does not imply KNOWN; HUMAN does not imply VERIFIED; UNKNOWN does not imply FALSE or STOP; KNOWN does not imply ACT.
- ACT — permissible action with sufficient grounds and authority; REQUEST EVIDENCE — request missing evidence; ESCALATE — refer to an authorized subject; STOP — prohibit or halt.

## 5. Stages, procedures, and checkpoints

### 5.1 FRAME — VBQ

Validated Business Question.

| Element | Description |
| --- | --- |
| Input | Business request, target object, as-of date, stakeholders |
| Operations and responsibility | AI drafts and identifies ambiguities; a human approves the meaning of the question |
| Control | Check the object, date, exclusions, answer criterion; prevent question substitution |
| Output / Gate | VBQ approved by the question owner |

**STATUS:** The above is a structured account of the presentation. The formal fields and requiredness below are **APPROVED IN v1.5**.

### 5.2 MODEL — MVTC

Minimum Viable Trusted Context.

| Element | Description |
| --- | --- |
| Input | Approved VBQ, available sources, and known gaps |
| Operations and responsibility | AI proposes types, entities, relations, and rules; REVIEW checks semantics; HUMAN approves sufficiency |
| Control | Check minimality, Evidence Needs, admissibility of relations and rules; do not invent unknown information |
| Output / Gate | MVTC is sufficient to answer VBQ |

**STATUS:** The above is a structured account of the presentation. The formal fields and requiredness below are **APPROVED IN v1.5**.

### 5.3 BUILD — TCBS

Trusted Context Build Snapshot.

| Element | Description |
| --- | --- |
| Input | Approved MVTC, target realm, write plan |
| Operations and responsibility | READ → PLAN → APPROVE → WRITE → READ BACK → COMPARE; AI performs approved operations |
| Control | Compare identifiers, versions, counts, and semantics of entities/relations; ensure no side effects |
| Output / Gate | PASS only if actual state matches the plan |

**STATUS:** The above is a structured account of the presentation. The formal fields and requiredness below are **APPROVED IN v1.5**.

### 5.4 GROUND — GCP

Grounded Context Package.

| Element | Description |
| --- | --- |
| Input | Sources and Claims from MVTC/TCBS |
| Operations and responsibility | AI extracts fragments and locators; REVIEW checks precision, dates, and applicability |
| Control | For each material Claim, show Source, Evidence, locator, scope, Rule, and conflict/gap |
| Output / Gate | Grounds are traceable; UNKNOWN is not concealed |

**STATUS:** The above is a structured account of the presentation. The formal fields and requiredness below are **APPROVED IN v1.5**.

### 5.5 CONNECT — TCAC

Trusted Context Access Check.

| Element | Description |
| --- | --- |
| Input | Addressable trusted context, permissions, and request |
| Operations and responsibility | AI performs actual retrieval through MCP or another interface; a human checks scope |
| Control | Record actual requests, retrieved IDs, permissions, and outcome |
| Output / Gate | Actual access to the required context is demonstrated |

**STATUS:** The above is a structured account of the presentation. The formal fields and requiredness below are **APPROVED IN v1.5**.

### 5.6 VERIFY — VRP

Verification Result Package.

| Element | Description |
| --- | --- |
| Input | Retrieved Claims, Evidence, Rules, and limitations |
| Operations and responsibility | AI checks support and conflicts; HUMAN assesses warrant admissibility |
| Control | Check time, scope of applicability, alternative evidence, and inference steps |
| Output / Gate | Conclusion and limits of what is established are explicit |

**STATUS:** The above is a structured account of the presentation. The formal fields and requiredness below are **APPROVED IN v1.5**.

### 5.7 DECIDE — DSP

Decision & Scope Package.

| Element | Description |
| --- | --- |
| Input | VRP, authority, constraints, available actions |
| Operations and responsibility | AI proposes options; HUMAN approves the status and next step |
| Control | Check authority, status, rationale, actor, deadline/revisit condition |
| Output / Gate | Action is authorized by the appropriate subject |

**STATUS:** The above is a structured account of the presentation. The formal fields and requiredness below are **APPROVED IN v1.5**.

## 6. Formal schemas of the seven artifacts

The following fields, types, and invariants form the recommended implementation contract; they were not presented as JSON Schema in the original presentation. Common fields: artifact_id (string), version (string), question_id (string), created_at (ISO date/time), owner (string), status (DRAFT/REVIEW/APPROVED), source_refs (array of IDs), reviewer (string or null), approved_at (date or null).

### 6.1 VBQ

| Field | Type | Required* | Purpose |
| --- | --- | --- | --- |
| question_text | string | Yes | Original business question |
| objective | string | Yes | Purpose of the answer |
| as_of_date | date | Yes | As-of date |
| scope_in / scope_out | array | Yes | Included scope and exclusions |
| stakeholders | array | Yes | Stakeholders |
| acceptance_criteria | array | Yes | Answer acceptance criteria |

### 6.2 MVTC

| Field | Type | Required* | Purpose |
| --- | --- | --- | --- |
| entity_types | array | Yes | Entity types |
| entities | array | Yes | Entities and IDs |
| relation_types / relations | array | Yes | Directed relations and semantics |
| claims | array | Yes | Claims and epistemic statuses |
| rules | array | Yes | Rules with applicability |
| evidence_needs | array | Yes | Evidence still needed |
| constraints | array | Yes | Model constraints |

### 6.3 TCBS

| Field | Type | Required* | Purpose |
| --- | --- | --- | --- |
| realm_id | string | Yes | Target realm |
| approved_plan_id | string | Yes | Approved plan |
| write_log | array | Yes | Actual writes |
| readback_snapshot | object | Yes | Read-back model |
| comparison_result | PASS/FAIL | Yes | Comparison outcome |
| diffs | array | Yes | Differences |

### 6.4 GCP

| Field | Type | Required* | Purpose |
| --- | --- | --- | --- |
| source_id / source_version | string | Yes | Source identification |
| evidence_id / locator | string | Yes | Exact fragment |
| claim_id | string | Yes | Supported claim |
| warrant_id | string | Conditional | Rule for a derived conclusion |
| validity / scope | object | Yes | Time and scope of applicability |
| gaps / conflicts | array | Yes | Gaps and contradictions |

### 6.5 TCAC

| Field | Type | Required* | Purpose |
| --- | --- | --- | --- |
| connector / interface | string | Yes | MCP or another mechanism |
| realm_id / resource_scope | string | Yes | Address and access scope |
| permission_snapshot | object | Yes | Permissions |
| request_log | array | Yes | Actual requests |
| retrieved_ids | array | Yes | Retrieved entities |
| access_result | PASS/FAIL | Yes | Retrieval check |

### 6.6 VRP

| Field | Type | Required* | Purpose |
| --- | --- | --- | --- |
| verified_claims | array | Yes | Claims and outcomes |
| evidence_links | array | Yes | Grounds |
| warrant_checks | array | Yes | Rule admissibility |
| assumptions / limitations | array | Yes | Assumptions and limits |
| unknowns / conflicts | array | Yes | Gaps and conflicts |
| verification_result | SUPPORTED/GAP/CONFLICT | Yes | Overall result |

### 6.7 DSP

| Field | Type | Required* | Purpose |
| --- | --- | --- | --- |
| decision_status | enum | Yes | ACT/REQUEST EVIDENCE/ESCALATE/STOP |
| rationale | string | Yes | Justification |
| verification_ref | string | Yes | VRP reference |
| authority | string | Yes | Authorized subject |
| next_action | object | Yes | WHO→DOES WHAT→NEXT |
| constraints / revisit_trigger | array | Yes | Constraints and reconsideration |

* “Required” denotes the approved requirement level for v1.5; exceptions must be documented separately.

## 7. Formal Gates: PASS/FAIL criteria

| Gate | Artifact | PASS criterion | FAIL / restriction |
| --- | --- | --- | --- |
| G1 FRAME | VBQ | Question, objective, date, object, scope, and human approval are present | Do not start MODEL with an ambiguous question |
| G2 MODEL | MVTC | All necessary types and Evidence Needs are described; unknowns are not fabricated | Do not build the graph until sufficiency is approved |
| G3 BUILD | TCBS | WRITE–READ BACK–COMPARE matches; no side effects | FAIL requires correction under a new approved plan |
| G4 GROUND | GCP | Each material Claim has exact Evidence/locator or is explicitly UNKNOWN | Do not promote unsupported content to KNOWN |
| G5 CONNECT | TCAC | Actual retrieval log and retrieved IDs within the correct scope | Authentication without retrieval is insufficient |
| G6 VERIFY | VRP | Each material conclusion is checked against evidence, warrant, time, and conflicts | Without an admissible rule, do not claim DERIVED |
| G7 DECIDE | DSP | Status, authority, rationale, WHO→DOES WHAT→NEXT are present | Do not assign ACT without authority |

A machine PASS against a schema means structural conformity only; semantic sufficiency and authority require REVIEW/HUMAN. No automatic “self-repair” after FAIL without an approved change plan.

## 8. Brief application example: contract approval

**Illustration, not a training case or evidence of a real-world conclusion:** the question is who has authority to approve a contract as of a specified date. FRAME identifies the contract, date, and distinction between approval and signing. MODEL defines roles, documents, relations, and Evidence Needs. BUILD checks the actual model against an approved plan. GROUND links material Claims to verifiable Evidence and locators. CONNECT confirms actual retrieval of the relevant context. VERIFY checks the applicability of rules and dates. DECIDE records the permissible decision status and next step. Appointment to a role alone does not establish signing authority.

Complete training documents, exercises, Evidence Packs, and guided walkthroughs belong to the separate commercial course and are not part of the open TCM edition.

## 9. Brief application example: equipment replacement

Equipment renewal decisions should consider operational context and employee experience alongside aggregated failure data. This may change the decision hypothesis, but economic benefit must be measured after implementation.

Value chain: TTD → TTC (context) → TTI (insight) → decision → TTM (implementation) → TTV (measured value). Hard data and Soft data complement each other.

## 10. Method evaluation protocol

Answer A: AI accesses the original source documents directly; Answer B: the same question is answered through structured Trusted Context in Onto/MCP without re-uploading the source documents. No superiority of B is presumed.

| Metric | Operational definition [v1.5 editorial formulation] |
| --- | --- |
| Evidence accuracy | Share of Evidence links verified against original fragments |
| Warrant correctness | Share of conclusions supported by admissible rules |
| Traceability | Share of material Claims with Source, locator, and version |
| Gate pass rate | Share of Gates passed on first review |
| Labor effort | Time per stage, HUMAN/REVIEW interventions |
| BUILD discrepancies | Number of WRITE–READ BACK–COMPARE differences |
| Uncertainty | Share of explicitly preserved UNKNOWN/CONFLICTED statuses |
| Authority compliance | Share of actions with verified authority |

Experiment controls: same question and Evidence Pack, fixed assessment criteria, preserved answer versions, independent review, and a discrepancy log. Mere persuasiveness of the text is not a valid comparison.

## 11. Limitations, risks, and change management

- Sources may be outdated, incomplete, contradictory, or legally inapplicable.
- A graph does not guarantee truth; technical BUILD verification does not replace VERIFY.
- AI inference may produce Epistemic Rule Hallucination: the facts are correct but the inference rule is fabricated.
- Changes to Source, Rule, scope, or authority require assessing affected Claims and re-verifying dependent VRP/DSP artifacts.
- Do not publish confidential Evidence in Onto without explicit authorization and an established storage policy.
- Application of TCM in a particular industry requires local procedures and designated responsible parties.

## 12. Review of method application results

| Artifact | Evidence to be checked |
| --- | --- |
| VBQ | The question was not substituted |
| MVTC | The model is sufficient for VBQ |
| TCBS | Actual model matches the plan |
| GCP | Grounds are traceable and UNKNOWN preserved |
| TCAC | Actual retrieval is confirmed |
| VRP | Evidence and limitations are explicit |
| DSP | Action does not exceed authority |

During a method application review, the practitioner explains: what AI prepared; the precise grounds; why passing each Gate is justified; and who has authority to decide. An Excel file or graph alone does not establish mastery of the method.

## 13. Provenance, bibliography, and license

Provenance classes: REFERENCE/STANDARD (defined by an external source), ADAPTED (reinterpreted in TCM), TCM ORIGINAL (an original operational construction). The presentation attributes the seven-stage composition, MVTC, and decision statuses to TCM ORIGINAL; Source–Evidence–Claim is described as an adaptation. References to standards do not validate the effectiveness of the method as a whole.

- W3C PROV-O: https://www.w3.org/TR/prov-o/
- W3C RDF 1.1: https://www.w3.org/TR/rdf11-concepts/
- W3C OWL 2: https://www.w3.org/TR/owl2-overview/
- NIST AI RMF: https://www.nist.gov/itl/ai-risk-management-framework
- NIST SP 800-53: https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final
- ISO/IEC 15026-2 — Assurance case.
- Gruber, T. R. (1993), A Translation Approach to Portable Ontology Specifications.
- Dey, A. K. (2001), Understanding and Using Context.
- Kelly, T. P. (1998), Arguing Safety: A Systematic Approach to Managing Safety Cases.

## Appendix A. Pre-publication checklist

- Confirm authorial attribution and licensing rights for all included elements.
- Approve the formal fields, requiredness, and identifiers of all seven artifacts.
- Approve the exact Gates and the procedure for resolving FAIL.
- Compare the “Stroypak” case against the S0–S4 originals and fill in locators.
- Check access, storage, and publication policies for Onto data.
- Run a pilot and record metric results.

## Approval record and version control

Document: TCM-NORM-1.5 | Status: APPROVED | Date: 15 October 2026 | Basis: TCM Method Reference v1.5 EXAMPLES (39 slides).

Basis for approval: the method owner's confirmation of the formal schemas for seven artifacts and the PASS/FAIL criteria for seven Gates in the working correspondence. This is editorial approval, not independent certification or an electronic signature.

Changes after approval must be recorded in a separate version. The meanings of statuses, Gates, or required fields must not be changed without revising the specification.

## Normative appendices

Templates for the seven artifacts and the Gate-control log are supplied as separate editable files in the release package. In case of discrepancy, this specification takes precedence.
