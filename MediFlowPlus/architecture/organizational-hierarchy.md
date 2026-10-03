# MediFlow+ Organizational Hierarchy

## Purpose

This document describes the organizational structure represented by the MediFlow+ application.

The eight PHC nodes described here are the project's application organization. They should not be presented as a verified real-world government count unless separately verified.

---

# Top-Level Structure

```text
MediFlow+
   ↓
District
   ↓
PHCs
   ↓
Official Users
```

## District

Project district context:

**Jalgaon District**

District-level operational roles include:

- District Health Authority
- Supply Chain users

---

# PHC Structure

The project application uses eight PHC organizational nodes:

1. Asoda PHC
2. Chalisgaon PHC
3. Jalgaon Rural PHC
4. Dharangaon PHC
5. Erandol PHC
6. Pachora PHC
7. Bhusawal Rural PHC
8. Jamner PHC

These names form the application's organizational dataset and workflow context.

---

# PHC Users

A PHC can contain multiple official users.

Example:

```text
Asoda PHC
   ├── Health Worker 001
   ├── Health Worker 002
   ├── Clinical Staff 001
   ├── Pharmacist 001
   └── Pharmacist 002
```

A PHC is not limited to one user per role.

---

# District Authority

The District Health Authority has district-level operational visibility.

The authority is responsible for workflows such as:

```text
PHC Replenishment Request
        ↓
Authority Review
        ↓
Approval / Adjustment / Rejection
        ↓
Allocation
```

The Authority should not automatically receive unrestricted clinical information.

---

# Supply Chain

Supply Chain operates at the supply/distribution layer.

```text
District Authority
       ↓
Approved Allocation
       ↓
Supply Chain
       ↓
Shipment
       ↓
PHC
```

Supply Chain does not approve the district request.

---

# Administrator

The System Administrator manages application and organizational access.

```text
Administrator
    ↓
Official Accounts
    ↓
Role Assignment
    ↓
District / PHC Assignment
    ↓
Access Scope
```

The administrator is an application-management role, not a healthcare operational role.

---

# Patient Organization Relationship

Patients have their own accounts.

A patient has:

- Own identity/account
- Registered/home PHC
- Appointment history
- Authorized appointment PHC relationships

The patient's home PHC does not necessarily equal the PHC where an appointment is booked.

The application can support booking at another PHC within the district where permitted.

---

# Example Identity

Example organizational account:

```text
User ID: PHARM-ASO-001
Role: Pharmacist
District: Jalgaon
PHC: Asoda PHC
```

The example illustrates organizational scoping.

---

# Authorization Concept

The hierarchy should ultimately map to database authorization.

Conceptually:

```text
User
 ↓
Role
 ↓
District
 ↓
PHC
 ↓
Authorized Records
```

For patients:

```text
Patient User
 ↓
Own Identity
 ↓
Own Authorized Records
```

The frontend should represent this model, while the backend/database must enforce it.
