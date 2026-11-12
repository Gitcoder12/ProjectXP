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
