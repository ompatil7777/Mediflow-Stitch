# MediFlow+ — Master Bolt Build Prompt

## One Connected Loop for Patient Care & Medicine Supply

---

# 1. ROLE

You are the lead software architect, senior React/TypeScript engineer, UX implementation engineer, and production-quality frontend developer for the **MediFlow+** project.

Your task is to transform the complete MediFlow+ Stitch design package into **one coherent, production-style web application**.

You are working with a complete design and architecture package.

Do **not** treat the Stitch phases as separate websites.

They are eight design phases of **one application**.

Your final implementation must be:

* professional
* responsive
* mobile-first
* multilingual
* accessible
* modular
* maintainable
* role-aware
* organization-aware
* workflow-driven
* ready for backend integration
* visually consistent with the Stitch designs

---

# 2. CRITICAL FIRST INSTRUCTION

## DO NOT START CODING IMMEDIATELY.

Before making major code changes, inspect the entire project.

You must first inspect:

```text
README.md

architecture/
├── application-flow.md
├── role-boundaries.md
├── organizational-hierarchy.md
├── screen-inventory.md
└── workflow-map.md

stitch/
├── 01-foundation/
├── 02-patient/
├── 03-health-worker/
├── 04-pharmacist/
├── 05-authority/
├── 06-supply-chain/
├── 07-admin/
└── 08-final-validation/
```

Inside the Stitch directories, inspect all available:

* HTML files
* screenshots
* DESIGN.md files
* assets
* visual references
* UI specifications
* navigation references
* responsive layouts
* forms
* tables
* cards
* dialogs
* states
* workflows

Do not inspect only one phase and start building.

Understand the complete system first.

---

# 3. SOURCE PRIORITY

When interpreting the project, use this priority order:

```text
1. architecture/
2. README.md
3. workflow-map.md
4. role-boundaries.md
5. organizational-hierarchy.md
6. screen-inventory.md
7. Stitch designs
8. Existing project code
9. Reasonable implementation decisions
```

Do not silently invent major business requirements.

If two visual designs represent the same reusable concept, consolidate them into a reusable component instead of creating duplicate implementations.

---

# 4. PROJECT CONCEPT

MediFlow+ is a healthcare coordination and medicine-supply platform.

The fundamental idea is a **connected operational loop**.

The system connects:

```text
Patient
    ↓
Health Worker / Clinical Staff
    ↓
PHC
    ↓
Pharmacist
    ↓
Medicine Dispensing
    ↓
Inventory
    ↓
Low Stock
    ↓
Replenishment Request
    ↓
District Health Authority
    ↓
Approval / Allocation
    ↓
Supply Depot
    ↓
Shipment
    ↓
Delivery
    ↓
PHC Receipt
    ↓
Inventory Update
    ↓
Medicine Availability
    ↓
Patient
```

This connected loop is the central product concept.

Do not build unrelated dashboards that happen to share branding.

---

# 5. ONE APPLICATION

The final result must be:

```text
ONE MediFlow+ application
```

Not:

```text
Patient application
+
Pharmacist application
+
Authority application
+
Supply application
+
Admin application
```

Instead:

```text
ONE APPLICATION
        ↓
Authentication
        ↓
Authorization
        ↓
Role
        ↓
District
        ↓
PHC
        ↓
Permissions
        ↓
Relevant experience
```

Every stakeholder is using the same underlying product.

---

# 6. TECHNOLOGY

Use the existing project technology where appropriate.

Preferred architecture:

```text
React
TypeScript
Vite
React Router
Tailwind CSS
```

Use modern React patterns.

Prefer:

* functional components
* reusable components
* TypeScript types
* feature-based organization
* reusable hooks
* service abstractions
* centralized constants
* centralized permissions
* centralized translations
* reusable UI primitives

Avoid:

* huge monolithic components
* duplicated screens
* duplicated business logic
* excessive `any`
* hard-coded role logic everywhere
* hard-coded strings everywhere

---

# 7. RECOMMENDED ARCHITECTURE

Use or improve the following structure:

```text
src/
│
├── app/
│   ├── router/
│   ├── providers/
│   ├── layouts/
│   └── config/
│
├── components/
│   ├── ui/
│   ├── forms/
│   ├── tables/
│   ├── cards/
│   ├── dialogs/
│   ├── navigation/
│   ├── feedback/
│   └── healthcare/
│
├── features/
│   ├── auth/
│   ├── patient/
│   ├── appointments/
│   ├── clinical/
│   ├── pharmacy/
│   ├── inventory/
│   ├── replenishment/
│   ├── authority/
│   ├── supply-chain/
│   ├── shipments/
│   ├── administration/
│   ├── notifications/
│   └── profile/
│
├── hooks/
├── services/
├── types/
├── constants/
├── utils/
├── i18n/
└── styles/
```

