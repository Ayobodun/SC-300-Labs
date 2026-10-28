# Microsoft Entra ID – Authentication Methods & Passwordless Authentication

## 📌 Overview

This lab focuses on Microsoft Entra ID authentication methods and how organisations configure secure, user-friendly ways for employees to verify their identities.

Authentication methods are an important part of identity security because they help protect accounts against unauthorised access, phishing, and credential theft.

The objective of this lab is to explore authentication method policies, understand how authentication methods are managed, and investigate how users register and use supported authentication methods.

---

## 🎯 Real-World Security Risk

Poorly managed authentication methods can expose organisations to several security risks, including:

- Compromised accounts due to stolen or reused passwords.
- Users relying on weak authentication methods.
- Inconsistent authentication requirements across the organisation.
- Users being unable to access resources because their authentication methods are not configured correctly.
- Increased exposure to phishing and social engineering attacks.

Microsoft Entra ID provides authentication method management capabilities that help administrators improve identity security and support stronger authentication experiences.

---

## 🛠️ What I Built

In this lab, I explored authentication method management in Microsoft Entra ID.

The lab covered:

- Reviewing the Authentication Methods policy area.
- Exploring available authentication methods.
- Reviewing the Microsoft Authenticator configuration.
- Examining methods such as SMS, voice calls, and FIDO2 security keys where available.
- Reviewing authentication method policy settings.
- Understanding how users register authentication methods.
- Reviewing user authentication method information.
- Understanding the relationship between authentication methods and multifactor authentication (MFA).

---

## 🧪 Environment

- Microsoft Entra ID
- Authentication Methods
- Microsoft Authenticator
- Test user accounts
- Microsoft Entra admin centre

---

## 📸 Step-by-Step Evidence

### 1. Authentication Methods Dashboard

Opened the Authentication Methods area in the Microsoft Entra admin centre and reviewed the available authentication method policies.

**Screenshot:** `Screenshot/authentication-methods-dashboard.png`

---

### 2. Available Authentication Methods

Reviewed the authentication methods available in the tenant.

Depending on the tenant configuration and licensing, these may include:

- Microsoft Authenticator.
- SMS.
- Voice calls.
- FIDO2 security keys and passkeys.
- Temporary Access Pass.
- Certificate-based authentication.
- Other supported authentication methods.

**Screenshot:** `Screenshot/available-authentication-methods.png`

---

### 3. Microsoft Authenticator Configuration

Reviewed the Microsoft Authenticator policy and its configuration options.

Microsoft Authenticator can support multifactor authentication and passwordless sign-in experiences, depending on the configuration.

**Screenshot:** `Screenshot/microsoft-authenticator-policy.png`

---

### 4. Authentication Method Policy

Reviewed how administrators enable or disable supported authentication methods and define which users or groups can use them.

Policy scope should be carefully considered before making changes that affect users.

**Screenshot:** `Screenshot/authentication-method-policy.png`

---

### 5. User Authentication Methods

Opened a designated test user's authentication method information and reviewed the methods registered to the account, where permitted.

This helps administrators understand how authentication methods can be managed and troubleshot for individual users.

**Screenshot:** `Screenshot/user-authentication-methods.png`

---

### 6. Authentication Method Registration

Explored the user registration experience for supported authentication methods.

Users may need to register methods before they can use them for MFA or passwordless authentication.

**Screenshot:** `Screenshot/authentication-method-registration.png`

---

### 7. Temporary Access Pass

Reviewed Temporary Access Pass (TAP), where available.

A Temporary Access Pass is a time-limited passcode that can help users register authentication methods or recover access in supported scenarios.

Its configuration and use should follow the organisation's identity security requirements.

**Screenshot:** `Screenshot/temporary-access-pass.png`

---

### 8. Authentication Validation

Tested the authentication experience using a designated test account, where possible, and reviewed the outcome.

The purpose was to understand how the configured authentication methods affect sign-in and how administrators can investigate authentication issues.

**Screenshot:** `Screenshot/authentication-validation.png`

---

## 🔐 Security Validation

The following security considerations were reviewed during the lab:

- Enable authentication methods according to organisational security requirements.
- Restrict policy scope to the appropriate users and groups.
- Prefer phishing-resistant authentication methods where appropriate and supported.
- Ensure users have suitable authentication and recovery options.
- Apply appropriate controls when creating and managing Temporary Access Passes.
- Review authentication failures when troubleshooting user access.
- Test policy changes with designated accounts before wider deployment.
- Avoid disabling authentication methods that users depend on without providing a safe alternative.

---

## 🧰 Tools & Services Used

- Microsoft Entra admin centre
- Authentication Methods
- Microsoft Authenticator
- Temporary Access Pass
- Microsoft Entra user management

---

## 📈 Outcome

This lab developed my understanding of authentication method management in Microsoft Entra ID and how administrators can support secure user authentication.

It also reinforced the importance of managing authentication method policies, reviewing user registration, and testing authentication changes before implementing them across an organisation.

---

## 🧠 Troubleshooting Notes

### Authentication Method Not Available

- Confirm that the authentication method is supported by the tenant.
- Check whether the method is enabled in the relevant policy.
- Review whether the user or group is included in the policy scope.
- Check licensing and feature requirements where applicable.

### User Cannot Register an Authentication Method

- Confirm that the method is enabled for the user.
- Review the user's registration experience and any applicable registration requirements.
- Check whether existing authentication requirements are affecting registration.
- Review available sign-in and authentication troubleshooting information.

### Temporary Access Pass Issues

- Confirm that Temporary Access Pass is enabled and configured.
- Check the pass's validity period and usage restrictions.
- Verify that the test account is eligible to use it.
- Never publish active passcodes or authentication secrets in a public repository.

---

## 🏁 Lab Result

**Status:** Document the result after completing and validating the lab.

This lab demonstrates practical knowledge of Microsoft Entra authentication methods, authentication policy management, user registration, and authentication troubleshooting.
