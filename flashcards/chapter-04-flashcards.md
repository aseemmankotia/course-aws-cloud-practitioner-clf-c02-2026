## Chapter 4: Security and Compliance: Identity and Access Management (IAM) — Flashcards

| # | Front (Question) | Back (Answer) |
|---|-----------------|---------------|
| 1 | Default max number of IAM users per AWS account? | 5,000 (soft limit, increasable via support request). Exam tip: IAM is a global, free service. |
| 2 | Default STS temporary credential duration when assuming an IAM role? | 1 hour by default, configurable up to 12 hours maximum. Exam tip: roles never use long-term access keys. |
| 3 | Max number of IAM groups a single IAM user can belong to? | 10 groups per user (default limit). Exam tip: IAM groups cannot be nested inside other groups. |
| 4 | Max size of an inline IAM policy attached to a role? | 10,240 characters. Exam tip: limits differ by entity — user 2,048, group 5,120, role 10,240. |
| 5 | IAM user vs IAM role — which uses temporary credentials? | IAM role. Users have long-term credentials; roles are assumed and issue temporary STS credentials. Exam tip: EC2/Lambda should always use roles, never embedded user keys. |
| 6 | IAM group vs IAM role — can either be assumed by an AWS service? | No — groups only collect users for permission assignment. Roles can be assumed by users, services, or applications. Exam tip: only roles generate temporary credentials. |
| 7 | Cross-account access to resources without sharing long-term credentials — which IAM feature? | An IAM role with a trust policy allowing the other account to assume it. Exam tip: this is AWS's standard cross-account access pattern. |
| 8 | Centralized SSO for workforce users across many AWS accounts and business apps? | AWS IAM Identity Center (formerly AWS SSO). Exam tip: integrates with AWS Organizations and supports permission sets. |
| 9 | Which IAM policy JSON element specifies what actions are allowed/denied? | "Action" (e.g., "s3:GetObject"). Exam tip: policy structure = Version, Statement, Effect, Action, Resource. |
| 10 | Which JSON policy element grants or denies access? | "Effect": "Allow" or "Deny". Exam tip: an explicit Deny always overrides any Allow. |
| 11 | What MFA device types does AWS IAM support? | Virtual MFA (authenticator app), U2F/FIDO security keys, and hardware TOTP tokens. Exam tip: SMS-based MFA is NOT supported for IAM. |
| 12 | What is the cost of AWS IAM and IAM Identity Center? | Both are free of charge. Exam tip: you only pay for the AWS resources accessed, not for IAM itself. |
