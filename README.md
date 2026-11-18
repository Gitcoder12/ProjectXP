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

## Branch Activity & Development History

**Audit date:** 2026-11-18 · **Comparison base:** `main`

| Branch | Difference from `main` | Observed work / changed paths |
|---|---:|---|
| `docs/portfolio-operating-kit-2026-11-13` | 4 ahead / 3 behind | Activity log, agent guidance, company-fit notes, feature plan, README support docs and skills; README has removals as well as additions |
| `docs/project-status-2026-11-16-projectxp` | 1 / 1 | Project status snapshot: `PROJECT_STATUS.md` |
| `docs/status-inventory-2026-11-16-v1` | 1 / 1 | Project status inventory: `PROJECT_STATUS.md` |

### Open pull requests observed during this audit

- [PR #3 — project status snapshot](https://github.com/Gitcoder12/ProjectXP/pull/3)
- [PR #2 — project status snapshot](https://github.com/Gitcoder12/ProjectXP/pull/2)
- [PR #1 — project handbook and collaboration guides](https://github.com/Gitcoder12/ProjectXP/pull/1)

**Review note:** The portfolio branch includes README removals as well as additions. Review its diff carefully before merging. No branches have been merged or deleted by this documentation update.
