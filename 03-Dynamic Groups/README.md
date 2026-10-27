# Microsoft Entra ID – Dynamic Groups

## 🧩 Overview

This lab demonstrates how to implement Dynamic Groups in Microsoft Entra ID.

Dynamic Groups automatically manage group memberships based on user or device attributes, eliminating the need for manual administration.

In this lab, users were automatically assigned to groups based on configured membership rules, demonstrating automated identity and access management.

---

# ⚠️ Real-World Risk

Without Dynamic Groups:

- User onboarding requires manual group assignments.
- Users may receive incorrect permissions.
- Administrative overhead increases.
- Access reviews become more difficult.

Dynamic Groups help organizations:

✅ Automate user provisioning

✅ Reduce administrative workload

✅ Improve access consistency

✅ Support identity lifecycle management

✅ Reduce human error

---

# 🛠 What I Built

- Created Dynamic Security Groups
- Configured dynamic membership rules
- Assigned users automatically based on attributes
- Validated automatic membership assignment
- Tested group updates when user attributes changed

---

# 🏗 Environment

### Microsoft Entra ID Components

- Dynamic Groups
- Users
- Group Membership Rules
- Security Groups

### Group Type

- Security Group
- Dynamic User Membership

---

# 📸 Step-by-Step Evidence

| Step | Action |
|--------|---------|
| 1 | Create Test Users |
| 2 | Create Dynamic Group |
| 3 | Configure Membership Rule |
| 4 | Validate Rule Syntax |
| 5 | Verify Automatic Membership |
| 6 | Test Membership Changes |

---

# 1️⃣ User Creation

Created test users with attributes that match the Dynamic Group membership rule.

### Example Users

- User1Sin
- User2Sin
- HrSin

### Result

Users were successfully created with the required attributes.

### Evidence

📸 Screenshot:

Screenshot/user-creation.png

---

# 2️⃣ Dynamic Group Creation

Created a Dynamic Security Group within Microsoft Entra ID.

### Configuration

- Group Type: Security
- Membership Type: Dynamic User

### Result

The group was successfully created.

### Evidence

📸 Screenshot:

Screenshot/create-dynamic-group.png

---

# 3️⃣ Membership Rule Configuration

Configured a Dynamic Membership Rule to automatically assign users.

### Example Rule

```text
(user.department -eq "HR")
```

### Result

Membership is now evaluated automatically by Microsoft Entra ID.

### Evidence

📸 Screenshot:

Screenshot/rule-configuration.png

---

# 4️⃣ Rule Validation

Validated the membership rule before deployment.

### Result

The rule passed validation and was successfully processed.

### Evidence

📸 Screenshot:

Screenshot/rule-validation.png

---

# 5️⃣ Automatic Membership Verification

Verified that users matching the configured criteria were automatically added to the group.

### Result

Users meeting the rule requirements appeared in the group membership list.

### Evidence

📸 Screenshot:

Screenshot/group-members.png

---

# 6️⃣ Membership Update Testing

Modified a user attribute and verified dynamic group membership updates automatically.

### Result

The user was automatically added or removed based on the updated attribute value.

### Evidence

📸 Screenshot:

Screenshot/membership-update.png

---

# 🔐 Security Validation

The Dynamic Group successfully:

✅ Assigned users automatically

✅ Removed users automatically

✅ Eliminated manual group administration

✅ Ensured consistent access assignment

---

# 🧰 Tools & Services Used

- Microsoft Entra ID
- Dynamic Groups
- Security Groups
- Microsoft Entra Admin Center

---

# 💡 Outcome

This lab demonstrates how Dynamic Groups can automate identity management by assigning group memberships based on user attributes.

By replacing manual group administration with automated rules, organizations can improve consistency, reduce administrative effort, and support scalable identity governance.

---

# 🧩 Troubleshooting

### User Not Added to Group

Verify:

- User attribute matches the membership rule.
- Membership processing has completed.
- Rule syntax is valid.

### Membership Rule Error

Verify:

- Rule syntax is correct.
- Supported attributes are used.
- Parentheses are correctly configured.

### Group Membership Not Updating

Verify:

- Dynamic membership processing has completed.
- User attributes have replicated successfully.
- Group membership evaluation is active.

---

# ✅ Lab Result

Successfully implemented Dynamic Groups in Microsoft Entra ID and validated automated group membership management using dynamic membership rules.
