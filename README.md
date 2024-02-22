# 💻 Test Automation Framework | API 

[![Cypress](https://img.shields.io/badge/Cypress-17202C?style=for-the-badge&logo=cypress&logoColor=white)](https://www.cypress.io/) 
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://js.org/index.html) 

[![VS Code](https://img.shields.io/badge/VS_Code-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)](https://code.visualstudio.com/)
[![Mochawesome Reports](https://img.shields.io/badge/Mochawesome%20Reports-<COLOR>?style=for-the-badge&logo=mochawesome&logoColor=white)](https://www.npmjs.com/package/cypress-mochawesome-reporter)
[![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions) 

## 📑 Table of Contents
- [Introduction](#introduction)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Running Tests](#running-tests)
- [Project Structure](#project-structure)
- [Configuration](#configuration)
- [Continuous Integration](#continuous-integration)
- [Reporting](#reporting)

## 📖 Introduction
This repository contains a Test Automation Framework built using Cypress and Javascript for automated testing of REST APIs.

## 🛠️ Prerequisites

- [![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/) (v18.16.1 or higher recommended)
- [![npm](https://img.shields.io/badge/npm-CB3837?style=for-the-badge&logo=npm&logoColor=white)](https://www.npmjs.com/) (v9.5.1 or higher recommended)

## ▶️ Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.gamma.bcg.com/Gamma-D/cypress-api-automation-framework.git
   ```

2. Navigate to the project directory:

   ```bash
   cd cypress-api-automation-framework
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

## 🚀 Running Tests

  ```bash
  npm run cy:tests
  ```

## 📁 Project Structure

The tests follow a modular and maintainable structure:

```
|-- .github
|     |-- workflows
|          |-- 01_api_tests.yml
|          |-- 02_api_tests_select_env.yml
|-- cypress
|     |-- e2e
|          |-- tests-reqres
|                |-- login.cy.js
|                |-- register.cy.js
|                |-- users.cy.js
|     |-- fixtures
|           |-- login
|                |-- login-successful.json.json
|                |-- login-unsuccessful.json.json
|           |-- register
|                |-- register-successful.json.json
|                |-- register-unsuccessful.json.json
|           |-- users
|                |-- user_create.json
|                |-- user_update_patch.json
|                |-- user_update_put.json
|     |-- reports
|     |-- support
|          |-- utils
|                |-- EndpointUtils.js
|                |-- RequestBodyUtils.js
|                |-- RequestUtils.js
|                |-- ResponseUtils.js
|                |-- VerificationUtils.js
|          |-- commands.js
|          |-- e2e.js
|-- .gitignore
|-- cypress.config.js
|-- package.json
```

- `cypress/e2e`: Contains the actual test files. You can organize your tests into subdirectories as needed. 
- `cypress/fixtures`: Contains external files (example: user create/update data) that can be used to mock data during tests.
- `cypress/reports`: Contains the report for tests (Logs are attached).
- `cypress/support`: Contains custom commands and global configuration.
- `cypress/support/utils`: Contains the Utilities that provides methods for asserting different conditions on web elements, handling requests and responses.

## ⚙️ Configuration

- Modify `cypress.config.json` for Cypress configuration settings.
- Customize `commands.js` and other files in `cypress/support` for reusable commands.

## 🔄 Continuous Integration

This project is configured for CI using Github Actions. Check the configurations in `.github/workflows/*.yml`.

- `01_api_tests.yml`: This workflow executes tests in pre-defined environment PROD.
- `02_api_tests_select_env.yml`: This workflow will first ask User to select the environment (DEV / Pre-PROD / PROD) for tests execution.

## 📊 Reporting

Mochawesome report (Logs are attached) is stored in the `cypress/reports` directory.