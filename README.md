# AWS IAM Security Lab

## Project Overview

This project demonstrates AWS Identity and Access Management (IAM) security best practices by creating users, groups, policies, and roles following the principle of least privilege.

## AWS Services Used

- AWS IAM
- Amazon EC2
- Amazon S3

## Architecture

![Architecture Diagram](architecture-diagram.png)

## Implementation

### IAM Users Created

- admin-user
- dev-user1
- dev-user2
- auditor-user

### Groups Created

- Administrators
- Developers
- Auditors

## Security Controls Implemented

- User groups for permission management
- Custom IAM policy for developers
- Least privilege permissions
- MFA enabled for administrative access
- IAM role for EC2 to access S3 securely

## Testing

### Developer Permissions

Allowed:
- View EC2 resources
- Start/stop EC2 instances
- Read S3 objects

Denied:
- Create S3 buckets
- Access IAM users

## Key Learnings

- Difference between IAM users and roles
- How policies control AWS permissions
- Importance of least privilege access
- Why IAM roles are preferred over access keys
