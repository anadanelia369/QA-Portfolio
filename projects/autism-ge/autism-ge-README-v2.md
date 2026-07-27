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

## Bug Reports

→ [View full bug report with all 14 findings](bug-report.md)

### Notable Find — BUG-04: Payment False Error

Payment completes successfully and confirmation email is delivered correctly with accurate subscription details. However, WordPress backend returns an error on the post-redirect page simultaneously.

**Business Risk:** Donors may believe payment failed and attempt to pay again — risk of duplicate charges or abandonment.

---

## ✅ Verified Working

- Social media links (YouTube, Instagram, Facebook) — correctly linked
- Payment via Visa — confirmed successful end-to-end
- Payment via Google Pay — confirmed successful
- Confirmation email — subscription details display correctly

---

## 💡 Key Recommendations

- **BUG-01:** Add "Forgot Password" recovery flow
- **BUG-04:** Fix WordPress post-payment redirect error (false failure)
- **BUG-09:** Persist language in `localStorage` — eliminates EN→GE flicker on redirect
- **UX:** Reorder donation boxes — Monthly first, more prominent color
