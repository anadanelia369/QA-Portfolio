# TC-ODIN-19

Feature: Order
Priority: High
Status: Pass
Title: Auction Order Creation — Full Valid Flow
Type: Positive

**`Preconditions:`**

- User is logged into ODIN App as Sender
- KYC verification completed
- Valid payment method added to account

**`Test Data:`**

- Order type: Auction
- Item: any valid category
- Price: above minimum limit
- Currency: USD
- Delivery dates: valid future range
- Photos: 1-5 valid format images

**`Steps to Reproduce:`**

1. Open ODIN App
2. Navigate to **Create Order**
3. Select category: **Auction**
4. Enter item name and description
5. Enter price above minimum limit → select currency: **USD**
6. Select valid departure country and city
7. Select valid destination country and city
8. Select valid delivery date range
9. Enter item dimensions and weight
10. Upload at least 1 photo
11. Tap **Create Order**

**`Expected Result:`**
Auction Order is created successfully and appears in Orders list with status **Pending**. Order is visible to Travelers matching the route. Sender can view all incoming offers from Travelers.

**`Notes:`**
Auction type allows Sender to receive multiple competing offers from different Travelers and choose the best one — key differentiator from Standard Order type.