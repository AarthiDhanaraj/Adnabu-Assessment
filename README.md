# AdNabu QA Assignment

## Overview
This repository contains the QA test cases and Selenium automation scripts for the **AdNabu Shopify store**.  
The automation validates the **search product** and **add to cart** functionality.

---

## Folder Structure
adnabu-qa-assignment/
│
├── automation/
│ └── test_search_addtocart_optimized.py # Selenium automation script
│
├── test-cases/
│ ├── TestDesign
│
└── README.md # This file

---

## Test Coverage

### Product Search
- Valid product search
- No matching product (negative)
- Partial keyword search (edge case)
- Long input search (edge case)
- Search with extra spaces (edge case)
- Search with only whitespace (negative)

### Add to Cart
- Add product successfully (positive)
- Add without internet (negative)
- Add same product multiple times (edge case)
- Add Other product (positive)
- Cart persistence after refresh (edge case)
- Sold out replaces Add to cart (negative)

---

## Automation Script

- **Script:** `automation/test_search_addtocart_optimized.py`  
- **Framework:** Python + Selenium WebDriver  
- **Browser:** Google Chrome (managed via `webdriver_manager`)  
- **Features:**  
  - Explicit waits (`WebDriverWait`) for stable execution  
  - No hardcoded `sleep()` statements  
  - Modular, reusable functions
  - Handles password-protected Shopify store
  - Validates product added to cart

---

## Prerequisites

- Python 3.8+
- Google Chrome installed
- Install Python dependencies:

```bash
pip install selenium webdriver-manager

How to Run
Open terminal in the project root folder
Run the automation script:
python automation/test_search_addtocart_optimized.py
The script will:
Open the AdNabu test store
Enter the password AdNabuQA
Search for "The Complete Snowboard"
Select the first product
Add it to the cart
Print Test Passed: Product successfully added to cart if successful

Notes:
Script uses explicit waits for reliable execution
Replace product name in search_product() function if needed

Author

Aarthi D – QA Engineer
