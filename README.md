# ProjectXP

**A browser-based project tracker for recording milestones, progress, and feature status.**

[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen)](https://gitcoder12.github.io/ProjectXP/)
[![License](https://img.shields.io/badge/license-see%20LICENSE-lightgrey)](LICENSE)

ProjectXP is a lightweight single-page tool for keeping a visual overview of software projects. Add project details, record feature states, and track progress from the browser.

## Features

- Create and edit project records.
- Track a project progress percentage.
- Record repository and live-demo URLs.
- Mark individual features as done, in progress, or planned.
- Save project data in browser local storage.
- Start with bundled demonstration projects.

## Quick Start

Open `index.html` in a modern browser, or run a local static server:

```bash
git clone https://github.com/Gitcoder12/ProjectXP.git
cd ProjectXP
python -m http.server 8000
```

Open `http://localhost:8000`.

## Tech Stack

HTML · CSS · Vanilla JavaScript · Browser Local Storage

## Scope and Limitations

Project data is stored in the browser's local storage. It is not synchronized to a server or shared across browsers and devices. Demo projects are seeded example records; their progress values are not connected to GitHub activity or deployment telemetry.

## License

See [LICENSE](LICENSE).

---

## Project handbook

- [Activity log](ACTIVITY_LOG.md) · [Feature upgrade plan](FEATURE_UPGRADE_PLAN.md)
- [Company and team fit](COMPANY_FIT.md) · [README explanation draft](README_ADDENDUM_DRAFT.md)
- [README quality checklist](README_QUALITY_CHECKLIST.md)
- [Contributing](CONTRIBUTING.md) · [Agent instructions](AGENTS.md) · [Agent skills](SKILLS.md)

## Understanding the project

### In plain language

A simple browser project tracker where you add projects, record features and see progress in one place.

### Technical and research view

A static single-page HTML/CSS/JavaScript application. Project and feature records are saved in browser localStorage. It supports progress percentages, repository/demo URLs, feature states and bundled examples. Local browser storage is not multi-user sync or a server backup.

Document the state model, localStorage keys, validation rules, progress calculation, import/export format and recovery behavior for malformed storage.

For future work, see [FEATURE_UPGRADE_PLAN.md](FEATURE_UPGRADE_PLAN.md), [ACTIVITY_LOG.md](ACTIVITY_LOG.md), [COMPANY_FIT.md](COMPANY_FIT.md) and [CONTRIBUTING.md](CONTRIBUTING.md).
