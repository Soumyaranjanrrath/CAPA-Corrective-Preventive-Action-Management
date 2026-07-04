# Solution Design

## Project Name

CAPA (Corrective & Preventive Action) Management

---

# 1. Solution Overview

The CAPA (Corrective & Preventive Action) Management application is designed to standardize and automate the complete CAPA lifecycle within the ServiceNow platform. The solution enables organizations to report issues, investigate root causes, manage corrective and preventive actions, obtain approvals, verify effectiveness, and close CAPA records in a controlled manner.

The application leverages ServiceNow App Engine Studio for application development, Flow Designer for workflow automation, Notifications for communication, ACLs for role-based security, and Reports & Dashboards for process visibility.

---

# 2. Application Modules

| Module | Description |
|---------|-------------|
| CAPA Management | Create and manage CAPA records throughout their lifecycle. |
| Root Cause Analysis | Record investigation findings and identify the root cause. |
| Action Management | Plan, assign, and track corrective and preventive actions. |
| Approval Management | Route CAPA action plans for manager approval. |
| Verification | Verify the effectiveness of completed actions before closure. |
| Reporting & Dashboard | Monitor CAPA status, overdue actions, and overall process performance. |

---

# 3. High-Level Data Model

The application consists of one primary CAPA record linked to corrective and preventive actions.

```
CAPA
 │
 ├── Corrective Actions
 │
 ├── Preventive Actions
 │
 └── Approval & Verification
```

This structure provides a simple and scalable design while maintaining clear relationships between CAPA records and their associated activities.

---

# 4. User Roles

| Role | Responsibilities |
|------|-------------------|
| Employee | Report issues requiring CAPA |
| CAPA Coordinator | Manage CAPA records and assign actions |
| Investigator | Perform root cause analysis |
| Manager | Review and approve action plans |
| Action Owner | Complete assigned corrective and preventive actions |
| QA Team | Verify completed actions before closure |
| System Administrator | Configure and maintain the application |

---

# 5. CAPA Workflow

The CAPA lifecycle consists of the following states:

```
Draft
   │
   ▼
Open
   │
   ▼
Investigation
   │
   ▼
Action Planning
   │
   ▼
Pending Approval
   │
   ▼
Approved
   │
   ▼
Implementation
   │
   ▼
Verification
   │
   ▼
Closed
```

Each state represents a specific stage of the CAPA process and controls user activities, approvals, and notifications.

---

# 6. Notifications

The application shall generate notifications for the following events:

- CAPA assigned to a user
- Action plan submitted for approval
- Approval completed
- Overdue corrective or preventive action
- Verification required
- CAPA successfully closed

---

# 7. Reports & Dashboard

The application shall provide reports for:

- Open CAPAs
- Closed CAPAs
- Pending approvals
- Overdue actions
- CAPAs by status
- CAPAs by priority

A management dashboard shall present key CAPA metrics and process visibility.

---

# 8. Security Design

Access to application data shall be controlled using ServiceNow roles and ACLs.

Role-based permissions will ensure that users can only perform actions relevant to their responsibilities while protecting sensitive CAPA information.

---

# 9. Design Assumptions

- Users authenticate through ServiceNow.
- Workflow automation is implemented using Flow Designer.
- Email notifications are configured using ServiceNow Notifications.
- Reports and dashboards use native ServiceNow reporting capabilities.
- The solution is designed for a single organization.

---