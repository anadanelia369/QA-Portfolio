# ODIN-995

**Title:** Time Picker Crash on Chat Screen
**Company:** ODIN
**Device:** Android 14 / Realme 10, and a Samsung tablet
**Environment:** UAT
**Severity:** High
**Status:** Done
**Type:** Functional
**Reproducibility:** 100%

## Summary

When scheduling a meeting time in the Sender-Traveler chat, the Time Picker fails to register the selected time and causes the app to crash on the first attempt, on two different Android devices (Realme 10 and a Samsung tablet).

## Preconditions

- Logged into ODIN as both Sender and Traveler accounts
- Active order exists between Sender and Traveler

## Steps to Reproduce

1. Open ODIN app
2. Navigate to Chat section
3. Open Sender-Traveler Chat
4. Tap "Schedule meeting time"
5. Select date: 16/02
6. Proceed to the time selection step
7. Attempt to select a specific hour

## Actual Result

Time Picker does not register the selected time. Scroll freezes automatically. App crashes on both devices on the first attempt.

## Expected Result

User should be able to select a specific time stably. Time Picker must register the selection without freezing or crashing.

## Impact & Rationale

App crash in a core communication feature (chat scheduling), reproduced on two different Android devices, which suggests the issue is not specific to one device. Affects both Sender and Traveler roles.

## Root Cause Guess

Time Picker component likely has an unhandled scroll event conflict that triggers an exception on first interaction.
