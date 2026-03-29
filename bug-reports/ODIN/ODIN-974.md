# ODIN-974

Title                          : Phone Country Code Auto-Changes on Back Navigation
Company: ODIN
Device/Browser: Android 14 / Realme 10
Environment: UAT
Severity: High
Status: Done
Type: Functional

Severity: `High` Reproducibility: `100%`

---

`Summary` During the order creation flow, navigating back from the "Completion" step to the "Contact" step automatically changes the country code of the previously entered phone number to match the delivery destination country.

---

`Preconditions:`

- Logged into ODIN

---

`Steps to Reproduce`

- Open ODIN → start order creation
- Fill all required fields → select delivery type: "Door to Airport"
- Set pickup: Georgia → Tbilisi → enter address
- Set delivery: United States → New York City
- Select airport → click "Continue"
- On Contact step: enter email address
- In phone number field: select country code `UNITED STATES +1`
- Enter phone number: `347 777 4444` → click "Continue" → Completion step opens
- Click "Back" → return to Contact step

---

`Actual Result:` Country code automatically changes to `CANADA (+1)` instead of retaining the originally selected `UNITED STATES (+1)`

---

 `Expected Result:`Country code must retain the originally selected value when navigating back.

---

`Impact & Rationale` Multi-step flow state management failure. User's contact data silently changes without any warning — could result in incorrect delivery contact information being submitted. Demonstrates cross-step data inconsistency in a critical order flow.

---

`Root Cause Guess` Country code field likely re-initializes on back navigation based on delivery country, without checking previously saved user input.