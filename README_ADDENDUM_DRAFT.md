# ProjectXP — README Explanation Draft

## In plain language

A simple browser project tracker where you add projects, record features and see progress in one place.

## How to use it

Create a project, add features, mark each feature as planned/in progress/done and review the progress summary. Data is saved in the browser used to access the app.

## Technical explanation

A static single-page HTML/CSS/JavaScript application. Project and feature records are saved in browser localStorage. It supports progress percentages, repository/demo URLs, feature states and bundled examples. Local browser storage is not multi-user sync or a server backup.

Document the state model, localStorage keys, validation rules, progress calculation, import/export format and recovery behavior for malformed storage.

## Limitations

The current storage model is local to one browser profile. Clearing site data can remove it. It does not currently imply account login, cloud sync or backups.

## Contribution

See FEATURE_UPGRADE_PLAN.md and CONTRIBUTING.md; log verified changes in ACTIVITY_LOG.md.
