# Part 1: Manual Detection – IAM User Policy
Scenario:
An IAM user has a dangerously permissive policy
This guide shows how to detect overly permissive IAM policies using built-in AWS tools like **IAM Access Analyzer** 

---

##  Scenario

We attached the following insecure policy to an IAM user:

 Steps:
Go to the IAM Console --> Users --> Click your test user.

Under the Permissions tab, find the attached policy.

Review the policy document:

If Action: "*", the user can perform any action.

If Resource: "*", this applies to all AWS resources.

Red flag: Full administrative access — this violates least privilege principles.

```json
{
  "Effect": "Allow",
  "Action": "*",
  "Resource": "*"
}
```

Part 2: Automatic Detection – IAM Access Analyzer (S3 Bucket)
Scenario:
A public S3 bucket policy allows anyone on the internet to download objects.
```{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::cyberveek-testbucket/*"
    }
  ]
}
```
Steps:
Go to S3 Console --> Select your bucket.

Click the Permissions tab --> Open Bucket Policy.

Paste in the public policy above and save.

In IAM Console, go to Access Analyzer.

Create an analyzer if you don’t have one already:

Name: iam-lab-analyzer

Type: Account

Wait ~30 seconds for analyzer results.

Result: A finding appears indicating that the bucket is publicly accessible.

 This finding will show:

Resource ARN (your bucket)

Action allowed (s3:GetObject)

Principal (* — meaning anyone)

Why it's a risk (unrestricted public access)






