# Ana Danelia | QA Portfolio

**Manual Testing · API Testing · Automation (in progress)**

Manual QA tester with hands-on UAT experience at ODIN — a Georgian P2P parcel delivery app (React Native, iOS/Android). Logged 20+ bug reports in Jira across functional, UX, localization, navigation, and security defect categories.

Skilled in bug reporting, test case design (EP, BVA, Decision Tables), and REST API validation with Postman. Currently developing Java + Selenium automation skills. ISTQB FL planned (prep starts June 2026).

> *"Every system has two realities: expected behavior and actual behavior. QA lives in the space between them."*
→ [Observation is my API — how I think about testing](assets/observation-is-my-api.md)
---

## 📊 By the Numbers

| Metric | Count |
|--------|-------|
| 🐛 Bug Reports | 20+ (ODIN UAT + GPI) |
| ✅ Test Cases | 57 total (37 ODIN + 20 GPI) |
| 📋 Checklists | 328 scenarios across 13 modules |
| 📱 Primary Device | Android 14 / Realme 10 + Tab A7 |
| 🌐 Browsers | Chrome, Firefox, Edge |

---

## 🗂️ Portfolio Structure

```
📁 bug-reports/
   📁 ODIN/          — 6 bug reports from UAT internship
   📁 GPI/           — 4 bug reports from independent testing
📁 test-cases/
   📁 ODIN/          — 37 test cases (TC-ODIN-01 to TC-ODIN-37)
   📁 GPI/           — 20 test cases (TC-GPI-01 to TC-GPI-20)
📁 projects/
   📁 ODIN/          — Testing observations & exploratory findings
   📁 GPI/           — Insurance web platform testing summary
   📁 autism-ge/     — Pro bono charity project
📁 api-testing/      — Postman collections & API testing diary
📁 assets/           — Personal statement & screenshots
```

---

## 🪲 Bug Reports

### ODIN (UAT Internship)

| Bug ID | Title | Type | Severity | Status |
|--------|-------|------|----------|--------|
| [ODIN-974](bug-reports/ODIN/ODIN-974.md) | Phone Country Code Auto-Changes on Back Navigation | Functional | High | Done |
| [ODIN-995](bug-reports/ODIN/ODIN-995.md) | Time Picker Crash on Chat Screen | Functional | Critical | Done |
| [ODIN-1009](bug-reports/ODIN/ODIN-1009.md) | Order Edit Shows Cached Data — Updates Multiple Times | Functional | Medium | Done |
| [ODIN-1013](bug-reports/ODIN/ODIN-1013.md) | System Back Button Breaks Trip Flow | Navigation | High | Done |
| [ODIN-1052](bug-reports/ODIN/ODIN-1052.md) | Phone Number Input Focus Jumps to City Field on First Tap | UX | Medium | Done |
| [ODIN-1079](bug-reports/ODIN/ODIN-1079.md) | Offers Tab Displays Incorrect Date Range (17–17 Instead of 17–18) | Functional | Medium | Done |

### GPI Holding (Independent Testing)

| Bug ID | Title | Type | Severity | Status |
|--------|-------|------|----------|--------|
| GPI-ANN-11 | Afghan Citizenship + Georgian ID Accepted Without Validation | Security | High | Open |
| GPI-ANN-12 | 366-Day Travel Period Accepted — No Validation | Functional | Medium | Open |
| GPI-ANN-13 | Autofill Returns Stranger's Personal Data | Security | High | Open |
| GPI-ANN-14 | Clinic List Truncated on iPad Air Resolution | UI/Visual | Low | Open |

---

## ✅ Test Cases

### ODIN — 37 Test Cases

