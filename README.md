# ProjectXP
A smart developer project progress tracker with completion stats, feature status, and visual progress insights for coding repositories.
Live: https://gitcoder12.github.io/ProjectXP/


---

## AI-maintained project notes (secondary — 2026-11-13)

This section supplements the maintainer-authored README above. The original text has been restored verbatim from Git-history baseline `de597bb46e6f58474ff1401e8f281cd7b9f03de4`; this addendum does not replace or certify the original claims.

- The current source tree, runtime data and tests are the implementation source of truth. A roadmap item, draft PR or AI-generated description is not a shipped feature by itself.
- Preserve real and maintainer-provided data. Never silently substitute generated or placeholder data. Clearly label and isolate synthetic fixtures.
- Mark unverified sources, identifiers, metrics, benchmark results and external claims as unknown/unverified rather than guessing.
- Verify setup, execution, tests and public claims against the exact current commit before using this repository in a job, research or academic application.
- See [MODEL_AUDIT_ROUTER.md](MODEL_AUDIT_ROUTER.md) for independent model review instructions and the merge gate.

---

## Engineering Audit & Handover — 2026-11-17

**Reviewed commit:** `c6cfae7d0c9e29f5a2055d173480203e28b203ef` (`main`). Static inspection covered the inline storage, import, and project-management logic in `index.html`.

### Confirmed findings
- Project data is stored in browser `localStorage`; it is not synchronized across devices or browsers.
- `load()` seeds demo projects whenever the loaded project array is empty. As a result, an intentionally empty saved portfolio (including an empty import) is repopulated with demo records on the next load.
- `importData()` replaces the entire current project array after confirmation. Users should export a backup before importing.
- No automated test suite was found in the reviewed tree.

### Next actions
1. Distinguish first-run/no-storage from a deliberately saved empty array; do not reseed after a valid empty save.
2. Validate imported project objects and provide a backup/restore path before replacement.
3. Add tests for first run, empty saved state, import/export round trips, malformed imports, and localStorage failures.

**Verification status:** static source inspection only; browser behavior and import/export tests remain unverified.

---

## Examples Used
- Tracking feature completion across a software project
- Comparing planned milestones with completed work
- Reviewing progress across multiple repositories


---

## Comparison with Existing Open-Source Projects

ProjectXP is described as a developer-oriented project progress tracker that summarizes completion, feature status and repository progress. The following tools provide adjacent project-management and engineering-visibility references.

| Project | Established focus | Relationship to ProjectXP |
|---|---|---|
| [OpenProject](https://github.com/opf/openproject) | Full project-management platform with work packages, timelines and collaboration | Much broader work-management suite; ProjectXP's intended focus is a compact progress view for software projects and repositories. |
| [Plane](https://github.com/makeplane/plane) | Open-source issue/project management with cycles, modules and roadmaps | A broader planning and execution workspace; ProjectXP aims to summarize project progress rather than replace issue tracking. |
| [Hygieia](https://github.com/CapitalOne/Hygieia) | Engineering dashboard aggregating software-delivery pipeline metrics | A closer engineering-visibility reference; ProjectXP's stated distinction is feature/completion-oriented tracking rather than a full DevOps metrics dashboard. |

### Where ProjectXP is different
- **Repository-centric progress:** the product is framed around project completion and feature status for coding work.
- **At-a-glance insights:** its intended value is a lightweight view of progress rather than a full issue-management workflow.
- **Developer portfolio context:** the concept can help developers review multiple personal projects in one place if repository data is kept current and attributable.

### Where established projects are stronger
OpenProject and Plane provide mature collaboration and planning workflows. Hygieia offers a more established engineering-dashboard concept. ProjectXP should not claim reliable automatic completion measurement unless it can explain how it infers status from issues, commits, tests or explicit user updates.

### Evidence and limitations
Document whether progress is manually entered or inferred, how stale data is handled, and how imports/exports preserve user data. Completion percentages are only as trustworthy as their underlying task definitions and update process. This is a positioning comparison, not a feature-parity or productivity benchmark.
