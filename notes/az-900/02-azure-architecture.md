# AZ-900 Domain 2: Azure Architecture & Hierarchy

## 1. The Resource Management Hierarchy
Access control (RBAC) and compliance policies inherit top-down through four distinct levels:

    [ Management Groups ]  --> Access, policy, and compliance for multiple subscriptions
             │
             ▼
      [ Subscriptions ]    --> Billing boundary and quota allocation
             │
             ▼
     [ Resource Groups ]   --> Logical container deployed and managed as a unit
             │
             ▼
        [ Resources ]      --> Individual instances (VMs, Storage Accounts, VNets, Web Apps)

> Inheritance Rule: Any policy or role assignment defined at a higher level automatically cascades to all child containers beneath it.

---

## 2. Structural Scopes Explained

- Management Groups:
  - Useful for enterprise governance across multiple departments/environments.
  - Supports hierarchies up to 6 levels deep.
- Subscriptions:
  - Billing Boundary: Invoices and chargebacks are generated per subscription.
  - Access Boundary: RBAC administrators can scope permissions across an entire project suite.
- Resource Groups (RG):
  - Resources can only exist in one Resource Group at a time.
  - Resources can communicate across different Resource Groups.
  - Deleting a Resource Group automatically purges every resource inside it.

---

## 3. Physical Datacenter Architecture

- Regions:
  - Geographical area containing one or more datacenters networked via low-latency links.
- Availability Zones (AZs):
  - Physically separate datacenters within the same Azure region.
  - Independent power, cooling, and networking.
  - Guarantees minimum 99.99% VM uptime SLA when deployed across multiple AZs.
- Region Pairs:
  - Each Azure region is paired with another region within the same geography (at least 300 miles apart).
  - Serialized platform updates prevent simultaneous downtime.
  - Automatic cross-region data replication.
