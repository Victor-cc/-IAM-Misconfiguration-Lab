#  Detection Steps for Insecure IAM Policies

This guide shows how to detect overly permissive IAM policies using built-in AWS tools like **IAM Access Analyzer** and **CloudTrail**.

---

##  Scenario

We attached the following insecure policy to an IAM user:

```json
{
  "Effect": "Allow",
  "Action": "*",
  "Resource": "*"
}

 
