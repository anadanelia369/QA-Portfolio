# TC-ODIN-34

Feature: Login
Priority: High
Status: Pass
Title: Forgot Password — Only Latest OTP Valid After Resend
Type: Edge Case

**`Preconditions:`**

- User has a registered ODIN account
- User is on the Login screen
- Email inbox is accessible for OTP verification

**`Test Data:`**

- Registered email: test account email
- OTP 1: first code received
- OTP 2: second code received after Resend

**`Steps to Reproduce:`**

1. Open ODIN App
2. Tap **Forgot Password?**
3. Enter registered email → tap **Continue**
4. Receive first OTP (OTP 1) in email inbox
5. Do NOT enter OTP 1 yet
6. Tap **Resend Code**
7. Receive second OTP (OTP 2) in email inbox
8. Attempt to enter **OTP 1** (the first, now invalidated code)
9. Observe system response
10. Enter **OTP 2** (the latest code)

**`Expected Result:`**
OTP 1 is rejected — system displays validation error indicating the code is invalid or expired. OTP 2 is accepted successfully and user proceeds to password reset screen.

**`Notes:`**
This validates that ODIN correctly invalidates previous OTP codes upon Resend — critical security behavior. Only the most recently issued code should be valid at any given time.