| TC ID | Title | Type | Priority | Feature | Status |
|-------|-------|------|----------|---------|--------|
| [TC-ODIN-01](test-cases/ODIN/TC-ODIN-01.md) | OTP Verification Attempted After 15-Minute Expiry | Edge Case | High | Register | Pass |
| [TC-ODIN-02](test-cases/ODIN/TC-ODIN-02.md) | Same Account Login on Two Devices Simultaneously | Edge Case | High | Login | Pass |
| [TC-ODIN-03](test-cases/ODIN/TC-ODIN-03.md) | Multiple Failed Login Attempts — Account Block | Negative | High | Login | Pass |
| [TC-ODIN-04](test-cases/ODIN/TC-ODIN-04.md) | Full Order Creation Flow — Standard | Positive | High | Order | Pass |
| [TC-ODIN-05](test-cases/ODIN/TC-ODIN-05.md) | City Selected Without Choosing Country First | Negative | Medium | Order | Pass |
| [TC-ODIN-06](test-cases/ODIN/TC-ODIN-06.md) | Arrival Date Set Before Departure Date | Negative | High | Trip | Pass |
| [TC-ODIN-07](test-cases/ODIN/TC-ODIN-07.md) | App Closed Before Trip Save — Data Not Persisted | Edge Case | High | Trip | Pass |
| [TC-ODIN-08](test-cases/ODIN/TC-ODIN-08.md) | Pending → Active → Completed Full Order Cycle | Positive | High | Order Flow | Pass |
| [TC-ODIN-09](test-cases/ODIN/TC-ODIN-09.md) | Two Travelers Place Bid on Same Trip Simultaneously | Edge Case | High | Order Flow | Not Executed |
| [TC-ODIN-10](test-cases/ODIN/TC-ODIN-10.md) | KYC Verification with Another Person's Document | Negative | Critical | Ident | Not Executed |
| [TC-ODIN-11](test-cases/ODIN/TC-ODIN-11.md) | Promo Code Assigned to User A, Used by User B | Negative | High | Promo | Pass |
| [TC-ODIN-12](test-cases/ODIN/TC-ODIN-12.md) | Payment Network Error During Transaction | Negative | High | Payment | Pass |
| [TC-ODIN-13](test-cases/ODIN/TC-ODIN-13.md) | Trip Creation — 1 Pickup + 1 Delivery City | Positive | High | Trip | Pass |
| [TC-ODIN-14](test-cases/ODIN/TC-ODIN-14.md) | Trip Creation — 4 Pickup + 4 Delivery Cities (Maximum) | Positive | High | Trip | Pass |
| [TC-ODIN-15](test-cases/ODIN/TC-ODIN-15.md) | Trip — En-Route Pickup Cities (Tbilisi → Gori → Kutaisi) | Positive | High | Trip | Pass |
| [TC-ODIN-16](test-cases/ODIN/TC-ODIN-16.md) | Trip — Delivery Across Multiple US Cities (NY, NJ) | Positive | High | Trip | Pass |
| [TC-ODIN-17](test-cases/ODIN/TC-ODIN-17.md) | Sender Receives Notification After Trip Confirmation | Positive | High | Trip | Pass |
| [TC-ODIN-18](test-cases/ODIN/TC-ODIN-18.md) | Standard Order Creation — Full Valid Flow | Positive | High | Order | Pass |
| [TC-ODIN-19](test-cases/ODIN/TC-ODIN-19.md) | Auction Order Creation — Full Valid Flow | Positive | High | Order | Pass |
| [TC-ODIN-20](test-cases/ODIN/TC-ODIN-20.md) | Order — 1 Photo Upload | Positive | Medium | Order | Pass |
| [TC-ODIN-21](test-cases/ODIN/TC-ODIN-21.md) | Order — 2 Photos Upload | Positive | Medium | Order | Pass |
| [TC-ODIN-22](test-cases/ODIN/TC-ODIN-22.md) | Order — 5 Photos Upload (Maximum) | Positive | High | Order | Pass |
| [TC-ODIN-23](test-cases/ODIN/TC-ODIN-23.md) | Order — Incompatible File Format Upload | Negative | High | Order | Pass |
| [TC-ODIN-24](test-cases/ODIN/TC-ODIN-24.md) | Traveler Makes Offer on Standard Order | Positive | High | Order Flow | Pass |
| [TC-ODIN-25](test-cases/ODIN/TC-ODIN-25.md) | Sender Accepts Offer — Order Moves to Active | Positive | High | Order Flow | Pass |
| [TC-ODIN-26](test-cases/ODIN/TC-ODIN-26.md) | Pickup Time Scheduled — Then Changed by Sender | Positive | High | Chat | Pass |
| [TC-ODIN-27](test-cases/ODIN/TC-ODIN-27.md) | Chat — Third Party Invited to Conversation | Positive | High | Chat | Pass |
| [TC-ODIN-28](test-cases/ODIN/TC-ODIN-28.md) | Chat — File Sent Between Sender and Traveler | Positive | Medium | Chat | Pass |
| [TC-ODIN-29](test-cases/ODIN/TC-ODIN-29.md) | Wallet — Withdraw EUR via Card | Positive | High | Wallet | Pass |
| [TC-ODIN-30](test-cases/ODIN/TC-ODIN-30.md) | Wallet — Withdraw USD via Card | Positive | High | Wallet | Pass |
| [TC-ODIN-31](test-cases/ODIN/TC-ODIN-31.md) | Withdraw GEL via Card | Positive | High | Wallet | Pass |
| [TC-ODIN-32](test-cases/ODIN/TC-ODIN-32.md) | Withdraw EUR via PayPal | Positive | High | Wallet | Pass |
| [TC-ODIN-33](test-cases/ODIN/TC-ODIN-33.md) | Withdraw at Minimum Limit | Positive | High | Wallet | Pass |
| [TC-ODIN-34](test-cases/ODIN/TC-ODIN-34.md) | Forgot Password — Only Latest OTP Valid After Resend | Edge Case | High | Login | Pass |
| [TC-ODIN-35](test-cases/ODIN/TC-ODIN-35.md) | Password 7 Characters — BVA Below Minimum | Negative | High | Register | Pass |
| [TC-ODIN-36](test-cases/ODIN/TC-ODIN-36.md) | Expired Card Payment Attempt | Negative | High | Payment | Pass |
| [TC-ODIN-37](test-cases/ODIN/TC-ODIN-37.md) | Already-Used Promo Code Reuse Attempt | Negative | High | Promo | Pass |

