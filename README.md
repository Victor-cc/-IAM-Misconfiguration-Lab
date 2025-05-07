# IAM Misconfiguration Lab: What Could Go Wrong?

##  Overview

This project simulates a basic AWS IAM misconfiguration where a user is given overly broad permissions. 
It walks through:
- Setting up a user with admin-level access via JSON policy
- Demonstrating dangerous operations they can perform
- Using AWS IAM Access Analyzer and CloudTrail to detect the issue
- Applying the Principle of Least Privilege to fix the problem

---

##  Objectives

- Understand how IAM misconfigurations can open up security risks
- Learn to detect issues using AWS native tools (IAM Access Analyzer, CloudTrail)
- Practice applying least privilege in real-world IAM policies

---

##  Tools Used

- AWS IAM
- AWS CloudTrail
- IAM Access Analyzer
- AWS CLI (optional)
- JSON policies

---

##  Project Structure

See the folder breakdown above.

---

## Setup Instructions

1. Log into your AWS account
2. Create a new IAM user named `test-user`
3. Attach the policy from `iam_policies/insecure_policy.json`
4. Try accessing S3, EC2, and other services
5. Use IAM Access Analyzer to inspect permissions
6. Replace policy with `secure_policy.json`
7. Re-test access

---

##  Detection Steps

See `detection_steps.md` — it covers:
- How to enable IAM Access Analyzer
- Interpreting findings
- Verifying via CloudTrail events

---

##  Fix Guide

See `fix_guide.md`:
- Step-by-step implementation of least privilege
- JSON policy examples
- Testing final permissions

---

##  Screenshots

Stored in `/screenshots/` — to be used in blog posts, LinkedIn content, or presentations.

---

##  Contributions

Pull requests are welcome — especially policy improvements or better detection steps.

---

##  License

MIT
