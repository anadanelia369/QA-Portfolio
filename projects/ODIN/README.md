# ODIN: P2P Parcel Delivery App

**UAT internship | Feb 2026 - Jul 2026**

## About the project

ODIN is a Georgian P2P parcel delivery mobile application built in React Native (iOS/Android). The platform connects Senders who need parcels delivered internationally with Travelers who have available luggage space on their flights.

## My role

Manual QA tester. Responsible for functional, UX, localization and exploratory testing across the full app.

## Scope

- 328 test scenarios across 13 feature modules: Registration, Login, Order Flow, Chat, Profile, Settings, Notifications, Dark Mode, Localization, Payments, Security, Navigation, Accessibility
- 20+ bugs filed in Jira, 6 documented in detail in this repository
- Exploratory testing findings documented as observations

## Key findings

- **State management in multi-step flows:** ODIN-974 (the phone country code silently changes on back navigation) and ODIN-1013 (the System Back button makes Trip B show Trip A's data).
- **Crash in a core feature:** ODIN-995, the Time Picker in the Sender-Traveler chat freezes and crashes the app on first use, reproduced on two Android devices (Realme 10 and a Samsung tablet).
- **Flight notification timing hypothesis:** identified a backend notification timing issue through hypothesis-based exploratory testing, using two real flights with different durations (LHR to AMS about 1h20m, LHR to JFK about 8h10m). Shared proactively with the Team Lead and a Developer. [Read the observation](https://github.com/anadanelia369/QA-Portfolio/blob/main/projects/ODIN/flight-notification-observation.md)

## Documented bug reports

| ID | Title | Severity | Type |
|---|---|---|---|
| ODIN-974 | Phone Country Code Auto-Changes on Back Navigation | High | Functional |
| ODIN-995 | Time Picker Crash on Chat Screen | High | Functional |
| ODIN-1009 | Order Edit Shows Cached Data, Updates Multiple Times | Medium | Functional |
| ODIN-1013 | System Back Button Breaks Trip Flow | High | Functional |
| ODIN-1052 | Phone Number Input Focus Jumps to City Field on First Tap | Medium | UX / Focus |
| ODIN-1079 | Offers Tab Shows an Incomplete Delivery Date Range (17-17 instead of 17-18) | Medium | Functional |

All reports: [ODIN bug reports](https://github.com/anadanelia369/QA-Portfolio/blob/main/bug-reports/ODIN)

Each report includes preconditions, steps to reproduce, expected and actual result, impact, and a root cause guess that is labeled as my assumption.

## Test cases

[View ODIN test cases](https://github.com/anadanelia369/QA-Portfolio/blob/main/test-cases/ODIN)

## Note

ODIN screens are not published. The reports in this repository are text only and anonymized where needed.
