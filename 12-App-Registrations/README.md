# Microsoft Entra ID – App Registrations & Application Permissions

## 📌 Overview

This lab explores application identity management in Microsoft Entra ID, focusing on app registrations, Microsoft Graph API permissions, permission consent, and enterprise applications.

App registrations allow applications to integrate with Microsoft Entra ID for authentication and access to protected resources.

The objective of this lab was to understand how applications are registered, how API permissions are managed, and how administrators can evaluate the security risks associated with application access.

---

## 🎯 Real-World Security Risk

Poorly managed application registrations can introduce significant security risks, including:

- Applications receiving excessive permissions.
- Unauthorised access to organisational data.
- Exposed application credentials.
- Applications retaining permissions that are no longer required.
- Unintended consent to application permissions.
- Limited visibility into application identities and their access.

Microsoft Entra ID provides controls for managing application identities, API permissions, consent, and credentials.

---

## 🛠️ What I Explored

In this lab, I explored application identity management in Microsoft Entra ID.

The lab covered:

- Reviewing the App registrations dashboard.
- Registering and reviewing a test application.
- Understanding application and tenant identifiers.
- Reviewing Microsoft Graph API permissions.
- Understanding delegated and application permissions.
- Exploring the admin consent process.
- Reviewing the relationship between app registrations and enterprise applications.
- Understanding application access and least-privilege principles.

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

Opened the App registrations section in the Microsoft Entra admin centre and reviewed the available application management options.

This area allows administrators to register applications, review existing registrations, and manage application configurations.

**Screenshot:**

![App Registrations Dashboard](./Screenshot/app-registration-overview.png)

---

### 2. Test Application Registration

Created a test application registration in Microsoft Entra ID.

Application registration establishes an application's identity in the tenant and provides a starting point for configuring authentication and API access.

The registration process includes selecting an application name and supported account types.

**Screenshot:**

![App Registration Created](./Screenshot/app-registration-created.png)

---

### 3. Application Overview

Opened the application's Overview page and reviewed its identifying information.

Application registrations can include identifiers such as:

- **Application (client) ID:** Identifies the application.
- **Directory (tenant) ID:** Identifies the Microsoft Entra tenant.
- **Object ID:** Identifies the application's registration object within the tenant.

These identifiers serve different purposes and should not be treated as interchangeable.

**Screenshot:**

![App Registration Overview](./Screenshot/app-registration-overview.png)

---

### 4. Microsoft Graph API Permissions

Reviewed the API permissions configured for the application.

Microsoft Graph provides APIs that applications can use to interact with Microsoft 365 and Microsoft Entra resources, subject to the permissions granted.

The test application included the delegated `User.Read` permission, which allows an application to read the signed-in user's profile information within the permission's scope.

Reviewing configured permissions helps administrators understand what an application is requesting and whether those permissions are appropriate.

**Screenshot:**

![App API Permissions](./Screenshot/app-api-permissions.png)

---

### 5. Delegated vs Application Permissions

Explored the distinction between delegated permissions and application permissions in Microsoft Graph.

**Delegated permissions**

Delegated permissions allow an application to access resources on behalf of a signed-in user. Access is subject to the granted permissions and the user's own access.

**Application permissions**

Application permissions allow an application to access supported resources using its own identity, without a signed-in user. These permissions are commonly used by background services and automated applications.

Application permissions can provide broader access to organisational data and may require administrator consent.

Understanding this distinction helps administrators select an appropriate permission model for each application's purpose.

**Screenshot:**

![Delegated and Application Permissions](./Screenshot/delegated-vs-application-permissions.png)

---

### 6. Admin Consent

Reviewed the admin consent controls available on the application's API permissions page.

Microsoft Entra ID uses consent to determine whether an application can use its requested API permissions. Depending on the permission and tenant configuration, consent may be granted by a user or require an administrator.

Before granting admin consent, administrators should:

- Confirm that the application has a legitimate business purpose.
- Review each requested permission.
- Verify that the permissions are necessary.
- Consider the potential impact of granting access.
- Follow organisational approval procedures.

The presence of an admin consent control does not mean that consent has been granted. The consent status should be checked separately.

**Screenshot:**

![App Admin Consent](./Screenshot/app-admin-consent.png)

---

### 7. Enterprise Application Overview

Reviewed the corresponding enterprise application where available.

An app registration defines the application's configuration in its home tenant. The associated service principal represents the application's identity in a particular tenant and supports tenant-specific access and consent management.

Enterprise applications provide administrators with a place to review application-related settings and manage aspects of access within the tenant.

Understanding the relationship between app registrations and enterprise applications is important when investigating application access and permissions.

**Screenshot:**

![Enterprise Application Overview](./Screenshot/enterprise-application-overview.png)

---

## 🔐 Security Considerations

Key security considerations for application identity management include:

- Apply the principle of least privilege to API permissions.
- Understand whether delegated or application permissions are appropriate.
- Review permissions before granting admin consent.
- Avoid granting broad application permissions without a clear business requirement.
- Protect client secrets and certificate private keys.
- Rotate credentials according to organisational requirements.
- Configure appropriate redirect URIs when application authentication requires them.
- Review application owners and remove unnecessary access.
- Periodically review application permissions and credentials.
- Monitor application sign-ins and audit events where available.
- Never store secrets, access tokens, or private keys in a public GitHub repository.

This lab focuses on app registrations, permissions, consent, and enterprise applications. Authentication settings and credential configuration are additional areas that can be explored in a future lab.

---

## 🧰 Tools & Services Used

- Microsoft Entra admin centre
- Microsoft Entra app registrations
- Microsoft Entra enterprise applications
- Microsoft Graph API permissions
- Microsoft Entra permission consent controls

---

## 📈 Key Learnings

This lab developed my understanding of:

- How application registrations establish application identities in Microsoft Entra ID.
- The purpose of application, tenant, and object identifiers.
- How Microsoft Graph API permissions control application access.
- The differences between delegated and application permissions.
- How admin consent affects an application's ability to use permissions.
- The relationship between app registrations and enterprise applications.
- Why least privilege and careful permission reviews are important for application security.

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

### Application Access Issues

- Confirm that the correct application and tenant are being used.
- Review the configured API permissions.
- Check whether the necessary consent has been granted.
- Review application sign-in logs and available error messages.

---

## 🏁 Lab Result

This lab documents my exploration of Microsoft Entra application identity management, including app registrations, Microsoft Graph API permissions, delegated and application permissions, admin consent controls, and enterprise applications.

It reinforced the importance of understanding application permissions, evaluating consent requests, and applying least-privilege principles when managing application access.

The lab forms part of my Microsoft Entra ID identity and access management portfolio.

---
