# Microsoft Entra ID – Dynamic Groups

## 🧩 Overview

This lab demonstrates how to implement Dynamic Groups in Microsoft Entra ID.

Dynamic Groups automatically manage group memberships based on user or device attributes, reducing the need for manual administration.

In this lab, I configured a Dynamic Security Group using a membership rule based on the user's country attribute. The rule identifies users whose country is set to Singapore and automatically manages their group membership.

This lab covers group creation, membership rule configuration, rule validation, membership verification, and the impact of changes to user attributes.

---

## ⚠️ Real-World Risk

Without Dynamic Groups:

- User onboarding requires manual group assignments.
- Users may retain inappropriate or outdated group memberships.
- Administrative overhead increases.
- Group membership becomes harder to maintain.
- Inconsistent group assignments can lead to access management issues.

Dynamic Groups help organisations:

- ✅ Automate group membership management.
- ✅ Reduce administrative workload.
- ✅ Improve consistency in access assignment.
- ✅ Support identity lifecycle management.
- ✅ Reduce errors caused by manual administration.

**Security consideration:** Dynamic Groups automate membership, but they do not grant access permissions by themselves. Access must be assigned separately where required.

---

## 🛠 What I Built

- Created a Dynamic Security Group.
- Configured a dynamic membership rule.
- Used the `Country` attribute to determine group membership.
- Validated the membership rule.
- Verified automatic group membership.
- Tested membership changes following user attribute updates.
- Documented the configuration using JSON.
- Structured the lab for CSV exports, validation evidence, and PowerShell automation.

---

## 🏗 Environment

### Microsoft Entra ID Components

- Microsoft Entra ID
- Dynamic Groups
- Dynamic Membership Rules
- User Attributes
- Security Groups

### Group Configuration

| Setting | Value |
|---|---|
| Group Type | Security |
| Membership Type | Dynamic User |
| Membership Attribute | Country |
| Operator | Equals |
| Attribute Value | Singapore |

### Example Test Users

- User1Sin
- User2Sin
- HrSin

These test accounts represent users whose country attribute is configured to match the membership rule.

---

## 📸 Step-by-Step Evidence

The following screenshots document the group creation, configuration, and validation process.

### 1. Dynamic Groups Dashboard

This screenshot shows the Dynamic Groups area in Microsoft Entra ID.

![Dynamic Groups Dashboard](./Screenshot/dynamic-groups-dashboard.png)

### 2. Dynamic Security Group Created

This screenshot documents the creation of the Dynamic Security Group.

![Dynamic Security Group Created](./Screenshot/dynamic-group-created.png)

### 3. Dynamic Membership Rule

This screenshot shows the membership rule configured for the group.

Example rule:

`(user.country -eq "Singapore")`

![Dynamic Membership Rule](./Screenshot/dynamic-membership-rule.png)

### 4. Dynamic Rule Validation

This screenshot documents the membership rule validation process.

![Dynamic Rule Validation](./Screenshot/dynamic-rule-validation.png)

### 5. Dynamic Group Members

This screenshot shows the group membership results after Microsoft Entra ID evaluates the configured rule.

![Dynamic Group Members](./Screenshot/dynamic-group-members.png)

---

## ⚙️ Membership Rule Configuration

The membership rule used in this lab is:

`(user.country -eq "Singapore")`

### How It Works

- `user.country` identifies the user's country attribute.
- `-eq` checks whether the attribute equals the specified value.
- `"Singapore"` is the value users must match to satisfy the rule.

Microsoft Entra ID evaluates the rule and updates group membership according to the users' attributes.

Users who match the rule become eligible for membership. Users who no longer match can be removed after dynamic membership processing completes.

### Configuration Evidence

The configuration is documented in:

`Evidence/Configuration/dynamic-membership-rule.json`

This file records the intended group configuration and membership rule for documentation and reference.

---

## 📊 Evidence and Exports

The lab uses a structured evidence layout to separate screenshots, exported data, configuration documentation, validation results, and automation scripts.

