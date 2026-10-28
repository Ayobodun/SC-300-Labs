# Microsoft Entra ID – Guest Identities & External Collaboration

## 📌 Overview

This lab focuses on managing guest identities and external collaboration in Microsoft Entra ID.

Microsoft Entra B2B collaboration allows organisations to work securely with external users, such as contractors, suppliers, business partners, and consultants, by granting them access to selected organisational resources.

The objective of this lab was to understand how guest users are invited, managed, and governed while maintaining appropriate security controls over external access.

---

## 🎯 Real-World Security Risk

Poorly managed guest identities can introduce security risks, including:

- External users retaining access after a project or contract ends.
- Guest accounts having excessive permissions.
- Unauthorised external collaboration.
- Sensitive organisational information being shared with unintended users.
- Limited visibility into guest account activity.
- Inactive guest accounts remaining in the directory indefinitely.

Microsoft Entra ID provides controls that help organisations manage external identities and restrict access to appropriate resources.

---

## 🛠️ What I Built

In this lab, I explored guest identity management and external collaboration in Microsoft Entra ID.

The lab covered:

- Reviewing guest users in the Microsoft Entra admin centre.
- Exploring external collaboration settings.
- Understanding Microsoft Entra B2B collaboration.
- Creating or inviting a test guest user where permitted.
- Reviewing guest user properties.
- Exploring how guest users can be assigned to groups.
- Reviewing external user access and permissions.
- Understanding guest invitation restrictions.
- Exploring access reviews for guest users where available.
- Reviewing guest account lifecycle and access removal considerations.

---

## 🧪 Environment

- Microsoft Entra ID
- External identities
- Microsoft Entra B2B collaboration
- Test guest account
- Microsoft Entra groups
- Microsoft Entra admin centre

---

## 📸 Step-by-Step Evidence

### 1. Guest Users Dashboard

Opened the Users area in the Microsoft Entra admin centre and reviewed the directory's guest accounts.

Reviewed how guest users are identified and managed separately from member users.

**Screenshot:** `Screenshot/guest-users-dashboard.png`

---

### 2. External Collaboration Settings

Reviewed the external collaboration settings in Microsoft Entra ID.

These settings help administrators control aspects of external user invitations and collaboration.

Depending on the tenant configuration, options may include:

- Who can invite guest users.
- Restrictions on guest invitations.
- Collaboration with external organisations.
- Controls relating to external user access.

**Screenshot:** `Screenshot/external-collaboration-settings.png`

---

### 3. Guest User Invitation

Created or invited a designated test guest user where permitted.

Reviewed the invitation process and the information required to invite an external identity.

**Screenshot:** `Screenshot/guest-user-invitation.png`

---

### 4. Guest User Properties

Opened the test guest account and reviewed its directory properties.

Examined how the account is represented in the directory and how administrators can identify its guest user type.

**Screenshot:** `Screenshot/guest-user-properties.png`

---

### 5. Guest Group Membership

Reviewed how a guest user can be added to an appropriate group.

Group membership can help control access to applications and resources, so external users should only receive the permissions required for their responsibilities.

**Screenshot:** `Screenshot/guest-group-membership.png`

---

### 6. Guest Access Permissions

Reviewed the permissions and access considerations applicable to guest users.

The goal was to understand how organisations can limit external access to the resources required for collaboration.

**Screenshot:** `Screenshot/guest-access-permissions.png`

---

### 7. Guest Access Review

Explored access reviews for guest users where the required features and licensing were available.

Access reviews help organisations periodically determine whether external users should retain access to selected resources.

**Screenshot:** `Screenshot/guest-access-review.png`

---

### 8. Guest Account Lifecycle

Reviewed the lifecycle considerations for external identities, including when access should be reviewed or removed.

For example, a guest account may need to be disabled or removed when a contractor's engagement ends.

**Screenshot:** `Screenshot/guest-account-lifecycle.png`

---

## 🔐 Security Validation

The following security considerations were reviewed during the lab:

- Restrict guest invitations to authorised users where appropriate.
- Grant guest users only the permissions required for their work.
- Review external collaboration settings regularly.
- Monitor guest account activity where appropriate.
- Use access reviews to evaluate whether guest access remains necessary.
- Remove or disable guest access when the business requirement ends.
- Review group memberships and application permissions.
- Apply appropriate controls before sharing sensitive organisational resources.
- Avoid granting guest users unnecessary directory roles.
- Test configuration changes before applying them broadly.

---

## 🧰 Tools & Services Used

- Microsoft Entra admin centre
- Microsoft Entra External Identities
- Microsoft Entra B2B collaboration
- Microsoft Entra users and groups
- Access reviews
- External collaboration settings

---

## 📈 Outcome

This lab developed my understanding of guest identity management and external collaboration in Microsoft Entra ID.

It reinforced the importance of restricting guest invitations, applying least privilege, reviewing external access, and managing guest accounts throughout their lifecycle.

---

## 🧠 Troubleshooting Notes

### Unable to Invite a Guest User

- Confirm that the signed-in administrator has the necessary permissions.
- Review the external collaboration settings.
- Check whether guest invitations are restricted.
- Verify that the invitation process is supported by the tenant configuration.

### Guest User Cannot Access a Resource

- Confirm that the guest invitation has been accepted where required.
- Check the guest user's group memberships.
- Review the permissions assigned to the resource.
- Check any applicable Conditional Access policies.
- Review sign-in logs for additional information.

### Guest User Has Excessive Access

- Review group memberships and assigned permissions.
- Check for unnecessary directory role assignments.
- Remove permissions that are no longer required, following the appropriate approval process.
- Confirm that the changes have taken effect.

### Guest Account Is No Longer Required

- Confirm that the guest's business engagement has ended.
- Review access to applications, groups, and resources.
- Disable or remove access in accordance with organisational procedures.
- Retain any records required by organisational policy.

---

## 🏁 Lab Result

**Status:** Document the result after completing and validating the lab.

This lab demonstrates practical knowledge of Microsoft Entra guest identities, B2B collaboration, external collaboration settings, guest access management, and external identity governance.
