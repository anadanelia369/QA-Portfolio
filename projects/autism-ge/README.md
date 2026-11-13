# autism.ge (Colorful City): Pro Bono UAT

Manual web testing of a live WordPress donation website for a nonprofit organization.

| | |
|---|---|
| **Type** | Pro bono UAT |
| **Environment** | Windows 11, Chrome |
| **Platform** | WordPress |
| **Tester** | Ana Danelia |
| **Approach** | Risk-based testing, prioritizing authentication and payment/donation flows |
| **Evidence** | 9 annotated screenshots, 2 screen recordings (full payment flow, insufficient funds scenario) |

## Testing scope

Authentication, Profile management, Subscriptions, Cart / Checkout, Payment processing (Visa, Google Pay), Localization (GE/EN).

## Results at a glance

| Severity | Count |
|---|---|
| Critical | 4 |
| High | 4 |
| Medium | 6 |
| **Total** | **14** |

## Notable find: BUG-04, error shown after a successful payment

The payment completes and the confirmation email arrives with the correct subscription details. At the same time, the post-redirect page shows a WordPress critical error.

- **Business risk:** donors may believe the payment failed and pay again, which risks duplicate charges or donor abandonment.
- **Reproducibility:** 100%.
- **Status:** fixed by the site team after this report.

## All findings

| ID | Title | Area | Severity | Priority |
|---|---|---|---|---|
| BUG-01 | Missing "Forgot Password" functionality | Authentication | Critical | High |
| BUG-02 | Missing password visibility toggle (eye icon) | Authentication | Critical | High |
| BUG-03 | Subscriptions not displaying on the Subscriptions page | User account / Subscriptions | Critical | High |
| BUG-04 | WordPress error shown after a successful payment | Payment processing | Critical | Critical |
| BUG-05 | Auth page still accessible after logout | Session management | High | High |
| BUG-06 | Cart shows only one-time donation for authorized users | Cart / Checkout | High | High |
| BUG-07 | "Update" button disabled, "Pay" redirects without confirmation | Cart / Checkout | High | High |
| BUG-08 | Misleading "Registration" button label for authorized users | UX / Checkout | High | Medium |
| BUG-09 | Language flicker on redirect (English to Georgian, about 2 seconds) | Localization | Medium | Medium |
| BUG-10 | Icon margin inconsistency on the post-redirect page only | UI | Medium | Low |
| BUG-11 | "No payment Found" message untranslated | Localization | Medium | Medium |
| BUG-12 | Profile edit screen has translation gaps | Localization | Medium | Medium |
| BUG-13 | Confirmation email contains untranslated English text | Localization | Medium | Low |
| BUG-14 | Order details untranslated on the payment page | Localization | Medium | Low |

Notes:
- BUG-05 is a potential session-handling concern and needs backend verification.
- BUG-10 was not yet verified in DevTools or responsive view. It is flagged for follow-up.
- BUG-13: the intro paragraph and the "Order summary" heading of the confirmation email remain in English, while the subject, greeting and product table are in Georgian.

## Verified working

- Social media links (YouTube, Instagram, Facebook) are linked correctly.
- "Donation" button (top and bottom of the page) redirects to the donation page.
- Payment via Visa is successful end-to-end.
- Payment via Google Pay is successful.
- Confirmation email shows the monthly / one-time subscription details correctly.
- Insufficient funds scenario shows a clear "Declined" message.

## Key recommendations

- **BUG-01:** add a "Forgot Password" recovery flow.
- **BUG-04:** fix the WordPress post-payment redirect error (false failure signal).
- **BUG-09:** persist the language choice in `localStorage` to remove the English-to-Georgian flicker on redirect.
- **UX:** reorder the donation boxes. Monthly donation first with a more prominent color, one-time donation second, merchandise third. Monthly giving is the organization's priority, while the current design draws more attention to the one-time box.

## Note on evidence

The screen recordings contain payment and personal details and are not published. Bug summary cards are available in the Upwork portfolio.
