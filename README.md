# IAM Misconfiguration Lab: Detecting & Fixing Insecure AWS Permissions

##  Overview

This lab simulates and fixes common IAM misconfigurations in AWS.
  It’s built to help beginners learn cloud security by:

  Creating insecure IAM and S3 policies
  
  Detecting risks manually and via IAM Access Analyzer
  
  Replacing them with secure, least-privilege policies
---

IAM-Misconfiguration-Lab/
├── insecure-policy.json
├── secure-policy.json
├── s3-insecure-bucket-policy.json
├── detection_steps.md
├── fix.md
└── screenshots/
    ├── insecure-policy-iam-user.png
    ├── insecure-policy-iam-user II.png 
    ├── access-analyzer-finding.png
    ├── S3 bucketpolicy updated.png

##  Objectives

- Understand how IAM misconfigurations can open up security risks
- Learn to detect issues using AWS native tools (IAM Access Analyzer, CloudTrail)
- Practice applying least privilege in real-world IAM policies

---

 Lab Workflow
Create a test IAM user and attach insecure-policy.json

Manually inspect permissions

Use secure-policy.json to fix

Attach s3-insecure-bucket-policy.json to a test bucket

Use IAM Access Analyzer to detect the risk

##  Tools Used

IAM Console – Manual policy inspection

IAM Access Analyzer – Automated detection of risky public access

S3 Bucket Policy – Simulated public misconfiguration

JSON policies

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

Stored in `/screenshots/` — for visual guidance on each step

---

##  Contributions

Pull requests are welcome — especially policy improvements or better detection steps.

---

Author
Victor C-C
##  License

MIT
