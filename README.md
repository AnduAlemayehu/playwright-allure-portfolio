# Playwright Automation QA Portfolio

A UI test automation framework built with **Playwright and TypeScript**, covering desktop and mobile experiences with Allure test reporting.

## Allure Test Report

**[View the Live Allure Report](https://andualemayehu.github.io/playwright-allure-portfolio/)**

## Tech Stack

- **Playwright** — browser automation
- **TypeScript** — test implementation
- **Page Object Model (POM)** — maintainable test architecture
- **Allure Report** — test execution reporting
- **GitHub Actions** — CI-ready configuration
- **Docker** — container-ready setup

## Test Coverage

| Platform | Automated Scenarios |
|---|---:|
| Desktop | 51 |
| Mobile | 45 |
| **Total** | **96** |

Coverage includes:

- Demo account login and authentication
- Sports navigation and event displays
- In-play events and market pages
- Page-loading performance measurements
- Bet slip content validation
- Profile editing and saving

## Framework Architecture

The framework separates tests, page objects, and platform-specific behavior.

```text
Playwright Test Suite
├── Desktop
│   ├── Fixtures & Version Detection
│   └── Page Objects
└── Mobile
    ├── Fixtures & Version Detection
    └── Page Objects

Shared Test Scenarios
        │
        ▼
Version-Specific Page Objects
        │
        ▼
Test Execution & Allure Report
```

### Key Design Decisions

- **Page Object Model:** Separates UI interactions from test scenarios.
- **Desktop and mobile separation:** Keeps platform-specific tests and page objects organized.
- **UI version detection:** Selects the appropriate page objects for supported UI versions.
- **Dynamic waits:** Reduces reliance on fixed sleep delays.
- **Performance checks:** Measures selected page-loading behavior.
- **Test safeguards:** Includes configuration to prevent accidental `test.only` usage.

## Project Structure

```text
tests/
├── desktop/
└── mobile/

pages/
├── desktop/
└── mobile/
```

## Getting Started

Install dependencies:

```bash
npm install
npx playwright install
```

Run all tests:

```bash
npx playwright test
```

Run mobile tests:

```bash
npx playwright test tests/mobile
```

Run desktop tests:

```bash
npx playwright test tests/desktop
```

Run a specific test:

```bash
npx playwright test tests/mobile/mobile-inplay-events.spec.ts
```

View the Playwright HTML report:

```bash
npx playwright show-report
```

## UI Version Handling

The framework detects the application UI version and selects the corresponding login and page-object implementations. This allows shared test scenarios to work across supported UI versions while keeping version-specific behavior isolated.

Desktop and mobile implementations follow the same architectural principle, making the framework easier to maintain as the application evolves.

## Project Highlights

- 96 automated desktop and mobile test scenarios
- Maintainable, page-object-based architecture
- UI version-aware test execution
- Performance-oriented test coverage
- Allure reporting for test analysis
- CI-ready and Docker-ready configuration

---

**Author:** Andu Alemayehu  
**Focus:** QA Automation · Playwright · TypeScript · Test Framework Design
