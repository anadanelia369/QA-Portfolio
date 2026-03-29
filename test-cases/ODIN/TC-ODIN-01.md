# TC-ODIN-01

Feature: Register
Priority: High
Status: Pass
Title: OTP Verification Attempted After 15-Minute Expiry
Type: Edge Case

---

**`Preconditions:`**

- User has initiated registration with a valid email
- OTP verification email has been received
- 15 minutes have passed since OTP was issued

**`Test Data:`**

- Registration email: test account email
- OTP: expired code (received 15+ minutes ago)

**`Steps to Reproduce:`**

1. Open ODIN App
2. Navigate to **Register**
3. Enter valid email and password
4. Tap **Continue** → OTP sent to email
5. Open email → note the OTP code
6. Wait **15+ minutes** without entering the code
7. Return to OTP input screen
8. Enter the expired OTP code

**`Expected Result:`**
System rejects the expired OTP and displays a validation message indicating the code has expired. User is prompted to request a new code via **Resend**. Registration is not completed with the expired code.

**`Notes:`**
15-minute OTP expiry is a standard security measure. This edge case validates that the backend correctly tracks token issuance time and enforces expiry — preventing replay attacks on the registration flow.