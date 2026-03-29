# Ana Danelia | QA Portfolio

**Manual Testing · API Testing · Automation (in progress)**

Manual QA tester with hands-on UAT experience at ODIN — a Georgian P2P parcel delivery app (React Native, iOS/Android). Logged 20+ bug reports in Jira across functional, UX, localization, navigation, and security defect categories.

Skilled in bug reporting, test case design (EP, BVA, Decision Tables), and REST API validation with Postman. Currently developing Java + Selenium automation skills. ISTQB FL planned (prep starts June 2026).

> *"Every system has two realities: expected behavior and actual behavior. QA lives in the space between them."*

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
   📁 GPI/           — 5 bug reports from independent testing
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
| KIWI-ANN-01 | Payment Page Closes During App Hijack — OTP Not Reached | Security | High | Open |

---

## ✅ Test Cases

- **[ODIN Test Cases](test-cases/ODIN/)** — 37 TCs covering Registration, Login, Order Flow, Chat, Profile, Notifications
- **[GPI Test Cases](test-cases/GPI/)** — 20 TCs covering Calendar validation, insurance flow, boundary values

Summary tables:
- [ODIN Test Cases Overview (CSV)](test-cases/ODIN/ODIN-test-cases-overview.csv)
- [GPI Test Cases Overview (CSV)](test-cases/GPI/GPI-test-cases-overview.csv)

---

## 🔬 Projects

### [ODIN — P2P Parcel Delivery App](projects/ODIN/)
UAT internship (Feb 2026 – present). Mobile testing on React Native (iOS/Android).
- 328 test scenarios across 13 feature modules
- 6 filed bugs + exploratory observations
- Notable finding: [Flight Notification Timing Hypothesis](projects/ODIN/flight-notification-observation.md) — hypothesis-based exploratory testing using real flight data

### [GPI Holding — Insurance Web Platform](projects/GPI/)
Independent exploratory testing project. Web (Chrome). Found 5 bugs including 2 security-level issues (autofill data leak, invalid citizenship/document combination accepted).

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
