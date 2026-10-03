# MediFlow+ — Final Production Audit

Audit the entire application; do not add unrelated features.

Check:
1. Routes — broken, duplicate, missing, bad redirects, dead navigation
2. Roles — Patient, Health Worker, Clinical Staff, Pharmacist, District Authority, Supply Chain, Admin
3. Workflow — Patient → Appointment → Clinical Visit → Medicine Availability → Dispensing → Inventory → Low Stock → Replenishment → Authority → Approval → Allocation → Shipment → Delivery → PHC Receipt → Inventory → Patient Availability
4. Buttons — every important action must work or be clearly disabled
5. Forms — validation, loading, errors, success, cancel, submit
6. Responsive — 360, 390, 430, 768, 1024, 1280, 1440
7. Languages — English, मराठी, हिन्दी
8. UI consistency — typography, spacing, buttons, cards, tables, dialogs, badges, navigation
9. User-facing text — remove inappropriate Demo, Synthetic, Sample, Fake, Mock, Test User, Prototype, Lorem ipsum, TODO and Coming Soon
10. Safety — no autonomous diagnosis, prescriptions, treatment recommendations, dosage recommendations or autonomous medical decisions
11. Security architecture — authentication, role, permissions, district scope, PHC scope and backend enforcement readiness
12. Build — npm run build and configured lint/typecheck

Fix issues where safe instead of merely reporting them.

Final report:
- routes
- roles
- workflows
- responsive
- languages
- access control
- UI consistency
- build
- typecheck
- lint
- remaining issues
- recommended backend/auth/database/realtime next step
