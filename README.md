### What Was Tested and Why

The suite validates business-critical user journeys where failures would directly impact revenue or user trust:

* **Authentication & Security:** Login flows for multiple user roles (Standard, Locked-out, Problem).
* **Core E-commerce Flows:** Product browsing, dynamic sorting, cart persistence, and a multi-step checkout process.
* **Data Integrity:** Mathematical validation of sub-totals, taxes, and final order confirmations.
* **API Layer:** Direct REST API testing for products, users, and JWT-based authentication to ensure backend stability and correct data structure.

### What Was Automated and Why

To maintain a high standard of quality while enabling fast feedback cycles, the following were automated:

* **88 UI End-to-End Tests:** Comprehensive coverage of the frontend to prevent regressions in user-facing features.
* **35+ API Tests:** Validating endpoints to catch logic errors before they reach the UI.
* **Cross-Browser Testing:** Ensuring compatibility across Chrome, Firefox, and Electron.
* **CI/CD Pipeline:** Integrated via GitHub Actions to run tests automatically on every pull request, ensuring that no breaking changes are merged.

### Tools Used and Why

* **Cypress:** Chosen for its fast execution, built-in waiting mechanisms, and excellent developer experience.
* **JavaScript:** Provides flexibility and wide community support for writing clean automation scripts.
* **Page Object Model (POM):** Implemented to separate test logic from UI selectors, making the framework easier to update when the UI changes.
* **Fixtures (JSON):** Used for Data-Driven Testing to manage credentials and test data without hard-coding.
* **GitHub Actions & Mochawesome:** Used for continuous integration and generating visual HTML reports with screenshots/videos on failure.

### How to Run Tests

**Prerequisites:** Node.js (v18+) and Git.

**Installation:**

```bash
git clone https://github.com/anatolii-v/js-cypress.git
cd js-cypress
npm install

```

**Execution:**

```bash
# To open the interactive Cypress Test Runner:
npx cypress open

# To run all tests in Headless mode (CLI):
npx cypress run

# To run a specific module (e.g., Checkout):
npx cypress run --spec "cypress/e2e/checkout/**/*.cy.js"

```