This is a guideline, not a rigid requirement.

Choose the structure that produces the cleanest maintainable application.

---

# 8. STITCH FILES ARE DESIGN REFERENCES

The Stitch exports are not separate applications.

Do not simply convert:

```text
code.html
```

into:

```text
Page.tsx
```

for every file.

Instead:

1. inspect the screen
2. understand its purpose
3. identify reusable components
4. identify common patterns
5. identify navigation relationships
6. identify role boundaries
7. identify workflow relationships
8. implement it inside the unified architecture

For example, if multiple Stitch screens contain the same:

* page header
* search bar
* filter bar
* table
* status badge

create reusable components.

---

# 9. DESIGN SYSTEM

Create one MediFlow+ design system.

The design system must maintain consistency across all phases.

Centralize:

* colors
* typography
* spacing
* border radius
* shadows
* buttons
* inputs
* cards
* tables
* badges
* dialogs
* alerts
* tabs
* navigation
* page headers
* breadcrumbs
* status indicators

Do not allow every page to invent its own styling.

---

# 10. VISUAL STYLE

The application should look like a professional healthcare/public-service platform.

It must NOT look like:

* a college assignment
* a generic dashboard template
* an AI-generated prototype
* a flashy startup landing page
* a collection of unrelated screens

Avoid excessive:

* gradients
* glassmorphism
* animations
* decorative graphics
* oversized cards
* excessive rounded elements
* unnecessary charts
* unnecessary visual effects

Prioritize:

* clarity
* trust
* accessibility
* information hierarchy
* operational efficiency
* readability
* touch usability
* consistency

---

# 11. NO USER-FACING DEMO LANGUAGE

Never display these terms in the application UI:

```text
Demo
Demo Data
Synthetic Data
Synthetic Demo Data
Sample
Sample Data
Fake
Fake Data
Test User
Test Account
Mock Data
Prototype
```

Development fixtures may exist internally.

However, the visible application must look like a real operational product.

---

# 12. MULTILINGUAL REQUIREMENT

The application must support:

```text
English
मराठी
हिन्दी
```

Implement this architecturally.

Prefer:

```text
src/i18n/
├── en.json
├── mr.json
└── hi.json
```

or an equivalent structure.

Do not hard-code major UI strings directly into components.

Provide a global language selector.

Example:

```text
English | मराठी | हिन्दी
```

Language selection should affect the application consistently.

Keep system identifiers such as:

```text
PHARM-ASO-001
```

unchanged.

---

# 13. RESPONSIVE REQUIREMENT

The application must work on:

```text
Mobile
Tablet
Laptop
Desktop
Large Desktop
```

Use mobile-first responsive design.

Do not merely shrink desktop layouts.

Test at approximately:

```text
360px
390px
430px
768px
1024px
1280px
1440px
```

Fix:

* overflow
* clipping
* broken tables
* overlapping dialogs
* navigation problems
* unreadable text
* inaccessible buttons

---

# 14. MOBILE EXPERIENCE

Mobile users may include:

* patients
* health workers
* pharmacists

Therefore, mobile is not a secondary experience.

Use:

* large touch targets
* clear navigation
* simple forms
* readable cards
* responsive tables
* appropriate mobile navigation
* simplified information hierarchy

---

# 15. ORGANIZATIONAL MODEL

The project uses this conceptual structure:

```text
District
   ↓
Jalgaon
   ↓
8 Project PHCs
   ↓
Multiple official users per PHC
```

The eight PHCs are project organizational nodes.

Do not represent the number eight as a verified real-world statistic unless independently verified.

Each PHC can have multiple:

```text
Health Workers
Doctors / Clinical Staff
Pharmacists
```

Do not assume one employee per PHC.

---

# 16. AUTHENTICATION

Authentication must answer:

> Who are you?

Do NOT use role selection as authentication.

Do not create:

```text
Select Role:
Patient
Pharmacist
Authority
Admin
```

as the login mechanism.

A user authenticates using their account credentials.

The system then determines their role and permissions.

---

# 17. AUTHORIZATION

Authorization answers:

> What are you allowed to access?

Conceptually:

```text
Identity
+
Role
+
District
+
PHC
+
Permissions
=
Access
```

Example:

```text
PHARM-ASO-001
Role: Pharmacist
District: Jalgaon
PHC: Asoda
```

should normally operate within the authorized PHC scope.

Do not give every authenticated user access to everything.

---

# 18. PATIENT ACCOUNTS

Patients can create their own accounts.

Patient registration may include:

