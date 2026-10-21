# TCM v1.5 — RU/EN bilingual reconciliation (21 October 2026)

**Compared:** docs/ru/method-reference.md and docs/en/method-reference.md on the repository default branch. **Status:** editorial structure and identifier check completed; independent professional translation review not performed.

## Verified parity
- 13 numbered sections, seven stage subsections (§5.1–5.7), seven formal schemas (§6.1–6.7), seven G1–G7 Gate rows, Appendix A, approval record, and normative appendices appear in both editions.
- All 57 checked shared field identifiers occur in both versions. Requiredness, enums and types in §§6–7 were reviewed editorially; this is not JSON Schema validation.
- KNOWN/DERIVED/INFERRED/UNKNOWN/CONFLICTED; AUTO/REVIEW/HUMAN; ACT/REQUEST EVIDENCE/ESCALATE/STOP are preserved.
- The examples retain the dates 25.05.2026 and 02.05.2026, Order No. 41, S0–S4, 20 laptops, four years, 18 failures/month and a hypothesis of eight replacements.
- Neither language states that Onto/MCP or an evidence graph proves truth or confers authority.

## Editorial issues to resolve before final sign-off
1. **English framing:** Russian “ЗАЧЕМ / ПОЧЕМУ / КТО” is rendered “WHY / ON WHAT GROUNDS / WHO”. This is semantically defensible but not word-for-word; preserve the Russian original alongside English terms in terminology guidance if necessary.
2. **EN §5.7:** “Action is authorized by the appropriate subject” must not be read as saying every DSP outcome authorizes ACT. REQUEST EVIDENCE, ESCALATE and STOP are valid outcomes. The same ambiguity is present in RU and should be resolved through a versioned editorial erratum rather than an untracked normative change.
3. **EN §7:** “Proposed PASS” accurately reflects the RU table heading “Предлагаемый PASS” although the same reference says Gates were author-approved. The inconsistency is inherited from RU; correct only through controlled editorial revision.
4. **EN §8:** “approval” versus “signing” refers to contract coordination/approval, not delegation of signature authority. A terminology note could avoid legal-process ambiguity.
5. **EN bibliography:** full publication details for ISO/IEC 15026-2, Gruber, Dey and Kelly still require external bibliographic verification; neither language should claim this is complete.
6. **Release language:** English is a complete editorial translation, **not** a certified or independently peer-reviewed translation.

## Disposition
**Structural parity: PASS (editorial).** **Terminology/source/rights release gate: OPEN.** No real-case G1–G7 execution or external certification is implied.
