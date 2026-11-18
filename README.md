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
