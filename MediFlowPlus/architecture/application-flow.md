# MediFlow+ Application Flow

## Purpose

MediFlow+ is one connected responsive healthcare coordination and medicine-supply web application.

The application contains multiple stakeholder experiences, but they are parts of one system rather than independent applications.

## High-Level Flow

```text
Public Website
      ↓
Authentication
      ↓
Identity
      ↓
Authorization
      ↓
Organizational Scope
      ↓
Role-Specific Application Experience
```

## Role Experiences

```text
Patient / Citizen
Health Worker / Clinical Staff
Pharmacist
District Health Authority
Supply Chain
System Administrator
```

All roles use the same application shell, design system, language system, and shared operational concepts where appropriate.

## Core Operational Flow

```text
Patient
   ↓
Health Worker / Clinical Staff
   ↓
PHC Pharmacist
   ↓
Medicine Inventory
   ↓
Low Stock
   ↓
Replenishment Request
   ↓
District Health Authority
   ↓
Review / Approval / Adjustment
   ↓
Allocation
   ↓
Supply Chain
   ↓
Shipment
   ↓
Dispatch
   ↓
In Transit
   ↓
Delivered
   ↓
PHC Pharmacist Receipt
   ↓
Inventory Updated
   ↓
Medicine Availability Updated
```

## Application Layers

### Public Layer

- Landing
- How It Works
- Stakeholder Overview

### Authentication Layer

- Login
- Patient Signup
- Verification
- Staff Account Activation
- Forgot Password
- Session States

### Authenticated Application Layer

After authentication, the application determines the user's authorized role and organizational scope.

### Operational Layer

The user sees only the workflows appropriate to the role.

## Patient Flow

```text
Patient Login
→ Dashboard
→ Find PHC
→ PHC Details
→ Appointment Booking
→ Slot Selection
→ Confirmation
→ My Appointments
→ Medicine Availability
→ Notifications
```

The patient's registered/home PHC and appointment PHC are separate concepts.

## Health Worker / Clinical Staff Flow

```text
Login
→ Dashboard
→ Patient Search
→ Patient Care View
→ Appointment
→ Start Visit
→ Encounter
→ Visit Confirmation
→ Medicine Availability
→ Pharmacist Coordination
```

## Pharmacist Flow

```text
Login
→ Assigned PHC Dashboard
→ Inventory
→ Medicine Details
→ Authorized Dispensing
→ Stock Transaction
→ Stock Threshold
→ Low Stock
→ Replenishment Request
→ Authority Review
```

## District Authority Flow

```text
Login
→ District Dashboard
→ Replenishment Inbox
→ Request Details
→ Review
→ Clarification / Approve / Adjust / Reject
→ Allocation
→ Supply Chain Handoff
→ Operational Tracking
```

## Supply Chain Flow

```text
Login
→ Approved Allocations
→ Allocation Details
→ Create Shipment
→ Verify Package
→ Dispatch
→ In Transit
→ Delivered
→ PHC Receipt Pending
```

## Administration Flow

```text
Login
→ Administration Dashboard
→ Account Management
→ Create / Activate / Suspend / Reactivate
→ Role Assignment
→ PHC Assignment
→ Organization Directory
→ Roles & Access
→ Audit Log
→ Security
```

## Important Architectural Principle

Do not implement these flows as separate applications.

They are interconnected workflows inside one MediFlow+ application.

The frontend should represent these connections clearly while backend authorization and state propagation are implemented later.