```text
Name
Mobile
Email
Password
Confirm Password
Location
Home / Registered PHC
```

Patient accounts are self-created.

Patients must not be able to create official organizational accounts.

---

# 19. OFFICIAL ACCOUNTS

Official accounts are created by authorized administrators.

Official users include:

```text
Health Worker
Clinical Staff
Pharmacist
District Health Authority
Supply Chain
System Administrator
```

Official accounts should be associated with appropriate:

```text
User ID
Role
District
PHC
Account Status
```

where applicable.

---

# 20. TEMPORARY PASSWORD

Official accounts may be created with a temporary password.

First login should support:

```text
Temporary Password
        ↓
New Password
        ↓
Confirm Password
        ↓
Account Activated
```

Do not expose the temporary password after it has been replaced.

---

# 21. PATIENT HOME PHC VS APPOINTMENT PHC

These are different concepts.

A patient has:

```text
Home / Registered PHC
```

An appointment has:

```text
Appointment PHC
```

A patient can book an appointment at another PHC within the district without changing their home PHC.

The UI must clearly display the distinction.

---

# 22. ROLE MODEL

The supported roles are:

```text
PATIENT
HEALTH_WORKER
CLINICAL_STAFF
PHARMACIST
DISTRICT_AUTHORITY
SUPPLY_CHAIN
ADMIN
```

Do not invent additional operational healthcare roles unless the source architecture explicitly requires them.

---

# 23. PATIENT MODULE

Implement the complete patient experience from the Stitch package.

Required capabilities include:

```text
Patient Dashboard
Patient Profile
Find PHC
PHC Search Results
PHC Details
Appointment Booking
Appointment Slot Selection
Appointment Confirmation
My Appointments
Appointment Details
Medicine Availability
Medicine Details
Medicine Request / Status where applicable
Notifications
Loading States
Empty States
Error States
```

Patients should understand:

```text
My home PHC
My appointment PHC
My appointment
My medicine availability
My notifications
```

---

# 24. HEALTH WORKER MODULE

Implement:

```text
Health Worker Dashboard
Clinical Staff Dashboard
Patient List
Patient Search
Patient Profile / Care View
Today's Appointments
Appointment Details
Start Visit
Visit / Encounter Form
Visit Summary
Medicine Availability
Pharmacist Coordination
Notifications
Profile
Unauthorized / Permission
Loading
Empty
Error
```

---

# 25. PHARMACIST MODULE

Implement:

```text
Pharmacist Dashboard
Inventory Overview
Inventory Search
Inventory Details
Stock Health
Low Stock Alerts
Dispense Medicine
Dispensing Validation
Dispensing Confirmation
Stock Transactions
Replenishment Request
Replenishment Status
Incoming Shipments
Shipment Details
Receiving
Receipt Confirmation
Notifications
Profile
Permission States
Loading States
Empty States
Error States
```

---

# 26. DISPENSING WORKFLOW

The dispensing workflow must logically represent:

```text
Authorized Context
        ↓
Patient
        ↓
Medicine
        ↓
Current Stock
        ↓
Quantity
        ↓
Projected Stock
        ↓
Validation
        ↓
Confirmation
        ↓
Dispense
        ↓
Stock Transaction
        ↓
Inventory Updated
```

If:

```text
Current Stock = 3
Requested = 5
```

the UI must prevent confirmation.

Never allow obvious negative inventory.

---

# 27. INVENTORY

Inventory should display meaningful information such as:

```text
Medicine
Available Quantity
Unit
Minimum Threshold
Stock Status
Last Updated
PHC
```

Stock states may include:

```text
Healthy
Low Stock
Critical
Out of Stock
```

Use consistent visual semantics.

---

# 28. LOW-STOCK WORKFLOW

The application should communicate:

```text
Inventory decreases
        ↓
Threshold reached
        ↓
Low-stock alert
        ↓
Replenishment Request
        ↓
District Authority
```

Do not make low stock an isolated dashboard card.

It should connect to the operational workflow.

---

# 29. REPLENISHMENT

Pharmacist can create a replenishment request containing appropriate information such as:

```text
Medicine
Current Stock
Requested Quantity
Reason
Priority
PHC
Request Date
```

The request then becomes visible to the district authority.

---

# 30. AUTHORITY MODULE

Implement:

```text
District Dashboard
PHC Network
PHC Details
Medicine Availability
Replenishment Inbox
Request Details
Request Review
Clarification
Approve
Reject
Adjust
Allocation
Notifications
Reports
Profile
Unauthorized
Loading
Empty
Error
```

Authority users operate at district operational scope.

---

# 31. AUTHORITY DATA BOUNDARY

District authority should have operational visibility needed for:

