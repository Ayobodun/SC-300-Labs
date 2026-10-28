# Microsoft Entra ID – Privileged Identity Management (PIM)

## 📌 Overview

This lab focuses on Microsoft Entra Privileged Identity Management (PIM), a service that helps organisations manage, control, and monitor privileged access to important resources.

PIM enables administrators to manage privileged role assignments using eligible and active assignments, time-bound access, approval requirements, and activation controls where supported.

The objective of this lab was to understand how PIM reduces standing administrative privileges and supports the principle of least privilege.

---

## 🎯 Real-World Security Risk

Permanent administrative access can expose organisations to significant security risks, including:

- Unauthorised changes to identity and access configurations.
- Privilege escalation following an account compromise.
- Excessive administrative permissions.
- Limited visibility into privileged role activation.
- Increased risk from unused or unnecessary administrator accounts.

PIM helps reduce these risks by allowing organisations to control when privileged access is granted and monitor how administrative roles are used.

---

## 🛠️ What I Built

In this lab, I explored privileged role management in Microsoft Entra ID.

The lab covered:

- Reviewing the PIM dashboard.
- Exploring Microsoft Entra roles.
- Understanding eligible versus active role assignments.
- Reviewing role assignment settings.
- Configuring or examining activation requirements where available.
- Exploring multifactor authentication requirements for role activation.
- Reviewing approval and justification settings where supported.
- Activating an eligible role using a designated test account, where available.
- Reviewing role activation history and audit information.

---

## 🧪 Environment

- Microsoft Entra ID
- Privileged Identity Management (PIM)
- Microsoft Entra roles
- Designated test administrator account
- Microsoft Entra audit logs

---

## 📸 Step-by-Step Evidence

### 1. PIM Dashboard

Opened the Privileged Identity Management area in the Microsoft Entra admin centre and reviewed the available management options.

**Screenshot:** `Screenshot/pim-dashboard.png`

---

### 2. Microsoft Entra Roles

Opened the Microsoft Entra roles area in PIM and reviewed the available directory roles.

The roles available for assignment depend on the tenant configuration and the permissions of the administrator performing the task.

**Screenshot:** `Screenshot/pim-entra-roles.png`

---

### 3. Eligible Role Assignment

Reviewed eligible role assignments and explored how a user can be assigned a role that they activate only when required.

Eligible assignments help reduce unnecessary standing administrative access.

**Screenshot:** `Screenshot/eligible-role-assignment.png`

---

### 4. Active Role Assignment

Reviewed active role assignments and compared them with eligible assignments.

An active assignment provides the role's privileges while the assignment is active, subject to the role and applicable access controls.

**Screenshot:** `Screenshot/active-role-assignment.png`

---

### 5. Role Activation Settings

Reviewed the activation settings available for a selected role.

Depending on the configuration and supported features, activation requirements may include:

- Multifactor authentication.
- Providing a justification.
- Entering a ticket or change-request reference.
- Obtaining approval.
- Limiting the activation duration.

**Screenshot:** `Screenshot/role-activation-settings.png`

---

### 6. Role Activation

Used a designated test account to activate an eligible role, where permitted.

Reviewed the activation process and the requirements presented before the role became active.

**Screenshot:** `Screenshot/role-activation.png`

---

### 7. Role Assignment Validation

Reviewed the role assignment after activation to determine whether the expected status and duration were displayed.

The validation process helps confirm that the assignment behaves as intended.

**Screenshot:** `Screenshot/role-assignment-validation.png`

---

### 8. Audit and Activation History

Reviewed available PIM history and audit information to understand how privileged role assignments and activation events can be investigated.

Audit information can help administrators investigate unexpected privileged access and support security reviews.

**Screenshot:** `Screenshot/pim-audit-history.png`

---

## 🔐 Security Validation

The following security considerations were reviewed during the lab:

- Use eligible assignments instead of permanent active assignments where appropriate.
- Apply the principle of least privilege.
- Require MFA for privileged role activation where supported and appropriate.
- Configure approval and justification requirements according to organisational risk.
- Use time-limited role assignments and activation durations where possible.
- Review privileged role assignments regularly.
- Monitor activation history and audit events.
- Avoid making unnecessary permanent assignments to highly privileged roles.
- Use designated test accounts and follow change-management procedures.

**Important:** Do not assign highly privileged roles to ordinary accounts or change production role settings without authorisation. Use a controlled test environment and the minimum permissions necessary.

---

## 🧰 Tools & Services Used

- Microsoft Entra admin centre
- Privileged Identity Management (PIM)
- Microsoft Entra directory roles
- Microsoft Entra audit logs
- Multifactor authentication (MFA)

---

## 📈 Outcome

This lab developed my understanding of privileged identity management and how Microsoft Entra PIM can reduce standing administrative privileges.

It also reinforced the importance of eligible role assignments, just-in-time access, activation requirements, time-bound privileges, and audit monitoring.

---

## 🧠 Troubleshooting Notes

### PIM Is Not Available

- Check whether the tenant has the required licensing.
- Confirm that the signed-in administrator has sufficient permissions.
- Verify that the correct Microsoft Entra tenant is selected.
- Review the available PIM options in the admin centre.

### Unable to Assign a Role

- Confirm that the administrator has the necessary permissions.
- Check the role assignment requirements.
- Verify that the target user or group is eligible for the assignment.
- Review applicable licensing and tenant restrictions.

### Unable to Activate an Eligible Role

- Confirm that an eligible assignment exists.
- Check whether MFA, justification, approval, or other activation requirements must be satisfied.
- Review the assignment's validity period.
- Check whether the assignment has expired or the activation request was denied.

### Role Activation Does Not Appear as Expected

- Refresh the role assignment view.
- Confirm that activation completed successfully.
- Review PIM history and available audit information.
- Verify that the expected role and account were used.

---

## 🏁 Lab Result

**Status:** Document the result after completing and validating the lab.

This lab demonstrates practical knowledge of Microsoft Entra Privileged Identity Management, eligible and active role assignments, privileged role activation, and administrative access governance.
