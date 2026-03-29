# TC-ODIN-15

Feature: Trip
Priority: High
Status: Pass
Title: Trip — En-Route Pickup Cities (Tbilisi → Gori → Kutaisi)
Type: Positive

**`Preconditions:`**

- User is logged into ODIN App as Traveler
- A Trip has been created and **confirmed by backend**
- Trip is visible in Dashboard

**`Test Data:`**

- Existing confirmed Trip: TK001
- Pickup cities to add: Gori, Kutaisi

**`Steps to Reproduce:`**

1. Open ODIN App
2. Navigate to **Dashboard**
3. Open confirmed Trip (TK001)
4. Tap **Add Pickup City**
5. Select **Gori** → Save
6. Tap **Add Pickup City** again
7. Select **Kutaisi** → Save

**`Expected Result:`**
Both cities (Gori, Kutaisi) are added successfully and visible in Trip detail screen alongside the original departure city. Senders from these cities can now see and offer on this Trip.

**`Notes:`**
Add City feature is only available after backend Trip confirmation — not during initial Trip creation. This is a core P2P differentiator enabling multi-city parcel collection along the Traveler's route.