* inventory
* replenishment
* PHC operations
* allocation
* supply coordination
* operational reporting

Do not automatically expose unrestricted sensitive patient clinical data.

---

# 32. SUPPLY CHAIN MODULE

Implement:

```text
Approved Allocations
Shipment Creation
Package Verification
Dispatch
Tracking
Delivery
Exceptions
Shipment Timeline
PHC Destination
Supply Reports
Notifications
Profile
Loading
Empty
Error
```

---

# 33. SHIPMENT STATES

Keep these states logically separate:

```text
Approved
Allocated
Packed
Dispatched
In Transit
Delivered
Received
Completed
```

Especially:

```text
Delivered ≠ Received
```

Correct workflow:

```text
Shipment Dispatched
        ↓
In Transit
        ↓
Delivered to PHC
        ↓
PHC Verification
        ↓
PHC Receipt
        ↓
Inventory Updated
```

---

# 34. ADMIN MODULE

Implement:

```text
Admin Dashboard
User Management
Official Account Creation
Account Details
Edit Account
Suspend Account
Reactivate Account
Role Assignment
PHC Assignment
Organization Directory
PHC Administration
Roles and Access
Permission Details
Audit Log
Audit Details
Security Alerts
Notifications
Profile
Confirmation States
Loading
Empty
Error
```

---

# 35. ADMIN BOUNDARY

The administrator is an application-management role.

The administrator manages:

```text
Accounts
Roles
Permissions
Organizational assignments
Security
Audit
```

The administrator is not automatically a:

```text
Doctor
Pharmacist
Health Worker
District Authority
Supply Chain Operator
```

Do not give unrelated healthcare operational capabilities to the admin.

---

# 36. AUDIT TRAIL

Important actions should produce visible audit information.

Examples:

```text
Account Created
Role Assigned
PHC Assigned
Medicine Dispensed
Inventory Changed
Replenishment Submitted
Request Approved
Allocation Created
Shipment Created
Shipment Dispatched
Shipment Delivered
Shipment Received
Account Suspended
Account Reactivated
```

Use reusable timeline/activity components.

---

# 37. NOTIFICATIONS

Create a centralized notification system.

Possible notification categories:

```text
Appointment
Medicine
Inventory
Replenishment
Authority
Shipment
Security
Account
```

Support:

```text
Read
Unread
Timestamp
Priority
Category
```

---

# 38. APPLICATION SHELL

Create one shared authenticated shell.

It should support:

```text
Header
Sidebar
Mobile Navigation
Breadcrumbs
Page Title
Notifications
Language Selector
Profile
Logout
```

Navigation must change based on permissions.

Do not show irrelevant navigation items.

---

# 39. PUBLIC WEBSITE

Implement the public experience:

```text
Landing Page
How It Works
Stakeholder Overview
Login
Patient Signup
Verification
Forgot Password
Staff Account Activation
```

The public site and application must share the same visual identity.

---

# 40. ROUTING

Use React Router.

Organize routes logically.

Conceptual structure:

```text
/
 /how-it-works
 /stakeholders
 /login
 /signup
 /verify
 /forgot-password
 /activate-account

/app
/app/dashboard
/app/profile
/app/notifications

/app/patient/...
/app/clinical/...
/app/pharmacy/...
/app/authority/...
/app/supply/...
/app/admin/...
```

Use the architecture documents to determine final routes.

---

# 41. ROUTE PROTECTION

Implement reusable concepts such as:

```text
AuthenticatedRoute
RoleGuard
PermissionGuard
PHCScopeGuard
DistrictScopeGuard
```

Do not scatter authorization logic throughout JSX.

---

# 42. UNAUTHORIZED

Create a professional unauthorized page:

```text
Access Restricted

You do not have permission to access this resource.

Return to Dashboard
```

---

# 43. SESSION STATES

Support UI for:

```text
Authentication Loading
Session Expired
Session Invalid
Logged Out
Unauthorized
Authentication Failure
```

---

# 44. LOADING STATES

Every data-heavy feature should have loading states.

Use:

* skeletons
* loading indicators
* loading buttons

where appropriate.

Avoid blank screens.

---

# 45. EMPTY STATES

Every list/table must have an appropriate empty state.

Examples:

```text
No appointments found
No patients found
No medicines found
No low-stock items
No replenishment requests
No shipments
No notifications
```

Provide useful next actions where appropriate.

---

# 46. ERROR STATES

Create reusable error states:

```text
Unable to load data
Something went wrong
Connection unavailable
Request failed
Permission denied
Try again
```

Do not show raw technical errors to normal users.

---

# 47. CONNECTIVITY

The platform may be used in environments with variable connectivity.

