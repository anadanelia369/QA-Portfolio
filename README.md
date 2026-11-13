# 🔍 Ana Danelia | QA Portfolio

**Manual QA Engineer | Web & Mobile | API Testing | Java/Selenium Automation**

![Manual QA](https://img.shields.io/badge/Manual_QA-6b48b5?style=for-the-badge)
![API Testing](https://img.shields.io/badge/API_Testing-d4af37?style=for-the-badge)
![Java Selenium](https://img.shields.io/badge/Java_%7C_Selenium-4caf7d?style=for-the-badge)
![Open to work](https://img.shields.io/badge/Open_to_work-e07a30?style=for-the-badge)

Manual QA engineer with hands-on UAT experience at ODIN, a Georgian P2P parcel delivery app (React Native, iOS/Android), plus independent web testing of an insurance platform (GPI Holding) and a pro bono UAT of a charity donation website (autism.ge). Strongest area: state-management and data-consistency defects in multi-step flows.

Skilled in bug reporting, test case design (EP, BVA, Decision Tables), REST API validation with Postman, and Java + Selenium test automation.

> "Every system has two realities: expected behavior and actual behavior. QA lives in the space between them."

> "Observation is my API. It's the interface through which I investigate systems and learn how they really behave."

---

## 📊 By the numbers

| Metric | Count |
|---|---|
| 🐞 ODIN bugs (Jira) | 20+ filed, 6 documented in detail here |
| 🛡️ GPI Holding bugs | 4 documented here |
| 💜 autism.ge findings | 14 (4 Critical, 4 High, 6 Medium) |
| 📱 Language-learning app (paid) | 14 findings (7 Medium, 7 Low) |
| ✅ Test cases | 57 total (37 ODIN + 20 GPI) |
| 📋 Checklists | 328 scenarios across 13 modules (ODIN) |
| 📱 Devices | Honor X8d (Android 16), Samsung Galaxy Tab A7 Lite (Android 14), Android TV, Windows laptop |
| 🌐 Browsers | Chrome, Brave, Firefox, Edge |
| 🏆 Recognition | Testlio Freelancer of the Month, September 2026 |

---

## 📁 Portfolio structure

```
QA-Portfolio/
├── bug-reports/
│   ├── ODIN/            6 bug reports from the UAT internship
│   └── GPI/             4 bug reports from independent testing
├── test-cases/
│   ├── ODIN/            37 test cases (TC-ODIN-01 to TC-ODIN-37)
│   └── GPI/             20 test cases (TC-GPI-01 to TC-GPI-20)
├── projects/
│   ├── ODIN/            Testing observations and exploratory findings
│   ├── GPI/             Insurance web platform testing summary
│   ├── autism-ge/       Pro bono charity project (14 findings)
│   ├── language-app/    Paid freelance QA test (14 findings)
│   └── crowdtesting/    Freelance crowdtesting experience
├── api-testing/         Postman collection with CI/CD (separate repo, linked below)
├── debug-diary/         Automation debugging notes (separate repo, linked below)
└── assets/              Personal statement and screenshots
```

---

## 🪲 Bug reports

### 📦 ODIN (UAT internship, Feb 2026 - Jul 2026)

| Bug ID | Title | Type | Severity | Status |
|---|---|---|---|---|
| ODIN-974 | Phone Country Code Auto-Changes on Back Navigation | Functional | High | Done |
| ODIN-995 | Time Picker Crash on Chat Screen | Functional | High | Done |
| ODIN-1009 | Order Edit Shows Cached Data, Updates Multiple Times | Functional | Medium | Done |
| ODIN-1013 | System Back Button Shows Previous Trip's Data | Functional | High | Done |
| ODIN-1052 | Phone Number Input Focus Jumps to City Field on First Tap | UX / Focus | Medium | Done |
| ODIN-1079 | Offers Tab Shows an Incomplete Delivery Date Range (17-17 instead of 17-18) | Functional | Medium | Done |

### 🛡️ GPI Holding (independent testing)

| Bug ID | Title | Type | Severity | Status |
|---|---|---|---|---|
| GPI-ANN-11 | Afghan Citizenship + Georgian ID Accepted Without Validation | Security | High | Open |
| GPI-ANN-12 | 366-Day Travel Period Accepted Without Validation | Functional | Medium | Open |
| GPI-ANN-13 | Autofill Returns a Stranger's Personal Data | Security / Privacy | High | Open |
| GPI-ANN-14 | Clinic List Truncated on iPad Air Resolution | UI / Visual | Low | Open |

### 💜 autism.ge (pro bono UAT)

14 findings from a risk-based UAT of a live WordPress donation site: 4 Critical, 4 High, 6 Medium. Highlight: BUG-04, a WordPress error shown after a successful payment (fixed by the site team after the report). Full report: [autism.ge README](projects/autism-ge/README.md)

---

## ✅ Test cases

### 📦 ODIN: 37 test cases

| TC ID | Title | Type | Priority | Feature | Status |
|---|---|---|---|---|---|
| TC-ODIN-01 | OTP Verification Attempted After 15-Minute Expiry | Edge Case | High | Register | Pass |
| TC-ODIN-02 | Same Account Login on Two Devices Simultaneously | Edge Case | High | Login | Pass |
| TC-ODIN-03 | Multiple Failed Login Attempts - Account Block | Negative | High | Login | Pass |
| TC-ODIN-04 | Full Order Creation Flow - Standard | Positive | High | Order | Pass |
| TC-ODIN-05 | City Selected Without Choosing Country First | Negative | Medium | Order | Pass |
| TC-ODIN-06 | Arrival Date Set Before Departure Date | Negative | High | Trip | Pass |
| TC-ODIN-07 | App Closed Before Trip Save - Data Not Persisted | Edge Case | High | Trip | Pass |
| TC-ODIN-08 | Pending → Active → Completed Full Order Cycle | Positive | High | Order Flow | Pass |
| TC-ODIN-09 | Two Travelers Place Bid on Same Trip Simultaneously | Edge Case | High | Order Flow | Not Executed |
| TC-ODIN-10 | KYC Verification with Another Person's Document | Negative | Critical | Ident | Not Executed |
| TC-ODIN-11 | Promo Code Assigned to User A, Used by User B | Negative | High | Promo | Pass |
| TC-ODIN-12 | Payment Network Error During Transaction | Negative | High | Payment | Pass |
| TC-ODIN-13 | Trip Creation - 1 Pickup + 1 Delivery City | Positive | High | Trip | Pass |
| TC-ODIN-14 | Trip Creation - 4 Pickup + 4 Delivery Cities (Maximum) | Positive | High | Trip | Pass |
| TC-ODIN-15 | Trip - En-Route Pickup Cities (Tbilisi → Gori → Kutaisi) | Positive | High | Trip | Pass |
| TC-ODIN-16 | Trip - Delivery Across Multiple US Cities (NY, NJ) | Positive | High | Trip | Pass |
| TC-ODIN-17 | Sender Receives Notification After Trip Confirmation | Positive | High | Trip | Pass |
| TC-ODIN-18 | Standard Order Creation - Full Valid Flow | Positive | High | Order | Pass |
| TC-ODIN-19 | Auction Order Creation - Full Valid Flow | Positive | High | Order | Pass |
| TC-ODIN-20 | Order - 1 Photo Upload | Positive | Medium | Order | Pass |
| TC-ODIN-21 | Order - 2 Photos Upload | Positive | Medium | Order | Pass |
| TC-ODIN-22 | Order - 5 Photos Upload (Maximum) | Positive | High | Order | Pass |
| TC-ODIN-23 | Order - Incompatible File Format Upload | Negative | High | Order | Pass |
| TC-ODIN-24 | Traveler Makes Offer on Standard Order | Positive | High | Order Flow | Pass |
| TC-ODIN-25 | Sender Accepts Offer - Order Moves to Active | Positive | High | Order Flow | Pass |
| TC-ODIN-26 | Pickup Time Scheduled - Then Changed by Sender | Positive | High | Chat | Pass |
| TC-ODIN-27 | Chat - Third Party Invited to Conversation | Positive | High | Chat | Pass |
| TC-ODIN-28 | Chat - File Sent Between Sender and Traveler | Positive | Medium | Chat | Pass |
| TC-ODIN-29 | Wallet - Withdraw EUR via Card | Positive | High | Wallet | Pass |
| TC-ODIN-30 | Wallet - Withdraw USD via Card | Positive | High | Wallet | Pass |
| TC-ODIN-31 | Withdraw GEL via Card | Positive | High | Wallet | Pass |
| TC-ODIN-32 | Withdraw EUR via PayPal | Positive | High | Wallet | Pass |
| TC-ODIN-33 | Withdraw at Minimum Limit | Positive | High | Wallet | Pass |
| TC-ODIN-34 | Forgot Password - Only Latest OTP Valid After Resend | Edge Case | High | Login | Pass |
| TC-ODIN-35 | Password 7 Characters - BVA Below Minimum | Negative | High | Register | Pass |
| TC-ODIN-36 | Expired Card Payment Attempt | Negative | High | Payment | Pass |
| TC-ODIN-37 | Already-Used Promo Code Reuse Attempt | Negative | High | Promo | Pass |

### 🛡️ GPI Holding: 20 test cases

| TC ID | Title | Type | Priority | Feature | Status |
|---|---|---|---|---|---|
| TC-GPI-01 | 7-Day Travel Period - Manual Input | Positive | High | Calendar | Pass |
| TC-GPI-02 | 150-Day Travel Period - Manual Input | Positive | High | Calendar | Pass |
| TC-GPI-03 | 365-Day Travel Period - Manual Input | Positive | High | Calendar | Pass |
| TC-GPI-04 | 7-Day Travel Period - Calendar Selection | Positive | High | Calendar | Pass |
| TC-GPI-05 | Calendar Collapse via Center Button | Positive | Low | Calendar | Pass |
| TC-GPI-06 | 150-Day Travel Period - Calendar Selection | Positive | High | Calendar | Pass |
| TC-GPI-07 | Return Date Change - Month Update | Positive | Medium | Calendar | Pass |
| TC-GPI-08 | Return Date Left Empty - Validation Check | Negative | High | Calendar | Pass |
| TC-GPI-09 | 6-Day Period - Below Minimum Limit | Negative | High | Calendar | Pass |
| TC-GPI-10 | 366-Day Period - BVA Above Maximum | Negative | High | Calendar | Fail |
| TC-GPI-11 | 400-Day Travel Period - Exceeds Maximum | Negative | High | Calendar | Pass |
| TC-GPI-12 | Departure Date Left Empty - Validation Check | Negative | High | Calendar | Pass |
| TC-GPI-13 | Past Year Selected as Return Date | Negative | High | Calendar | Pass |
| TC-GPI-14 | Back Button After Period Selection | Positive | Low | Calendar | Pass |
| TC-GPI-15 | Page Refresh After Period Selection | Positive | Low | Calendar | Pass |
| TC-GPI-16 | Past Date Inserted via Copy-Paste | Edge Case | Low | Calendar | Pass |
| TC-GPI-17 | Invalid Day Entry in Departure Field (32/01) | Negative | Low | Calendar | Pass |
| TC-GPI-18 | Zero Date Entry (00/00/00) in Departure Field | Negative | Low | Calendar | Pass |
| TC-GPI-19 | Next → Back Navigation - Period Preserved | Positive | Medium | Calendar | Pass |
| TC-GPI-20 | Rapid Repeated Clicking on Calendar Date | Edge Case | Medium | Calendar | Pass |

---

## 🚀 Projects

### 📦 ODIN: P2P Parcel Delivery App

UAT internship (Feb 2026 - Jul 2026). Mobile testing on React Native (Android).

- 📋 328 test scenarios across 13 feature modules
- 🐞 20+ bugs filed in Jira, 6 documented in detail
- ✈️ Notable finding: **Flight Notification Timing Hypothesis**, hypothesis-based exploratory testing using real flight data

### 🛡️ GPI Holding: Insurance Web Platform

Independent exploratory testing project. Web (Chrome). Found 4 documented bugs, including 2 security-level issues (autofill data leak, invalid citizenship and document combination accepted).

### 🔌 API testing with CI/CD: Simple Grocery Store API (in progress)

Public repo: [Grocery-API-Postman-Tests](https://github.com/anadanelia369/Grocery-API-Postman-Tests)

- 📬 Postman collection for a public REST API (products, cart, orders, auth). Each resource folder is split into Positive and Negative subfolders, with the base URL kept in a Postman Environment.
- 🧪 Test design with the BINMEN mnemonic (Boundary, Invalid, Nulls, Method, Empty, Negatives): one parameter at a time, positive and negative cases, assertions on status code, body structure and data types.
- 📌 Known Issues convention: tests assert the behavior from the API documentation. Where the real API differs (for example, invalid results values such as 0, abc or empty return 200 with the full list), the request keeps its failing test, is renamed with "[Known Issue]" and is explained in its Docs tab.
- ⚙️ Newman + htmlextra: the collection runs from the command line and produces an HTML report.
- 🔁 GitHub Actions: a workflow runs the collection with Newman on every run and uploads the HTML report as an artifact.
- 🚧 Status: Status and Products folders are done. Cart, Orders and Auth are still being reworked.

### 🪲 Debug Diary: automation debugging notes

Repo: [Debug-Diary](https://github.com/anadanelia369/Debug-Diary)

> *Observation is my API.*

12 short entries from my Java/Selenium/TestNG calendar automation project (GPI travel insurance calendar). Each entry has the same structure: what happened, what I found, what I changed. Examples:

- ⏱️ **Race condition, not a slow page:** a test failed about 1 in 5 runs. The wait covered the input becoming visible, not the dropdown content rendering. Fixed with an explicit wait inside the getters instead of `Thread.sleep()`.
- 🎭 **An assertion that could never fail:** it located the element by the same class it then checked. Rewritten with XPath and a real `aria-current="date"` assertion.
- 💻 **Passed in the IDE, not in the terminal:** `mvn clean test` ran 6 of 7 tests because one class was missing from `testNG.xml`. IntelliJ's Run button had hidden the gap.
- 📅 **Wrong only at the end of the month:** `plusDays(7)` landed in the next month while the calendar showed only the current one. `selectDate()` now clicks "Next month" when the target date is not visible.

### 📱 Language-learning app: Paid QA Test

Paid freelance project (Upwork, November 2026) on a mobile language-learning app with an AI practice chat. Android and iPhone. Tested the Explore, Chats and Rooms pages as a normal user, plus additional findings from registration, profile, practice and settings. 14 findings (7 Medium, 7 Low), no crashes. Highlights: the Android Back button ends an active call without asking, and a password rule shown in the hint is not enforced at registration or Change Password. Delivered as a PDF report with a separate screen recording. Published with the client's permission, without the app name or screens.

### 💜 autism.ge: Charity Project

Pro bono UAT for an NGO website. Risk-based approach focused on authentication, donation flow and payment processing. 14 findings, including a backend redirect error after a successful payment.

### 🌍 Freelance crowdtesting (2026)

Paid and unpaid test cycles on Testlio, Test.io, uTest, Tester Work and Ubertesters, on real devices (phone, tablet, Android TV) and desktop browsers. Client names are not published, in line with platform policies.

- 🏆 **Recognition:** Testlio Freelancer of the Month, September 2026, for the highest Community Engagement Score and thorough issue reports.
- 🔄 **Cycles:** e-commerce, food delivery, streaming and mobile apps. Scope-restricted work (severity limits, staging only, no order placement, language-specific stores). Reports include a screencast, the requested device and clear reproduction steps.
- 📚 **Lessons applied:** match the device the test requests, attach a screencast for functional bugs, check the severity scope before reporting.
- 🔧 **Environment debugging:** on one cycle an authenticated proxy would not work on a Samsung tablet. I traced it with `adb logcat` to a Samsung Knox firmware error (NullPointerException in the VPN manager service) and worked around it by relaying traffic through Charles Proxy on a laptop.
- 🎓 **uTest Academy:** passed the Introduction to Testing certification cycle (bug report and test case both approved).
- 📜 **Certificates:** Tester Work (Functional Testing, Payment Testing, KYC Testing), Testlio (Freelancer Conduct Guidelines, Usability 101, Usability 102).

---

## 🧠 How I work

- 🧩 **Test design:** EP and BVA for valid and invalid boundaries, Decision Tables for complex business logic. Mobile testing follows the I SLICED UP FUN framework.
- 📝 **Bug reporting:** clear, reproducible titles. Every report includes preconditions, numbered action steps, actual vs expected result, severity and impact, device/OS/environment and reproducibility rate. Cross-checked against Figma designs. Root cause guesses are labeled as assumptions.
- 🔌 **API testing:** status codes, response body structure, data types, positive and negative scenarios including invalid inputs, missing auth tokens and boundary values.
- 🤖 **Automation:** Java + Selenium WebDriver + TestNG, Page Object Model, Maven. Completed the Quality Academy Java/Selenium course (Mar - Jul 2026).

---

## 🛠️ Skills and tools

- 🧪 **Testing types:** Manual, Functional, Regression, Exploratory, Smoke, Mobile, Cross-browser, Localization, UX
- 📐 **Test design:** Equivalence Partitioning (EP), Boundary Value Analysis (BVA), Decision Tables, State Transition Testing
- 🗂️ **Test management:** Jira, Testiny, TestCaseLab, Qase.io
- 🐞 **Bug tracking:** Jira, Linear, ClickUp, Jam.dev, Trello
- 🔌 **API testing:** Postman (Collections, Environments, Assertions, Runner), REST API, Swagger
- 🔬 **Debugging and diagnostics:** Browser DevTools, ADB, Logcat, Android Studio, Charles Proxy
- ⚙️ **API testing in CI:** Newman, GitHub Actions
- 💡 **Other:** basic SQL, basic HTML/CSS, Git

---

## 🔗 Links

- 💼 LinkedIn: [linkedin.com/in/ana-danelia-42567139b](https://linkedin.com/in/ana-danelia-42567139b)
- 🪲 Debug Diary: [github.com/anadanelia369/Debug-Diary](https://github.com/anadanelia369/Debug-Diary)
- 🔌 API testing with CI/CD: [Grocery-API-Postman-Tests](https://github.com/anadanelia369/Grocery-API-Postman-Tests)
- 🤖 Selenium automation: [GpiCalendarAutomation](https://github.com/anadanelia369/GpiCalendarAutomation)
- 📄 CV: Ana_Danelia_QA_Engineer.pdf
