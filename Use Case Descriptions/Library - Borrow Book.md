# Use Case Description: Borrow Book

## Use Case ID
UC-LIB-001

## Use Case Name
Borrow Book from Library

## Brief Description
This use case allows a library member to borrow a book from the library collection.

## Actors
- **Primary Actor**: Library Member
- **Secondary Actors**: Librarian, Library System

## Preconditions
1. Member must be registered in the system
2. Member must have a valid membership card
3. Member must not have overdue books
4. Book must be available (not already borrowed)
5. Member must not exceed borrowing limit

## Postconditions
**Success End Condition:**
- Book status changes to "Borrowed"
- Loan record is created with due date (14 days)
- Member's borrowed books count increases
- Receipt is printed

**Failure End Condition:**
- Book remains available
- No loan record created
- Error message displayed

## Main Flow (Basic Flow)
1. Member searches for desired book in catalog
2. System displays book availability status
3. Member requests to borrow the book
4. Member presents membership card to librarian
5. Librarian scans membership card
6. System verifies member status
7. System checks member has no overdue books
8. System checks member borrowing limit (max 5 books)
9. Librarian scans book barcode
10. System checks book availability
11. System creates loan record
12. System sets due date to 14 days from today
13. System updates book status to "Borrowed"
14. System prints loan receipt with due date
15. Librarian gives book and receipt to member

## Alternative Flows

### AF1: Book Not Available
**At step 10:**
- System detects book is already borrowed
- System offers to place reservation
- If member accepts:
  - System creates reservation
  - System notifies when available
- If member declines, use case ends

### AF2: Member Has Overdue Books
**At step 7:**
- System detects overdue books
- System displays outstanding fines
- Librarian informs member to pay fines
- Member pays fines at counter
- System updates fine payment
- Continue from step 8

### AF3: Borrowing Limit Exceeded
**At step 8:**
- System detects member has reached borrowing limit (5 books)
- System displays error message
- Librarian informs member to return books before borrowing more
- Use case ends

### AF4: Member Status Suspended
**At step 6:**
- System detects member account is suspended
- System displays suspension reason
- Librarian informs member to contact administration
- Use case ends

## Exception Flows

### EF1: System Unavailable
**At any system interaction:**
- Library system is down
- Librarian records borrowing manually
- Data will be entered when system is back online

### EF2: Barcode Scanner Malfunction
**At step 5 or 9:**
- Barcode scanner fails to read
- Librarian manually enters member ID or book ISBN
- Continue with use case

### EF3: Invalid Membership Card
**At step 6:**
- System cannot find member record
- Librarian requests additional identification
- Member may need to renew membership
- Use case ends

## Special Requirements
- **Performance**:
  - System response time < 2 seconds for queries
  - Barcode scan recognition rate > 98%
- **Security**:
  - Member data must be protected
  - Only authorized librarians can access system
- **Usability**:
  - System should display clear status messages
  - Receipt should include due date prominently
- **Reliability**:
  - System should log all transactions
  - Backup should run daily

## Frequency of Use
High - 50-100 times per day in medium-sized library

## Business Rules
1. Maximum borrowing period: 14 days
2. Maximum books per member: 5 books
3. Fine for overdue books: 5 THB per day per book
4. Books can be renewed once if not reserved by others
5. Reference books cannot be borrowed (in-library use only)
6. New releases have shorter borrowing period: 7 days
7. Members must be 18+ or have parental consent