Provide clear states for:

```text
Connection lost
Slow connection
Retry
Request failed
Data unavailable
```

---

# 48. FORMS

All important forms should support:

* validation
* required fields
* clear errors
* disabled submit while processing
* success state
* failure state
* cancel
* back

---

# 49. IMPORTANT ACTION CONFIRMATIONS

Use confirmation dialogs for important actions such as:

```text
Dispense Medicine
Approve Request
Reject Request
Create Shipment
Dispatch Shipment
Receive Shipment
Suspend Account
Deactivate Account
```

---

# 50. SUCCESS STATES

Important actions should provide confirmation.

Examples:

```text
Medicine dispensed successfully
Replenishment request submitted
Request approved
Shipment dispatched
Shipment received
Account created
Password changed
Profile updated
```

---

# 51. DOMAIN TYPES

Create proper TypeScript types for core entities.

Examples:

```text
User
Patient
District
PHC
HealthWorker
ClinicalStaff
Pharmacist
Medicine
InventoryItem
StockTransaction
Appointment
Encounter
ReplenishmentRequest
Allocation
Shipment
ShipmentItem
Notification
AuditEvent
```

Avoid excessive use of `any`.

---

# 52. USER ROLE TYPE

Create a centralized role definition similar to:

```ts
type UserRole =
  | "PATIENT"
  | "HEALTH_WORKER"
  | "CLINICAL_STAFF"
  | "PHARMACIST"
  | "DISTRICT_AUTHORITY"
  | "SUPPLY_CHAIN"
  | "ADMIN";
```

Use the actual architecture conventions if already established.

---

# 53. PERMISSION SYSTEM

Create centralized permissions.

Conceptually:

```text
VIEW_PATIENT_PROFILE
VIEW_APPOINTMENTS
DISPENSE_MEDICINE
VIEW_INVENTORY
MANAGE_INVENTORY
CREATE_REPLENISHMENT
REVIEW_REPLENISHMENT
APPROVE_REPLENISHMENT
CREATE_ALLOCATION
CREATE_SHIPMENT
DISPATCH_SHIPMENT
RECEIVE_SHIPMENT
MANAGE_USERS
MANAGE_ROLES
VIEW_AUDIT_LOG
```

Do not duplicate role logic throughout the application.

---

# 54. ORGANIZATION CONTEXT

Represent organizational scope explicitly.

Conceptually:

```ts
interface OrganizationContext {
  districtId: string;
  phcId?: string;
  role: UserRole;
}
```

Use this architecture to prepare for future backend authorization.

---

# 55. SERVICE LAYER

Do not directly scatter mock data throughout UI components.

Create service abstractions such as:

```text
authService
patientService
appointmentService
clinicalService
inventoryService
pharmacyService
replenishmentService
authorityService
shipmentService
adminService
notificationService
```

The UI should interact with services rather than knowing where data comes from.

---

# 56. FRONTEND DATA ARCHITECTURE

For the frontend stage, development fixtures are acceptable.

Keep them:

* centralized
* typed
* replaceable
* separate from components

The UI should be capable of switching from:

```text
development service
```

to:

```text
real backend service
```

without rewriting every page.

---

# 57. BACKEND PREPARATION

The eventual architecture may use:

```text
Supabase
PostgreSQL
Authentication
Row-Level Security
Realtime
```

Do not assume this is already configured unless the existing project says so.

For this stage, prioritize a clean frontend architecture that can integrate with the backend later.

---

# 58. SECURITY PRINCIPLE

Remember:

```text
Authentication != Authorization
```

Authentication identifies the user.

Authorization determines permissions.

Organizational scope determines which records the user can access.

Frontend checks are not sufficient security.

The eventual backend/database must enforce authorization.

---

# 59. REALTIME ARCHITECTURE

The eventual system should support connected state changes.

Conceptually:

```text
Pharmacist Dispenses
        ↓
Inventory Changes
        ↓
Low Stock
        ↓
Replenishment
        ↓
Authority Approval
        ↓
Allocation
        ↓
Shipment
        ↓
Delivery
        ↓
PHC Receipt
        ↓
Inventory Increase
        ↓
Availability Update
```

Build the frontend state model so these transitions can later be driven by realtime backend events.

---

# 60. PATIENT SAFETY

MediFlow+ is a coordination platform.

Do NOT implement autonomous:

```text
Diagnosis
Prescription Generation
Treatment Recommendations
Medication Dosage Recommendations
Medical Decision-Making
```

The system may support:

```text
Appointments
Care Coordination
Patient Information
Medicine Availability
Operational Communication
Medicine Workflow
```

Professional medical decisions remain with authorized healthcare professionals.

---

