# MediFlow+ Workflow Map

## Purpose

This document defines the connected operational workflows that should be preserved when the Stitch designs are implemented in the final application.

The core principle is:

> MediFlow+ is a connected operational system, not a collection of independent dashboards.

---

# Master Closed Loop

```text
Patient
   ↓
Health Worker / Clinical Staff
   ↓
PHC Pharmacist
   ↓
Medicine Inventory
   ↓
Medicine Dispensed
   ↓
Stock Transaction
   ↓
Stock Threshold
   ↓
Low Stock
   ↓
Replenishment Request
   ↓
District Health Authority
   ↓
Review
   ├── Clarification
   ├── Reject
   └── Approve / Adjust
             ↓
         Allocation
             ↓
        Supply Chain
             ↓
      Shipment Created
             ↓
          Verified
             ↓
         Dispatched
             ↓
          In Transit
             ↓
          Delivered
             ↓
      PHC Pharmacist
             ↓
       Verify Receipt
             ↓
       Confirm Receipt
             ↓
      Inventory Updated
             ↓
   Medicine Availability
             ↓
           Patient
```

---

# Workflow 1 — Patient Appointment

```text
Patient Login
    ↓
Patient Dashboard
    ↓
Find PHC
    ↓
PHC Search Results
    ↓
PHC Details
    ↓
Appointment Booking
    ↓
Slot Selection
    ↓
Appointment Confirmation
    ↓
My Appointments
    ↓
Appointment Details
```

## Important rule

The registered/home PHC and appointment PHC are separate concepts.

A patient may book an appointment at another PHC within the district where permitted.

---

# Workflow 2 — Health Worker Visit

```text
Health Worker Login
    ↓
Dashboard
    ↓
Patient Search
    ↓
Patient Care View
    ↓
Appointment
    ↓
Start Visit
    ↓
Encounter / Visit Form
    ↓
Visit Confirmation
    ↓
Medicine Availability
    ↓
Pharmacist Coordination
```

The workflow must respect authorized patient and PHC scope.

---

# Workflow 3 — Medicine Dispensing

```text
Authorized Patient / Visit Context
          ↓
      Pharmacist
          ↓
    Search Medicine
          ↓
    View Current Stock
          ↓
    Enter Quantity
          ↓
    Validate Quantity
          ↓
 Confirm Dispensing
          ↓
 Stock Transaction Created
          ↓
 Inventory Decreases
```

The interface should prevent obviously invalid dispensing quantities such as quantities greater than available stock.

---

# Workflow 4 — Low Stock

```text
Inventory
   ↓
Stock Transaction
   ↓
Stock Falls
   ↓
Threshold Evaluated
   ↓
Low Stock
   ↓
Pharmacist Alert
   ↓
Replenishment Request
```

This is the bridge between pharmacist operations and district supply operations.

---

# Workflow 5 — Replenishment

```text
Pharmacist
   ↓
Create Replenishment Request
   ↓
Submit
   ↓
Pending Review
   ↓
District Authority
   ↓
Under Review
```

Possible authority outcomes:

```text
Under Review
   ├── Clarification Required
   │       ↓
   │   Clarification Response
   │       ↓
   │   Under Review
   │
   ├── Rejected
   │
   └── Approved / Adjusted
           ↓
        Allocated
```

---

# Workflow 6 — Authority Approval

The authority reviews:

- PHC
- Medicine
- Current stock
- Threshold
- Requested quantity
- Relevant operational context

The authority can:

- Request clarification
- Approve
- Adjust quantity
- Reject

The authority does not dispense medicine or create patient prescriptions.

---

# Workflow 7 — Supply Allocation

```text
Authority Approval
       ↓
Approved Allocation
       ↓
Supply Chain Queue
       ↓
Allocation Details
       ↓
Prepare Shipment
```

Allocation represents the handoff from district approval to supply operations.

---

# Workflow 8 — Shipment

```text
Allocation
   ↓
Create Shipment
   ↓
Package Verification
   ↓
Shipment Created
   ↓
Ready for Dispatch
   ↓
Dispatch
   ↓
Dispatched
   ↓
In Transit
   ↓
Delivered
```

---

# Workflow 9 — PHC Receipt

Important distinction:

```text
Delivered
   ≠
Received
```

The shipment being delivered to the PHC does not automatically mean the pharmacist has accepted the inventory.

Correct sequence:

```text
Delivered
   ↓
PHC Pharmacist Opens Shipment
   ↓
Verify Shipment
   ↓
Check Medicines / Quantities
   ↓
Confirm Receipt
   ↓
Inventory Updated
```

---

# Workflow 10 — Inventory Reconciliation

After confirmed receipt:

```text
Receipt Confirmed
      ↓
Stock Transaction
      ↓
Inventory Increased
      ↓
Stock Status Recalculated
      ↓
Medicine Availability Updated
```

The updated availability can then become visible to authorized users, including patients where appropriate.

---

# Workflow 11 — Notifications

Notifications should be connected to real workflow events.

Examples:

```text
New Replenishment Request
        ↓
Authority Notification

Request Approved
        ↓
Supply Chain Notification

Shipment Dispatched
        ↓
PHC Notification

Shipment Delivered
        ↓
Pharmacist Notification

Receipt Confirmed
        ↓
Inventory / Availability Update
```

Notifications should deep-link to the relevant record.

---

# Workflow 12 — Administrative Account Lifecycle

```text
Administrator
    ↓
Create Official Account
    ↓
Assign Role
    ↓
Assign District
    ↓
Assign PHC Where Applicable
    ↓
Pending Activation / Active
    ↓
First Login
    ↓
Temporary Password Change
    ↓
Authorized Application Access
```

Later:

```text
Active
  ↓
Role / PHC Change
  ↓
Audit Event
```

or:

```text
Active
  ↓
Suspend
  ↓
Suspended
  ↓
Reactivate
  ↓
Active
```

---

# Workflow 13 — Authorization

Conceptual model:

```text
Authenticated User
       ↓
Role
       ↓
District Scope
       ↓
PHC Scope
       ↓
Authorized Resource
       ↓
Permitted Action
```

For patients:

```text
Authenticated Patient
       ↓
Own Identity
       ↓
Own Authorized Records
```

The frontend should reflect this structure, but the backend/database must enforce it.

---

# Workflow 14 — Unauthorized Access

If a user attempts an action outside their authorization:

```text
Action Attempt
     ↓
Authorization Check
     ↓
Not Authorized
     ↓
Unauthorized State
     ↓
Return to Authorized Area
```

Do not expose internal permission logic or database details.

---

# Workflow 15 — Connection Failure

Important operational actions must not falsely appear successful when connectivity is unavailable.

Conceptual state:

```text
User Action
    ↓
Connection Failure
    ↓
Action Not Confirmed
    ↓
Connection Lost State
    ↓
Retry
```

Do not claim that inventory, approval, dispatch, or receipt succeeded without confirmation.

---

# Core State Transitions

## Inventory

```text
Available
   ↓
Dispensed
   ↓
Stock Reduced
   ↓
Low Stock
   ↓
Replenishment
   ↓
Shipment Received
   ↓
Stock Increased
   ↓
Available
```

## Replenishment

```text
Pending Review
→ Under Review
→ Clarification Required
→ Under Review
→ Approved / Adjusted
→ Allocated
```

or:

```text
Pending Review
→ Under Review
→ Rejected
```

## Shipment

```text
Preparing
→ Ready for Dispatch
→ Dispatched
→ In Transit
→ Delivered
→ Received
```

Possible exception:

```text
Any relevant delivery stage
→ Delivery Exception
```

---

# Final End-to-End Validation Scenario

The final implementation should be able to represent this complete scenario:

1. Patient uses the platform.
2. Health Worker coordinates a visit.
3. Pharmacist dispenses an authorized medicine.
4. Inventory decreases.
5. Stock crosses a configured threshold.
6. Pharmacist sees low-stock status.
7. Pharmacist submits replenishment request.
8. District Authority receives the request.
9. Authority reviews it.
10. Authority approves/adjusts/rejects or requests clarification.
11. Approved request becomes an allocation.
12. Supply Chain receives the allocation.
13. Supply operator prepares shipment.
14. Shipment is verified.
15. Shipment is dispatched.
16. Shipment becomes in transit.
17. Shipment is delivered to the PHC.
18. Pharmacist verifies the shipment.
19. Pharmacist confirms receipt.
20. Inventory increases.
21. Medicine availability is updated.
22. Relevant users receive workflow notifications.

This is the central connected loop of MediFlow+.

---

# Implementation Principle

Do not hard-code each phase as an isolated mini-application.

Use shared entities, shared state concepts, reusable components, and connected routes.

The frontend should make the workflow understandable before the backend is connected.

Later backend implementation should make these transitions real and secure.
