# Real Testing Observations — ODIN App

## `Overview`

During exploratory testing of the ODIN P2P parcel delivery app, I identified an issue with flight tracking notification timing by comparing two real flights with different durations.

---

## `Background`

In ODIN, a **Traveler** adds a flight to their Trip. Once the flight departs, the Sender should receive a notification that allows them to open FlightRadar and track the parcel in real time.

I wanted to verify: *when exactly does the Sender receive the notification after departure?*

---

## `Test Cases Compared`

### ✈️ Flight 1 — London Heathrow (LHR) → Amsterdam Schiphol (AMS)

| Field | Detail |
| --- | --- |
| Flight | BA430 |
| Departure | 06:45 (BST, UTC+1) |
| Arrival | 09:15 (CEST, UTC+2) |
| Flight Duration | ~1h 20m |
| Time Zone Diff | Amsterdam is +1h ahead of London |

**Result:** Sender received the notification only after the flight had already **landed**. FlightRadar was not accessible in time — tracking was not possible.

---

### ✈️ Flight 2 — London Heathrow (LHR) → New York JFK

| Field | Detail |
| --- | --- |
| Flight duration | ~8h 10m |
| Time Zone Diff | New York is -4h behind London (BST) |

**Result:** Sender received the notification ~1 hour after departure. The flight was still in the air. FlightRadar opened correctly and tracking worked.

---

## `Hypothesis`

The backend sends the Sender notification with a **fixed delay of ~1 hour after departure**, regardless of the flight duration.

- For **short flights** (≤ ~1.5h): notification arrives at or after landing → tracking is **impossible**
- For **long flights** (8h+): notification arrives in-flight → tracking **works correctly**

---

## `What I Did`

- Tested using **real flights** with confirmed schedules
- Compared **two data points** with significantly different flight durations
- Formed a hypothesis based on observed behavior
- Shared the finding with the **Team Lead and Developer** proactively
- This was logged as an **observation**, not a bug report — the team discussed it internally

---

## `Skills Demonstrated`

- Exploratory testing
- Hypothesis-based testing
- Root cause analysis
- Cross-referencing multiple test cases
- Proactive communication with dev team
- Real-world flight data used as test input

---