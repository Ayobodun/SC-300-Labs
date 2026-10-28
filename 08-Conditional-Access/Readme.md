# Microsoft Entra ID – Conditional Access Policies

## 📌 Overview

This lab focuses on configuring and evaluating Microsoft Entra Conditional Access policies to strengthen identity security and control how users access organisational resources.

Conditional Access uses signals such as user identity, device state, location, application, and sign-in risk to determine whether access should be granted, blocked, or require additional authentication.

The objective was to understand how Conditional Access policies help implement a Zero Trust security model.

---

## 🎯 Real-World Security Risk

Without properly configured Conditional Access policies, organisations may expose themselves to risks such as:

- Unauthorised access to Microsoft 365 applications.
- Compromised accounts accessing corporate resources.
- Users accessing sensitive resources without multifactor authentication (MFA).
- Inconsistent access controls across users and applications.
- Increased exposure from unmanaged or non-compliant devices.

Conditional Access helps reduce these risks by enforcing access requirements based on defined conditions.

---

## 🛠️ What I Built

In this lab, I explored Conditional Access policy configuration and evaluation in Microsoft Entra ID.

The lab covered:

- Reviewing the Conditional Access dashboard.
- Creating a Conditional Access policy.
- Configuring users and groups within the policy scope.
- Selecting target cloud applications.
- Configuring access controls, including MFA.
- Reviewing policy conditions and grant controls.
- Evaluating the policy using Report-only mode where available.
- Reviewing sign-in logs and policy evaluation results.
- Documenting the policy configuration in `Policy.json`.

---

## 🧪 Environment

- Microsoft Entra ID
- Conditional Access
- Microsoft 365 test environment
- Test user accounts
- Microsoft Entra sign-in logs
- JSON policy documentation

---

## 📸 Step-by-Step Evidence

### 1. Conditional Access Dashboard

Reviewed the Conditional Access area in the Microsoft Entra admin centre to understand the available policies and configuration options.

**Screenshot:** `Screenshot/conditional-access-dashboard.png`

---

### 2. Policy Creation

Created a Conditional Access policy for testing and learning purposes.

The policy was configured to target a designated test user or group rather than applying unrestricted changes to the organisation.

**Screenshot:** `Screenshot/conditional-access-policy-created.png`

---

### 3. User and Group Scope

Configured the users or groups that the policy would apply to.

Careful scoping is important to avoid unintentionally blocking legitimate users from accessing organisational resources.

**Screenshot:** `Screenshot/policy-users-and-groups.png`

---

### 4. Target Resources

Selected the cloud applications that the policy would evaluate.

The applications selected should reflect the purpose of the policy and the test environment being used.

**Screenshot:** `Screenshot/policy-target-resources.png`

---

### 5. Conditions Configuration

Reviewed and configured available policy conditions, such as:

- Sign-in risk, where licensed and available.
- Device platforms.
- Locations.
- Client applications.
- Device filters, where supported.

The conditions determine when the policy should apply.

**Screenshot:** `Screenshot/policy-conditions.png`

---

### 6. Grant Controls

Configured the access requirements for the policy.

For example, a policy can require multifactor authentication before allowing access to a selected application.

The available controls depend on the tenant configuration, licensing, and selected policy conditions.

**Screenshot:** `Screenshot/policy-grant-controls.png`

---

### 7. Report-Only Evaluation

Used Report-only mode where available to evaluate the policy without immediately enforcing its access controls.

This helps administrators understand the potential impact of a policy before enabling enforcement.

**Screenshot:** `Screenshot/policy-report-only-mode.png`

---

### 8. Sign-In Log Validation

Reviewed sign-in logs to investigate how the policy was evaluated during a test sign-in.

Checked the Conditional Access results to understand whether the policy was applied, not applied, or reported a failure.

**Screenshot:** `Screenshot/conditional-access-sign-in-validation.png`

---

## 🔐 Security Validation

The following security considerations were reviewed during the lab:

- Policy scope should be restricted to the intended users and applications.
- Report-only mode should be used for initial evaluation where appropriate.
- Emergency access or break-glass accounts must be handled carefully to reduce the risk of administrative lockout.
- Policy changes should be tested with designated accounts before production enforcement.
- Sign-in logs should be reviewed to confirm how the policy behaves.
- MFA requirements should align with the organisation's security requirements.
- Policies should be monitored and reviewed after implementation.

**Important:** Do not enable an untested policy that could lock out administrators or other users. Use a test environment and follow your organisation's change-management process.

---

## 📁 Policy Documentation

The lab directory includes a `Policy.json` file for documenting the Conditional Access policy.

The file should contain an actual policy export or clearly labelled example configuration.

**File:** `Policy.json`

Policy documentation can help administrators:

- Maintain a record of policy settings.
- Review configuration changes.
- Support troubleshooting and audits.
- Compare configurations between environments.

> Note: Do not include credentials, access tokens, secrets, or other sensitive tenant information in the repository. A manually written JSON example is not the same as an actual policy export.

---

## 🧰 Tools & Services Used

- Microsoft Entra admin centre
- Conditional Access
- Microsoft Entra sign-in logs
- Multifactor authentication (MFA)
- JSON policy documentation

---

## 📈 Outcome

This lab developed my understanding of how Conditional Access policies can strengthen identity security by evaluating sign-in conditions and enforcing appropriate access requirements.

It also reinforced the importance of careful policy scoping, staged testing, sign-in log analysis, and validating security changes before production enforcement.

---

## 🧠 Troubleshooting Notes

### Policy Not Applying

- Confirm that the test user is included in the policy scope.
- Check whether the selected application is covered by the policy.
- Review the configured conditions and exclusions.
- Inspect the Conditional Access details in the sign-in logs.

### Unexpected Sign-In Results

- Check whether another Conditional Access policy is affecting the sign-in.
- Review the policy's Report-only or On status.
- Confirm that the test account meets the configured conditions.
- Review applicable licensing and feature requirements.

### Risk of Administrator Lockout

- Test policies with designated accounts.
- Review exclusions carefully.
- Keep emergency access arrangements in place.
- Avoid enabling broad policies without validating their impact.

---

## 🏁 Lab Result

**Status:** Document the result after completing and validating the lab.

This lab demonstrates practical knowledge of Microsoft Entra Conditional Access, policy scoping, MFA enforcement, Report-only evaluation, and sign-in troubleshooting.
