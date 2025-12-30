# Lab 02 — Custom Domain Setup in Microsoft Entra ID

This lab walks through adding and verifying a custom domain in Microsoft Entra ID (Azure Active Directory).  
A custom domain allows the organization to use real, branded user accounts instead of the default `onmicrosoft.com` domain.

---

## 🎯 Objectives
By the end of this lab, you will:
- Add a custom domain to Microsoft Entra ID
- Verify domain ownership using DNS
- Understand how custom domains are used for user identities

---

## 🛠️ Prerequisites
- Active Azure tenant
- Access to Microsoft Entra ID
- Ownership of a public domain (example: `jsfrancislegacy.com`)
- Access to the domain’s DNS provider

---

## 🧵 Step 1 — Open Custom Domain Names
1. Sign in to https://portal.azure.com  
2. Navigate to **Microsoft Entra ID**  
3. Select **Custom domain names**

📸 **Screenshot:** Custom domain names page  
_Save screenshot in:_  
`/screenshots/lab02/custom-domain-overview.png`

---

## 🧵 Step 2 — Add a New Custom Domain
1. Click **Add custom domain**  
2. Enter your domain name:
   - `jsfrancislegacy.com`
3. Click **Add domain**

📸 **Screenshot:** Add custom domain screen  
_Save screenshot in:_  
`/screenshots/lab02/add-domain.png`

---

## 🧵 Step 3 — Review DNS Verification Details
Azure will display a **TXT record** used to verify ownership.

Take note of:
- **Record type:** TXT  
- **Name / Host:** `@` (or blank, depending on DNS provider)  
- **Value:** A long `MS=` verification string

📸 **Screenshot:** TXT verification record provided by Azure  
_Save screenshot in:_  
`/screenshots/lab02/txt-record-details.png`

---

## 🧵 Step 4 — Add TXT Record to DNS Provider
1. Sign in to your DNS provider  
2. Add a new **TXT record** using the values provided by Azure  
3. Save the record

⚠️ DNS propagation may take several minutes.

📸 **Screenshot:** TXT record added at DNS provider  
_Save screenshot in:_  
`/screenshots/lab02/dns-provider-txt.png`

---

## 🧵 Step 5 — Verify Domain Ownership
1. Return to **Microsoft Entra ID → Custom domain names**  
2. Select your domain: `jsfrancislegacy.com`  
3. Click **Verify**

If the TXT record has propagated, verification will complete successfully.

📸 **Screenshot:** Domain successfully verified  
_Save screenshot in:_  
`/screenshots/lab02/domain-verified.png`

---

## 🧵 Step 6 — (Optional) Set Domain as Primary
After verification:
1. Select the domain  
2. Click **Set as primary**

This makes the custom domain the default for new users.

📸 **Screenshot:** Domain set as primary  
_Save screenshot in:_  
`/screenshots/lab02/set-primary.png`

---

## 🎉 Lab Completed!
You now have:
- A verified custom domain in Microsoft Entra ID
- The ability to create users with branded email addresses
- A more realistic enterprise Azure environment

**Next Lab:**  
➡️ `Lab 03 — Creating Admin Users and Enabling MFA`
