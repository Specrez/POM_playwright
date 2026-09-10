# Playwright Login Automation

A Playwright-based UI automation project developed using **JavaScript** and the **Page Object Model (POM)** design pattern. The project automates the login functionality of **The Internet – Herokuapp** and demonstrates reusable page objects, locators, test actions, and browser automation.

## 🛠️ Tech Stack

* JavaScript
* Playwright
* Node.js
* NPM
* Chromium
* Page Object Model (POM)

## 📌 Project Overview

This project demonstrates how a login workflow can be automated using Playwright while following the **Page Object Model** approach.

The login page elements and actions are separated into a dedicated `LoginPage` class. The test file creates an instance of this page object and uses reusable methods to navigate to the login page and perform the login operation.

The application under test is:

```text
https://the-internet.herokuapp.com/login
```

The automation uses Playwright's role-based locators to identify the username field, password field, and login button.

## 📁 Project Structure

```text
playwright-login/
│
├── pages/
│   └── login.js
│
├── tests/
│   └── login.spec.js
│
├── playwright.config.js
├── package.json
├── package-lock.json
└── README.md
```

### Page Object

The `LoginPage` class contains:

* Username textbox locator
* Password textbox locator
* Login button locator
* Navigation method
* Login method

Example:

```javascript
async login(username, password) {
    await this.username_textbox.fill(username);
    await this.password_textbox.fill(password);
    await this.login_button.click();
}
```

This keeps the actual test case simple and makes the login functionality reusable.

## 🔄 Automation Flow

The automated workflow is:

```text
Launch Browser
      ↓
Navigate to Login Page
      ↓
Locate Username Field
      ↓
Enter Username
      ↓
Locate Password Field
      ↓
Enter Password
      ↓
Click Login
      ↓
Validate Login Result
```

## ▶️ Running the Tests

Install dependencies:

```bash
npm install
```

Install Playwright browsers:

```bash
npx playwright install
```

Run the tests:

```bash
npx playwright test
```

Run using Chromium:

```bash
npx playwright test --project chromium
```

Run in headed mode:

```bash
npx playwright test --project chromium --headed
```

Run in debug mode:

```bash
npx playwright test --debug
```

Open the HTML report:

```bash
npx playwright show-report
```

If port `9323` is already in use:

```bash
npx playwright show-report --port 9324
```

## 🎯 Skills Demonstrated

* Playwright UI automation
* JavaScript test automation
* Page Object Model
* Reusable page methods
* Role-based locators
* Form interaction
* Browser automation
* Test execution
* HTML reporting
* Basic test framework organization
