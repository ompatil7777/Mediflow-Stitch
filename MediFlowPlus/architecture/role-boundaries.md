# MediFlow+ Role Boundaries

## Purpose

This document defines the intended application-level boundaries for each MediFlow+ role.

The UI should communicate these boundaries clearly. Actual security must later be enforced by the backend/database authorization layer.

## Authentication vs Authorization

Authentication answers:

> Who is the user?

Authorization answers:

> What is this user allowed to access?

A visible role label must never be treated as sufficient security.

---

# Patient / Citizen

## Can

- Create own patient account
- Manage own profile
- Search PHCs
- View PHC information
- Book appointments
- View own appointments
- View appointment details
- View medicine availability
- Receive notifications

## Cannot

- Access another patient's records
- Manage PHC inventory
- Dispense medicine
- Approve replenishment
- Create shipments
- Manage official accounts
- Access administrative functions

---

# Health Worker

## Can

- Access authorized patient/care-coordination information
- View assigned appointments
- Search authorized patients
- Start visits
- Record permitted encounter information
- View medicine availability
- Coordinate with pharmacists
- Receive notifications

## Cannot

- Manage inventory
- Dispense medicine
- Approve replenishment
- Create shipments
- Manage users
- Access unrelated PHCs

---

# Clinical Staff

## Can

- Access authorized clinical/care-coordination information
- View appointments
- Conduct the designed visit/encounter workflow
- View medicine availability
- Coordinate with pharmacists
- Receive notifications

## Cannot

- Perform pharmacist inventory transactions
- Approve district replenishment
- Manage shipments
- Manage application accounts

Clinical functionality must remain within the defined healthcare safety boundary.

---

# Pharmacist

## Can

- Access assigned PHC inventory
- Search medicines
- View stock
- Perform authorized dispensing
- Record stock transactions
- Submit replenishment requests
- View incoming shipments
- Verify received shipments
- Update inventory through authorized receipt workflows
- Receive operational notifications

## Cannot

- Approve district replenishment requests
- Manage other PHC inventory without authorization
- Create system users
- Perform system administration
- Make diagnosis or treatment decisions

---

# District Health Authority

## Can

- View district operational overview
- View authorized PHC operational summaries
- Review replenishment requests
- Inspect relevant stock context
- Request clarification
- Approve requests
- Adjust approved quantities where permitted
- Reject requests
- Create/advance allocations within the authority workflow
- Monitor downstream operational progress
- Receive district notifications

## Cannot

- Dispense medicine
- Enter pharmacist inventory transactions
- Perform patient diagnosis
- Create prescriptions
- Manage application users
- Perform supply-depot shipment operations

The Authority should receive only the patient/clinical information necessary for its operational purpose.

---

# Supply Chain Operator

## Can

- View approved allocations
- Process allocations
- Prepare shipments
- Verify shipment contents
- Dispatch shipments
- Track shipment status
- Record delivery status
- Record delivery exceptions
- View PHC supply operations
- Receive supply notifications

## Cannot

- Approve district replenishment requests
- Dispense medicine
- Modify patient clinical records
- Perform pharmacist inventory transactions
- Manage application users

Important distinction:

```text
Delivered ≠ Received
```

Delivered means the shipment reached the PHC.

Received means the PHC pharmacist verified and accepted it.

---

# System Administrator

## Can

- Create official accounts
- Activate accounts
- Suspend/reactivate accounts
- Assign organizational roles
- Assign district/PHC scope where applicable
- View organization directory
- View role/access information
- View audit records
- View security events
- Manage application-level organizational access

## Cannot

The administrator does not automatically become a healthcare or supply operator.

The administrator should not directly:

- Diagnose patients
- Dispense medicine
- Approve replenishment
- Create shipments
- Receive medicine
- Modify clinical records

---

# Organizational Scope

Typical scope model:

```text
District
   ↓
PHC
   ↓
Official User
```

Patient scope is different:

```text
Patient
   ↓
Own Account / Own Authorized Information
```

District-scoped roles can have district visibility appropriate to their function.

PHC-scoped roles should be limited to their assigned PHC unless explicitly authorized otherwise.

---

# Least Privilege

Every role should receive the minimum application access required for its workflow.

The frontend should reflect this principle, but the backend must enforce it.

---

# Safety Boundary

MediFlow+ must not autonomously:

- Diagnose
- Generate prescriptions
- Recommend treatment
- Make unsafe clinical decisions

The platform supports coordination, navigation, medicine availability, inventory, replenishment, and supply operations.
