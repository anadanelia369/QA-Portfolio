# Language-Learning App: Paid QA Test

Manual testing of a mobile language-learning app with an AI practice chat, delivered as a paid Upwork project. The client gave permission to use the report in my portfolio. The app name, test accounts and app screens are not published.

| | |
|---|---|
| **Type** | Paid freelance QA test (Upwork) |
| **Date** | 1 November 2026 |
| **Devices** | Honor X8d (Android 16), iPhone (landscape checks and the photo reply check) |
| **Approach** | Testing as a normal user. Requested scope: Explore, Chats and Rooms pages. Additional findings from other parts of the app are listed separately |
| **Deliverable** | PDF report with steps, actual and expected result, severity and evidence, plus a separate screen recording |

## Results at a glance

| | Medium | Low | Total |
|---|---|---|---|
| Part A: requested pages (Explore, Chats, Rooms) | 2 | 5 | 7 |
| Part B: additional findings (registration, profile, practice, Privacy Policy, comments) | 5 | 2 | 7 |
| **Total** | **7** | **7** | **14** |

No crashes were found. Explore worked without problems.

Severity: **Medium** means a feature is broken, misleading or unsafe, but there is a workaround. **Low** means a cosmetic or small usability problem.

## What worked well

- Profile view notifications arrive right away when another user opens the profile.
- The welcome bonus coupon was claimed and activated without problems.
- Call recordings: opening them with coins and deleting them both worked.
- Sending, receiving and accepting invitations worked.

## Not tested

- **Create Room:** the page requires a coin balance that the test account did not have. I asked the client to add coins if this flow should be tested.

## Highlighted findings

### KON-01 | Medium | Android Back button ends a call

**Steps:**
1. Start or accept an audio or video call.
2. Press the Android system Back button.

**Actual:** the call ends right away, with no question.
**Expected:** Back does not end the call silently. It asks for confirmation or minimizes the call. The red End Call button ends the call.

### KON-08 | Medium | Registration accepts a password with letters only

**Steps:**
1. Open the registration screen.
2. Enter a name and an email.
3. Type a password with letters only in both password fields.

**Actual:** the hint says "At least 6 characters, include a number or symbol", but the password is accepted and no error is shown.
**Expected:** a password without a number or symbol is rejected with an error.

### KON-09 | Medium | Change Password has the same problem

**Steps:**
1. Open Profile and go to Change Password.
2. Enter a new password with only letters.
3. Confirm the change.

**Actual:** the password is accepted. The rule shown at registration is not checked here either.
**Expected:** the same rule as in registration, and a wrong password is rejected.

## All findings

### Part A: requested pages

| ID | Area | Severity | Title |
|---|---|---|---|
| KON-01 | Chats | Medium | Android Back button ends a call |
| KON-02 | Chats | Medium | Screen turns off during a video call |
| KON-03 | Chats | Low | Incoming call shows the app name as my own name |
| KON-04 | Chats | Low | Voice message spinner stays after playback starts |
| KON-05 | Chats | Low | Reply bar shows a gray placeholder instead of the photo (checked on iPhone) |
| KON-06 | Chats | Low | Landscape on iPhone: keyboard hides the chat (usability suggestion) |
| KON-07 | Rooms | Low | Landscape on iPhone: camera cutout covers content |

### Part B: additional findings

| ID | Area | Severity | Title |
|---|---|---|---|
| KON-08 | Registration | Medium | Registration accepts a password with letters only |
| KON-09 | Profile | Medium | Change Password has the same problem |
| KON-10 | Profile | Medium | Profile picture needs two uploads |
| KON-11 | Practice, Lessons | Medium | Lesson screen: Next button covers the Back arrow |
| KON-12 | Privacy Policy | Medium | Privacy Policy page names a different app |
| KON-13 | Privacy Policy | Low | Language selector overlaps the header |
| KON-14 | Comments | Low | Reaction button shows a thumbs-up after choosing Haha |

## Observations

- **Translate:** a message with mixed languages and spelling mistakes came back almost unchanged. It may be normal, so I asked the client what should happen when a text cannot be translated.
- **Georgian:** the AI practice chat teaches Georgian phrases, but Georgian is missing from the translation language options.

## Note on evidence

The screen recordings and the full PDF report are not published. A summary card is available in the Upwork portfolio.
