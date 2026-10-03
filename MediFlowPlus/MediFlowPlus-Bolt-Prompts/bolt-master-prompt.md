# MediFlow+ — Master Bolt Build Prompt

You are the lead software architect and senior React/TypeScript engineer for MediFlow+ — One Connected Loop for Patient Care & Medicine Supply.

## Critical first instruction
Do NOT start coding immediately. First inspect the entire repository:
- README.md
- bolt-master-prompt.md
- architecture/
- stitch/
- prompts/
- all Stitch HTML files, screenshots, DESIGN.md files and assets
- existing source code
- package.json and configuration
- routes, components, services, styles and types

Treat all eight Stitch phases as design phases of ONE application, not eight applications.

## Product
The connected workflow is:
Patient → Health Worker / Clinical Staff → PHC → Pharmacist → Medicine Dispensing → Inventory → Low Stock → Replenishment Request → District Health Authority → Approval / Allocation → Supply Depot → Shipment → Delivery → PHC Receipt → Inventory Update → Medicine Availability → Patient.

## Technology
Preferred direction:
- React
- TypeScript
- Vite
- React Router
- Tailwind CSS

Use reusable components, typed domain models, hooks, services, centralized permissions, centralized translations and feature-based organization.

## Repository separation
- stitch/ = Stitch design/reference material
- architecture/ = product architecture
- prompts/ = implementation instructions
- src/ = actual application

## Design
Build one professional healthcare/public-service design system. Reuse buttons, inputs, cards, tables, dialogs, badges, alerts, tabs, headers, breadcrumbs, search, filters and state components. Avoid excessive gradients, glassmorphism, animations and meaningless charts.

## User-facing language
Never display: Demo, Demo Data, Synthetic Data, Sample, Fake, Mock Data, Test User, Test Account, Prototype, or similar development wording in production UI.

## Languages
Support:
- English
- मराठी
- हिन्दी

Use centralized translation files.

## Responsive
Mobile-first and responsive for mobile, tablet, laptop and desktop. Test approximately 360, 390, 430, 768, 1024, 1280 and 1440px.

## Organization
Conceptual project structure:
District → Jalgaon → 8 Project PHCs → Multiple official users per PHC.
Do not present eight as a verified real-world PHC count unless separately verified.

## Authentication and authorization
Do not use role selection as login.
Authentication identifies the user; authorization determines access.

Patients may self-register.
Official accounts are created by authorized administrators.
Official roles:
- Health Worker
- Clinical Staff
- Pharmacist
- District Health Authority
- Supply Chain
- Admin

Support temporary-password / first-login password change.

Access should conceptually depend on:
Identity + Role + District + PHC + Permissions.

Frontend checks are not sufficient backend security; prepare for backend/database enforcement.

## Patient
Implement dashboard, profile, PHC search/results/details, appointment booking and slot selection, confirmation, appointments, medicine availability/details, notifications and loading/empty/error states.

Home/registered PHC and appointment PHC are separate. A patient can book at another PHC in the same district without changing home PHC.

## Health Worker / Clinical
Implement dashboards, patient list/search/profile, appointments, visit/encounter, visit summary, medicine availability, pharmacist coordination, notifications, profile and permission/state screens.

Do not implement autonomous diagnosis, prescription generation, treatment recommendations, dosage recommendations or autonomous medical decisions.

## Pharmacist
Implement dashboard, inventory, stock health, low-stock alerts, dispensing, validation, confirmation, stock transactions, replenishment, incoming shipments and receiving.

Dispensing flow:
Patient / authorized context → Medicine → Current Stock → Quantity → Projected Stock → Validation → Confirmation → Dispense → Stock Transaction → Inventory Update.

Prevent insufficient-stock confirmation and obvious negative inventory.

Low stock connects to replenishment. Delivered is not Received; inventory increases after authorized PHC receipt.

## District Authority
Implement district dashboard, PHC network/details, medicine availability, replenishment inbox, request review, clarification, approve/reject/adjust, allocation, reports, notifications, profile and states.

Do not automatically expose unrestricted sensitive clinical data.

## Supply Chain
Implement approved allocations, shipment creation, package verification, dispatch, tracking, delivery, exceptions, timeline, PHC destination, reports and notifications.

Shipment states:
Approved → Allocated → Packed → Dispatched → In Transit → Delivered → PHC Verification → Received → Completed.

## Admin
Implement dashboard, official account creation, account details/edit, suspend/reactivate, role and PHC assignment, organization directory, PHC administration, roles/access, permission details, audit logs/details, security alerts, notifications and profile.

Admin manages accounts, roles, permissions, organization, security and audit; admin is not automatically a healthcare operator.

## Shared architecture
Create reusable:
- application shell
- navigation
- profile
- notifications
- status system
- permission system
- loading/empty/error/success
- unauthorized
- session/connectivity states
- audit timeline

Create typed domain models for User, Patient, District, PHC, Medicine, InventoryItem, StockTransaction, Appointment, Encounter, ReplenishmentRequest, Allocation, Shipment, Notification and AuditEvent.

Create service abstractions such as authService, patientService, appointmentService, inventoryService, pharmacyService, replenishmentService, authorityService, shipmentService, adminService and notificationService.

Development fixtures may be used but must be centralized, typed and replaceable by real APIs.

## Routing
Use React Router with public, authentication, authenticated, role/permission-aware routes. Prefer reusable guards such as AuthenticatedRoute, RoleGuard, PermissionGuard, PHCScopeGuard and DistrictScopeGuard.

## Quality
No dead buttons, broken routes, duplicate applications, placeholder UI or unrelated features. Use semantic HTML, accessible controls, keyboard navigation, focus states, accessible dialogs and meaningful labels.

## Connected workflow validation
Validate:
Patient registration → Appointment → Clinical Visit → Medicine Availability → Pharmacist → Dispensing → Inventory Change → Low Stock → Replenishment → Authority → Approval → Allocation → Supply Chain → Shipment → Delivery → PHC Receipt → Inventory Update → Patient Medicine Availability.

Do not shortcut approval directly into inventory increase.

## Backend readiness
Prepare for Authentication, PostgreSQL, RLS, Realtime and API services. Supabase/PostgreSQL/Auth/RLS/Realtime is a likely direction, but do not make irreversible backend decisions before architecture review.

## Implementation order
1. Inspect repository
2. Analyze architecture and Stitch
3. Analyze existing code
4. Design system
5. Shell
6. Routing
7. Auth UI
8. Shared components
9. Patient
10. Health Worker / Clinical
11. Pharmacist
12. Authority
13. Supply Chain
14. Admin
15. Shared states
16. Multilingual
17. Responsive audit
18. Role audit
19. Workflow audit
20. Build/type/lint
21. Final polish

## First action
Before major coding, provide a concise assessment of repository structure, existing code, Stitch phases, architecture documents, routes, reusable components, dependencies, gaps, duplicate screens, role model, workflow model, implementation plan and critical ambiguities. Then proceed according to the execution prompts.
