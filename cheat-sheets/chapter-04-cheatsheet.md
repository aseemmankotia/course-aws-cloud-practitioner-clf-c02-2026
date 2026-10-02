## IAM Cheat Sheet — Users, Groups, Roles, Policies, MFA, Identity Center

### Core Entities
| Entity | Credentials | Use Case |
|---|---|---|
| IAM User | Long-term (password/access keys) | Individual human identity |
| IAM Group | None (container only) | Collection of users sharing permissions |
| IAM Role | Temporary (STS-issued) | AWS services, apps, cross-account access |
| IAM Policy | N/A (JSON document) | Defines permissions (Allow/Deny) |

**Exam rule:** Roles = temporary credentials, always. Users = permanent credentials. Groups cannot be nested and cannot be 'assumed'.

### Policy JSON Structure
```json
{
  "Version": "2012-10-17",
  "Statement": [{
    "Effect": "Allow",
    "Action": "s3:GetObject",
    "Resource": "arn:aws:s3:::my-bucket/*"
  }]
}
```
Explicit **Deny** always wins over any Allow.

### Key Limits
| Item | Limit |
|---|---|
| IAM users per account | 5,000 (soft) |
| Groups per user | 10 |
| Inline policy size (user) | 2,048 chars |
| Inline policy size (group) | 5,120 chars |
| Inline policy size (role) | 10,240 chars |
| Default STS session duration | 1 hour (max 12 hrs) |

### MFA
- Supported: Virtual MFA app, hardware token, U2F/FIDO security key.
- **NOT supported:** SMS-based MFA for IAM.
- Enable MFA on root user immediately after account creation.

### Root User Best Practices
- Enable MFA on root.
- Do NOT create root access keys (delete if they exist).
- Do NOT use root for daily tasks — create an admin IAM user/role instead.
- Lock away root credentials; use only for account-level tasks (e.g., closing account, changing support plan).

### IAM Identity Center (formerly AWS SSO)
- Centralized SSO across multiple AWS accounts + SAML 2.0 business apps.
- Integrates with AWS Organizations.
- Uses **Permission Sets** instead of individual IAM policies per account.
- Free service.

### Least Privilege
- Grant only required actions/resources — avoid `"Action":"*", "Resource":"*"`.
- Regularly audit and right-size permissions using IAM Access Analyzer.

### Common Exam Traps
- Thinking EC2 instances can join an IAM group (they cannot — groups hold users only).
- Believing SMS MFA is supported by IAM (it is not).
- Confusing IAM Identity Center (multi-account SSO) with IAM (single-account access management).
- Assuming roles have permanent credentials (they don't — always temporary via STS).
