# Agent Instructions — ProjectXP

Read README.md, CONTRIBUTING.md and FEATURE_UPGRADE_PLAN.md first.

- Preserve existing user data and inspect storage schema before changing it.
- Do not clear localStorage or migrate data destructively without a tested migration path.
- Validate user text, numeric progress, feature states and URLs.
- Add tests for corrupted storage, old schemas and import/export round trips.
- Keep local-only and server-synced behavior clearly distinguished.
- Work on a branch and submit a PR with browser/test evidence; do not deploy autonomously.
