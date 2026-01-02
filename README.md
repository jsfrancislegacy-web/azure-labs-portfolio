# Azure Labs Portfolio

This repository contains hands-on Azure documentation, configuration walkthroughs, and operational notes demonstrating how I design, secure, and manage Microsoft Azure environments.

The focus of this portfolio is **identity, security, governance, and readiness** for real-world client and small business Azure tenants.

---

## Repository Structure

- `/labs` – Step-by-step lab documentation and readiness walkthroughs
- `/screenshots` – Screenshots used in applicable labs
- `/scripts` – Scripts used during configuration (where applicable)

---

## Labs

### Lab 01 — Create an Azure Tenant
Initial setup of a Microsoft Entra ID tenant, establishing the foundation for identity and access management.

📸 Includes screenshots

---

### Lab 02 — Custom Domain Setup
Configuration of a custom domain in Microsoft Entra ID, including DNS setup and validation steps.

> **Note:**  
> DNS configuration was completed successfully; however, Azure domain verification remained pending due to platform-side validation delays. This lab documents the full process and reflects a real-world scenario where verification may take extended time.

📝 Documentation-only (no screenshots)

---

### Lab 03 — Admin Accounts & MFA
Creation of dedicated administrative accounts and enforcement of multi-factor authentication to secure privileged access.

📸 Includes screenshots

---

### Lab 04 — Conditional Access Baseline
Design and implementation of a Conditional Access policy to protect administrative roles.

> **Note:**  
> This lab was completed using a Microsoft Entra ID P2 trial.  
> The policy is intentionally left in **Report-only** mode to validate scope and behavior prior to enforcement, aligning with Microsoft best practices.

📸 Includes screenshots

---

### Lab 05 — Azure Subscription & RBAC Readiness
Documentation of Azure subscription requirements and Role-Based Access Control (RBAC) design principles.

This lab focuses on readiness and architecture, outlining how least-privilege access would be implemented once a subscription is present.

📝 Documentation-only (no screenshots)

---

### Lab 06 — Azure Cost Management & Budget Readiness
Overview of Azure cost management concepts, budget planning, alerting strategy, and governance considerations.

This lab documents how cost controls are designed and monitored in client environments prior to active billing configuration.

📝 Documentation-only (no screenshots)

---

## Summary

This portfolio demonstrates:
- Secure identity and access design using Microsoft Entra ID
- MFA and Conditional Access implementation
- Readiness for Azure RBAC and cost governance
- Practical, client-aligned Azure operational planning

The labs reflect real-world conditions, including licensing considerations and platform constraints, rather than idealized or academic examples.

