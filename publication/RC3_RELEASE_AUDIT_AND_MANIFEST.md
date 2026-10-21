# TCM v1.5 — RC3 Release Audit and distribution manifest

**Audit date:** 2026-10-21. **Status:** CONDITIONAL / NOT RELEASED. **Basis:** actual GitHub default-branch recursive tree, RU/EN reference texts, template license headers, publication and site documents. This manifest governs the *separately assembled distribution package*, not the entire repository or GitHub's automatic source-code archives.

## Distribution allowlist — RC3

Include only the following paths, with their actual contents rechecked at packaging time:

1. `README.md`
2. `LICENSE`
3. `CITATION.cff`
4. `CHANGELOG.md` — only after checking release language
5. `docs/ru/method-reference.md`
6. `docs/en/method-reference.md`
7. `references/REFERENCES.md` — bibliography must be finalized
8. `templates/ru/schema-aligned/VBQ.md`
9. `templates/ru/schema-aligned/MVTC.md`
10. `templates/ru/schema-aligned/TCBS.md`
11. `templates/ru/schema-aligned/GCP.md`
12. `templates/ru/schema-aligned/TCAC.md`
13. `templates/ru/schema-aligned/VRP.md`
14. `templates/ru/schema-aligned/DSP.md`

**Total allowlisted paths: 14.** This is a planned manifest, **not** proof that all 14 files have passed release review. The release archive must be assembled explicitly from the allowlist; do not use the full repository checkout.

## Excluded from the distributable package

- `examples/STROYPACK_END_TO_END_TEST.md`: detailed commercial-course scenario remains in the Git repository; **not suitable for a public course-free distribution**. Assess whether to move to private storage; Git history remains accessible even after deletion.
- `examples/README.md`: refers to course examples and is excluded.
- `templates/ru/{VBQ,MVTC,TCBS,GCP,TCAC,VRP,DSP}.md`: original CC BY-NC-SA educational templates. Do not distribute under public CC BY-SA.
- `site/**`: separate web deployment; `site/docs/en/method-reference.md` is an obsolete English overview and `site/docs/ru/method-reference.md` is an older copy. Must be synchronized before web publication.
- `publication/**`: internal release audits, deployment tasks, draft metadata, and operational plans; not part of the method distribution.
- Source 39-slide PPTX, source S0–S4 documents, training packs, prompts, workbook, mentor notes, proprietary and third-party assets.

## Content audit of §§10 and 12

- RU/EN §10 describes an optional A/B method evaluation protocol (direct access vs structured context); it contains no actual source documents, prompts, or participant worksheets. **Retain** as an evaluation method, not as proof of comparative advantage.
- RU/EN §12 has been edited to replace learner-mastery language with correctness of method application. **Retain** the generic review criteria.
- RU/EN §§8–9 now contain only short abstract examples; no original Evidence Pack, named company, or numerical laptop exercise is reproduced.

## Critical release blockers

1. **Public-repository exposure:** a restricted course-derived end-to-end example and seven CC BY-NC-SA template files remain visible in a GitHub repository. A distribution allowlist does not make publicly accessible repository content private. Decide on private migration and history remediation before advertising the repository as course-free.
2. **GitHub release assets:** GitHub automatically provides source archives for a tagged commit. A custom allowlisted ZIP cannot prevent access to full tagged source. Therefore **do not tag or create a GitHub Release** on this repository until restricted files and history have been addressed; consider a separate clean public-release repository.
3. **Third-party rights:** authorial CC BY-SA consent is documented, but third-party quotations, borrowed diagrams and bibliographic references have not received final clearance.
4. **Bilingual review:** editorial parity was checked; independent professional translation review has not occurred.
5. **Bibliography:** ISO/IEC 15026-2 edition and academic source details need verification. External references are conceptual antecedents, not endorsement.
6. **Website copies:** `site/docs/**` is stale relative to `docs/**`. Do not deploy the stale site package.
7. **Technical QA:** automated link checks, Markdown linting, full content inventory of all release files, and signed author acceptance remain pending.

## Audit verdict

**Content scope for an open-method package: DEFINED. Distribution clearance: FAIL / HOLD.** Next action: create a clean release-only repository or remediate public repository and history, then perform final QA and author approval. No GitHub Release, DOI or assertion of third-party legal clearance has been made.
