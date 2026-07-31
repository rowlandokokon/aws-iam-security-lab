</> Markdown

# AWS IAM Security Lab

## Project Overview

This project demonstrates AWS Identity and Access Management (IAM) security best practices by creating users, groups, policies, and roles following the principle of least privilege.

## AWS Services Used

- AWS IAM
  
- Amazon S3

## Architecture

![Architecture Diagram](aws-iam-security-lab.drawio.png)

## Implementation

## Project Objectives

- Create IAM users
- Create IAM groups
- Create a custom IAM policy
- Assign users to groups
- Test user permissions
- Apply the principle of least privilege

---

## Project Scenario

A company wants developers to access only a specific Amazon S3 bucket. Rather than granting AdministratorAccess, a custom IAM policy is created and attached to the Developers group. Any user added to the group automatically receives the required permissions.

---

# Step 1 – Create an IAM Group

Created a Developers IAM group to manage permissions centrally.

![IAM Group Created](IMG_9758.jpeg)

---

# Step 2 – Create IAM Users

Created two IAM users:

- Dev-User1
- Dev-User2

Both users were added to the Developers group so they inherit the assigned permissions.

**Screenshot**

---

# Step 3 – Create a Custom IAM Policy

A custom IAM policy was created to allow developers to list the S3 bucket and access objects while restricting unnecessary permissions.

**Screenshot**

---

# Step 4 – Attach the Policy to the Developers Group

The custom policy was attached to the Developers group instead of individual users. This follows AWS best practices by managing permissions through groups.

**Screenshot**

---

# Step 5 – Test User Permissions

Logged in as **Dev-User1** and verified that the custom IAM policy was working correctly.

Validation included:

- Access to the approved S3 bucket was successful.
- Unauthorized IAM actions were denied.
- Attempting to list IAM users returned an **Access Denied** error, confirming that the principle of least priviledge was successfully enforced.

![Access Denied - Least Priviledge Verification](IMG_9754.jpeg)

---

# Results

✅ Successfully created IAM users and groups.

✅ Successfully created and attached a custom IAM policy.

✅ Successfully verified least-privilege access using an IAM user.

---

# Skills Demonstrated

- AWS IAM
- Identity and Access Management
- IAM Policies
- IAM Groups
- Principle of Least Privilege
- Amazon S3 Permissions
- AWS Security Best Practices

---

# Lessons Learned

This project reinforced AWS IAM best practices, including managing permissions through groups, creating custom IAM policies, and applying the Principle of Least Privilege to improve cloud security.
