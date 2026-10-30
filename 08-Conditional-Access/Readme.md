## 📸 Step-by-Step Evidence

### 1. Conditional Access Dashboard

Reviewed the Conditional Access section within Microsoft Entra ID to view existing policies and security controls configured within the tenant.

**Screenshot:** `Screenshot/01-conditional-access-dashboard.png`

---

### 2. Policy Overview

Reviewed the Conditional Access policies configured within the tenant.

The environment included policies designed to enforce multifactor authentication (MFA) and block legacy authentication methods.

**Screenshot:** `Screenshot/02-policy-overview.png`

---

### 3. Require MFA for All Users

Reviewed a Conditional Access policy that requires multifactor authentication before users can access cloud resources.

This helps reduce the risk of unauthorized access through compromised credentials.

**Screenshot:** `Screenshot/03-require-mfa-for-all-users.png`

---

### 4. Require MFA for Admins

Reviewed a Conditional Access policy designed to enforce MFA for privileged administrative accounts.

Administrative accounts are high-value targets and should always be protected with stronger authentication controls.

**Screenshot:** `Screenshot/04-require-mfa-for-admins.png`

---

### 5. Block Legacy Authentication

Reviewed a Conditional Access policy configured to block legacy authentication protocols.

Legacy authentication does not support modern security controls such as MFA and is commonly targeted by password-spray attacks.

**Screenshot:** `Screenshot/05-block-legacy-authentication.png`

---

### 6. User and Group Assignments

Reviewed the users and groups included within the Conditional Access policy scope.

Proper scoping helps ensure the policy applies only to the intended users while reducing the risk of disruptions.

**Screenshot:** `Screenshot/06-policy-users-and-groups.png`

---

### 7. Grant Controls (MFA)

Reviewed the selected grant controls used to enforce multifactor authentication before access is granted.

Grant controls form a key part of Conditional Access security enforcement.

**Screenshot:** `Screenshot/07-grant-controls-mfa.png`

---

### 8. Policy State and Enforcement

Reviewed the policy status and confirmed that the Conditional Access policy was enabled and actively enforcing security controls.

**Screenshot:** `Screenshot/08-policy-state-enabled.png`

---

### 9. Sign-In Log Analysis

Reviewed Microsoft Entra sign-in logs to investigate authentication events and determine how Conditional Access policies were evaluated during sign-in attempts.

**Screenshot:** `Screenshot/09-sign-in-logs.png`

---

### 10. Conditional Access Evaluation Results

Reviewed Conditional Access evaluation results to validate that the applicable policies were triggered and enforced correctly during authentication.

**Screenshot:** `Screenshot/10-conditional-access-evaluation.png`
