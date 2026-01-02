# Lab 05 — Azure Subscription & RBAC Readiness

This lab documents the Azure subscription and access model required to implement Role-Based Access Control (RBAC) in client environments.

RBAC governs access to Azure resources such as virtual machines, storage accounts, and resource groups. Unlike Microsoft Entra ID (identity), RBAC requires an active Azure subscription and is enforced at the resource level.

This lab focuses on readiness, architecture understanding, and operational intent rather than resource creation.

---

## 🎯 Objectives
By the end of this lab, you will:
- Understand the relationship between Microsoft Entra ID and Azure subscriptions
- Identify prerequisites for implementing Azure RBAC
- Document how least-privilege access would be applied in a client environment
- Demonstrate readiness to manage Azure subscriptions securely

---

## 🧠 Key Concept — Identity vs Resources

Microsoft Entra ID (Azure AD) and Azure subscriptions serve different purposes:

- **Microsoft Entra ID**
  - Manages users, groups, roles, and authentication
  - Controls *who* can sign in
  - Enforces security policies such as MFA and Conditional Access

- **Azure Subscription**
  - Contains Azure resources (VMs, storage, networking, etc.)
  - Enforces RBAC permissions
  - Controls *what* users can access and modify

RBAC cannot be implemented without an active Azure subscription.

---

## 🧵 Step 1 — Subscription Prerequisites
To implement Azure RBAC, the following must exist:

- An active Azure subscription (Pay-As-You-Go, CSP, or Enterprise)
- Subscription associated with the appropriate Entra ID tenant
- At least one administrative account with **Owner** permissions

These prerequisites are typically handled during initial client onboarding or cloud adoption planning.

---

## 🧵 Step 2 — Subscription-to-Tenant Association
In client environments, Azure subscriptions are either:

- Created directly under the client’s Entra ID tenant, or
- Transferred from another tenant and reassigned

This ensures:
- Identity and access are centrally managed
- RBAC assignments align with organizational users and groups
- Security policies apply consistently

---

## 🧵 Step 3 — RBAC Design (Least Privilege Model)
Once a subscription is available, RBAC is implemented using the following principles:

- **Avoid subscription-wide Owner or Contributor access**
- Assign permissions at the **resource group** level when possible
- Use built-in roles such as:
  - Reader (view-only access)
  - Contributor (resource management without permission delegation)
- Grant elevated access only when operationally required

This approach limits blast radius and reduces the impact of compromised accounts.

---

## 🧵 Step 4 — Separation of Duties
A secure Azure access model separates responsibilities:

- **Identity administrators**
  - Manage users, MFA, and Conditional Access
- **Resource operators**
  - Manage workloads within scoped resource groups
- **Billing administrators**
  - Monitor costs without modifying resources

This separation aligns with Microsoft and industry security best practices.

---

## 🎉 Lab Completed
You now have:
- A clear understanding of Azure subscription requirements
- Documented RBAC readiness for client environments
- A least-privilege access model aligned with security best practices
- An operational plan for implementing RBAC once subscriptions are present

This lab demonstrates the ability to design, explain, and manage Azure access models responsibly in real-world client scenarios.