### GPI Holding — 20 Test Cases

| TC ID | Title | Type | Priority | Feature | Status |
|-------|-------|------|----------|---------|--------|
| [TC-GPI-01](test-cases/GPI/TC-GPI-01.md) | 7-Day Travel Period — Manual Input | Positive | High | Calendar | Pass |
| [TC-GPI-02](test-cases/GPI/TC-GPI-02.md) | 150-Day Travel Period — Manual Input | Positive | High | Calendar | Pass |
| [TC-GPI-03](test-cases/GPI/TC-GPI-03.md) | 365-Day Travel Period — Manual Input | Positive | High | Calendar | Pass |
| [TC-GPI-04](test-cases/GPI/TC-GPI-04.md) | 7-Day Travel Period — Calendar Selection | Positive | High | Calendar | Pass |
| [TC-GPI-05](test-cases/GPI/TC-GPI-05.md) | Calendar Collapse via Center Button | Positive | Low | Calendar | Pass |
| [TC-GPI-06](test-cases/GPI/TC-GPI-06.md) | 150-Day Travel Period — Calendar Selection | Positive | High | Calendar | Pass |
| [TC-GPI-07](test-cases/GPI/TC-GPI-07.md) | Return Date Change — Month Update | Positive | Medium | Calendar | Pass |
| [TC-GPI-08](test-cases/GPI/TC-GPI-08.md) | Return Date Left Empty — Validation Check | Negative | High | Calendar | Pass |
| [TC-GPI-09](test-cases/GPI/TC-GPI-09.md) | 6-Day Period — Below Minimum Limit | Negative | High | Calendar | Pass |
| [TC-GPI-10](test-cases/GPI/TC-GPI-10.md) | 366-Day Period — BVA Above Maximum | Negative | High | Calendar | **Fail** |
| [TC-GPI-11](test-cases/GPI/TC-GPI-11.md) | 400-Day Travel Period — Exceeds Maximum | Negative | High | Calendar | Pass |
| [TC-GPI-12](test-cases/GPI/TC-GPI-12.md) | Departure Date Left Empty — Validation Check | Negative | High | Calendar | Pass |
| [TC-GPI-13](test-cases/GPI/TC-GPI-13.md) | Past Year Selected as Return Date | Negative | High | Calendar | Pass |
| [TC-GPI-14](test-cases/GPI/TC-GPI-14.md) | Back Button After Period Selection | Positive | Low | Calendar | Pass |
| [TC-GPI-15](test-cases/GPI/TC-GPI-15.md) | Page Refresh After Period Selection | Positive | Low | Calendar | Pass |
| [TC-GPI-16](test-cases/GPI/TC-GPI-16.md) | Past Date Inserted via Copy-Paste | Edge Case | Low | Calendar | Pass |
| [TC-GPI-17](test-cases/GPI/TC-GPI-17.md) | Invalid Day Entry in Departure Field (32/01) | Negative | Low | Calendar | Pass |
| [TC-GPI-18](test-cases/GPI/TC-GPI-18.md) | Zero Date Entry (00/00/00) in Departure Field | Negative | Low | Calendar | Pass |
| [TC-GPI-19](test-cases/GPI/TC-GPI-19.md) | Next → Back Navigation — Period Preserved | Positive | Medium | Calendar | Pass |
| [TC-GPI-20](test-cases/GPI/TC-GPI-20.md) | Rapid Repeated Clicking on Calendar Date | Edge Case | Medium | Calendar | Pass |

