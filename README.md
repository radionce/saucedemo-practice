# Playwright + TypeScript: Learning Automation by Practice

This repository documents how I'm learning UI test automation with Playwright and TypeScript. Each part of the work lands through its own pull request, the same way it would on a real project.

## What I built
- End-to-end UI tests for [saucedemo.com](https://www.saucedemo.com) (login, inventory, cart, checkout), running in Chromium, Firefox and WebKit
- A shared login helper and `beforeEach` hooks to keep tests short and independent
- Positive and negative scenarios: invalid credentials, locked-out user, access to pages without login, form validation
- Data checks on the product list: price format with regular expressions, unique product images, item counts
- A known site defect (cart contents survive logout), recorded with `test.fail` and written up as a bug report

## What I practiced
- Choosing stable locators (`getByRole`, `getByLabel`, `getByTestId`) instead of brittle CSS paths
- Web-first assertions and auto-waiting instead of fixed timeouts
- Handling SPA race conditions and finding flaky tests with `--repeat-each`, UI mode and the trace viewer
- Project setup: `playwright.config.ts`, `baseURL`, `testIdAttribute`, projects, reporters
- Git workflow: feature branches, small pull requests with clear descriptions, reviewing my own diffs

## How to run

npm install

npx playwright install

npx playwright test

npx playwright show-report

