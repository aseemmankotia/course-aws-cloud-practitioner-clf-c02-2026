## Chapter 4: Security and Compliance: Identity and Access Management (IAM) — Practice Questions

**Q1.** A company runs an application on an EC2 instance that needs to read objects from an S3 bucket. Which approach BEST follows AWS security best practices?

A) Create an IAM user with programmatic access keys and store them in the application code
B) Use the AWS account root user's access keys for the application
C) Create an IAM group with S3 permissions and add the EC2 instance to the group
D) Attach an IAM role with an S3 read policy to the EC2 instance

<details>
<summary>Answer</summary>

**Correct: D**

IAM roles attached to EC2 instances provide temporary, automatically rotated credentials via the instance metadata service, eliminating the need to store long-term keys.

**Why the others are wrong:**
- Hardcoded long-term access keys in application code are a major security risk and violate least privilege practices.
- The root user should never be used for application workloads under any circumstance.
- IAM groups can only contain IAM users, not EC2 instances or other resources.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q2.** An organization has 50 employees who need single sign-on access to multiple AWS accounts and third-party business applications using their existing corporate credentials. Which AWS service BEST meets this requirement?

A) AWS IAM Identity Center
B) IAM users created individually in each AWS account
C) IAM roles with cross-account trust policies only
D) AWS Organizations service control policies

<details>
<summary>Answer</summary>

**Correct: A**

AWS IAM Identity Center provides centralized single sign-on across multiple AWS accounts and integrates with SAML 2.0 business applications.

**Why the others are wrong:**
- Creating individual IAM users per account does not scale and requires managing separate credentials everywhere.
- Cross-account roles enable access between AWS accounts but do not provide SSO for third-party applications.
- Service control policies manage permission boundaries within an organization, not authentication or SSO.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q3.** A solutions architect wants to protect the AWS account root user according to AWS best practices. Which action should be taken?

A) Use the root user for daily administrative tasks to ensure full access
B) Enable multi-factor authentication (MFA) on the root user and avoid using it for everyday tasks
C) Share the root user credentials with the operations team for convenience
D) Create access keys for the root user for programmatic automation tasks

<details>
<summary>Answer</summary>

**Correct: B**

AWS best practice is to enable MFA on the root user, lock away the credentials, and use IAM users/roles for all routine tasks.

**Why the others are wrong:**
- Using root for daily tasks increases risk of accidental full-account compromise.
- Sharing root credentials violates the principle of individual accountability.
- Root access keys are strongly discouraged and should be deleted if they exist.

</details>

---

**Q4.** Which AWS service allows an organization to centrally manage single sign-on access for employees across multiple AWS accounts and cloud applications?

A) AWS IAM
B) AWS Organizations
C) AWS Directory Service
D) AWS IAM Identity Center

<details>
<summary>Answer</summary>

**Correct: D**

IAM Identity Center is purpose-built for centralized workforce SSO across multiple AWS accounts and integrated applications.

**Why the others are wrong:**
- IAM manages access within a single AWS account, not centralized multi-account SSO.
- Organizations manages account structure and policies but does not itself provide the SSO portal.
- Directory Service provides a managed Active Directory but is not the SSO access management layer.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q5.** A serverless function needs permission to write logs to Amazon CloudWatch Logs. Which IAM feature should be attached to the function to grant this access?

A) IAM group
B) IAM role
C) IAM user with access keys
D) Root account permissions

<details>
<summary>Answer</summary>

**Correct: B**

AWS services like Lambda assume an execution IAM role, which provides temporary credentials scoped to the required permissions.

**Why the others are wrong:**
- IAM groups only apply to human IAM users, not services.
- Embedding user access keys in a function is a security anti-pattern.
- Root account permissions should never be used for service execution.

</details>

---

**Q6.** When writing an IAM policy following the principle of least privilege, which approach is correct?

A) Grant "Action": "*" and "Resource": "*" to simplify management
B) Attach the AdministratorAccess managed policy to all users for flexibility
C) Grant broad permissions initially and never review them again
D) Grant only the specific actions and resources required for the task

<details>
<summary>Answer</summary>

**Correct: D**

Least privilege means scoping permissions to exactly what is needed, nothing more.

**Why the others are wrong:**
- Wildcard actions/resources grant excessive, unnecessary access.
- Giving every user full admin access violates least privilege entirely.
- Permissions should be regularly reviewed and tightened, not left unchecked.

</details>

---

**Q7.** Which of the following is a supported multi-factor authentication (MFA) method for an AWS account?

A) Virtual MFA device using an authenticator app
B) SMS text message sent to a personal phone (only option)
C) Emailing a one-time password
D) Using the same password twice

<details>
<summary>Answer</summary>

**Correct: A**

AWS IAM supports virtual MFA apps (e.g., authenticator apps), hardware MFA devices, and FIDO security keys.

**Why the others are wrong:**
- AWS IAM does not support SMS-based MFA; this option is also incorrect in stating it as the 'only' option.
- Email-based one-time passwords are not a supported IAM MFA method.
- Reusing the same password is not a form of multi-factor authentication.

> ⚠️ Frequently missed on the exam — read the options carefully.

</details>

---

**Q8.** What is the key difference between an IAM user and an IAM role?

A) IAM users have permanent long-term credentials, while IAM roles provide temporary credentials that are assumed
B) IAM users provide temporary credentials, while IAM roles provide permanent credentials
C) IAM roles can only be used by the root account
D) IAM users and IAM roles are functionally identical

<details>
<summary>Answer</summary>

**Correct: A**

IAM users have long-term credentials (password and/or access keys), while roles are assumed and issue short-term STS credentials.

**Why the others are wrong:**
- This reverses the actual credential types of users and roles.
- Roles can be assumed by users, applications, and AWS services, not just root.
- Users and roles serve different purposes and are not functionally identical.

</details>

---

