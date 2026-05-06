# INVM HSE Travel Register System

---

# Experimental / Beta Notice

The INVM HSE Travel Register System is currently operating in an experimental / beta phase.

Features, workflows, and interfaces may continue to evolve to improve usability, operational efficiency, and overall user experience for both employees and management.

Your feedback is highly important in helping improve and mature the system. Users are encouraged to share suggestions, issues, usability concerns, or improvement ideas throughout the beta phase.

---

# System Overview

The system is designed to manage:

* Employee travel declarations
* Participant coordination
* Approval workflow
* Route and transport tracking
* Supporting document management
* Audit and traceability records

The platform consists of:

1. Travel Declaration Form
2. Coordinator Portal
3. Approval Portal
4. Google Drive Trip Folder

---

# Overall Workflow

```text id="xj4nxf"
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
```

---

# Travel Submission

After submitting the Travel Declaration Form, the system automatically:

* Generates a unique Travel ID
* Creates trip records
* Creates participant records
* Creates route segmentation
* Creates a Google Drive folder

The coordinator will receive an email containing:

* Trip summary
* Route summary
* Google Drive folder link
* Coordinator Portal link

---

# Coordinator Portal

The Coordinator Portal is used to:

* Review trip details
* Manage participants
* Update trip information
* Submit trips for approval
* Access supporting document folder

---

# Available Actions

## Trip Actions

* Update Trip Dates
* Update Route / Transport
* Cancel Trip

## Participant Actions

* Add Participant
* Remove Participant
* Replace Participant

## Approval Actions

* Submit for Approval
* Withdraw Submission
* Request Change After Approval

---

# Supporting Documents

Supporting documents may be uploaded before, during, or after approval submission depending on operational needs.

Examples:

* Invitation letters
* Itineraries
* Meeting documents
* Supporting approvals

---

# Approval Workflow

## Submit for Approval

Coordinator reviews trip and presses:

```text id="yy6h8r"
Submit for Approval
```

The system:

* Creates approval request
* Sends approval email
* Updates approval status
* Locks controlled changes

After submitting for approval, coordinators are encouraged to inform their assigned approver directly to help ensure timely review and approval processing.

---

## Approval Review

Approver receives:

* Approval email
* Approval Portal link

Approver can:

* Review trip details
* Access supporting documents
* Approve or reject request

---

# Status Definitions

## Trip Status

| Status    | Meaning                  |
| --------- | ------------------------ |
| Draft     | Editable / not finalized |
| Upcoming  | Approved future trip     |
| Active    | Trip currently ongoing   |
| Completed | Trip completed           |
| Cancelled | Trip cancelled           |

---

## Approval Status

| Status              | Meaning                        |
| ------------------- | ------------------------------ |
| Not Submitted       | Not yet submitted              |
| Pending Approval    | Awaiting approval              |
| Approved            | Approved                       |
| Rejected            | Rejected                       |
| Withdrawn           | Submission withdrawn           |
| Change Requested    | Approved trip requires changes |
| Re-approval Pending | Awaiting re-approval           |

---

# Audit & Traceability

The system records:

* Participant changes
* Route updates
* Date updates
* Approval actions
* Cancellation actions

All actions are logged for audit and traceability purposes.

---

# System Architecture

```text id="6wk44t"
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

# Intended Benefits

The system improves:

* Travel visibility
* Approval governance
* Operational traceability
* Document centralization
* Administrative efficiency
* Structured travel coordination
