# Playwright Automation

This project uses Playwright Test for browser automation and UI validation across desktop browsers.

## Prerequisites

- Node.js LTS
- npm

## Installation

```bash
npm install
npx playwright install
```

If you are running on Linux and need system dependencies:

```bash
npx playwright install --with-deps
```

## Run tests

This repository does not define custom npm scripts, so tests are run directly through Playwright:

```bash
npx playwright test
```

Run a single browser project:

```bash
npx playwright test --project=chromium
```

Run a specific test file:

```bash
npx playwright test tests/example.spec.js
```

Open the HTML report after a run:

```bash
npx playwright show-report
```

## Project structure

```text
.
├── package.json
├── playwright.config.js
├── tests/
│   └── example.spec.js
└── README.md
```

## Configuration

The Playwright configuration is defined in [playwright.config.js](playwright.config.js). It currently includes:

- test directory: `./tests`
- parallel execution enabled
- HTML reporter enabled
- traces captured on first retry
- browser projects for:
  - Chromium
  - Firefox
  - WebKit

## Example tests

The sample test file checks basic behavior on the Playwright website, including:

- page title contains "Playwright"
- the "Get started" link is clickable
- the "Installation" heading is visible after navigation

## Notes

This project is set up as a basic Playwright starter and can be expanded with additional test suites, fixtures, and CI integration as the project grows.
