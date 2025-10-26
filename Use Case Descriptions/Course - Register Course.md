# Use Case Description: Register for Course

## Use Case ID
UC-ACAD-001

## Use Case Name
Register for Course

## Brief Description
This use case allows a student to register for a course through the university's course registration system.

## Actors
- **Primary Actor**: Student
- **Secondary Actors**: Registration System, Course Database, Student Database, Academic Advisor (optional)

## Preconditions
1. Student must be enrolled and have active status
2. Student must be logged into the registration system
3. Registration period must be open
4. Course must be offered in the current semester
5. Student must meet course prerequisites (if any)

## Postconditions
**Success End Condition:**
- Student is enrolled in the course
- Course capacity is reduced by 1
- Student's schedule is updated
- Course appears on student's registered courses list
- Confirmation email sent

**Failure End Condition:**
- Student not enrolled
- Course capacity unchanged
- Error message displayed explaining reason

## Main Flow (Basic Flow)
1. Student logs into course registration system
2. System displays student dashboard
3. Student clicks "Course Registration"
4. System displays course search interface
5. Student searches for course (by code, name, or department)
6. System displays list of matching courses
7. Student selects a course to view details
8. System displays course information (instructor, schedule, credits, description, prerequisites)
9. Student clicks "Register" button
10. System checks student prerequisites
11. System validates prerequisites are met
12. System checks course seat availability
13. System validates seats are available
14. System checks for schedule conflicts
15. System validates no time conflicts
16. System checks credit limit (max 22 credits per semester)
17. System validates student under credit limit
18. System enrolls student in course
19. System updates course enrollment count
20. System adds course to student's schedule
21. System displays success confirmation
22. System sends confirmation email
23. Student can continue registering for more courses or finish

## Alternative Flows

### AF1: Prerequisites Not Met
**At step 11:**
- System detects missing prerequisites
- System displays error: "Prerequisites not met"
- System lists required prerequisite courses
- Student options:
  - View available prerequisite courses
  - Request override from advisor
  - Cancel registration for this course

### AF2: Course Full
**At step 13:**
- System detects no available seats
- System displays "Course Full"
- System offers options:
  - Join waitlist
  - View alternative sections
  - Set notification when seat available
- Student makes selection

### AF3: Schedule Conflict
**At step 15:**
- System detects time conflict with already-registered course
- System displays conflicting courses and times
- System prevents registration
- Student must:
  - Drop conflicting course first
  - Select different section
  - Cancel this registration

### AF4: Credit Limit Exceeded
**At step 17:**
- System detects total credits would exceed 22
- System displays current credits and limit
- Student options:
  - Drop another course to stay under limit
  - Request exception from academic advisor
  - Cancel this registration

### AF5: Advisor Approval Required
**At step 9:**
- Course requires advisor approval (e.g., honors courses, special topics)
- System sends approval request to assigned advisor
- Student receives pending status
- Once approved, system completes registration
- If denied, student is notified with reason

## Exception Flows

### EF1: System Unavailable
**At any step:**
- System experiences downtime
- Student session is saved
- Student notified to try again later
- System queues notification when back online

### EF2: Registration Period Closed
**At step 3:**
- Student attempts to register outside registration window
- System blocks access to registration
- System displays next registration period dates
- Student can only view courses, not register

### EF3: Student Account Suspended
**At step 1:**
- System detects account hold (unpaid fees, academic probation)
- System prevents login to registration
- System displays reason for hold
- Student directed to resolve issue with relevant office

## Special Requirements
- **Performance**:
  - System must handle 5,000 concurrent students during peak registration
  - Course search results within 2 seconds
  - Registration confirmation within 3 seconds
- **Security**:
  - Student authentication required (2FA recommended)
  - Cannot register for another student's account
  - Audit log of all registration actions
- **Usability**:
  - Clear error messages
  - Mobile-friendly interface
  - Save draft selections
  - Visual schedule planner (calendar view)
- **Reliability**:
  - 99.9% uptime during registration period
  - Automatic backup every hour
  - Transaction rollback on failure

## Frequency of Use
Very High during registration period - 1,000-5,000 registrations per day

## Business Rules
1. Minimum credits per semester: 9 credits (full-time)
2. Maximum credits per semester: 22 credits (without approval)
3. Maximum students per course: Varies by course (typically 30-50)
4. Registration priority by year: Seniors → Juniors → Sophomores → Freshmen
5. Late registration fee: 500 THB after first week
6. Drop/Add period: First 2 weeks of semester
7. Withdraw deadline: Before week 12 of 16-week semester
8. Core courses mandatory: Must complete before graduation
9. Prerequisite waiver requires department head approval
10. Lab courses require concurrent lecture enrollment
11. Some courses limited to major students only
12. Pass/Fail option must be declared before midterm
