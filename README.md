# 🔍 Ana Danelia | QA Portfolio

**Manual QA Engineer | Web & Mobile | API Testing | Java/Selenium Automation**

[![Portfolio website](https://img.shields.io/badge/Portfolio_website-6b48b5?style=for-the-badge)](https://anadanelia369.github.io/QA-Portfolio/)
[![API tests repo](https://img.shields.io/badge/API_tests_repo-d4af37?style=for-the-badge)](https://github.com/anadanelia369/Grocery-API-Postman-Tests)
[![Selenium repo](https://img.shields.io/badge/Selenium_repo-4caf7d?style=for-the-badge)](https://github.com/anadanelia369/GpiCalendarAutomation)
[![Open to work on LinkedIn](https://img.shields.io/badge/Open_to_work_on_LinkedIn-e07a30?style=for-the-badge)](https://linkedin.com/in/ana-danelia-42567139b)

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

## 🚀 Projects

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

### 🌍 Freelance crowdtesting (2026)

Paid and unpaid test cycles on Testlio, Test.io, uTest, Tester Work and Ubertesters, on real devices (phone, tablet, Android TV) and desktop browsers. Client names are not published, in line with platform policies.

- 🏆 **Recognition:** Testlio Freelancer of the Month, September 2026, for the highest Community Engagement Score and thorough issue reports.
- 🔄 **Cycles:** e-commerce, food delivery, streaming and mobile apps. Scope-restricted work (severity limits, staging only, no order placement, language-specific stores). Reports include a screencast, the requested device and clear reproduction steps.
- 📚 **Lessons applied:** match the device the test requests, attach a screencast for functional bugs, check the severity scope before reporting.
- 🔧 **Environment debugging:** on one cycle an authenticated proxy would not work on a Samsung tablet. I traced it with `adb logcat` to a Samsung Knox firmware error (NullPointerException in the VPN manager service) and worked around it by relaying traffic through Charles Proxy on a laptop.
- 🎓 **uTest Academy:** passed the Introduction to Testing certification cycle (bug report and test case both approved).
- 📜 **Certificates:** Tester Work (Functional Testing, Payment Testing, KYC Testing), Testlio (Freelancer Conduct Guidelines, Usability 101, Usability 102).

### 💜 autism.ge: Charity Project

Pro bono UAT for an NGO website. Risk-based approach focused on authentication, donation flow and payment processing. 14 findings, including a backend redirect error after a successful payment.

👉 [Read the full autism.ge report](projects/autism-ge/README.md)

### 🛡️ GPI Holding: Insurance Web Platform

Independent exploratory testing project. Web (Chrome). Found 4 documented bugs, including 2 security-level issues (autofill data leak, invalid citizenship and document combination accepted).

- ✅ 20 test cases (TC-GPI-01 to TC-GPI-20), covering the travel period calendar with EP and BVA
- 🐞 4 bug reports (GPI-ANN-11 to GPI-ANN-14)

👉 [View the GPI test cases](test-cases/GPI)

### 📦 ODIN: P2P Parcel Delivery App

UAT internship (Feb 2026 - Jul 2026). Mobile testing on React Native (Android).

- 📋 328 test scenarios across 13 feature modules
- ✅ 37 test cases (TC-ODIN-01 to TC-ODIN-37)
- 🐞 20+ bugs filed in Jira, 6 documented in detail
- ✈️ Notable finding: **Flight Notification Timing Hypothesis**, hypothesis-based exploratory testing using real flight data

👉 [View the ODIN test cases](test-cases/ODIN)

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

14 findings from a risk-based UAT of a live WordPress donation site: 4 Critical, 4 High, 6 Medium. Highlight: BUG-04, a WordPress error shown after a successful payment (fixed by the site team after the report).

👉 [Read the full autism.ge report](projects/autism-ge/README.md)

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
