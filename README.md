# Ana Danelia | QA Portfolio

**Manual QA Engineer | Web & Mobile | API Testing | Java/Selenium Automation**

[![Portfolio website](https://img.shields.io/badge/Portfolio_website-6b48b5?style=for-the-badge)](https://anadanelia369.github.io/QA-Portfolio/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-d4af37?style=for-the-badge)](https://linkedin.com/in/ana-danelia-42567139b)
[![GitHub](https://img.shields.io/badge/GitHub-4caf7d?style=for-the-badge)](https://github.com/anadanelia369)
[![CV](https://img.shields.io/badge/CV-e07a30?style=for-the-badge)](https://github.com/anadanelia369/QA-Portfolio/blob/main/Ana_Danelia_QA_Engineer.pdf)

Manual QA engineer with hands-on UAT experience at ODIN, a Georgian P2P parcel delivery app (React Native, iOS/Android), plus independent web testing of an insurance platform (GPI Holding) and a pro bono UAT of a charity donation website (autism.ge). Strongest area: state-management and data-consistency defects in multi-step flows.

On the automation side: Java/Selenium/TestNG tests for the GPI travel insurance calendar, and a Postman API collection that runs with Newman in GitHub Actions.

Skilled in bug reporting, test case design (EP, BVA, Decision Tables), REST API validation with Postman, and Java + Selenium test automation.

Based in Tbilisi, Georgia (GMT+4). Open to remote QA opportunities.

---

## 👤 About me

> "Observation is my API. It's the interface through which I investigate systems and learn how they really behave."

**In progress**

- Interested in AI testing, learning AI fundamentals for QA using [Evidently AI](https://www.evidentlyai.com) materials
- Reading *Taking Testing Seriously* by James Bach and Michael Bolton

---

## 📊 By the numbers

| Metric | Count |
|---|---|
| ODIN bugs (Jira) | 20+ filed, 6 documented in detail here |
| GPI Holding bugs | 4 documented here |
| autism.ge findings | 14 (4 Critical, 4 High, 6 Medium) |
| Language-learning app (paid) | 14 findings (7 Medium, 7 Low) |
| Test cases | 57 total (37 ODIN + 20 GPI) |
| Checklists | 328 scenarios across 13 modules (ODIN) |
| Devices | Honor X8d (Android 16), Samsung Galaxy Tab A7 Lite (Android 14), Android TV, Windows laptop |
| Browsers | Chrome, Brave, Firefox, Edge |
| Recognition | Testlio Freelancer of the Month, September 2026 |

---

## 📱 Manual testing projects

### Language-learning app: paid QA test

Paid freelance project ([Upwork](https://www.upwork.com/freelancers/~01f0789182111f1160), November 2026) on a mobile language-learning app with an AI practice chat. Android and iPhone. Tested the Explore, Chats and Rooms pages as a normal user, plus additional findings from registration, profile, practice and settings. 14 findings (7 Medium, 7 Low), no crashes. Highlights: the Android Back button ends an active call without asking, and a password rule shown in the hint is not enforced at registration or Change Password. Delivered as a PDF report with a separate screen recording. Published with the client's permission, without the app name or screens.

### Freelance crowdtesting (2026)

Paid and unpaid test cycles on Testlio, Test.io, uTest, Tester Work and Ubertesters, on real devices (phone, tablet, Android TV) and desktop browsers. Currently participating in Test.io cycles. Client names are not published, in line with platform policies.

- **Recognition:** [Testlio Freelancer of the Month](https://www.linkedin.com/posts/testlio-community_we-created-freelancer-of-the-month-to-celebrate-activity-7513242201838211074-875_), September 2026, for the highest Community Engagement Score and thorough issue reports.
- **Cycles:** e-commerce, food delivery, streaming and mobile apps. Scope-restricted work (severity limits, staging only, no order placement, language-specific stores). Reports include a screencast, the requested device and clear reproduction steps.
- **Lessons applied:** match the device the test requests, attach a screencast for functional bugs, check the severity scope before reporting.
- **Environment debugging:** on one cycle an authenticated proxy would not work on a Samsung tablet. I traced it with `adb logcat` to a Samsung Knox firmware error (NullPointerException in the VPN manager service) and worked around it by relaying traffic through Charles Proxy on a laptop.

### autism.ge: charity project (pro bono UAT)

Risk-based UAT of a live WordPress donation site for an NGO, focused on authentication, donation flow and payment processing. 14 findings: 4 Critical, 4 High, 6 Medium. Highlight: BUG-04, a WordPress error shown after a successful payment (fixed by the site team after the report).

[Full autism.ge report](projects/autism-ge/README.md)

### GPI Holding: insurance web platform

Independent exploratory testing project. Web (Chrome). Found 4 documented bugs, including 2 security-level issues (autofill data leak, invalid citizenship and document combination accepted). 20 test cases cover the travel period calendar with EP and BVA.

[Test cases](test-cases/GPI/GPI-test-cases-overview.csv) | [Bug reports](bug-reports/GPI)

### ODIN: P2P parcel delivery app

UAT internship (Feb 2026 - Jul 2026). Mobile testing on React Native (Android).

- 328 test scenarios across 13 feature modules
- 37 test cases (TC-ODIN-01 to TC-ODIN-37)
- 20+ bugs filed in Jira, 6 documented in detail
- Notable finding: **Flight Notification Timing Hypothesis**, hypothesis-based exploratory testing using real flight data

[Test cases](test-cases/ODIN) | [Bug reports](bug-reports/ODIN)

---

## 🤖 Automation projects

### GPI Calendar Automation: Java, Selenium, TestNG

Automated tests for the travel period calendar of the GPI travel insurance website. Java, Selenium WebDriver, TestNG, Page Object Model and Maven. The debugging notes from this project are in the Debug Diary below.

[Repository: GpiCalendarAutomation](https://github.com/anadanelia369/GpiCalendarAutomation)

### API testing with CI/CD: Simple Grocery Store API (in progress)

Postman collection for a public REST API (products, cart, orders, auth). Each resource folder is split into Positive and Negative subfolders, with the base URL kept in a Postman Environment.

- **Test design:** BINMEN mnemonic (Boundary, Invalid, Nulls, Method, Empty, Negatives): one parameter at a time, positive and negative cases, assertions on status code, body structure and data types.
- **Known Issues convention:** tests assert the behavior from the API documentation. Where the real API differs (for example, invalid results values such as 0, abc or empty return 200 with the full list), the request keeps its failing test, is renamed with "[Known Issue]" and is explained in its Docs tab.
- **Newman + htmlextra:** the collection runs from the command line and produces an HTML report.
- **GitHub Actions:** a workflow runs the collection with Newman on every run and uploads the HTML report as an artifact.
- **Status:** Status and Products folders are done. Cart, Orders and Auth are still being reworked.

[Repository: Grocery-API-Postman-Tests](https://github.com/anadanelia369/Grocery-API-Postman-Tests)

### Debug Diary: debugging notes

Short entries from my Java/Selenium/TestNG calendar automation project and other testing work.

- **Race condition, not a slow page:** a test failed about 1 in 5 runs. The wait covered the input becoming visible, not the dropdown content rendering. Fixed with an explicit wait inside the getters instead of `Thread.sleep()`.
- **An assertion that could never fail:** it located the element by the same class it then checked. Rewritten with XPath and a real `aria-current="date"` assertion.
- **Passed in the IDE, not in the terminal:** `mvn clean test` ran 6 of 7 tests because one class was missing from `testNG.xml`. IntelliJ's Run button had hidden the gap.
- - **A generic error and the logs behind it:** a search flow showed only "Something happened". The console showed `400` with `Invalid station code.` and two later `400 Bad Request` failures. I could not prove the first explained the others, so the root cause stays unconfirmed in my notes.

[Repository: Debug-Diary](https://github.com/anadanelia369/Debug-Diary)

---

## 🐞 Selected bug reports

| Project | Bug ID | Title | Severity | Status |
|---|---|---|---|---|
| ODIN | ODIN-974 | Phone Country Code Auto-Changes on Back Navigation | High | Done |
| ODIN | ODIN-995 | Time Picker Crash on Chat Screen | High | Done |
| ODIN | ODIN-1009 | Order Edit Shows Cached Data, Updates Multiple Times | Medium | Done |
| ODIN | ODIN-1013 | System Back Button Shows Previous Trip's Data | High | Done |
| ODIN | ODIN-1052 | Phone Number Input Focus Jumps to City Field on First Tap | Medium | Done |
| ODIN | ODIN-1079 | Offers Tab Shows an Incomplete Delivery Date Range (17-17 instead of 17-18) | Medium | Done |
| GPI Holding | GPI-ANN-11 | Afghan Citizenship + Georgian ID Accepted Without Validation | High | Open |
| GPI Holding | GPI-ANN-12 | 366-Day Travel Period Accepted Without Validation | Medium | Open |
| GPI Holding | GPI-ANN-13 | Autofill Returns a Stranger's Personal Data | High | Open |
| GPI Holding | GPI-ANN-14 | Clinic List Truncated on iPad Air Resolution | Low | Open |


### Text-to-speech skips "++" in programming language names

Found while listening to an audiobook of "Thinking in Java" in a text-to-speech app: the narrator read "C++" as "C". I tested more inputs and found where it starts to fail. Read correctly: C+, 2+2, +1, C#, .NET, Node.js. Skipped: C++, 2++, 1++, ++2. A single "+" works, two in a row do not. This changes the meaning of the text, because C and C++ are different languages. Written up with three answers: what fails, where exactly it starts to fail, and why it matters to the user.

[Read the LinkedIn post](https://lnkd.in/p/dP4z6ZHs)

---

## 🛠️ Skills and tools

- **Testing types:** Manual, Functional, Regression, Exploratory, Smoke, Mobile, Cross-browser, Localization, UX
- **Test design:** Equivalence Partitioning (EP), Boundary Value Analysis (BVA), Decision Tables, State Transition Testing
- **Test management:** Jira, Testiny, TestCaseLab, Qase.io
- **Bug tracking:** Jira, Linear, Jam.dev, Trello
- **API testing:** Postman (Collections, Environments, Assertions, Runner), REST API, Swagger
- **API testing in CI:** Newman, GitHub Actions
- **Automation:** Java, Selenium WebDriver, TestNG, Maven, Page Object Model, IntelliJ IDEA
- **Debugging and diagnostics:** Browser DevTools, ADB, Logcat, Android Studio, Charles Proxy
- **Other:** basic SQL, basic HTML/CSS, Git

---

## 🧠 How I work

- **Test design:** EP and BVA for valid and invalid boundaries, Decision Tables for complex business logic. Mobile testing follows the I SLICED UP FUN framework.
- **Bug reporting:** clear, reproducible titles. Every report includes preconditions, numbered action steps, actual vs expected result, severity and impact, device/OS/environment and reproducibility rate. Cross-checked against Figma designs. Root cause guesses are labeled as assumptions.
- **API testing:** status codes, response body structure, data types, positive and negative scenarios including invalid inputs, missing auth tokens and boundary values.
- **Automation:** Java + Selenium WebDriver + TestNG, Page Object Model, Maven.

---

## 🎓 Learning and certificates

- **Completed:** [Quality Academy](https://www.linkedin.com/company/quality-academy-%E2%80%A2-%E1%83%AE%E1%83%90%E1%83%A0%E1%83%98%E1%83%A1%E1%83%AE%E1%83%98%E1%83%A1-%E1%83%90%E1%83%99%E1%83%90%E1%83%93%E1%83%94%E1%83%9B%E1%83%98%E1%83%90/) Manual QA course (Oct 2025 - Jan 2026)
- **Completed:** [Quality Academy](https://www.linkedin.com/company/quality-academy-%E2%80%A2-%E1%83%AE%E1%83%90%E1%83%A0%E1%83%98%E1%83%A1%E1%83%AE%E1%83%98%E1%83%A1-%E1%83%90%E1%83%99%E1%83%90%E1%83%93%E1%83%94%E1%83%9B%E1%83%98%E1%83%90/) Java/Selenium course (Mar - Jul 2026)
- **Completed:** uTest Academy, Introduction to Testing certification cycle (bug report and test case both approved)
- **Certificates:** Tester Work (Functional Testing, Payment Testing, KYC Testing), Testlio (Usability 101, Usability 102), Ubertesters (onboarding completed)

---

> "Every system has two realities: expected behavior and actual behavior. QA lives in the space between them."

---

## 📬 Contact

Based in Tbilisi, Georgia (GMT+4). Open to remote QA opportunities.

[LinkedIn](https://linkedin.com/in/ana-danelia-42567139b) | [Portfolio website](https://anadanelia369.github.io/QA-Portfolio/) | [GitHub](https://github.com/anadanelia369)
