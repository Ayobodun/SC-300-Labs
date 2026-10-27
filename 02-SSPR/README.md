# Microsoft Entra ID – Self-Service Password Reset (SSPR)

## 🧩 Overview

This lab demonstrates how to configure and validate Self-Service Password Reset (SSPR) in Microsoft Entra ID.

Self-Service Password Reset enables users to securely reset or unlock their accounts without requiring assistance from the helpdesk. This reduces operational costs, minimizes downtime, and improves the overall user experience.

In this lab, SSPR was configured for cloud users and tested through the Microsoft password reset portal to verify secure account recovery.

---

# ⚠️ Real-World Risk

Without Self-Service Password Reset:

- Users depend on IT support for password resets.
- Password-related tickets increase helpdesk workload.
- Productivity is lost while users wait for assistance.
- Account recovery processes become slower and less efficient.

SSPR helps organizations:

✅ Reduce helpdesk workload

✅ Improve user productivity

✅ Enable secure account recovery

✅ Strengthen identity security

✅ Support Zero Trust principles

---

# 🛠 What I Built

- Enabled Self-Service Password Reset (SSPR)
- Configured password reset settings
- Registered user authentication methods
- Tested password reset functionality
- Validated successful account recovery

---

# 🏗 Environment

### Microsoft Entra ID Components

- Self-Service Password Reset (SSPR)
- Authentication Methods
- Security Information Registration
- Cloud Users

### Authentication Methods Used

- Microsoft Authenticator
- Email Verification
- Mobile Phone Verification

---

# 📸 Step-by-Step Evidence

| Step | Action | Screenshot |
|--------|---------|---------|
| 1 | Enable Self-Service Password Reset | ![SSPR Enabled](Screenshot/enable-sspr.png) |
| 2 | Configure Authentication Methods | ![Authentication Methods](Screenshot/authentication-methods.png) |
| 3 | Register Security Information | ![Security Info](Screenshot/security-info-registration.png) |
| 4 | Start Password Reset Process | ![Password Reset](Screenshot/password-reset-start.png) |
| 5 | Verify Identity | ![Verification](Screenshot/verification-method.png) |
| 6 | Successful Password Reset | ![Success](Screenshot/password-reset-success.png) |

---

# 1️⃣ Enable Self-Service Password Reset

Enabled Self-Service Password Reset within Microsoft Entra ID.

### Configuration

- Self-Service Password Reset: Enabled
- Scope: Selected Users

### Result

Eligible users can reset their passwords without contacting the helpdesk.

### Evidence

📸 Screenshot:

![SSPR Enabled](Screenshot/enable-sspr.png)

---

# 2️⃣ Configure Authentication Methods

Configured authentication methods used during the password reset process.

### Configuration

- Microsoft Authenticator
- Email Verification
- Mobile Phone Verification

### Result

Users are required to verify their identity before resetting their password.

### Evidence

📸 Screenshot:

![Authentication Methods](Screenshot/authentication-methods.png)

---

# 3️⃣ Register Security Information

Registered authentication methods for the test user account.

### Authentication Methods Registered

- Microsoft Authenticator
- Recovery Email
- Mobile Phone

### Result

The user successfully completed security information registration.

### Evidence

📸 Screenshot:

![Security Info](Screenshot/security-info-registration.png)

---

# 4️⃣ Start Password Reset Process

Initiated the password reset process using the Microsoft password reset portal.

### Steps Performed

1. Navigated to the password reset portal.
2. Entered the username.
3. Completed identity verification.

### Result

The password reset process was successfully initiated.

### Evidence

📸 Screenshot:

![Password Reset](Screenshot/password-reset-start.png)

---

# 5️⃣ Identity Verification

Verified user identity using the configured authentication method.

### Verification Method

- Microsoft Authenticator

### Result

Identity validation completed successfully.

### Evidence

📸 Screenshot:

![Verification](Screenshot/verification-method.png)

---

# 6️⃣ Successful Password Reset

Successfully reset the password and validated access using the new credentials.

### Result

✅ Password successfully reset

✅ User account recovered

✅ Sign-in successful using new password

### Evidence

📸 Screenshot:

![Success](Screenshot/password-reset-success.png)

---

# 🔐 Security Validation

The user was able to:

✅ Register authentication methods

✅ Verify identity securely

✅ Reset password without administrator assistance

✅ Regain access to the account

The user could NOT:

❌ Bypass identity verification

❌ Reset passwords without registered authentication methods

---

# 🧰 Tools & Services Used

- Microsoft Entra ID
- Self-Service Password Reset (SSPR)
- Microsoft Authenticator
- Microsoft Entra Admin Center
- Microsoft 365 Admin Center

---

# 💡 Outcome

This lab demonstrates how Self-Service Password Reset can reduce operational overhead while improving security and user productivity.

By enabling secure self-service account recovery, organizations can reduce reliance on helpdesk support and strengthen their identity protection strategy.

---

# 🧩 Troubleshooting

### Unable to access the password reset portal

Verify:

- SSPR is enabled for the user.
- The user is licensed appropriately.
- The account is not blocked.

### User cannot reset password

Verify:

- Security information has been registered.
- The required authentication methods are available.
- Password reset policy applies to the user.

### Authentication method not available

Verify:

- Microsoft Authenticator is registered.
- A mobile phone number is configured.
- Email verification is configured where applicable.

---

# ✅ Lab Result

Successfully configured and tested Self-Service Password Reset (SSPR) in Microsoft Entra ID, enabling secure account recovery while reducing support overhead and improving the user experience.