---

## 🔬 Projects

### [ODIN — P2P Parcel Delivery App](projects/ODIN/)
UAT internship (Feb 2026 – present). Mobile testing on React Native (iOS/Android).
- 328 test scenarios across 13 feature modules
- 6 filed bugs + exploratory observations
- Notable finding: [Flight Notification Timing Hypothesis](projects/ODIN/flight-notification-observation.md) — hypothesis-based exploratory testing using real flight data

### [GPI Holding — Insurance Web Platform](projects/GPI/)
Independent exploratory testing project. Web (Chrome). Found 4 bugs including 2 security-level issues (autofill data leak, invalid citizenship/document combination accepted).

### [autism.ge — Charity Project](projects/autism-ge/)
Pro bono UAT for NGO website. Risk-based approach focused on donation flow and payment processing. Found 6 issues including a backend redirect error post-payment.

---

## 🔧 API Testing

Structured **Postman Diary** using the [Grocery Store API](https://simple-grocery-store-api.click).

Topics covered: Collections, Environments (`{{BaseURL}}`), Status code testing (200/201/400/401/403/404), JavaScript assertions (`pm.test`, `pm.expect`, `.to.eql`, `.to.exist`), Query params vs path params, POST/GET flows, Cart creation.

**Notable finding:** `GET /products?limit=3` returns 20 products instead of 3 — the `limit` parameter is not implemented on this endpoint. Verified via `console.log(pm.response.json().length)` in Postman Console.

→ [API Testing folder](api-testing/)

---

## ⚙️ How I Work

**Test Design:** EP and BVA for valid/invalid boundaries, Decision Tables for complex business logic. Mobile testing follows the I SLICED UP FUN framework.

**Bug Reporting:** Clear, reproducible titles. Every report includes: preconditions, numbered steps, actual vs expected result, severity/priority rationale, device/OS/environment, reproducibility rate. Cross-checked against Figma designs.

**API Testing:** Status codes, response body structure, data types, positive and negative scenarios including invalid inputs, missing auth tokens, boundary values.

**Automation (in progress):** Java + Selenium WebDriver + TestNG. Building foundational skills in Page Object Model and Maven project structure. Course started March 2026 (Quality Academy).

---

## 🛠️ Skills & Tools

**Testing Types:** Manual, Functional, Regression, Exploratory, Smoke, Mobile, Cross-browser, Localization, UX

**Test Design:** Equivalence Partitioning (EP), Boundary Value Analysis (BVA), Decision Tables, State Transition Testing

**Test Management:** Jira, Testiny, TestCaseLab, Qase.io

**Bug Tracking:** Jira, Linear, ClickUp, Jam.dev, Trello

**API Testing:** Postman (Collections, Environments, Assertions, Runner), REST API, Swagger

**Other:** Browser DevTools, basic SQL, basic HTML/CSS, Git (basic)

---

## 🔗 Links

- **LinkedIn:** [linkedin.com/in/ana-danelia-42567139b](https://linkedin.com/in/ana-danelia-42567139b)
- **CV:** [Ana_Danelia_CV_2026.pdf](Ana_Danelia_CV_2026.pdf)
- **Notion Portfolio:** [View on Notion](https://dani369.short.gy/Portfolio)
