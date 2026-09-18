# SauceLab Checkout Flow Automation - Playwright

This repository contains automated end-to-end tests for the **Sauce Labs** checkout flow using [Playwright](https://playwright.dev/).

---

## 📂 Project Structure
- `src/pages/` – Page Object Models (POM)
- `fixtures/` – Test data and environment variables
- `tests/` – Test specifications
- `playwright.config.js` – Playwright configuration
- `.env` – Environment variables (not committed to GitHub)

---

## 🚀 Setup & Installation

   1. **Clone the repository**

 -  `git clone https://github.com/aster-go/SauceLab-CheckoutFlow-Automation-Playwright.git`
 -  `cd SauceLab-CheckoutFlow-Automation-Playwright`

2. **Install dependencies**
    npm install

3. **Install Playwright browsers**
    npx playwright install

4. **Configure environment variables**
    Create a .env file in the root directory:env

   - BASE_URL=https://www.saucedemo.com
   - USERNAME=standard_user
   - PASSWORD=secret_sauce
   - FIRST_NAME=Rafia
   - LAST_NAME=Ejaz
   - POSTAL_CODE=54000
  
### 🧪 How the Tests Work

The test suite automates the happy path checkout flow on SauceDemo:

**Login Page**
- Opens the Sauce Labs site
- Logs in with valid credentials

**Inventory Page**
- Selects 3 random unique items to add to cart

**Cart Page**
- Verifies exactly 3 items are in the cart
- Proceeds to checkout

**Checkout Step One**
- Fills in customer information from .env file

**Checkout Step Two**
- Verifies order summary is displayed
- Order Completion
- Finishes the order and verifies the success message

### 🧪 Running Tests

 - **Run all tests in headless mode:** 
     npx playwright test
 
-  **Run tests in headed (UI) mode:**
     npx playwright test --headed
  
 - **Run a specific test file:**
   npx playwright test tests/CheckOutFlow.spec.js

### 📊 Viewing Test Reports

  **After running tests, open the HTML report:**
    npx playwright show-report


### ⚙️ CI/CD with GitHub Actions
  This project includes a GitHub Actions workflow (.github/workflows/playwright.yml) to:

  - Run tests on push or pull requests to main / master
  - Upload Playwright HTML reports as artifacts for 30 days



### 📦 Dependencies
  Node.js (LTS recommended)

  Playwright

  dotenv (for environment variables)

### 👩‍💻 Author
  Rafia Ijaz | 
  QA Automation Engineer | 
  GitHub: aster-go
