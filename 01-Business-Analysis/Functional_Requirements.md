# Functional Requirements

## Project Name

CAPA (Corrective & Preventive Action) Management

---

# 1. Overview

The CAPA (Corrective & Preventive Action) Management application enables organizations to manage the complete CAPA lifecycle from issue reporting to final closure. The system standardizes the process, assigns ownership, automates approvals and notifications, and provides visibility into corrective and preventive actions.

---

# 2. User Roles

| Role | Responsibilities |
|------|-------------------|
| Employee | Report issues requiring CAPA |
| CAPA Coordinator | Create, assign, monitor, and manage CAPA records |
| Investigator | Perform root cause analysis |
| Manager | Review and approve action plans |
| Action Owner | Complete assigned corrective and preventive actions |
| QA Team | Verify action effectiveness and recommend closure |
| System Administrator | Configure and maintain the application |

---

# 3. Functional Requirements

### FR-01 Issue Reporting

- Employees shall be able to submit a new issue.
- Each issue shall create a CAPA record.
- The system shall assign a unique CAPA number.

---

### FR-02 CAPA Record Management

The system shall allow users to:

- View CAPA details
- Update CAPA information
- Track current status
- View complete lifecycle history

---

### FR-03 Root Cause Analysis

The assigned investigator shall:

- Record investigation findings
- Document the root cause
- Submit the analysis for review

---

### FR-04 Corrective Actions

The system shall allow the CAPA Coordinator to:

- Create corrective actions
- Assign action owners
- Define due dates
- Track completion status

---

### FR-05 Preventive Actions

The system shall allow preventive actions to be:

- Created
- Assigned
- Scheduled
- Tracked until completion

---

### FR-06 Approval Process

Managers shall be able to:

- Approve action plans
- Reject action plans
- Provide comments during approval

---

### FR-07 Notifications

The system shall notify users when:

- A CAPA is assigned
- An approval is pending
- An action becomes overdue
- A CAPA is approved
- A CAPA is closed

---

### FR-08 Verification

The QA Team shall:

- Review completed actions
- Verify effectiveness
- Approve or reject verification

---

### FR-09 CAPA Closure

The system shall allow closure only after:

- All corrective actions are completed
- All preventive actions are completed
- Verification is successful
- Required approvals are completed

---

### FR-10 Reporting

The system shall provide reports for:

- Open CAPAs
- Closed CAPAs
- Pending approvals
- Overdue actions
- CAPA status summary

---

# 4. High-Level Workflow

```
Issue Reported
      │
      ▼
CAPA Created
      │
      ▼
Root Cause Analysis
      │
      ▼
Corrective & Preventive Planning
      │
      ▼
Manager Approval
      │
      ▼
Action Implementation
      │
      ▼
Verification
      │
      ▼
Closure
```

---

# 5. Assumptions

- Users are authenticated through ServiceNow.
- Role-based access controls determine user permissions.
- Notifications are delivered through email.
- Reports and dashboards use ServiceNow reporting features.

---

# 6. Future Enhancements

The following features are outside the current project scope but may be considered in future versions:

- Third-party integrations
- Mobile support
- AI-assisted root cause suggestions
- Predictive risk analysis
- Advanced audit management
- Digital signatures

---