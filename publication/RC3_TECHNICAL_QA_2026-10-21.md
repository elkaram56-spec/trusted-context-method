# TCM v1.5 — RC3 technical QA report

**Date:** 2026-10-21. **Scope:** current main branch after course-file cleanup. **Status:** CONDITIONAL PASS for checked structural controls; NOT a release authorization.

## Verified from GitHub contents
- **Current branch inventory:** 38 tracked files at initial audit head `70b5081c7d72a9e55a4cf457e6791c7066e337c5`. The eight course-only paths previously identified are absent. Seven schema-aligned public templates are present.
- **Canonical/site text:** `docs/ru/method-reference.md` equals `site/docs/ru/method-reference.md`; likewise for English (exact text comparison).
- **Section parity:** both RU and EN normative references contain sections 1–13 in order and seven formal schemas (§6.1–6.7), Gates G1–G7.
- **Normative identifiers:** reviewed §6 field tables and common metadata; RU and EN use the same field identifiers, enum spellings, types and requiredness. Earlier editorial 7/7 template comparisons are recorded in `SCHEMA_ALIGNED_ACCEPTANCE_REVIEW.md`. No executable JSON Schema validator was run.
- **Local Markdown links:** inspected links in README and all seven public templates. Template references `../../../docs/ru/method-reference.md` resolve by path. README's template link was updated to `templates/ru/schema-aligned/`.
- **Static site:** inspected href targets in `site/index.html`, `site/ru.html`, `site/en.html`: CSS, bilingual switches and local document links target files present in the repository. Page anchors `#method`, `#stages`, `#controls`, `#resources` appear in site navigation; this was a source-level check, not a browser or Tilda deployment test.
- **Metadata:** `CITATION.cff` identifies the author, repository and CC BY-SA 4.0; `publication/zenodo-metadata.json` contains title, author, license, language and version. No DOI is assigned.

## Remaining open items
1. **External URL and runtime QA:** no end-to-end HTTP check of every external reference or production Tilda bilingual switch; no automated Markdown linter run.
2. **Translation:** no independent RU/EN professional editorial sign-off; structural parity is not linguistic certification.
3. **Source and reuse rights:** third-party rights and claim-level provenance still require explicit approval. Source presentation and course files are excluded from current branch but previous Git history remains publicly accessible.
4. **Template status:** seven templates are RC3 editorially accepted, not evidence of actual Gate execution or runtime verification.
5. **Bibliography:** citation details were expanded in `references/REFERENCES.md`, but live publisher/DOI resolution and claim-level mappings were not checked in this QA run.
6. **Repository vs package:** GitHub's auto-generated source archive includes all tracked repository files, including `publication/**` and `site/**`; the earlier 14-file allowlist is a separately assembled distribution scope, not the full tagged source tree.

## Release disposition
**RC3 technical source-level QA: CONDITIONAL PASS. Public GitHub Release/Zenodo DOI: HOLD.** Obtain final rights/translation review, external-link and website checks, and explicit author approval before tagging.
