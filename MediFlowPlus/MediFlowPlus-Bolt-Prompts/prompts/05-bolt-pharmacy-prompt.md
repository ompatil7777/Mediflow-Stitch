# MediFlow+ — Phase 4: Pharmacist + Inventory

Implement:
- Pharmacist Dashboard
- Inventory Overview/Search/Details
- Stock Health
- Low Stock Alerts
- Dispense Medicine
- Validation
- Confirmation
- Stock Transactions
- Replenishment Request/Status
- Incoming Shipments
- Shipment Details
- Receiving
- Receipt Confirmation
- Notifications
- Profile
- Permission/Loading/Empty/Error/Success

Dispensing flow:
Patient / authorized context → Medicine → Current Stock → Quantity → Projected Stock → Validation → Confirmation → Dispense → Stock Transaction → Inventory Update.

Prevent insufficient-stock confirmation and obvious negative inventory.

Low stock must connect to replenishment.

Keep pharmacist operations within authorized PHC scope.

Delivered is not Received. Inventory increases only after authorized PHC receipt.

Run build/typecheck/lint.
