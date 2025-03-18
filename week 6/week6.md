# Tasks Completed

Create Admin page to let the admin manage student work hours by either approving or denying work hours

## Tasks To Do

### Displaying Students' Work Hours

The page lists all students who have logged their working hours.
Each row in the table represents a student, showing:

- Student Name
- Hours Worked
- Current Status (Pending, Approved, Denied)
- Action Buttons (Approve or Deny)

### Approving or Denying Work Hours

#### Admin Actions

The "Approve" button confirms that the logged hours are valid.
The "Deny" button rejects the hours if there are discrepancies.
How it Works in the Code:

Each row includes two forms, one for approving and one for denying work hours.
When an admin clicks a button, a POST request is sent to the corresponding URL (approve_hours or deny_hours).
The csrf_token ensures the request is secure.

### Workflow for Admins

Open the page to see a list of students and their logged hours.
Review the hours and decide whether to approve or deny them.
Click the appropriate button, which submits a form request to update the student’s record.
Backend processes the request and updates the database.
Page reloads with updated statuses (Approved/Deny).

### Improvements & Fixes Needed

- The commented-out {{ student.name }}, {{ student.hours_worked }}, and {{ student.status }} should be uncommented so that the real student data is displayed dynamically.

- The incorrect `approved` should be replaced with `{{ student.status }}` to reflect actual approval status.

- If a student has no logged hours, a message should be shown (e.g., "No working hours submitted yet.").

### Expected User Experience

- Admins can efficiently approve or reject work hours.
- Students can see their updated status after an admin review.
- Ensures fair and accurate work hour tracking.
