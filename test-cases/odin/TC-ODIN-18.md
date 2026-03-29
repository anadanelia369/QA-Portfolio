# TC-ODIN-18

Feature: Order
Priority: High
Status: Pass
Title: Standard Order Creation — Full Valid Flow
Type: Positive

**`Preconditions:`**

- Two test accounts exist: Sender and Traveler
- Both accounts have completed KYC verification
- Traveler has an active confirmed Trip
- Sender has created an Order matching the Trip route

**`Test Data:`**

- Sender account: test account 1
- Traveler account: test account 2
- Order: standard, valid route and dates

**`Steps to Reproduce:`**

1. Sender creates an Order → status: **Pending**
2. Traveler opens Offers tab → finds matching Order
3. Traveler places an offer on the Order
4. Sender accepts the offer → Order status: **Active**
5. Traveler meets Sender → Sender enters **Pickup Code**
6. Traveler confirms pickup → parcel collected
7. Traveler enters destination → Sender enters **Delivery Code**
8. Traveler confirms delivery → Order status: **Completed**

**`Expected Result:`**
Order correctly transitions through all three statuses: Pending → Active → Completed. Both Sender and Traveler see the correct final status. Transaction is reflected in Wallet.

**`Notes:`**
This is the core E2E flow of ODIN — the world's first P2P parcel delivery app. Full cycle validation is critical for every release.