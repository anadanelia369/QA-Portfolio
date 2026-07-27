# autism.ge (ფერადი ქალაქი) — Pro Bono UAT

**Type:** Pro Bono / Volunteer UAT  
**Platform:** WordPress  
**Environment:** Windows 11 · Chrome  
**Tester:** Ana Danelia  
**Approach:** Risk-based testing — prioritizing authentication and payment/donation flows  

---

## Summary

| Severity | Count |
|----------|-------|
| 🔴 Critical | 4 |
| 🟠 High | 4 |
| 🟡 Medium | 6 |
| **Total Findings** | **14** |

**Testing Scope:** Authentication · Profile Management · Subscriptions · Cart/Checkout · Payment Processing (Visa, Google Pay) · Localization (GE/EN)  
**Evidence:** 9 annotated screenshots · 2 screen recordings (full payment flow; insufficient funds scenario)

---

## 🔴 Critical

### BUG-01 — Missing "Forgot Password" Functionality
**Area:** Authentication  
**Description:** No password recovery mechanism exists on the login page. Users who forget their password have no self-service way to regain account access.  
**Impact:** Users are permanently locked out without support intervention.

---

### BUG-02 — Missing Password Visibility Toggle (Eye Icon)
**Area:** Authentication  
**Description:** The password input field has no "show password" option, forcing users to type blind.  
**Impact:** Increases login errors, especially on mobile; reduces usability.

---

### BUG-03 — Subscriptions Not Displaying on Subscriptions Page
**Area:** User Account / Subscriptions  
**Description:** Active subscriptions do not appear on the dedicated Subscriptions page, even when confirmed active elsewhere in the system.  
**Impact:** Users cannot verify or manage their own subscription status — high risk of confusion and support tickets.

---

### BUG-04 — WordPress Backend Returns Error Despite Successful Payment
**Area:** Payment Processing  
**Steps to Reproduce:**
1. Add donation (monthly or one-time) to cart while authorized
2. Proceed to payment, complete with Visa or Google Pay
3. Observe redirect page after transaction

**Actual Result:** Payment succeeds (confirmed via email with correct subscription details), but backend simultaneously shows an error on the post-redirect page.  
**Expected Result:** Clean confirmation page with no error.  
**Business Risk:** "False failure" signal may cause donors to believe payment failed and attempt to pay again — risk of duplicate charges or donor abandonment.  
**Evidence:** Screen recording of full payment flow (Visa); screen recording of insufficient-funds card scenario.

---

## 🟠 High / Functional

### BUG-05 — Auth Page Still Accessible After Logout
**Area:** Session Management  
**Description:** After clicking "Logout," the authentication/login page remains accessible in a state suggesting the session was not properly invalidated.  
**Impact:** Potential session-handling security concern; needs backend session verification.

---

### BUG-06 — Cart Shows Only One-Time Donation for Authorized Users
**Area:** Cart / Checkout  
**Description:** When an authorized user has both monthly and one-time donation options, the cart only displays the one-time donation.  
**Impact:** Monthly donors may be unable to complete or verify their intended recurring contribution.

---

### BUG-07 — "Update" Button Disabled, "Pay" Button Redirects Unexpectedly
**Area:** Cart / Checkout  
**Description:** The "Update" button in the cart is non-functional (disabled), while clicking "Pay" triggers an immediate redirect without expected intermediate confirmation.  
**Impact:** Users cannot adjust cart contents before payment; workflow is abrupt and confusing.

---

### BUG-08 — Misleading Button Label — "Registration" Shown to Already-Authorized Users
**Area:** UX / Checkout Flow  
**Description:** The payment flow displays a "Registration" button even for users who are already logged in.  
**Impact:** Confusing UX — implies account creation is needed when it is not.  
**Recommendation:** Label should read "Payment" for authorized users; "Registration" is only relevant on first-time flows.

---

## 🟡 Medium / UI & Localization

### BUG-09 — Language Flicker on Redirect (English → Georgian)
**Area:** Localization  
**Description:** On page redirect, the interface briefly displays English (~2 seconds) before switching to Georgian once backend data loads.  
**Recommendation:** Persist the user's language choice in `localStorage` so the correct language renders immediately.

### BUG-10 — Icon Margin Inconsistency (Post-Redirect Page Only)
**Area:** UI  
**Description:** Spacing between profile and cart icons is inconsistent specifically on the post-redirect page.

### BUG-11 — "No Payment Found" Message Untranslated
**Area:** Localization  
**Description:** Error message "No payment Found" displays in English regardless of selected site language.

### BUG-12 — Profile Edit Screen — Translation Gaps
**Area:** Localization  
**Description:** Several UI strings on the profile editing screen are untranslated; eye-icon also missing (see BUG-02).

### BUG-13 — Confirmation Email — Translation Quality
**Area:** Localization  
**Description:** Payment confirmation email correctly displays subscription details, but translation quality needs improvement.

### BUG-14 — Order Details Untranslated on Payment Page
**Area:** Localization  
**Description:** Since the payment page has a language-switch feature, the order summary itself should also switch accordingly.  
**Priority:** Low

---

## ✅ Verified Working

- Social media links (YouTube, Instagram, Facebook) — correctly linked
- "Donation" button (top & bottom of page) — redirects correctly
- Payment via Visa — confirmed successful
- Payment via Google Pay — confirmed successful
- Confirmation email — subscription details (monthly/one-time) display correctly

---

## 💡 UX Recommendations

**Donation Box Ordering:**  
Monthly donations are the organization's priority. Recommended order:
1. **Monthly Donation** — moved to first position, more prominent color
2. One-Time Donation — second position
3. Product/Merchandise — third position

Current design draws more visual attention to the one-time donation box due to color choice — recommend shifting emphasis toward recurring/monthly giving.
