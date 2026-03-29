# Charity Project — autism.ge

Pro bono UAT, web (Windows 11 / Chrome)

**Scope:**

Authentication, donation flow (one-time & monthly), payment processing (Visa, Google Pay), confirmation email

**Approach:**

Risk-based — tested only critical path (user registration → donation completion)

**Found:**

6 issues including missing password recovery, broken social links, UI inconsistencies post-payment

**Notable find:**

Payment completes successfully and confirmation email is delivered correctly — however, WordPress backend returns an error on redirect. Identified as backend validation issue, not a payment failure.

**Key recommendations:**

Prioritize monthly donation CTA visibility; persist language preference in localStorage to eliminate default-language flash on navigation