# AZ-900 Domain 3: Identity, Access & Governance

## 1. Microsoft Entra ID (formerly Azure AD)
Cloud-based identity and access management (IAM) service.

- Key Capabilities:
  - Authentication: Verifying identities (who you are).
  - Authorization: Granting permissions to resources (what you can do).
  - Single Sign-On (SSO): Sign in once to access cloud apps, Power Platform, and internal portals.
  - Multi-Factor Authentication (MFA): Enforces two or more verification methods (password + authenticator app/FIDO2 key).
  - Conditional Access: If-then identity policies (e.g., "If signing in from an untrusted country, then require MFA and compliant device").

---

## 2. Azure Role-Based Access Control (RBAC)
Grants fine-grained access to Azure management plane resources based on the principle of least privilege.

- Core Built-In Roles:
  - Owner: Full access to all resources, including permission to delegate access to others.
  - Contributor: Can create and manage all types of Azure resources, but cannot grant access to others.
  - Reader: Can view existing Azure resources only.
  - User Access Administrator: Can manage user access to Azure resources (assign roles) without managing the actual infrastructure.

---

## 3. Resource Locks
Prevents accidental deletion or modification of critical cloud assets, regardless of a user's RBAC role.

- Lock Types:
  - CanNotDelete (Delete): Authorized users can still read and modify a resource, but cannot delete it.
  - ReadOnly (Read-only): Authorized users can only read a resource; they cannot modify, update, or delete it.
- Key Rule: Resource locks inherit down the resource tree. An administrator with `Owner` permissions cannot delete a resource locked with `CanNotDelete` without removing the lock first.

---

## 4. Azure Policy & Zero Trust Architecture

- Azure Policy:
  - Enforces organizational standards and assesses compliance at scale (e.g., "Only allow resource deployments in East US" or "Block non-encrypted storage accounts").
  - Evaluates resources at deployment time and continuously audits existing resources.
- Zero Trust Model:
  - Never trust, always verify.
  - 3 Core Principles:
    1. Verify explicitly (always authenticate and authorize based on all available data points).
    2. Use least privilege access (JIT/JEA, risk-based adaptive policies).
    3. Assume breach (minimize blast radius, segment access, inspect end-to-end traffic).
