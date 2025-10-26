# Use Case Description: Book Hotel Room

## Use Case ID
UC-HTL-001

## Use Case Name
Book Hotel Room

## Brief Description
This use case allows a guest to book a hotel room through the hotel booking system.

## Actors
- **Primary Actor**: Guest
- **Secondary Actors**: Booking System, Payment Gateway, Email Service

## Preconditions
1. Hotel booking system must be accessible
2. Hotel must have available rooms
3. Payment gateway must be operational
4. Guest must have valid payment method

## Postconditions
**Success End Condition:**
- Room is reserved for specified dates
- Payment is processed
- Booking confirmation is sent via email
- Confirmation number is generated
- Room status updated to "Reserved"

**Failure End Condition:**
- No reservation created
- No payment processed
- Guest notified of failure reason

## Main Flow (Basic Flow)
1. Guest opens hotel booking website/app
2. Guest enters check-in date and check-out date
3. Guest selects room type (single, double, suite, etc.)
4. System searches for available rooms
5. System displays available rooms with prices
6. Guest reviews room details (photos, amenities, price)
7. Guest selects desired room
8. Guest enters personal information (name, email, phone)
9. Guest enters payment information
10. Guest reviews booking summary
11. Guest clicks "Confirm Booking"
12. System validates payment information
13. System processes payment through payment gateway
14. System reserves room in database
15. System generates unique confirmation number
16. System sends confirmation email to guest
17. System displays confirmation page with booking details
18. Guest receives confirmation email

## Alternative Flows

### AF1: No Rooms Available
**At step 5:**
- System finds no available rooms for selected dates/type
- System displays "No rooms available"
- System suggests:
  - Alternative room types
  - Nearby dates with availability
  - Sister properties
- Guest can modify search or cancel

### AF2: Payment Declined
**At step 13:**
- Payment gateway declines payment
- System displays error message
- System offers options:
  - Try different payment method
  - Contact bank
  - Cancel booking
- Guest can retry or cancel

### AF3: Promotional Code
**At step 10:**
- Guest enters promotional/discount code
- System validates code
- If valid: discount applied to total
- If invalid: error message shown
- Continue with booking

### AF4: Account Login
**At step 8:**
- Guest chooses to login to existing account
- System retrieves saved information
- Guest information auto-filled
- Continue from step 9

## Exception Flows

### EF1: System Timeout
**At any step:**
- System times out due to network issues
- Session data is saved temporarily
- Guest can resume where they left off within 30 minutes
- After 30 minutes, session expires and must restart

### EF2: Room Becomes Unavailable During Booking
**At step 14:**
- Another guest books the same room simultaneously
- System detects room no longer available
- System notifies guest
- System offers similar available rooms
- Guest can select alternative or cancel

### EF3: Payment Processing Error
**At step 13:**
- Technical error during payment processing
- System logs error
- No charge made to guest
- Guest notified to try again later
- Guest receives apology email

## Special Requirements
- **Security**:
  - Payment information must be encrypted (PCI DSS compliant)
  - SSL/TLS for all transactions
  - Guest data must be protected (GDPR compliant)
- **Performance**:
  - Search results within 3 seconds
  - Payment processing within 10 seconds
  - System should handle 100 concurrent bookings
- **Usability**:
  - Mobile-responsive design
  - Support multiple languages
  - Clear cancellation policy displayed
- **Availability**:
  - System available 24/7 (99.9% uptime)

## Frequency of Use
High - 50-200 bookings per day depending on hotel size

## Business Rules
1. Minimum booking: 1 night
2. Maximum advance booking: 365 days
3. Cancellation policy:
   - Free cancellation up to 48 hours before check-in
   - 50% charge for cancellation within 48 hours
   - 100% charge for no-show
4. Deposit required: 50% of total cost or full prepayment
5. Check-in time: 14:00, Check-out time: 12:00
6. Extra guest charge: 500 THB per person per night
7. Children under 12 stay free (same room with parents)
8. Maximum occupancy per room type must be enforced
