# TC-ODIN-09

Feature: Order Flow
Priority: High
Status: Not Executed 
Title: Two Travelers Place Bid on Same Trip Simultaneously
Type: Edge Case

**`Preconditions:`**

- Two separate Traveler accounts are logged into ODIN
- An active Sender order is visible in both accounts
- Both travelers are on the bid submission screen at the same time

**`Test Data:`**

- Traveler A: [account_traveler_A@test.com](mailto:account_traveler_A@test.com)
- Traveler B: [account_traveler_B@test.com](mailto:account_traveler_B@test.com)
- Sender order: active, unaccepted

**`Steps to Reproduce:`**

1. Open ODIN on two devices (or two browser sessions) simultaneously
2. Log in Traveler A on Device 1, Traveler B on Device 2
3. Both travelers navigate to the same open Sender order
4. Both click "Submit Bid" at the exact same moment (within 1-2 seconds)

**`Actual Result:`**

Not yet executed — environment requires two test accounts and simultaneous action.

**`Expected Result:`**

Only one bid should be accepted. The second bid should receive a clear error or "Order already taken" message. No duplicate state, no crash, no silent failure.

**`Notes:`**

This is a race condition / concurrency scenario. Most likely requires coordination with the dev team or backend logs to verify.