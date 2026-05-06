# INVM HSE Travel Register System

## User Guide, Workflow & Instructions

---

# Experimental / Beta Notice

The INVM HSE Travel Register System is currently operating in an experimental / beta phase.

During this phase:

* Features, workflows, and interfaces may continue to evolve
* Certain processes may be adjusted to improve usability and operational efficiency
* Additional controls, automation, and approval mechanisms may be introduced progressively
* User feedback from employees, coordinators, approvers, and management will be used to refine the system

The primary objective of this beta phase is to:

* Improve overall user experience
* Ensure the workflow aligns with actual operational needs
* Enhance clarity, governance, and practicality for both employees and management
* Identify gaps, edge cases, and improvement opportunities before wider operational adoption

As such, users may occasionally experience:

* Minor UI changes
* Workflow adjustments
* New fields or validation requirements
* Changes to approval or coordination processes

Your feedback is highly important in helping improve and mature the system. Users are encouraged to share suggestions, issues, usability concerns, or improvement ideas throughout the beta phase to help shape a more efficient, practical, and user-friendly platform for everyone involved.

---

# 1. System Overview

The INVM HSE Travel Register System is a centralized platform used to manage employee travel declarations, approvals, participant coordination, and supporting documents.

The system consists of:

1. **Travel Declaration Form**
   Used by employees/coordinators to submit a new travel request.

2. **Coordinator Portal**
   Used to review, manage, update, and submit trips for approval.

3. **Approval Portal**
   Used by approvers to review and approve/reject travel requests.

4. **Google Drive Trip Folder**
   Automatically created for uploading supporting documents.

---

# 2. Overall Workflow

```text id="5r9o3t"
Travel Form Submission
        ↓
System Generates Travel Record + Folder
        ↓
Coordinator Reviews Trip
        ↓
Coordinator Submits for Approval
        ↓
(Optional) Upload Supporting Documents
        ↓
Approver Reviews Request
        ↓
Approved / Rejected
        ↓
Trip Becomes Official Record
```

---

# 3. Travel Submission Process

## Step 1 — Submit Travel Declaration Form

The coordinator submits the Travel Declaration Form with:

* Trip details
* Travel dates
* Participants
* Route information
* Transport method
* Overnight stay information

---

## Step 2 — System Automatically Generates

After submission, the system automatically creates:

* Unique Travel ID
* Trip record
* Participant records
* Route segmentation
* Stay details
* Google Drive trip folder

The coordinator will receive a confirmation email containing:

* Trip summary
* Route summary
* Travel ID
* Google Drive folder link
* Coordinator Portal link

---

# 4. Coordinator Portal Workflow

The Coordinator Portal is the primary workspace for managing trips before approval.

## Coordinator Responsibilities

The coordinator is responsible for:

* Reviewing trip details
* Updating trip information
* Managing participants
* Submitting trips for approval
* Uploading supporting documents when necessary

---

# 5. Coordinator Portal Actions

## A. Review Trip Information

The portal displays:

* Trip status
* Approval status
* Participants
* Route summary
* Transport method
* Overnight stays
* Supporting document folder

---

## B. Upload Supporting Documents

The provided Google Drive folder may be used to upload supporting documents before, during, or after the approval process, depending on operational needs.

Examples include:

* Invitation letters
* Itineraries
* Meeting documents
* Supporting approvals
* Travel-related files

---

## C. Add Participant

Used when additional employees join the trip after submission.

The system:

* Adds participant records
* Updates participant summary
* Logs the action in the audit trail

---

## D. Remove Participant

Used when participants are no longer joining the trip.

Coordinator removal is restricted.

---

## E. Replace Participant

Used when one participant is replaced by another.

The system:

* Removes previous participant
* Adds replacement participant
* Records change history

---

## F. Update Trip Dates

Used when travel schedules change.

The system automatically:

* Updates trip status
* Maintains audit history

---

## G. Update Route / Transport

Used when:

* Destination changes
* Additional stops are required
* Transport method changes

Domestic trips support:

* Main destination
* Up to 3 stops
* Final end location

International trips support:

* Destination country
* Destination city
* Transit locations

---

## H. Cancel Trip

Used when travel is no longer required.

Cancelled trips:

* Remain recorded for audit purposes
* Cannot continue approval workflow

---

# 6. Approval Workflow

## Step 1 — Submit for Approval

Once all information is complete:

1. Coordinator reviews trip
2. Coordinator presses:

   ```text
   Submit for Approval
   ```

The system:

* Creates approval request
* Sends email to approver
* Locks controlled trip changes
* Updates approval status

---

## Step 2 — Approver Reviews Request

Approver receives:

* Approval email
* Approval Portal link

Approver can:

* Review full trip details
* Access supporting folder
* Approve or reject request

---

## Step 3 — Approval Outcome

### Approved

Trip becomes officially approved.

### Rejected

Trip returns to coordinator for revision.

Coordinator may:

* Update information
* Resubmit for approval

---

# 7. Change Request After Approval

If an approved trip requires changes:

1. Coordinator presses:

   ```text
   Request Change
   ```

2. System changes approval state to:

   ```text
   Change Requested
   ```

3. Coordinator updates trip

4. Coordinator resubmits for approval

This creates a controlled re-approval process.

---

# 8. Trip Status Definitions

| Status    | Meaning                    |
| --------- | -------------------------- |
| Draft     | Newly submitted / editable |
| Upcoming  | Approved future trip       |
| Active    | Trip currently ongoing     |
| Completed | Trip end date passed       |
| Cancelled | Trip cancelled             |

---

# 9. Approval Status Definitions

| Status              | Meaning                             |
| ------------------- | ----------------------------------- |
| Not Submitted       | Not yet submitted for approval      |
| Pending Approval    | Awaiting approver action            |
| Approved            | Approved                            |
| Rejected            | Rejected by approver                |
| Withdrawn           | Submission withdrawn                |
| Change Requested    | Approved trip requires modification |
| Re-approval Pending | Awaiting approval after changes     |

---

# 10. Audit & Traceability

The system records:

* Participant changes
* Route changes
* Date updates
* Approval actions
* Cancellation actions

All updates are logged for audit and traceability purposes.

---

# 11. Important Usage Notes

* Supporting documents may be uploaded before, during, or after approval submission depending on operational requirements.
* Trips under approval may have restricted editing.
* Coordinators should review all route information carefully before submission.
* Travel IDs should be used in all travel-related communication.
* Cancelled trips remain part of historical records.

---

# 12. System Architecture (High Level)

```text id="x5z6kb"
Google Form
    ↓
Apps Script Processing
    ↓
Google Sheets Database
    ↓
Coordinator Portal
    ↓
Approval Portal
    ↓
Google Drive Folder Storage
```

---

# 13. Intended Benefits

The system improves:

* Travel visibility
* Approval governance
* Operational traceability
* Document centralization
* Audit readiness
* Administrative efficiency
* Structured travel coordination
