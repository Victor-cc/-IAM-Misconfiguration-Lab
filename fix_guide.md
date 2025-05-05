#  Fix Guide: Replacing Overly Permissive IAM Policies

This guide explains how to safely remove a dangerously permissive policy and replace it with a **least-privilege** secure version.

---

##  Problem

The attached policy gives **full admin-like access**:
This violates the Principle of Least Privilege, which is essential in cloud security
```json
{
  "Effect": "Allow",
  "Action": "*",
  "Resource": "*"
}

