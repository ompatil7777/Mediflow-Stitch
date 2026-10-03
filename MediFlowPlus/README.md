# MediFlow+

## One Connected Loop for Patient Care & Medicine Supply

MediFlow+ is a single responsive healthcare coordination and medicine-supply web application connecting patients, healthcare workers, clinical staff, pharmacists, district health authorities, supply-chain operators, and system administrators.

This folder contains the complete UI/UX design package produced through Stitch across eight phases.

---

## Important

This is ONE application.

The eight folders represent different functional areas of the same application.

They are NOT eight separate websites or eight separate applications.

Bolt must analyze the entire package before implementing the frontend.

---

# Application Structure

```text
Public Website
      ↓
Authentication
      ↓
Application Shell
      ↓
Role-Based Authorized Experience
      │
      ├── Patient / Citizen
      ├── Health Worker / Clinical Staff
      ├── Pharmacist
      ├── District Health Authority
      ├── Supply Chain
      └── System Administrator
```

---

# Organizational Structure

```text
District
   ↓
PHC
   ↓
Official Users
   ├── Health Workers
   ├── Clinical Staff
   └── Pharmacists
```

District-level users include:

- District Health Authority
- Supply Chain users

Administrators manage organizational accounts and access.

The application uses an organizational structure containing eight PHC nodes for the project.

---

# Core Workflow

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

This connected loop is the central concept of MediFlow+.

---

# Stitch Phases

## 01 — Foundation

Contains:

- Public landing
- How it works
- Stakeholder overview
- Authentication
- Patient signup
- Verification
- Staff activation
- Forgot password
- Application shell
- Generic dashboard
- Profile
- Notifications
- Unauthorized
- Session/security states
- Responsive foundation
- Multilingual foundation

---

## 02 — Patient / Citizen

Contains:

- Patient dashboard
- Patient profile
- PHC search
- PHC details
- Appointment booking
- Slot selection
- Appointment confirmation
- My appointments
- Appointment details
- Medicine availability
- Medicine details
- Notifications
- Loading states
- Error states
- Empty states

Patient home/registered PHC and appointment PHC are separate concepts.

A patient may book an appointment at another PHC within the district where permitted.

---

## 03 — Health Worker / Clinical Staff

Contains:

- Health Worker dashboard
- Clinical Staff dashboard
- Patient list
- Patient search
- Patient care view
- Today's appointments
- Appointment details
- Visit workflow
- Encounter form
- Visit confirmation
- Medicine availability
- Pharmacist coordination
- Notifications
- Profile
- Permission states
- Loading/error/empty states

---

## 04 — Pharmacist / Inventory

Contains:

- Pharmacist dashboard
- Inventory overview
- Medicine search
- Medicine details
- Stock health
- Low-stock alerts
- Dispensing workflow
- Quantity validation
- Dispensing confirmation
- Stock transactions
- Replenishment request
- Request status
- Incoming shipments
- Shipment verification
- PHC receipt
- Inventory update
- Notifications
- Loading/error/empty states

---

## 05 — District Health Authority

Contains:

- District dashboard
- District operational overview
- PHC network
- PHC details
- Medicine availability
- Replenishment request inbox
- Request details
- Request review
- Clarification
- Approval
- Quantity adjustment
- Rejection
- Allocation
- Allocation details
- Reports
- Notifications
- Activity
- Permission states
- Loading/error/empty states

---

## 06 — Supply Chain

Contains:

- Supply chain dashboard
- Operational queue
- Approved allocations
- Allocation details
- Shipment creation
- Package verification
- Shipment verification
- Shipment list
- Shipment details
- Dispatch
- Tracking
- Delivery
- Delivery exceptions
- Shipment audit timeline
- PHC supply view
- Medicine supply view
- Reports
- Notifications
- Loading/error/empty states

---

## 07 — System Administration

Contains:

- Administration dashboard
- User/account management
- Account creation
- Official account activation
- Role assignment
- PHC assignment
- Account details
- Account editing
- Suspension/reactivation
- Security
- Session management
- Organization directory
- PHC administration
- Roles/access
- Permission details
- Audit log
- Security alerts
- Notifications
- Administrative activity
- Profile

---

## 08 — Final Polish

Contains cross-application UX consistency and final validation for:

- Navigation
- Components
- Statuses
- Buttons
- Forms
- Tables
- Search
- Filters
- Loading
- Error
- Empty
- Success
- Unauthorized
- Session states
- Connectivity states
- Responsive behavior
- English
- मराठी
- हिन्दी
- Accessibility
- Role boundaries
- End-to-end workflows

---

# Design Principles

The final application must maintain:

- Professional healthcare/public-service visual language
- Mobile-first responsive design
- Desktop/tablet/mobile support
- Accessible interaction
- Clear information hierarchy
- Consistent components
- Clear operational states
- Least-privilege UX
- Organizational scope
- Multilingual readiness

---

# Authentication

The application must NOT use a role-selection dropdown as the mechanism for authentication.

Authentication determines who the user is.

Authorization determines what that user can access.

Patient users may create their own accounts.

Official users are created/managed through authorized administration.

---

# Official Account Model

Official users can be associated with:

- Role
- District
- PHC where applicable
- Organization

Multiple official users can belong to the same PHC.

Examples:

- Multiple health workers
- Multiple clinical staff
- Multiple pharmacists

---

# Security Principle

Synthetic organizational/development data does not mean synthetic security.

The final implementation must use real:

- Authentication
- Authorization
- Organizational scoping
- Database-level access control
- Auditability

These are implementation responsibilities and are not being implemented by Stitch.

---

# Language

The application must support:

**English | मराठी | हिन्दी**

The interface must be designed so translated text does not break layouts.

---

# Safety Boundary

MediFlow+ is a healthcare coordination and supply platform.

It must not autonomously:

- Diagnose patients
- Generate prescriptions
- Recommend treatment
- Make unsafe clinical decisions

The system supports care navigation, coordination, medicine availability, inventory, replenishment, and supply operations.

---

# User-Facing Text

Do not display:

- Demo
- Synthetic Data
- Sample
- Test
- Fake
- Mock
- Prototype

The final interface should appear production-ready.

---

# Important Instruction for Bolt

Do NOT treat the phase folders as independent applications.

Before coding:

1. Inspect every phase.
2. Inspect screenshots.
3. Inspect HTML/code.
4. Inspect DESIGN.md files.
5. Understand shared visual patterns.
6. Build one unified application architecture.
7. Reuse common components.
8. Reconcile repeated screens.
9. Preserve the intended workflows.
10. Do not blindly concatenate HTML files.

The final result must be a single coherent MediFlow+ application.

---

# Technology Direction

The final frontend is expected to become a modern:

- React
- TypeScript
- Vite
- React Router
- Responsive web application

The backend/database/authentication/realtime layer will be implemented after the frontend architecture is stable.

---

# Final Development Principle

Do not build eight dashboards.

Build one connected operational system.

Every important state change should eventually propagate through the appropriate workflow:

```text
Dispensing
→ Inventory
→ Low Stock
→ Replenishment
→ Authority
→ Approval
→ Allocation
→ Shipment
→ PHC Receipt
→ Inventory
→ Availability
```

This connected state model is more important than reproducing individual screenshots literally.

---

# Package Status

Stitch design phases:

1. Foundation
2. Patient
3. Health Worker / Clinical Staff
4. Pharmacist
5. District Authority
6. Supply Chain
7. Administration
8. Final Polish

All phases together constitute the MediFlow+ frontend design source package.
