# TC-ODIN-27

Feature: Chat
Priority: High
Status: Pass
Title: Chat — Third Party Invited to Conversation
Type: Positive

**`Preconditions:`**

- Two test accounts exist: Sender and Traveler
- Order is in **Active** status
- Chat between Sender and Traveler is accessible
- A third test account exists (third party user)

**`Test Data:`**

- Sender account: test account 1
- Traveler account: test account 2
- Third party account: test account 3

**`Steps to Reproduce:`**

1. Open ODIN App as **Sender**
2. Navigate to active Order → open **Chat**
3. Tap **Invite** / Add participant option
4. Search and select third party user (test account 3)
5. Confirm invitation
6. Observe chat screen on all three accounts
7. Third party sends a message

**`Expected Result:`**
Third party is successfully added to the conversation. All three participants can see each other's messages in real time. Chat history is visible to the newly added participant. Original Sender and Traveler retain full chat access.

**`Notes:`**
Third party invite is useful when Sender wants to include a recipient at the delivery destination in the conversation — a unique feature supporting real-world P2P delivery coordination.