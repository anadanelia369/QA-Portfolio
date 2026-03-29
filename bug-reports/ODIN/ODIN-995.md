# ODIN-995

Title                          : Time Picker Crash on Chat Screen
Company: ODIN
Device/Browser: Android 14 / Realme 10
Environment: UAT
Severity: Critical
Status: Done
Type: Functional

Severity: `High,`Reproducibility: `100%`

---

`Summary` When scheduling a meeting time in the Sender-Traveler chat, the Time Picker fails to register the selected time and causes the app to crash on first attempt across two different Android devices.

---

`Preconditions`

- Logged into ODIN as both Sender and Traveler accounts
- Active order exists between Sender and Traveler

---

`Steps to Reproduce`

1. Open ODIN app
2. Navigate to Chat section
3. Open Sender–Traveler Chat
4. Tap "Schedule meeting time"
5. Select date: 16/02
6. System navigates to time selection step
7. Attempt to select a specific hour

---

`Actual Result:`Time Picker does not register the selected time. Scroll freezes automatically. App crashes on both devices on first attempt.

---

`Expected Result:` User should be able to select a specific time stably. Time Picker must register selection without freezing or crashing.

---

`Impact & Rationale` Critical bug  — app crash on a core communication feature (chat scheduling) across multiple devices indicates a systemic UI component failure, not a device-specific issue. Affects both Sender and Traveler roles.

---

`Root Cause Guess` Time Picker component likely has an unhandled scroll event conflict that triggers an exception on first interaction.