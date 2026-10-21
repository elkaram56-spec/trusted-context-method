# Deployment plan

1. Create public repo: https://github.com/elkaram56-spec/trusted-context-method (requires account-owner action).
2. Push files from this package. Suggested commands:

```bash
git init
git add .
git commit -m "TCM v1.5 Open Edition 1.0 release candidate"
git branch -M main
git remote add origin https://github.com/elkaram56-spec/trusted-context-method.git
git push -u origin main
```

3. Complete publication checklist and remove release-candidate disclaimers only after editorial QA.
4. Coordinate IM Center CMS deployment under an agreed route (proposed `/tcm/`; this URL has NOT been verified or reserved). Upload static site; fix relative Markdown document links or publish generated HTML documentation.
5. Create Zenodo account at https://zenodo.org; enable GitHub integration; create a GitHub release only when approved; verify deposit metadata and obtain DOI.
6. Update website, CITATION.cff and README with verified DOI and published URLs; announce the release.

Do not push SOURCE_INTERNAL_DO_NOT_PUBLISH.docx (stored outside repository).
