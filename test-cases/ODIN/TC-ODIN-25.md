# TC-ODIN-25

Feature: Order Flow
Priority: High
Status: Pass
Title: Sender Accepts Offer — Order Moves to Active
Type: Positive

---

**`Preconditions:`**

- Two test accounts exist: Sender and Traveler
- Sender has an active Auction Order in **Pending** status
- Traveler has placed an offer on the Order
- Offer is visible in Sender's Order detail screen

**`Test Data:`**

- Sender account: test account 1
- Traveler account: test account 2
- Offer amount: any valid amount

**`Steps to Reproduce:`**

1. Open ODIN App as **Sender**
2. Navigate to **Orders**
3. Open Pending Auction Order
4. Navigate to **Offers** tab
5. Review incoming offer from Traveler
6. Tap **Accept Offer**
7. Confirm acceptance
8. Observe Order status on Sender's screen
9. Switch to Traveler account → observe Order status

**`Expected Result:`**
Order status changes from **Pending** → **Active** on both Sender and Traveler accounts immediately after acceptance. Traveler receives push notification. Chat between Sender and Traveler becomes accessible. No other Travelers can place offers on this Order.

**`Notes:`**
This is the critical handoff moment in ODIN's P2P flow — once an offer is accepted, the delivery commitment is established between two users.