# 61. TABLES

Reusable tables should support, where relevant:

```text
Search
Filter
Sort
Pagination
Status
Actions
Responsive behavior
```

On mobile, use:

* cards
* expandable rows
* horizontal scrolling
* simplified layouts

as appropriate.

---

# 62. SEARCH

Create reusable search patterns for:

```text
Patients
Medicines
PHCs
Users
Appointments
Replenishment Requests
Shipments
```

Support appropriate:

```text
Loading
No Results
Clear
Error
```

---

# 63. FILTERS

Use reusable filters for:

```text
Status
PHC
District
Date
Priority
Role
Medicine
Shipment Status
```

Only show filters relevant to the screen.

---

# 64. ACCESSIBILITY

Use:

* semantic HTML
* labels
* keyboard navigation
* focus states
* accessible dialogs
* accessible buttons
* meaningful form errors
* sufficient contrast
* accessible icons

Do not create icon-only controls without accessible labels.

---

# 65. ICONS

Use a consistent icon library.

Do not mix unrelated icon styles.

Icons should improve usability.

---

# 66. DASHBOARD DESIGN

A dashboard should answer:

```text
What needs my attention?
What changed?
What is pending?
What requires action?
What is blocked?
```

Do not fill dashboards with meaningless metrics.

Use charts only where they provide operational value.

---

# 67. ROLE-SPECIFIC PRIORITIES

## Patient

Prioritize:

```text
Appointments
PHC Search
Medicine Availability
Notifications
Profile
```

## Health Worker

Prioritize:

```text
Today's Appointments
Patients
Patient Search
Visits
Medicine Availability
Pharmacist Coordination
```

## Pharmacist

Prioritize:

```text
Inventory
Low Stock
Dispensing
Replenishment
Incoming Shipments
Receiving
```

## Authority

Prioritize:

```text
District Overview
PHC Status
Low Stock
Replenishment Requests
Approvals
Allocations
Reports
```

## Supply Chain

Prioritize:

```text
Approved Allocations
Shipments
Dispatch
Tracking
Delivery
Exceptions
```

## Admin

Prioritize:

```text
Users
Accounts
Roles
PHC Assignments
Security
Audit
```

---

# 68. SHARED COMPONENTS

Create reusable components for repeated patterns.

Examples:

```text
PageHeader
Breadcrumbs
SearchBar
FilterBar
DataTable
StatusBadge
NotificationCard
EmptyState
ErrorState
LoadingState
ConfirmDialog
FormField
PHCCard
MedicineCard
AppointmentCard
InventoryCard
ShipmentTimeline
ActivityTimeline
PatientSummary
```

Do not duplicate these unnecessarily.

---

# 69. BUSINESS LOGIC

Do not put complex business logic inside JSX.

Separate:

```text
Components
Hooks
Services
Utils
Permissions
Types
Constants
```

Keep components focused on presentation and interaction.

---

# 70. IMPORTANT WORKFLOW

The complete frontend should represent this scenario:

```text
Patient Registration
        ↓
Home PHC
        ↓
Find PHC
        ↓
Book Appointment
        ↓
Appointment
        ↓
Health Worker / Clinical Staff
        ↓
Visit
        ↓
Medicine Availability
        ↓
Pharmacist
        ↓
Dispensing
        ↓
Inventory Transaction
        ↓
Low Stock
        ↓
Replenishment Request
        ↓
District Authority
        ↓
Approval
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
PHC Verification
        ↓
Received
        ↓
Inventory Updated
        ↓
Medicine Availability Updated
```

Do not break this logical chain.

---

# 71. DO NOT CREATE UNREALISTIC SHORTCUTS

Do not implement:

```text
Authority Approval
        ↓
Inventory Instantly Increases
```

The correct workflow is:

```text
Approval
↓
Allocation
↓
Shipment
↓
Delivery
↓
PHC Receipt
↓
Inventory Increase
```

---

# 72. NAVIGATION

Navigation must be permission-aware.

A patient should not see:

```text
District Authority
Supply Chain
Admin
```

unless explicitly authorized.

A pharmacist should not see:

```text
Admin User Management
```

unless they have that permission.

---

# 73. PROFILE

Profile should be role-aware.

Patient profile:

```text
Personal Information
Contact
Home PHC
```

Official profile:

```text
Name
User ID
Role
District
PHC
Account Status
```

Users must not arbitrarily modify organizational permissions.

---

# 74. SECURITY SETTINGS

Support appropriate security actions such as:

```text
Change Password
Session Information
Recent Security Activity
Logout
```

---

# 75. NO DEAD BUTTONS

Every important interactive element must:

1. perform an action
2. navigate
3. open a dialog
4. update state
5. submit data
6. or be clearly disabled

