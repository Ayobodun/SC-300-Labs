# Microsoft Entra ID – App Registrations & Application Permissions

## 📌 Overview

This lab focuses on application identity management in Microsoft Entra ID, including app registrations, enterprise applications, API permissions, and application authentication.

App registrations allow developers and administrators to integrate applications with Microsoft Entra ID for authentication and access to protected resources.

The objective of this lab was to understand how applications are registered, how permissions are configured, and how administrators can reduce security risks associated with application access.

---

## 🎯 Real-World Security Risk

Poorly managed application registrations can introduce significant security risks, including:

- Applications receiving excessive permissions.
- Unauthorised access to organisational data.
- Exposed client secrets or application credentials.
- Applications retaining permissions that are no longer required.
- Unintended tenant-wide consent to application permissions.
- Limited visibility into application identities and their access.

Microsoft Entra ID provides controls for managing application identities, API permissions, consent, and credentials.

---

## 🛠️ What I Built

In this lab, I explored application identity management in Microsoft Entra ID.

The lab covered:

- Reviewing the App registrations dashboard.
- Creating a test app registration where permitted.
- Configuring application name and supported account types.
- Understanding application (client) IDs and tenant IDs.
- Reviewing the relationship between app registrations and enterprise applications.
- Exploring Microsoft Graph API permissions.
- Understanding delegated versus application permissions.
- Reviewing admin consent requirements.
- Exploring client secrets and certificate credentials.
- Reviewing authentication and redirect URI configuration.
- Understanding least-privilege application access.

---

## 🧪 Environment

- Microsoft Entra ID
- App registrations
- Enterprise applications
- Microsoft Graph API permissions
- Microsoft Entra admin centre
- Test application registration

---

## 📸 Step-by-Step Evidence

### 1. App Registrations Dashboard

Opened the App registrations area in the Microsoft Entra admin centre and reviewed the available application management options.

**Screenshot:** `Screenshot/app-registrations-dashboard.png`

---

### 2. Create an App Registration

Created a test application registration where permitted.

Configured the application name and reviewed the supported account types available for the registration.

**Screenshot:** `Screenshot/app-registration-created.png`

---

### 3. Application Overview

Opened the application overview and reviewed its key identifiers.

These may include:

- Application (client) ID.
- Directory (tenant) ID.
- Object ID.

These identifiers serve different purposes and should not be treated as interchangeable.

**Screenshot:** `Screenshot/app-registration-overview.png`

---

### 4. Authentication Configuration

Reviewed the Authentication section of the app registration.

Explored the supported authentication configuration options, including redirect URIs where applicable.

Redirect URIs must be configured carefully because they determine where authentication responses can be sent.

**Screenshot:** `Screenshot/app-authentication-settings.png`

---

### 5. API Permissions

Opened the API permissions section and reviewed how an application requests access to APIs such as Microsoft Graph.

Explored the permissions available for the test application.

**Screenshot:** `Screenshot/app-api-permissions.png`

---

### 6. Delegated vs Application Permissions

Reviewed the difference between delegated permissions and application permissions.

**Delegated permissions:**
Allow an application to access resources on behalf of a signed-in user, subject to the granted permissions and the user's access.

**Application permissions:**
Allow an application to access resources as its own identity, without a signed-in user, subject to the permissions granted.

Application permissions can provide broad access, so they require careful review and appropriate administrative consent.

**Screenshot:** `Screenshot/delegated-vs-application-permissions.png`

---

### 7. Admin Consent

Reviewed the admin consent process and the implications of granting permissions to an application.

Where permitted, examined the consent status of the test application's requested API permissions.

Admin consent should only be granted after confirming that the permissions are necessary and appropriately scoped.

**Screenshot:** `Screenshot/app-admin-consent.png`

---

### 8. Certificates & Secrets

Reviewed the Certificates & secrets section of the app registration.

Explored how applications can authenticate using credentials such as client secrets or certificates.

Client secrets should be protected, rotated when necessary, and never committed to a public repository.

Where supported, certificate-based authentication can provide an alternative to client secrets.

**Screenshot:** `Screenshot/app-certificates-and-secrets.png`

---

### 9. Enterprise Application / Service Principal

Reviewed the corresponding enterprise application where available.

An app registration defines the application's configuration in its home tenant, while the service principal represents the application's identity in a particular tenant.

Explored how administrators can review the enterprise application's properties and access-related settings.

**Screenshot:** `Screenshot/enterprise-application-overview.png`

---

## 🔐 Security Validation

The following security considerations were reviewed during the lab:

- Apply the principle of least privilege to API permissions.
- Understand whether delegated or application permissions are appropriate.
- Review permissions before granting admin consent.
- Avoid granting broad application permissions without a clear business requirement.
- Protect client secrets and certificate private keys.
- Rotate credentials according to organisational requirements.
- Use appropriate redirect URIs.
- Review application owners and remove unnecessary access.
- Periodically review application permissions and credentials.
- Monitor application sign-ins and audit events where available.
- Avoid storing secrets, tokens, or private keys in GitHub repositories.

**Important:** Use a test application and an authorised tenant. Do not grant tenant-wide consent or create production credentials unless you are authorised and understand the impact.

---

## 🧰 Tools & Services Used

- Microsoft Entra admin centre
- App registrations
- Enterprise applications
- Microsoft Graph API permissions
- Application authentication settings
- Certificates & secrets
- Microsoft Entra audit logs

---

## 📈 Outcome

This lab developed my understanding of application identity management in Microsoft Entra ID.

It reinforced the differences between app registrations and enterprise applications, delegated and application permissions, and the security implications of granting API access.

It also highlighted the importance of least privilege, secure credential management, and careful review of administrative consent.

---

## 🧠 Troubleshooting Notes

### Unable to Create an App Registration

- Confirm that the signed-in account has the necessary permissions.
- Review whether users are allowed to register applications in the tenant.
- Check the organisation's application management policies.

### API Permission Is Not Available

- Confirm that the correct API has been selected.
- Review the permission type being requested.
- Check whether the application and tenant support the requested permission.
- Verify any relevant licensing or administrative requirements.

### Unable to Grant Admin Consent

- Confirm that the signed-in administrator has the necessary permissions.
- Review the API permissions requested by the application.
- Check whether organisational policies restrict consent.
- Ensure that the requested permissions are justified before proceeding.

### Application Authentication Fails

- Confirm that the tenant ID and application client ID are correct.
- Review the authentication configuration and redirect URIs.
- Check that the required permissions have been granted.
- Verify that credentials are valid and have not expired.
- Review available sign-in logs and application error messages.

---

## 🏁 Lab Result

**Status:** Document the result after completing and validating the lab.

This lab demonstrates practical knowledge of Microsoft Entra app registrations, enterprise applications, API permissions, application authentication, and application security governance.
