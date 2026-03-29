# TC-ODIN-10

Feature: Ident mat
Priority: Critical
Status: Not Executed
Title: KYC Verification with Another Person's Document
Type: Negative

**`Preconditions:`**

- User is logged into ODIN
- KYC verification flow is accessible (Identomat integration)
- A second person's physical ID document is available for testing

**`Test Data:`**

- Account under test: own test account
- Document: another person's valid ID card (with their consent for testing)

**`Steps to Reproduce:`**

1. Navigate to the KYC verification screen in ODIN
2. Initiate the identity verification process
3. When prompted for a document scan, present a different person's ID
4. Complete the face scan / liveness check step

**`Actual Result:`**

Not yet executed — requires a controlled environment with consenting participants and coordinated testing session.

**`Expected Result:`**

The system (Identomat) should detect the mismatch between the live face and the document photo, and reject the KYC verification with an appropriate error message.

**`Notes:`**

This is a critical security scenario. If the system passes mismatched documents, it creates a serious identity fraud risk. Should be flagged to the security team if any bypass is found.