Do not leave decorative buttons pretending to work.

---

# 76. NO PLACEHOLDER CONTENT

Do not leave:

```text
Lorem ipsum
TODO
Coming Soon
Placeholder
Test
Sample
Click here
```

unless the actual product specification requires such a state.

---

# 77. ROUTE AUDIT

After implementation, inspect every route.

Check:

```text
No broken routes
No missing pages
No duplicate routes
No unreachable important screens
No incorrect redirects
No dead navigation
```

---

# 78. BUTTON AUDIT

Inspect important actions.

For every action, determine:

```text
What does it do?
Where does it go?
What changes?
What happens on success?
What happens on failure?
```

If an important button does nothing, fix it.

---

# 79. FORM AUDIT

Check:

```text
Required fields
Validation
Errors
Loading
Success
Failure
Cancel
Back
Submit
```

---

# 80. ROLE AUDIT

Test all roles:

```text
Patient
Health Worker
Clinical Staff
Pharmacist
District Authority
Supply Chain
Admin
```

Verify that each receives the correct navigation and permissions.

---

# 81. ORGANIZATIONAL AUDIT

Verify examples such as:

```text
Asoda Pharmacist
        ↓
Asoda Inventory
```

does not automatically become:

```text
All PHC Inventory
```

Also verify:

```text
Patient A
```

cannot access:

```text
Patient B
```

---

# 82. LANGUAGE AUDIT

Switch through:

```text
English
मराठी
हिन्दी
```

and inspect the entire application.

Find untranslated UI strings and fix them.

---

# 83. RESPONSIVE AUDIT

Inspect major screens on:

```text
360px
390px
430px
768px
1024px
1280px
1440px
```

Fix all significant responsive issues.

---

# 84. BUILD CHECK

Run the available project checks.

At minimum, where configured:

```bash
npm install
npm run build
```

Also run:

```bash
npm run lint
npm run typecheck
```

if those scripts exist.

Fix errors.

Do not declare completion with known build or TypeScript errors.

---

# 85. DO NOT DESTROY EXISTING WORK WITHOUT REVIEW

Before replacing existing files:

1. inspect them
2. determine whether they are reusable
3. preserve useful work
4. refactor where appropriate
5. replace only when necessary

Do not repeatedly restart the entire project.

Maintain one source of truth.

---

# 86. IMPLEMENTATION ORDER

Use this sequence:

```text
1. Inspect entire project
2. Understand architecture
3. Understand all Stitch phases
4. Analyze existing code
5. Create implementation plan
6. Establish design system
7. Establish application shell
8. Establish routing
9. Establish authentication UI
10. Establish reusable components
11. Implement patient
12. Implement health worker / clinical
13. Implement pharmacist
14. Implement authority
15. Implement supply chain
16. Implement administration
17. Implement notifications/profile/shared states
18. Implement multilingual system
19. Implement responsive behavior
20. Integrate service abstractions
21. Run route audit
22. Run role audit
23. Run workflow audit
24. Run responsive audit
25. Run language audit
26. Run build/type/lint
27. Fix issues
28. Final polish
```

---

# 87. DO NOT OVERBUILD

Do not randomly add:

```text
Social Media
Payments
Chat
AI Diagnosis
AI Prescription
Unrelated Analytics
Gamification
Unrelated Healthcare Features
```

Stay within MediFlow+ scope.

---

# 88. VISUAL FIDELITY

The Stitch package is the primary visual reference.

Preserve:

* major layout hierarchy
* visual language
* screen purpose
* component patterns
* responsive intent
* information hierarchy

However, implementation quality takes priority over blindly copying HTML.

---

# 89. CONFLICT RESOLUTION

If two Stitch screens contain different implementations of the same concept:

Determine whether the difference is:

```text
Role-specific
Context-specific
Responsive
Workflow-specific
```

If not, consolidate them into one reusable component.

Example:

```text
NotificationCard
```

rather than:

```text
PatientNotificationCard
PharmacistNotificationCard
AuthorityNotificationCard
AdminNotificationCard
```

unless their behavior genuinely differs.

---

# 90. DATA VISUALIZATION

Use charts only where they communicate useful information.

Possible examples:

```text
Inventory Trends
Low Stock Trends
Replenishment Status
PHC Medicine Availability
Shipment Status
Operational Summaries
```

Do not add charts merely to make dashboards look sophisticated.

---

# 91. FINAL END-TO-END VALIDATION

Before completion, validate this entire conceptual flow:

