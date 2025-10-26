# Use Case Description: Purchase Product Online

## Use Case ID
UC-ECOM-001

## Use Case Name
Purchase Product from E-commerce Website

## Brief Description
This use case allows a customer to browse products, add items to cart, and complete an online purchase.

## Actors
- **Primary Actor**: Customer
- **Secondary Actors**: Web Application, Product Service, Cart Service, Payment Gateway, Order Service, Shipping Service

## Preconditions
1. E-commerce website must be accessible
2. Products must be available in inventory
3. Payment gateway must be operational
4. Customer must have valid email address
5. Shipping service must be available

## Postconditions
**Success End Condition:**
- Order is created with unique order number
- Payment is processed successfully
- Inventory is reduced
- Order confirmation email sent
- Shipping label generated
- Customer receives order number

**Failure End Condition:**
- No order created
- No payment charged
- Inventory unchanged
- Customer notified of failure

## Main Flow (Basic Flow)
1. Customer visits e-commerce website
2. Customer browses product categories or searches for product
3. System displays product list with images and prices
4. Customer clicks on product to view details
5. System displays product details (description, price, reviews, availability)
6. Customer selects quantity
7. Customer clicks "Add to Cart"
8. System adds item to shopping cart
9. Customer can continue shopping (return to step 2) or proceed to checkout
10. Customer clicks "Proceed to Checkout"
11. System displays cart summary with total price
12. Customer enters/confirms shipping address
13. Customer selects shipping method (standard, express)
14. Customer enters payment information (credit card, e-wallet, etc.)
15. Customer reviews order summary
16. Customer clicks "Place Order"
17. System validates payment information
18. System processes payment through payment gateway
19. System creates order record
20. System reduces product inventory
21. System clears shopping cart
22. System generates order number
23. System sends order confirmation email
24. System displays order confirmation page
25. Customer receives confirmation email with order number

## Alternative Flows

### AF1: Product Out of Stock
**At step 5:**
- System shows "Out of Stock"
- System offers options:
  - Notify when available
  - View similar products
- Customer can select alternative or continue browsing

### AF2: Apply Discount Code
**At step 15:**
- Customer enters promotional/discount code
- System validates code
- If valid: discount applied to total, update display
- If invalid: error message shown
- Continue with order

### AF3: Guest Checkout (No Account)
**At step 12:**
- Customer chooses to checkout as guest
- System requests email for order confirmation
- System skips account-related features
- Continue with shipping address entry

### AF4: Saved Payment Methods
**At step 14:**
- Customer has account with saved payment methods
- System displays saved cards/methods
- Customer selects saved method
- Skip payment entry, continue to step 15

## Exception Flows

### EF1: Payment Declined
**At step 18:**
- Payment gateway declines transaction
- System displays error message with reason
- System offers to retry with different payment method
- Cart contents remain intact
- Customer can:
  - Try different payment method
  - Save cart and pay later
  - Cancel order

### EF2: Inventory Insufficient During Checkout
**At step 20:**
- Item becomes unavailable between cart and checkout
- System notifies customer
- System removes unavailable item from order
- Customer can:
  - Continue with remaining items
  - Cancel entire order

### EF3: Shipping Address Invalid
**At step 12:**
- System cannot validate shipping address
- System displays error message
- Customer must correct address
- If address cannot be served, order cannot proceed

### EF4: Session Timeout
**During shopping:**
- Customer idle for 30 minutes
- System expires session
- Cart items saved for 24 hours
- Customer can login to retrieve cart

## Special Requirements
- **Security**:
  - SSL/TLS encryption for all pages
  - PCI DSS compliance for payment handling
  - Password must be hashed (bcrypt/argon2)
  - Customer data protected per GDPR/PDPA
- **Performance**:
  - Page load time < 3 seconds
  - Search results within 2 seconds
  - Checkout process within 5 minutes
  - Support 10,000 concurrent users
- **Usability**:
  - Mobile responsive design
  - Clear product images (multiple angles)
  - Easy cart management (update quantities, remove items)
  - Guest checkout option
- **Reliability**:
  - 99.9% uptime
  - Transaction logging
  - Automated backup daily

## Frequency of Use
Very High - 1,000-10,000 orders per day depending on platform size

## Business Rules
1. Minimum order value: 100 THB (or free shipping threshold)
2. Maximum items per order: 50 items
3. Shipping fees:
   - Standard: 50 THB (3-5 days)
   - Express: 100 THB (1-2 days)
   - Free shipping for orders > 1,000 THB
4. Payment methods accepted: Credit card, Debit card, E-wallet, Bank transfer
5. Return policy: 7 days from delivery
6. Refund processing: 7-14 business days
7. Customer support: Available via chat, email, phone
8. Product reviews: Only verified purchasers can review
9. Maximum discount: 50% off
10. Tax: 7% VAT applied automatically
