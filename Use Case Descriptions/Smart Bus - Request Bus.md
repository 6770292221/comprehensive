# Use Case Description: Request Smart Bus

## Use Case ID
UC-SMART-001

## Use Case Name
Request and Track Smart Bus

## Brief Description
This use case allows a passenger to request a smart bus, track its real-time location, and complete a trip using a mobile application.

## Actors
- **Primary Actor**: Passenger
- **Secondary Actors**: Bus Driver, Mobile App, Routing Service, Bus Tracker, Notification Service, Operations Center

## Preconditions
1. Passenger must have mobile app installed
2. Passenger must be registered and logged in
3. GPS location services must be enabled
4. Bus fleet must be available in service area
5. Network connectivity available

## Postconditions
**Success End Condition:**
- Bus is assigned to passenger
- Trip is completed successfully
- Passenger arrives at destination
- Trip record saved in system
- Payment processed (if applicable)

**Failure End Condition:**
- No bus assigned
- Trip cancelled
- Passenger not transported
- No charges made

## Main Flow (Basic Flow)
1. Passenger opens smart bus mobile app
2. System displays map with current location
3. Passenger enters/selects pickup location
4. Passenger enters/selects destination
5. Passenger selects number of passengers
6. Passenger clicks "Request Bus"
7. System calculates optimal route
8. System calculates estimated time of arrival (ETA)
9. System searches for available buses in area
10. System finds nearest available bus
11. System assigns bus to request
12. System displays bus details (bus number, ETA 15 min)
13. System sends notification to assigned driver
14. Driver accepts the request
15. Driver starts navigation to pickup location
16. Passenger sees real-time bus location on map (updates every 10 seconds)
17. System sends notification when bus is 5 minutes away
18. System sends notification when bus arrives
19. Passenger boards the bus
20. Driver confirms passenger boarding in driver app
21. Bus starts trip to destination
22. System tracks trip progress
23. Bus arrives at destination
24. Passenger alights from bus
25. Driver marks trip as completed
26. System displays trip summary
27. System requests passenger rating (optional)
28. Trip completed

## Alternative Flows

### AF1: No Bus Available
**At step 10:**
- System cannot find available bus
- System displays "No buses available nearby"
- System shows estimated wait time (e.g., 20 minutes)
- Passenger options:
  - Wait and system will retry automatically
  - Modify pickup/destination to find alternatives
  - Cancel request

### AF2: Driver Declines Request
**At step 14:**
- Assigned driver declines the request
- System immediately searches for another driver
- If another driver found: continue from step 11
- If no driver available: display "Unable to find driver" and suggest retry

### AF3: Passenger Cancels Before Pickup
**Before step 19:**
- Passenger cancels request
- System notifies driver
- Bus assignment is released
- Small cancellation fee may apply (policy-based)
- Use case ends

### AF4: Passenger No-Show
**At step 19:**
- Bus arrives but passenger doesn't board within 5 minutes
- Driver marks as "no-show"
- Trip is cancelled
- No-show fee charged to passenger account
- Use case ends

### AF5: Route Change/Detour
**During step 22:**
- Traffic/road closure requires route change
- System recalculates route
- System notifies passenger of delay
- New ETA displayed
- Trip continues on new route

## Exception Flows

### EF1: GPS Signal Lost
**At any step:**
- GPS signal becomes unavailable
- System switches to last known location
- Driver can still navigate using offline maps
- System attempts to reconnect
- Trip continues but tracking may be intermittent

### EF2: Network Connection Lost
**During trip:**
- Network connection drops
- App caches last known state
- Driver continues to destination using offline navigation
- Once reconnected, system syncs trip data
- Trip can still be completed

### EF3: Emergency Situation
**At any time during trip:**
- Passenger or driver triggers emergency button
- System immediately alerts operations center
- Emergency services contacted if needed
- GPS location shared with emergency responders
- Trip is suspended

### EF4: Driver/Bus Breakdown
**During step 16 or 21:**
- Bus experiences mechanical failure
- Driver reports issue in app
- System immediately searches for replacement bus
- Passenger notified of situation
- If replacement found: new bus assigned
- If no replacement: trip cancelled, no charge

## Special Requirements
- **Performance** (from Requirements Document):
  - ETA calculation within 2 seconds (NFR-P1)
  - Bus location updates every 5-10 seconds (NFR-P2)
  - End-to-end latency ≤ 3 seconds
- **Availability**:
  - System uptime ≥ 99.8% per month (NFR-R1)
  - Support 5,000 concurrent users (NFR-R2)
- **Security** (NFR-SEC1-3):
  - TLS 1.2+ encryption for data transmission
  - AES-256 encryption for personal data at rest
  - Location data tokenized/anonymized for analytics
  - 2FA for admin/operator access
- **Usability** (NFR-U1-2):
  - First request completed within 60 seconds for new users
  - Support Thai/English languages
  - WCAG AA accessibility standards
- **Scalability** (NFR-S1):
  - Scale without downtime
  - p95 latency < 3 seconds when scaling
- **Compliance**:
  - PDPA compliant (NFR-C1)
  - Consent management
  - Right to deletion
  - Clear data usage policy

## Frequency of Use
Very High - 1,000-5,000 trips per day in medium-sized city

## Business Rules
1. Service area: Within designated city zones
2. Minimum passenger age: 13+ (under 13 requires adult)
3. Maximum passengers per request: 4 people
4. Service hours: 06:00 - 23:00 daily
5. Fare calculation:
   - Base fare: 15 THB
   - Per kilometer: 8 THB/km
   - Peak hour surcharge: +20% (07:00-09:00, 17:00-19:00)
6. Payment methods: E-wallet, Credit card, Cash (with driver)
7. Cancellation policy:
   - Free cancellation before driver accepts
   - 10 THB fee after driver accepts but before pickup
   - 50 THB fee for no-show
8. Driver assignment: Nearest available bus within 10km radius
9. Maximum wait time: 20 minutes (system suggests alternative if exceeded)
10. Rating system: Both passenger and driver can rate (1-5 stars)
11. Luggage: One carry-on bag free, large luggage requires advance notice
12. Shared rides: Multiple passengers can be pooled on same route (with consent)
