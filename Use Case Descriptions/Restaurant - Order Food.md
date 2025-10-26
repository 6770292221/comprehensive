# Use Case Description: Order Food

## Use Case ID
UC-REST-001

## Use Case Name
Order Food at Restaurant

## Brief Description
This use case allows a customer to order food at a restaurant through a waiter.

## Actors
- **Primary Actor**: Customer
- **Secondary Actors**: Waiter, Kitchen Staff, POS System

## Preconditions
1. Customer must be seated at a table
2. Restaurant must be open for service
3. Menu must be available
4. Kitchen must be operational

## Postconditions
**Success End Condition:**
- Order is recorded in POS system
- Kitchen receives order
- Food is prepared and served
- Customer receives ordered items

**Failure End Condition:**
- Order is cancelled
- No food prepared
- Alternative items suggested

## Main Flow (Basic Flow)
1. Customer requests menu from waiter
2. Waiter provides menu to customer
3. Customer reviews menu
4. Customer decides on items to order
5. Customer calls waiter
6. Waiter comes to table
7. Customer places order (dishes and quantities)
8. Waiter writes down order
9. Waiter enters order into POS system
10. POS system checks ingredient availability
11. POS system sends order to kitchen
12. Waiter confirms order with customer
13. Kitchen receives and acknowledges order
14. Kitchen prepares food
15. Kitchen notifies waiter when food is ready
16. Waiter picks up food from kitchen
17. Waiter serves food to customer
18. Customer enjoys meal

## Alternative Flows

### AF1: Item Not Available
**At step 10:**
- POS system detects ingredients not available for selected item
- System alerts waiter
- Waiter informs customer
- Customer can:
  - Choose alternative item, return to step 7
  - Remove item from order, continue to step 11
  - Cancel entire order, use case ends

### AF2: Special Request/Modifications
**At step 7:**
- Customer requests modifications (no onions, extra spicy, etc.)
- Waiter notes special requests
- Waiter enters modifications in POS system
- Special instructions are sent to kitchen
- Continue from step 12

### AF3: Takeaway Order
**At step 7:**
- Customer indicates order is for takeaway
- Waiter marks order as takeaway
- Food is packed in takeaway containers
- Customer pays and leaves with food

## Exception Flows

### EF1: POS System Down
**At step 9:**
- POS system is unavailable
- Waiter writes order on paper slip
- Waiter manually delivers order to kitchen
- Order is entered into system when available

### EF2: Kitchen Too Busy
**At step 13:**
- Kitchen cannot handle more orders (over capacity)
- Kitchen manager notifies waiter
- Waiter informs customer of longer wait time (e.g., 45 minutes)
- Customer can:
  - Accept wait time and continue
  - Cancel order and leave

### EF3: Wrong Order Delivered
**At step 17:**
- Customer notices incorrect items
- Customer informs waiter
- Waiter verifies order with POS system
- If error from kitchen: correct items are prepared
- If error from waiter: order is corrected
- Correct food is served with apology

## Special Requirements
- **Performance**:
  - Order entry time < 2 minutes
  - Average food preparation time: 15-20 minutes
- **Usability**:
  - Menu should have clear descriptions and prices
  - POS system should have easy item selection
- **Hygiene**:
  - All food safety standards must be followed
- **Accessibility**:
  - Menu available in multiple languages
  - Dietary information (allergens, vegetarian, etc.) clearly marked

## Frequency of Use
Very High - 100-300 orders per day depending on restaurant size

## Business Rules
1. Minimum order: None (customers can order single item)
2. Maximum wait time before informing customer: 30 minutes
3. Service charge: 10% added to bill
4. VAT: 7% applied
5. Modifications are free of charge
6. No food can be served after kitchen closes
7. Special dietary requirements must be accommodated if possible
8. Kitchen can refuse overly complex modifications
