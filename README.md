# Ana Danelia

## Manual QA Tester | Web & Mobile Testing | API Testing | Bug Reports

I test web and mobile applications, design test cases, investigate defects, and write clear, reproducible bug reports. I also build Java/Selenium automation tests and API test collections.

**Based in Tbilisi, Georgia (GMT+4) | Open to remote QA opportunities**

[Portfolio website](https://anadanelia369.github.io/QA-Portfolio/) | [LinkedIn](https://linkedin.com/in/ana-danelia-42567139b) | [GitHub](https://github.com/anadanelia369)

### What I bring

- Manual testing for web, Android, iOS and Android TV applications
- Test case design using Equivalence Partitioning, Boundary Value Analysis and Decision Tables
- Clear, reproducible bug reports with severity, impact, environment and evidence
- REST API testing with Postman, assertions and negative scenarios
- Java, Selenium WebDriver, TestNG, Page Object Model, Maven and RestAssured
- Practical experience with Jira, Testiny, Qase.io, browser DevTools, ADB and Logcat

---

## Highlights

| Area | Result |
|---|---|
| ODIN UAT internship | 328 test scenarios, 37 test cases and 20+ bugs filed in Jira |
| autism.ge UAT | 14 findings, including 4 Critical defects, on a live donation website |
| GPI Holding web testing | 20 test cases and 4 documented defects, including security-related findings |
| Simple Grocery Store API | Postman API test collection with Newman and GitHub Actions |
| Java/Selenium automation | Test framework using Java, Selenium WebDriver, TestNG, Page Object Model and Maven |
| Crowdtesting | Paid and unpaid cycles on Testlio, Test.io, uTest, Tester Work and Ubertesters |
| Recognition | Testlio Freelancer of the Month, September 2026 |

---

## Featured projects

### 1. Simple Grocery Store API: API testing with CI/CD

**Type:** API testing  
**Stack:** Postman, Newman, htmlextra, GitHub Actions  
**Status:** In progress  
**Repository:** [Grocery-API-Postman-Tests](https://github.com/anadanelia369/Grocery-API-Postman-Tests)

I created a Postman collection for a public REST API covering products, cart, orders and authentication.

- Designed positive and negative test scenarios for each API resource
- Applied boundary, invalid, null, empty and method-based test design
- Added assertions for status codes, response body structure and data types
- Separated test requests into Positive and Negative folders
- Stored the base URL in a Postman Environment
- Configured Newman and htmlextra to generate an HTML test report
- Added a GitHub Actions workflow that runs the collection and uploads the report as an artifact
- Documented API behavior that differs from the documentation as Known Issues

**Completed:** Status and Products folders  
**In progress:** Cart, Orders and Authentication folders

### 2. GPI Calendar Automation: Java and Selenium

**Type:** UI automation  
**Stack:** Java, Selenium WebDriver, TestNG, Page Object Model, Maven, RestAssured  
**Repository:** [GpiCalendarAutomation](https://github.com/anadanelia369/GpiCalendarAutomation)  
**Debugging notes:** [Debug Diary](https://github.com/anadanelia369/Debug-Diary)

I built a Java/Selenium/TestNG automation framework for a travel insurance calendar.

- Used the Page Object Model to separate page structure from test logic
- Wrote automated tests for calendar navigation and date selection
- Used Maven for project and dependency management
- Investigated unstable tests, incorrect assertions and configuration issues
- Replaced unnecessary waits with explicit waits where appropriate
- Documented 12 debugging cases in the Debug Diary repository

**Example findings**

- A test failed intermittently because the wait checked input visibility, not dropdown rendering
- An assertion could not fail because it used the same locator for locating and checking the element
- A test passed in IntelliJ but failed through Maven because one test class was missing from testNG.xml
- A date calculation issue appeared only at the end of the month, when the selected date moved to the next month

### 3. ODIN: P2P Parcel Delivery App

**Type:** Manual mobile UAT  
**Role:** UAT intern  
**Period:** February 2026 to July 2026  
**Platform:** React Native Android application  
**Test cases:** [ODIN test cases](test-cases/ODIN)

I performed UAT for ODIN, a Georgian P2P parcel delivery application.

- Created 328 test scenarios across 13 feature modules
- Designed and documented 37 test cases
- Filed 20+ defects in Jira
- Documented 6 defects in detail in this portfolio
- Tested multi-step flows, including orders, trips, offers, chat and notifications
- Used hypothesis-based exploratory testing for flight notification timing

**Selected defects**

| Bug ID | Title | Severity |
|---|---|---|
| ODIN-974 | Phone Country Code Auto-Changes on Back Navigation | High |
| ODIN-995 | Time Picker Crash on Chat Screen | High |
| ODIN-1009 | Order Edit Shows Cached Data, Updates Multiple Times | Medium |
| ODIN-1013 | System Back Button Shows Previous Trip's Data | High |
| ODIN-1052 | Phone Number Input Focus Jumps to City Field on First Tap | Medium |
| ODIN-1079 | Offers Tab Shows an Incomplete Delivery Date Range | Medium |

### 4. autism.ge: Charity Donation Website

**Type:** Pro bono UAT  
**Platform:** WordPress website  
**Focus:** Authentication, donation flow and payment processing  
**Full report:** [autism.ge report](projects/autism-ge/README.md)

I performed risk-based UAT for a live charity donation website.

- Focused on high-risk areas: login, registration, donation flow and payment processing
- Identified 14 findings
- Reported 4 Critical, 4 High and 6 Medium issues
- Found a WordPress error displayed after a successful payment
- The site team fixed the reported payment-related issue after my report

---

## Additional testing experience

### GPI Holding: Insurance Web Platform

**Type:** Independent exploratory web testing  
**Platform:** Web, Chrome  
**Test cases:** [GPI test cases](test-cases/GPI)

I independently tested a travel insurance web platform.

- Created 20 test cases using Equivalence Partitioning and Boundary Value Analysis
- Focused on the travel period calendar and form validation
- Documented 4 defects
- Identified 2 security-related issues: autofill data exposure and acceptance of an invalid citizenship and document combination

| Bug ID | Title | Severity |
|---|---|---|
| GPI-ANN-11 | Afghan Citizenship + Georgian ID Accepted Without Validation | High |
| GPI-ANN-12 | 366-Day Travel Period Accepted Without Validation | Medium |
| GPI-ANN-13 | Autofill Returns a Stranger's Personal Data | High |
| GPI-ANN-14 | Clinic List Truncated on iPad Air Resolution | Low |

### Language-learning app: Paid QA test

**Type:** Paid freelance mobile QA  
**Platform:** Android and iOS  
**Client permission:** Published without app name or screenshots

I tested a mobile language-learning application with an AI practice chat.

- Tested Explore, Chats and Rooms pages as a regular user
- Also tested registration, profile, practice and settings
- Delivered 14 findings: 7 Medium and 7 Low severity
- Found that the Android Back button ended an active call without confirmation
- Found that a password rule shown in the hint was not enforced during registration or password change
- Delivered a PDF report and a separate screen recording

### Freelance crowdtesting

**Platforms:** Testlio, Test.io, uTest, Tester Work and Ubertesters  
**Devices:** Android phone, Android tablet, Android TV and desktop browsers  
**Project types:** E-commerce, food delivery, streaming and mobile applications

I participate in paid and unpaid crowdtesting cycles on real devices and desktop browsers.

- Follow platform-specific scope, severity and staging requirements
- Test on the requested device, OS and browser configuration
- Attach screencasts and clear reproduction steps to functional defects
- Check severity limits and reporting rules before submitting a defect
- Use ADB, Logcat and Charles Proxy for environment troubleshooting

**Recognition**

- Testlio Freelancer of the Month, September 2026
- uTest Academy: Introduction to Testing certification cycle passed
- Tester Work certificates: Functional Testing, Payment Testing and KYC Testing
- Testlio certificates: Freelancer Conduct Guidelines, Usability 101 and Usability 102

---

## How I work

### Test design

- Use Equivalence Partitioning and Boundary Value Analysis for valid and invalid inputs
- Use Decision Tables for complex business rules
- Use State Transition Testing where user flows depend on changing states
- Apply the I SLICED UP FUN framework for mobile testing

### Bug reporting

- Write clear, specific and reproducible defect titles
- Include preconditions, numbered reproduction steps, actual result and expected result
- Add severity, impact, environment, device, OS and reproducibility rate
- Attach screenshots, screen recordings and logs when available
- Compare behavior with Figma designs when designs are available
- Clearly label root-cause assumptions as assumptions

### API testing

- Validate status codes, response bodies, data types and response structure
- Test positive, negative, boundary, missing authentication and invalid input scenarios
- Use Postman Collections, Environments, assertions and Runner
- Run collections with Newman and generate HTML reports

### Automation

- Build tests with Java, Selenium WebDriver, TestNG and Maven
- Apply the Page Object Model
- Use explicit waits instead of fixed sleeps where possible
- Investigate failures through logs, browser DevTools and controlled debugging

---

## Skills and tools

| Area | Tools and skills |
|---|---|
| Testing | Manual, functional, regression, exploratory, smoke, mobile, cross-browser, localization and UX testing |
| Test design | Equivalence Partitioning, Boundary Value Analysis, Decision Tables, State Transition Testing |
| Test management | Jira, Testiny, TestCaseLab, Qase.io |
| Bug tracking | Jira, Linear, ClickUp, Jam.dev, Trello |
| API testing | Postman, REST API, Swagger, Newman |
| Automation | Java, Selenium WebDriver, TestNG, Page Object Model, Maven, RestAssured |
| Debugging | Browser DevTools, ADB, Logcat, Android Studio, Charles Proxy |
| CI/CD | GitHub Actions, Newman, htmlextra |
| Other | Basic SQL, basic HTML/CSS, Git |

---

## Devices and browsers

| Category | Details |
|---|---|
| Mobile devices | Honor X8d, Android 16; Samsung Galaxy Tab A7 Lite, Android 14 |
| TV device | Android TV |
| Computer | Windows laptop |
| Browsers | Chrome, Brave, Firefox, Edge |

---

## Links

- [Portfolio website](https://anadanelia369.github.io/QA-Portfolio/)
- [LinkedIn](https://linkedin.com/in/ana-danelia-42567139b)
- [GitHub](https://github.com/anadanelia369)
- [Simple Grocery Store API tests](https://github.com/anadanelia369/Grocery-API-Postman-Tests)
- [Debug Diary](https://github.com/anadanelia369/Debug-Diary)
- [GPI Calendar Automation](https://github.com/anadanelia369/GpiCalendarAutomation)
- [CV: Ana_Danelia_QA_Engineer.pdf](Ana_Danelia_QA_Engineer.pdf)
