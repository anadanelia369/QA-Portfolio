# Bug Report — autism.ge (ფერადი ქალაქი)

**Type:** Pro Bono UAT  
**Environment:** Windows 11 · Chrome  
**Platform:** WordPress  
**Tester:** Ana Danelia  
**Approach:** Risk-based testing — prioritizing authentication and payment/donation flows  
**Evidence:** 9 annotated screenshots · 2 screen recordings (full payment flow; insufficient funds scenario)

---

## Summary

| Severity | Count |
|----------|-------|
| 🔴 Critical | 4 |
| 🟠 High | 4 |
| 🟡 Medium | 6 |
| **Total** | **14** |

---

## 🔴 Critical

### BUG-01 — Missing "Forgot Password" Functionality
**Area:** Authentication  
**Description:** No password recovery mechanism exists on the login page. Users who forget their password have no self-service way to regain account access.  
**Expected Result:** "Forgot Password" link present on login page, triggering recovery flow.  
**Actual Result:** No such option exists.  
**Impact:** Users are permanently locked out without support intervention.  
**Severity:** Critical | **Priority:** High

---

### BUG-02 — Missing Password Visibility Toggle (Eye Icon)
**Area:** Authentication  
**Description:** The password input field has no "show password" (eye icon) option, forcing users to type blind.  
**Expected Result:** Eye icon present on password field; toggles visibility on tap/click.  
**Actual Result:** No visibility toggle exists.  
**Impact:** Increases login errors, especially on mobile; reduces usability.  
**Severity:** Critical | **Priority:** High

---

### BUG-03 — Subscriptions Not Displaying on Subscriptions Page
**Area:** User Account / Subscriptions  
**Description:** Active subscriptions do not appear on the dedicated Subscriptions page, even when a subscription is confirmed active elsewhere in the system.  
**Expected Result:** Active subscriptions listed on Subscriptions page.  
**Actual Result:** Subscriptions page appears empty despite confirmed active subscription.  
**Impact:** Users cannot verify or manage their own subscription status — high risk of confusion and support tickets.  
**Severity:** Critical | **Priority:** High

---

### BUG-04 — WordPress Backend Returns Error Despite Successful Payment
**Area:** Payment Processing  
**Steps to Reproduce:**
1. Add donation (monthly or one-time) to cart while authorized
2. Proceed to payment, complete with Visa or Google Pay
3. Observe redirect page after transaction

**Expected Result:** Clean confirmation page with no error shown.  
**Actual Result:** Payment succeeds (confirmed via email with correct subscription details), but WordPress backend simultaneously displays an error on the post-redirect page.  
**Business Risk:** "False failure" signal may cause donors to believe payment failed and attempt to pay again — risk of duplicate charges or donor abandonment.  
**Evidence:** Screen recording of full payment flow (Visa); screen recording of insufficient-funds card scenario.  
**Severity:** Critical | **Priority:** Critical

---

## 🟠 High / Functional

### BUG-05 — Auth Page Still Accessible After Logout
**Area:** Session Management  
**Steps to Reproduce:**
1. Log in to account
2. Click "Logout"
3. Navigate back to authentication/login page

**Expected Result:** Session invalidated; login page shows clean logged-out state.  
**Actual Result:** Auth page remains accessible in a state suggesting session was not properly invalidated.  
**Impact:** Potential session-handling security concern; needs backend session verification.  
**Severity:** High | **Priority:** High

---

### BUG-06 — Cart Shows Only One-Time Donation for Authorized Users
**Area:** Cart / Checkout  
**Description:** When an authorized user has both monthly and one-time donation options, the cart only displays the one-time donation.  
**Expected Result:** Both donation types visible in cart.  
**Actual Result:** Only one-time donation displayed.  
**Impact:** Monthly donors may be unable to complete or verify their intended recurring contribution.  
**Severity:** High | **Priority:** High

---

### BUG-07 — "Update" Button Disabled, "Pay" Redirects Without Confirmation
**Area:** Cart / Checkout  
**Description:** The "Update" button in the cart is non-functional (disabled state), while clicking "Pay" triggers an immediate redirect without expected intermediate confirmation.  
**Expected Result:** "Update" button functional; "Pay" shows confirmation step before redirect.  
**Actual Result:** "Update" disabled; "Pay" redirects immediately.  
**Impact:** Users cannot adjust cart contents before payment; workflow feels abrupt.  
**Severity:** High | **Priority:** High

---

### BUG-08 — Misleading Button Label — "Registration" Shown to Authorized Users
**Area:** UX / Checkout Flow  
**Description:** The payment flow displays a "Registration" button even for users who are already logged in and authorized.  
**Expected Result:** Button label reads "Payment" for already-authorized users.  
**Actual Result:** Label reads "Registration" regardless of auth state.  
**Impact:** Confusing UX — implies account creation is needed when it is not.  
**Recommendation:** "Registration" label only relevant for first-time/guest flows.  
**Severity:** High | **Priority:** Medium

---

## 🟡 Medium / UI & Localization

### BUG-09 — Language Flicker on Redirect (English → Georgian)
**Area:** Localization  
**Description:** On page redirect, the interface briefly displays English (~2 seconds) before switching to Georgian once backend data loads.  
**Expected Result:** Correct language renders immediately on redirect.  
**Actual Result:** English displays briefly before switching to Georgian.  
**Recommendation:** Persist user's language choice in `localStorage` to eliminate reliance on backend round-trip.  
**Severity:** Medium | **Priority:** Medium

---

### BUG-10 — Icon Margin Inconsistency (Post-Redirect Page Only)
**Area:** UI  
**Description:** Spacing between profile and cart icons is inconsistent specifically on the post-redirect page; not observed elsewhere.  
**Note:** Not yet verified in DevTools/responsive view — flagged for follow-up.  
**Severity:** Medium | **Priority:** Low

---

### BUG-11 — "No Payment Found" Message Untranslated
**Area:** Localization  
**Description:** Error message "No payment Found" displays in English regardless of selected site language.  
**Expected Result:** Message displays in currently selected language.  
**Actual Result:** Message always displays in English.  
**Severity:** Medium | **Priority:** Medium

---

### BUG-12 — Profile Edit Screen — Translation Gaps
**Area:** Localization  
**Description:** Several UI strings on the profile editing screen are untranslated. Eye-icon also missing (see BUG-02).  
**Severity:** Medium | **Priority:** Medium

---

### BUG-13 — Confirmation Email — Translation Quality
**Area:** Localization  
**Description:** Payment confirmation email correctly displays monthly/one-time subscription details, but overall translation quality needs improvement.  
**Severity:** Medium | **Priority:** Low

---

### BUG-14 — Order Details Untranslated on Payment Page
**Area:** Localization  
**Description:** Payment page includes a language-switch feature, but the order summary itself does not switch language accordingly.  
**Expected Result:** Order details translate when language is switched.  
**Actual Result:** Order details remain in original language.  
**Severity:** Medium | **Priority:** Low

---

## ✅ Verified Working

- Social media links (YouTube, Instagram, Facebook) — correctly linked
- "Donation" button (top & bottom of page) — redirects correctly to donation page
- Payment via Visa — confirmed successful end-to-end
- Payment via Google Pay — confirmed successful
- Confirmation email — subscription details (monthly/one-time) display correctly

---

## 💡 UX Recommendations

**Donation Box Ordering:**  
Since monthly donations are the organization's priority, recommend reordering:
1. **Monthly Donation** — first position, more prominent color
2. One-Time Donation — second position
3. Product/Merchandise — third position

Current design draws more visual attention to the one-time donation box due to color — recommend shifting emphasis toward recurring/monthly giving.