```text
Patient
↓
Appointment
↓
Health Worker / Clinical Staff
↓
Visit
↓
Medicine Availability
↓
Pharmacist
↓
Dispensing
↓
Inventory Change
↓
Low Stock
↓
Replenishment
↓
Authority
↓
Approval
↓
Allocation
↓
Supply
↓
Shipment
↓
Delivery
↓
PHC Receipt
↓
Inventory Update
↓
Patient Medicine Availability
```

Every major stage should have a corresponding screen, route, component, state, or workflow representation where specified by the design package.

---

# 92. FRONTEND FIRST

Your immediate goal is to build and stabilize the complete frontend.

Prioritize:

```text
UI
Routing
Components
Role Architecture
Authorization Architecture
Workflow Architecture
State Architecture
Responsive Design
Multilingual Architecture
```

Do not prematurely spend the majority of implementation time configuring production infrastructure.

The backend will be integrated after the frontend architecture is stable.

---

# 93. BACKEND READINESS

Prepare clean interfaces for eventual:

```text
Authentication
PostgreSQL
Row-Level Security
Realtime
API Services
```

A likely backend direction is:

```text
Supabase
+
PostgreSQL
+
Auth
+
RLS
+
Realtime
```

but do not force this architecture if the project already specifies a different implementation.

---

# 94. IMPORTANT SECURITY REMINDER

Frontend authorization is not real security.

The eventual backend must enforce:

```text
Authentication
Role
Permissions
District Scope
PHC Scope
Record Ownership
Data Access
```

Do not claim that hiding a button provides security.

---

# 95. FINAL ACCEPTANCE CRITERIA

The implementation is complete only when all of the following are satisfied.

## Architecture

* One React application
* Modular architecture
* Reusable components
* Typed domain models
* Service abstraction
* Centralized permissions

## UI

* Professional
* Responsive
* Mobile-first
* Accessible
* Stitch-aligned
* Consistent

## Roles

* Patient
* Health Worker
* Clinical Staff
* Pharmacist
* District Authority
* Supply Chain
* Admin

## Organization

```text
District
↓
Jalgaon
↓
8 Project PHCs
↓
Multiple Users
```

## Authentication

* Patient self-registration
* Official admin-created accounts
* Temporary password workflow
* No role-selection login

## Authorization

* Role-aware
* District-aware
* PHC-aware
* Permission-aware

## Language

* English
* मराठी
* हिन्दी

## Workflow

* Appointment
* Clinical coordination
* Medicine availability
* Dispensing
* Inventory
* Low stock
* Replenishment
* Authority review
* Approval
* Allocation
* Shipment
* Delivery
* Receipt
* Inventory update

## UX States

* Loading
* Empty
* Error
* Success
* Unauthorized
* Session expired
* Connectivity failure

## Quality

* No dead buttons
* No broken routes
* No duplicate applications
* No visible demo/sample/test wording
* No placeholder content
* No unnecessary features
* No known build errors
* No known TypeScript errors
* No major responsive issues

---

# 96. FIRST RESPONSE / FIRST ACTION

Your first task is NOT to write hundreds of components.

Your first task is to inspect the repository.

After inspection, produce a concise implementation assessment containing:

```text
1. Current project structure
2. Existing application architecture
3. Stitch phases discovered
4. Architecture documents discovered
5. Existing reusable components
6. Existing routes
7. Existing dependencies
8. Major implementation gaps
9. Recommended implementation order
10. Any critical conflicts or ambiguities
```

Then begin implementation.

Do not ask me to manually explain information that already exists in the repository.

---

# 97. FINAL DIRECTIVE

Treat the complete repository as the specification for one product.

Do not build eight separate applications.

Do not blindly convert HTML files into pages.

Do not ignore architecture documentation.

Do not ignore role boundaries.

Do not ignore organizational scope.

Do not ignore the connected workflow.

Do not ignore mobile responsiveness.

Do not ignore English/मराठी/हिन्दी.

Do not expose development/demo terminology to users.

Do not implement autonomous medical decision-making.

Do not create dead buttons.

Do not create disconnected dashboards.

Do not prematurely replace the project with an unrelated architecture.

Instead:

# BUILD ONE COHERENT MEDIFLOW+ APPLICATION

with:

```text
One Product
        ↓
One Design System
        ↓
One Application Shell
        ↓
One Routing System
        ↓
One Authentication Model
        ↓
One Authorization Model
        ↓
District → PHC Organizational Scope
        ↓
Multiple Role Experiences
        ↓
Connected Operational Workflow
        ↓
Backend-Ready Architecture
```

The final product should feel like a real professional healthcare/public-service coordination platform.

# START BY INSPECTING THE ENTIRE REPOSITORY.

Then plan.

Then implement.

Then test.

Then audit.

Then polish.

Do not skip the inspection stage.
