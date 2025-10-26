# Use Case Description: Book Movie Ticket

## Use Case ID
UC-MOV-001

## Use Case Name
Book Movie Ticket Online

## Brief Description
This use case allows a customer to book movie tickets online by selecting a movie, showtime, seats, and completing payment.

## Actors
- **Primary Actor**: Customer
- **Secondary Actors**: Booking System, Seat Management Service, Payment Gateway, Ticket Service, Email Service

## Preconditions
1. Movie booking system must be accessible
2. Movies and showtimes must be available
3. Seats must be available for selected showtime
4. Payment gateway must be operational
5. Customer must have valid email

## Postconditions
**Success End Condition:**
- Seats are reserved and marked as booked
- E-ticket is generated with QR code
- Payment is processed
- Confirmation email sent with e-ticket
- Customer can use QR code for cinema entry

**Failure End Condition:**
- No seats booked
- No payment processed
- Seats released back to available pool
- Customer notified of failure

## Main Flow (Basic Flow)
1. Customer opens movie booking website/app
2. System displays list of currently showing movies
3. Customer browses available movies
4. Customer selects a movie
5. System displays movie details (synopsis, rating, duration, trailer)
6. System displays available showtimes for selected date
7. Customer selects preferred showtime
8. System displays seat map of cinema hall
9. System shows available seats (green) and occupied seats (gray)
10. Customer selects desired seats (click on seats)
11. System locks selected seats for 5 minutes
12. System displays seat selection summary with price
13. Customer clicks "Proceed to Payment"
14. Customer enters personal information (name, email, phone)
15. Customer enters payment information
16. Customer reviews booking summary
17. Customer clicks "Confirm Booking"
18. System validates payment
19. System processes payment through payment gateway
20. System confirms seat booking permanently
21. System generates e-ticket with QR code
22. System sends confirmation email with e-ticket attached
23. System displays booking confirmation with QR code
24. Customer receives email and can save/print e-ticket

## Alternative Flows

### AF1: Seats Not Available
**At step 9:**
- System shows all seats occupied for selected showtime
- System displays "Fully Booked"
- System suggests:
  - Different showtime for same movie
  - Different cinema location
- Customer can select alternative or go back to movie list

### AF2: Seat Selection Timeout
**At step 12:**
- Customer takes longer than 5 minutes to complete booking
- System releases locked seats
- System displays timeout message
- Customer must restart seat selection (return to step 8)

### AF3: Multiple Seats for Group
**At step 10:**
- Customer selecting for group booking
- Customer selects multiple adjacent seats
- System validates seats are together
- Continue with normal flow

### AF4: Apply Promo Code
**At step 16:**
- Customer enters promotional code
- System validates code (valid dates, usage limits)
- If valid: discount applied (e.g., buy 2 get 1 free)
- If invalid: error message shown
- Continue with payment

### AF5: Member Discount
**At step 14:**
- Customer logs in with membership account
- System applies member discount automatically
- Points earned added to account
- Continue with payment

## Exception Flows

### EF1: Payment Declined
**At step 19:**
- Payment gateway declines payment
- System displays error message
- Seats remain locked for 2 more minutes
- Customer can:
  - Retry with different payment method
  - Cancel booking (seats released)

### EF2: Seats Taken During Process
**At step 20:**
- Another customer books same seats simultaneously
- System detects conflict
- System releases seats and notifies customer
- System offers:
  - Similar available seats
  - Restart selection
- Customer decides next action

### EF3: E-ticket Generation Fails
**At step 21:**
- System error during ticket generation
- Payment successful but ticket not generated
- System logs error
- System queues for retry
- Confirmation email sent with temporary booking ID
- Customer support notified automatically

## Special Requirements
- **Security**:
  - PCI DSS compliant payment processing
  - E-ticket QR code encrypted to prevent fraud
  - One-time use QR code (cannot be reused)
- **Performance**:
  - Seat map loads within 2 seconds
  - Real-time seat availability updates
  - Payment processing within 10 seconds
  - Support 500 concurrent bookings
- **Usability**:
  - Interactive seat map (zoom, pan)
  - Clear pricing display
  - Mobile-friendly interface
  - Color-coded seat categories (VIP, regular, couple)
- **Reliability**:
  - 99.5% uptime during peak hours
  - Automated retry for failed transactions
  - Seat locking mechanism prevents double booking

## Frequency of Use
High - 500-2,000 bookings per day per cinema complex

## Business Rules
1. Minimum advance booking: 30 minutes before showtime
2. Maximum advance booking: 7 days
3. Seat lock duration: 5 minutes during selection
4. Cancellation policy:
   - Free cancellation up to 2 hours before showtime
   - No refund after 2 hours
5. Pricing:
   - Regular seats: 150-200 THB
   - VIP seats: 300-400 THB
   - Children/senior discount: 20% off
   - Weekday discount: 50 THB off
6. Maximum 10 tickets per transaction
7. One e-ticket per person (separate QR codes)
8. QR code valid only for specific showtime
9. Late entry policy: No entry after 15 minutes from start time
10. Combo deals: Ticket + Popcorn packages available
