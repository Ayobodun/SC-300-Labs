# Microsoft Entra ID – Entitlement Management & Access Packages

## 🧩 Overview

This lab demonstrates how to configure Entitlement Management in Microsoft Entra ID to manage user access to organizational resources through access packages.

Entitlement Management enables organizations to manage the access lifecycle by allowing users to request resources through controlled policies. Access packages can bundle resources such as groups, applications, and SharePoint sites, simplifying access provisioning and governance.

In this lab, an access package catalog is created, resources are added, and an access package and policy are configured to demonstrate how organizations can manage access requests and assignments.

---

# ⚠️ Real-World Risk

Without proper identity governance:

- Users may retain access to resources they no longer need.
- Access requests may be handled manually and inconsistently.
- Employees may receive excessive permissions.
- Onboarding and offboarding can become difficult to manage.
- Organizations may lack visibility into who has access to specific resources.

Microsoft Entra Entitlement Management helps organizations:

✅ Centralize access request management

✅ Apply approval workflows to access requests

✅ Standardize resource provisioning

✅ Manage access assignments and expiration

✅ Improve identity governance and compliance

---

# 🛠 What I Built

- Created an access package catalog
- Added resources to the catalog
- Created an access package
- Configured resources and resource roles
- Created an access policy
- Configured request and approval settings
- Tested the access package configuration
- Validated access assignments

---

# 🏗 Environment

### Microsoft Entra ID Components

- Microsoft Entra Entitlement Management
- Access Package Catalogs
- Access Packages
- Resource Roles
- Access Policies
- Access Requests and Approvals
- User and Group Assignments

### Access Governance

- Request-based access provisioning
- Approval workflows, where configured
- Assignment lifecycle management

---

# 📸 Step-by-Step Evidence

| Step | Action |
|---|---|
| 1 | Create an Access Package Catalog |
| 2 | Add Resources to the Catalog |
| 3 | Create an Access Package |
| 4 | Configure Resources and Roles |
| 5 | Configure the Access Policy |
| 6 | Test the Access Package |
| 7 | Validate the Access Assignment |

---

# 1️⃣ Access Package Catalog Creation

Created an access package catalog within Microsoft Entra Entitlement Management.

The catalog acts as a container for organizing resources that can be included in access packages.

### Result

The catalog provides a central location for managing resources used in the access request and provisioning process.

### Evidence

📸 Screenshot:

Screenshot/catalog-created.png

---

# 2️⃣ Adding Resources to the Catalog

Added supported resources to the access package catalog.

Resources can include groups, enterprise applications, and SharePoint sites, depending on the available configuration and permissions.

### Result

The catalog contains resources that can be selected when creating access packages.

### Evidence

📸 Screenshot:

Screenshot/catalog-resources.png

---

# 3️⃣ Access Package Creation

Created an access package within the catalog.

An access package combines selected resources into a single package that can be assigned to eligible users through an access policy.

### Result

The access package provides a structured way to manage access to organizational resources without configuring each user's access independently.

### Evidence

📸 Screenshot:

Screenshot/access-package-created.png

---

# 4️⃣ Resource and Role Configuration

Configured the resources and associated resource roles within the access package.

Resource roles determine the level of access users receive when the package is assigned.

### Result

The access package is configured to provide the selected resource roles to users who receive the package.

### Evidence

📸 Screenshot:

Screenshot/package-resources-and-roles.png

---

# 5️⃣ Access Policy Configuration

Configured an access policy to define who can request the access package and how requests are handled.

Depending on the requirements, a policy can specify:

- Eligible users or groups
- Approval requirements
- Approvers
- Assignment duration
- Access expiration settings

### Result

The access policy defines the conditions under which eligible users can request and receive access to the resources included in the package.

### Evidence

📸 Screenshot:

Screenshot/access-policy.png

---

# 6️⃣ Access Package Testing

Tested the access package configuration to verify that the package and policy were configured as intended.

### Validation

- Reviewed the resources included in the package.
- Checked the policy's eligible requestors.
- Reviewed approval settings.
- Confirmed that the access package was available for the intended workflow.

### Result

The configuration was reviewed to establish whether the access package was ready for testing through the intended request workflow.

### Evidence

📸 Screenshot:

Screenshot/access-package-testing.png

---

# 7️⃣ Access Assignment Validation

Validated the resulting access assignment after completing a test request or assignment, where available.

### Validation

- Checked the assignment status.
- Reviewed the resources associated with the package.
- Verified the assigned resource roles.
- Confirmed the expected access where testing was possible.

### Result

The assignment demonstrates how Entitlement Management can associate users with approved resources through an access package.

### Evidence

📸 Screenshot:

Screenshot/access-assignment-validation.png

---

# 🔐 Security Validation

The solution supports:

✅ Centralized access package management

✅ Controlled access requests

✅ Approval-based provisioning where configured

✅ Defined resource roles and permissions

✅ Access assignment lifecycle management

✅ Improved visibility into resource assignments

Entitlement Management can help reduce the risk of:

❌ Inconsistent manual access provisioning

❌ Uncontrolled access requests

❌ Excessive resource permissions

❌ Users retaining access beyond their requirements

**Security note:** These benefits depend on the access package, resource roles, policies, and lifecycle settings configured. Creating an access package alone does not guarantee that unauthorized access is prevented.

---

# 🧰 Tools & Services Used

- Microsoft Entra ID
- Microsoft Entra Entitlement Management
- Access Package Catalogs
- Access Packages
- Microsoft Entra Admin Center

---

# 💡 Outcome

This lab demonstrates how Microsoft Entra Entitlement Management can simplify identity governance by grouping resources into access packages and applying policies to control how users request and receive access.

By using access packages, organizations can establish a consistent process for resource provisioning, approval workflows, and assignment management.

This approach supports the principle of least privilege by helping organizations grant users the access they require according to defined policies.

---

# 🧩 Troubleshooting

### Resources Not Appearing in the Catalog

Verify:

- The correct catalog has been selected.
- The resource type is supported.
- The resource is available in the tenant.
- The account has the required permissions.
- The resource has been added to the catalog before configuring the package.

### Users Cannot Request an Access Package

Verify:

- An applicable access policy exists.
- The user meets the policy's requestor requirements.
- The package and policy are configured correctly.
- The user is using the appropriate access request portal.
- The required licensing and permissions are available.

### Access Request Is Not Approved

Verify:

- Whether approval is required by the policy.
- The configured approver settings.
- Whether the request is awaiting approval.
- Whether the approver can access and process the request.

### User Does Not Receive the Expected Access

Verify:

- The access package assignment status.
- The resources included in the package.
- The selected resource roles.
- Whether the request or assignment has completed.
- Whether additional permissions are required on the target resource.

---

# ✅ Lab Result

Configured an access package catalog and explored how Microsoft Entra Entitlement Management can organize resources and manage access through access packages and policies.

The lab demonstrates how access packages can support structured access requests, resource assignments, and identity governance within Microsoft Entra ID.
