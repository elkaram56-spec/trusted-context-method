# Trusted Context Method (TCM) — Method Reference v1.5

**Open Edition 1.0 · English methodological overview**

**Editorial status:** This English document is a structured overview, **not yet a complete certified translation** of the Russian method reference. The Russian document is the detailed reference pending bilingual editorial reconciliation.

## Purpose and scope

TCM is an authorial, evidence-oriented seven-stage methodology for constructing, grounding, verifying and governing context used by AI systems to support decisions and authorized actions. It is not a NIST, W3C or ISO standard. Onto and MCP are implementation options, not requirements.

## Seven stages, seven artifacts, seven Gates

| Stage | Artifact | Purpose | Gate criterion |
| --- | --- | --- | --- |
| FRAME | VBQ — Validated Business Question | Frame the decision question, date, scope, acceptance criteria and authority boundary. | Question, scope, decision criteria and temporal frame are explicit. |
| MODEL | MVTC — Minimum Viable Trusted Context | Model the smallest sufficient set of entities, relations, rules, claims, evidence needs and unknowns. | The model is minimal, sufficient and explicit about unknowns. |
| BUILD | TCBS — Trusted Context Build Snapshot | Implement a reviewed model; record READ → PLAN → APPROVE → WRITE → READ BACK → COMPARE. | Read-back matches the approved plan without unauthorized side effects. |
| GROUND | GCP — Grounded Context Package | Link each claim to identifiable source, exact evidence locator and explicit inference rule or warrant. | Evidence is traceable; gaps and conflicts are disclosed. |
| CONNECT | TCAC — Trusted Context Access Check | Demonstrate actual authorized retrieval using connector calls, identifiers and permission scopes. | Retrieval and permissions are demonstrated, not merely configured. |
| VERIFY | VRP — Verification Result Package | Evaluate claims, evidence, rules, dates, scope, contradictions and unknowns. | Inferences are justified and limits made explicit. |
| DECIDE | DSP — Decision & Scope Package | Record ACT / REQUEST EVIDENCE / ESCALATE / STOP with rationale, authority and next owner/action. | The proposed action is justified and within authority. |

## Three independent control dimensions

1. **Epistemic status:** KNOWN, DERIVED, INFERRED, UNKNOWN, CONFLICTED.
2. **Delegation level:** AUTO, REVIEW, HUMAN.
3. **Decision disposition:** ACT, REQUEST EVIDENCE, ESCALATE, STOP.

These dimensions must not be collapsed: KNOWN ≠ ACT; UNKNOWN ≠ FALSE; UNKNOWN ≠ STOP; AUTO ≠ KNOWN; HUMAN ≠ VERIFIED; RETRIEVED ≠ GROUNDED ≠ VERIFIED; SUPPORTED ANSWER ≠ ACT.

## Evidence and reasoning chain

Source → Evidence (exact locator) → Claim + Rule/Warrant → Verification → Authority → Decision. Provenance and data lineage are distinct; neither guarantees truth. Grounded Context ≠ Grounded Reasoning.

## Core operational controls

- BUILD: READ → PLAN → APPROVE → WRITE → READ BACK → COMPARE.
- GROUND: identify a source, exact evidence locator, claim, warrant and gaps.
- CONNECT: demonstrate retrieval with concrete returned identifiers and authorization scope.
- VERIFY: preserve contradictory evidence and UNKNOWNs; do not invent inference rules.
- DECIDE: distinguish a supported answer from an authorized action and name WHO → DOES WHAT → NEXT.

## Illustrative cases and validation

- **Stroypak (training example):** Who is responsible for approval of Contract No. 1 as of 25 May 2026? An evidence pack S0–S4 is examined; appointment to a role does not alone imply signature authority. The final answer must not be fabricated.
- **Laptop replacement:** The illustrative case contrasts replacing 20 laptops with a hypothesis of targeted replacement of eight; it is not an independently validated financial result.
- **Comparison protocol:** Compare direct AI use of original documents (Answer A) with AI using structured context through Onto/MCP (Answer B). No performance advantage is presumed. Preserve the same question and evidence pack, independently evaluate correctness, provenance, limitations and action legitimacy.

## Known limitations

Sources can be outdated, incomplete or contradictory; a graph is not proof of truth; technical build verification does not replace epistemic verification; inference rules may be hallucinated; source/rule/authority changes can invalidate downstream results. Protect confidential evidence.

## Source and formalization status

Method structure and illustrative cases originate in the 39-slide TCM Method Reference v1.5 EXAMPLES. The artifact schemas and PASS/FAIL Gates were subsequently approved as the author's v1.5 formalization. Consult the full Russian reference for field-level schemas and Gate tables. An aligned full English translation is a publication prerequisite.

## Licensing

Intended public license: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). Third-party content remains subject to its own rights. Do not reuse material from the separate CC BY-NC-SA 4.0 training edition without rights review.
