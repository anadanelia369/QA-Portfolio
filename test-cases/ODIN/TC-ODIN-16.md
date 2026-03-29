# TC-ODIN-16

Feature: Trip
Priority: High
Status: Pass
Title: Trip — Delivery Across Multiple US Cities (NY, NJ)
Type: Positive

**`Preconditions:`**

- User is logged into ODIN App as Traveler
- A Trip has been created with destination: USA, and **confirmed by backend**
- Trip is visible in Dashboard

**`Test Data:`**

- Existing confirmed Trip: destination USA
- Delivery cities to add: New York, New Jersey

**`Steps to Reproduce:`**

1. Open ODIN App
2. Navigate to **Dashboard**
3. Open confirmed Trip (USA destination)
4. Tap **Add Delivery City**
5. Select country: **United States** → city: **New York** → Save
6. Tap **Add Delivery City** again
7. Select country: **United States** → city: **New Jersey** → Save

**`Expected Result:`**
Both US delivery cities (New York, New Jersey) are added successfully and visible in Trip detail screen. Senders in both cities can now see this Trip and place offers.

**`Notes:`**
This validates ODIN's international multi-city delivery feature — a Traveler flying to the USA can accept parcels destined for multiple American cities in a single Trip.