### CSV Exports

The `Evidence/Exports/` directory is intended to contain the following files:

**`dynamic-groups.csv`**

Contains exported information about dynamic groups, including:

- Group ID
- Display Name
- Description
- Group Type
- Security Enabled
- Membership Rule
- Membership Rule Processing State

**`dynamic-group-members.csv`**

Contains exported group membership information, including:

- Group ID
- Group Name
- User ID
- Display Name
- User Principal Name
- Email Address

These files should contain actual data exported from the test environment.

### Configuration

Location:

`Evidence/Configuration/dynamic-membership-rule.json`

Documents the dynamic group's configuration and membership rule.

### Validation

Location:

`Evidence/Validation/validation-results.md`

The validation report should document:

- The membership rule tested.
- The test users evaluated.
- Expected membership.
- Actual membership.
- Any discrepancies identified.
- The final validation result.

### PowerShell Automation

Location:

`Scripts/Export-DynamicGroups.ps1`

This script is intended to export dynamic group configuration and membership data using Microsoft Graph PowerShell.

The script must be implemented and tested before it can generate the CSV exports.

---

## 🔐 Security Validation

The lab focuses on the following checks:

- ✅ Dynamic membership rule configured using the country attribute.
- ✅ Membership rule syntax validated.
- ✅ Eligible users checked against the rule.
- ✅ Group membership reviewed.
- ✅ Attribute changes considered during membership testing.

Dynamic membership processing may take time. Changes to user attributes do not necessarily result in immediate membership updates.

The final validation status should reflect the results observed in the test environment.

---

## 🧰 Tools & Services Used

- Microsoft Entra ID
- Microsoft Entra Admin Center
- Dynamic Security Groups
- Dynamic Membership Rules
- PowerShell
- Microsoft Graph PowerShell
- CSV
- JSON
- GitHub

---

## 💡 Outcome

This lab demonstrates how Dynamic Groups can simplify identity administration by automatically managing group membership according to user attributes.

Using attribute-based membership rules can reduce manual administration, improve consistency, and support scalable identity management.

The lab also establishes a foundation for exporting identity data, documenting configurations, and automating administrative tasks with PowerShell.

---

## 🧩 Troubleshooting

### User Not Added to Group

Verify:

- The user's country attribute matches the membership rule.
- The membership rule is configured correctly.
- Dynamic membership processing has completed.
- The user satisfies the rule's conditions.

### Membership Rule Error

Verify:

- The rule syntax is correct.
- Supported attributes and operators are used.
- Quotation marks and parentheses are correct.
- The membership rule validation feature reports no errors.

### Group Membership Not Updating

Verify:

- Dynamic membership processing has completed.
- The user's attributes have been updated correctly.
- The group is configured for dynamic user membership.
- The user still satisfies the membership rule.

### CSV Export Fails

Verify:

- Microsoft Graph PowerShell is installed.
- Authentication succeeds.
- The account has the required permissions.
- The required Microsoft Graph consent has been granted.

---

## 📁 Repository Structure

```text
03-Dynamic-Groups/
├── README.md
├── Screenshot/
│   ├── dynamic-groups-dashboard.png
│   ├── dynamic-group-created.png
│   ├── dynamic-membership-rule.png
│   ├── dynamic-rule-validation.png
│   └── dynamic-group-members.png
├── Evidence/
│   ├── Exports/
│   │   ├── dynamic-groups.csv
│   │   └── dynamic-group-members.csv
│   ├── Configuration/
│   │   └── dynamic-membership-rule.json
│   └── Validation/
│       └── validation-results.md
└── Scripts/
    └── Export-DynamicGroups.ps1
```

---

## ✅ Lab Result

Implemented and documented a Dynamic Security Group configuration in Microsoft Entra ID using a country-based membership rule.

The lab demonstrates how attribute-based membership rules can automate group membership management and reduce reliance on manual administration.

Screenshots, configuration documentation, CSV exports, validation results, and PowerShell automation provide supporting evidence as each artefact is created and verified.
